---
title: 'A summary of Automated Payment Terminal Testing: How to Achieve Continuous
  Integration for Systems that are Almost Impossible to Virtualize by Martin Gloor
  et al.'
description: Posted in IEEE Computing Edge, December 2022
summary: Posted in IEEE Computing Edge, December 2022

categories: [summary, magazine, article]
citations: [https://doi.org/10.1109/MS.2021.3094955]

draft: false

date: 2023-02-19T15:42:36-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *Automated Payment Terminal Testing: How to Achieve Continuous Integration for Systems that are Almost Impossible to Virtualize*

> Martin Gloor et al. IEEE Computing Edge, December 2022 DOI \[0\]

## Table of Contents

- [A summary of *Automated Payment Terminal Testing: How to Achieve Continuous Integration for Systems that are Almost Impossible to Virtualize*](#a-summary-of-automated-payment-terminal-testing-how-to-achieve-continuous-integration-for-systems-that-are-almost-impossible-to-virtualize)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
    - [Shift Left of Die - Or, Why are We Doing This?](#shift-left-of-die---or-why-are-we-doing-this)
    - [To Virtualize or Not To Virtualize](#to-virtualize-or-not-to-virtualize)
    - [A Journey of Trial and Error](#a-journey-of-trial-and-error)
    - [Scaling With Cards](#scaling-with-cards)
    - [Coping With Calibration](#coping-with-calibration)
    - [APIs and Abstraction Layers](#apis-and-abstraction-layers)
    - [Generic, But Not!](#generic-but-not)
    - [Habemus Automation!](#habemus-automation)
    - [A Continuous Journey](#a-continuous-journey)
  - [Citations](#citations)

______________________________________________________________________

## Summary

Pure software solutions benefit from continuous integration platforms. However,
solutions that involve both hardware and software - such as payment terminals -
need to develop custom continuous integration platforms that test both
components in order to meet modern Agile development practices.

### Shift Left of Die - Or, Why are We Doing This?

Since Abrantix (the company the authors work at) design and development payment
terminal systems, they typically test end-to-end solutions with human testers.
However, as tests involve many repetitive tasks, human error and fatigue can
invalidate many tests. Therefore, they needed to develop an automated platform
to not only handle software testing and continuous integration, but also
hardware testing and integration. In doing so, they aim to catch bugs earlier in
the development cycle, reduce human error, and run regression testing all
autonomously.

### To Virtualize or Not To Virtualize

While it is possible to abstract hardware interfaces virtually, there is
difficulty in virtualizing some actions that need to be tested. For example:

- Card readers are hard to mock as they need to test magstripe, contactless and
  contact chip payments, and the Eurocard, MasterCard, Visa (EMV) standard would
  need to be virtualized as well.
- Secure modules are hard to mock as the required cryptographic functions are
  often proprietary, can involve both symmetric and asymmetric keys, and have to
  comply with rigorous standards.
- No real end-to-end testing of hardware and software is tested.

### A Journey of Trial and Error

Abrantix decided to go with a robot to solve the end-to-end hardware and
software testing. They started with a cheap robotic arm and found that it was
capable of handling both contactless and contact based chip solutions, but was
unable to enter PIN codes. They therefore pivoted to a 3D printed solution to
enter PIN codes and to drop the robotic arm solution.

### Scaling With Cards

To scale with multiple cards, a multiplexer was built to handle inputs from
multiple different cards into a single output.

### Coping With Calibration

In order to calibrate the robot for each terminal, a layout of each terminal was
made and a user could select what terminal to test. It was therefore on the user
to swap in and out the terminals for each test. This way a single test could be
written and abstracted away from the terminal interface.

### APIs and Abstraction Layers

At this point the base end-to-end testing solution was built. However, as the
solution scaled to meet the demands of the company and partners, it became
apparent that the software architecture couldn't handle all of the requested
features. Therefore, abstraction layers were written and a REST HTTP API
interface was created to simplify both the development of the software solution
as well as to allow third party orchestration tools to hook into the state of
the testing solution.

### Generic, But Not!

To allow for control of the robotic testing platform as well as to provide
extensibility to the REST API, a schema based on JSON was developed that can be
used to control the robot.

### Habemus Automation!

Now that the testing solution had been developed, a stress test of running 5,000
transactions on individual terminals was ran. 70 bugs were found on average per
terminal model. These bugs couldn't have been found in such a short time without
the development of this tool.

### A Continuous Journey

There a number of security concerns and procedures not currently implemented in
the testing solution. However, Abrantix is intending to continue the development
of this solution and iterate upon, just as any developer would working with
continuous integration.

______________________________________________________________________

## Citations
