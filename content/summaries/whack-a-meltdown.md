---
title: A summary of Whack-a-Meltdown by Daniel Genkin and Yuval Yarom
description: Posted in the IEEE Computing Edge, October 2022
summary: Posted in the IEEE Computing Edge, October 2022

categories: [summary, magazine, article]
citations: [https://doi.org/10.1109/MSEC.2020.3036146]

draft: false

date: 2023-02-20T08:34:58-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *Whack-a-Meltdown*

> Daniel Genkin and Yuval Yarom IEEE Computing Edge, October 2022 DOI \[0\]

## Table of Contents

- [A summary of *Whack-a-Meltdown*](#a-summary-of-whack-a-meltdown)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
    - [Out-Of-Order Execution](#out-of-order-execution)
    - [Transient Execution Attacks](#transient-execution-attacks)
    - [Leaking Information From The Transient Domain](#leaking-information-from-the-transient-domain)
    - [First-Generation Transient Execution Attacks](#first-generation-transient-execution-attacks)
    - [Defenses](#defenses)
    - [Second-Generation Attacks](#second-generation-attacks)
  - [Citations](#citations)

______________________________________________________________________

## Summary

The Spectre and Meltdown vulnerabilities reported in 2018 exposed that there
exists side effects in speculative and out-of-order execution that allow for an
attacker to extract data from the micro architecture of a CPU. These and similar
attack patterns share a root cause - the micro architecture allowing to execute
code after an instruction fails. To resolve these issues, the straightforward
answer is to ensure that subsequent instructions do not use data produced by the
failed instruction. However, this is easier said than done and will take time to
implement. In the meantime, countermeasures put out by organizations - such as
Intel - only act as band aids that can quickly be bypassed.

### Out-Of-Order Execution

Out-of-order execution allows multiple computational units of a processor (known
as *ports*) to run in parallel, each working on an individual instruction. This
is because some instructions take longer than others to complete. To keep track
of the instruction order, the processor maintains a reorder buffer (ROB) that
keeps track of the instructions and commits the results post instruction
completion. If the instruction fails, the ROB quashes the instruction. These
instructions are known as transient.

However, there are a few issues with out-of-order execution:

1. Misspeculation of instructions to run by incorrectly guessing the control
   flow of the program.
2. Exceptions when an instruction performs an illegal operation, causing the
   program to abort. Future instructions are no longer part of the program.
3. Microcode assists that handle complex edge cases require that the instruction
   be thrown out and code from the processor firmware be used to handle that
   case.
4. "When a Transactional Synchronization Extension (TSX) transaction aborts, all
   of the instructions within that transaction are not a part of the nominal
   program execution."

### Transient Execution Attacks

Transient execution attacks take advantage that while an instruction fails, the
state of the processor does not rollback to its previous state. Therefore,
memory addresses, cached data, and address translation are still in the
processor state post-transient instruction.

### Leaking Information From The Transient Domain

Attackers will target the instruction cache post-transient instruction
execution. They will measure the amount of time it takes for a memory address to
be accessed. If it was quick, then the cache most likely has cached that data.

### First-Generation Transient Execution Attacks

Meltdown is a transient execution attack where the security between user and
kernel memory is bypassed. A user space program tries to access kernel memory
and fails, but the cache contains information from that attempted memory
address.

Foreshadow takes advantage of Intel processors when they fail to resolve virtual
addresses to physical addresses. This attack targets the L1 processor cache.
Data can then be sampled from various secure enclaves.

Fallout, RIDL, and ZombieLoad sample data from various caches using micro
architecture data sampling (MDS). They lack precision, but when repeatedly
targeted, the probability of getting important data increases.

### Defenses

Intel and industry have released software security patches. Most of these
patches apply at OS level.

The Kernel Page Table Isolation (KPTI) patch removes kernel space addresses from
the address space of processes thereby preventing user space programs from
performing lookups on kernel addresses.

Page Table Entry (PTE) Inversion is a countermeasure against Foreshadow in which
the address space following transient execution does not point towards valid
page frames. Gang Scheduling is implemented by some VM hypervisors that ensure
that two hyper threads of a core always operate under the same protective
domain.

Intel has released microcode to protect against MDS attacks. This includes
clearing the L1 cache when leaving the SGX enclave and an instruction to flush
the cache on a context switch.

Additionally, new processors from Intel do not read across protective domains.
With this, KPTI protection can be disabled in order to regain lost performance.

### Second-Generation Attacks

The CacheOut attack takes advantage of the fact that L1 cache tends to end up in
the LFBs post cache flush, allowing data to be read from those locations.

"The CrossTalk attack shows that data can be from a shared staging buffer can be
loaded to an leaked from LFBs, allowing attackers to compromise the SGX's random
number generator."

The Load Value Injection (LVI) attack takes advantage of aborted instructions to
get around the cache flushing of data. This allows for an attacker to modify the
control flow of a program allowing for the execution of code not intended to be
ran.

The authors recommend that to prevent these attacks in the future, micro
architecture designs will need to prevent execution of data dependent
instructions post aborted instructions. Alternatively, the processor will have
to modify the pipeline stages to not process invalid data.

______________________________________________________________________

## Citations
