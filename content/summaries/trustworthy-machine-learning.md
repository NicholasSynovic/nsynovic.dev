---
title: A summary of Trustworthy Machine Learning by Bhavani Thuraisingham et al.
description: Posted in the IEEE Computing Edge, January 2023
summary: Posted in the IEEE Computing Edge, January 2023

categories: [summary, magazine, article, ai focus]
citations: [https://doi.org/10.1109/MIS.2022.3152946]

draft: false

date: 2023-02-20T20:47:27-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *Trustworthy Machine Learning*

> Bhavani Thuraisingham et al.; IEEE Computing Edge, January 2023 DOI \[0\]

## Table of Contents

- [A summary of *Trustworthy Machine Learning*](#a-summary-of-trustworthy-machine-learning)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
    - [Architecture To Support Trustworthy Machine Learning](#architecture-to-support-trustworthy-machine-learning)
    - [Concepts In Trustworthy ML](#concepts-in-trustworthy-ml)
      - [Security](#security)
      - [Privacy](#privacy)
      - [Fairness](#fairness)
      - [Integrity](#integrity)
  - [Citations](#citations)

______________________________________________________________________

## Summary

ML models are being used across industry and academia to solve a number of
problems. However, ML techniques are subject to attacks and may discriminate
against individuals based on the training data. Therefore, trustworthy AI must
be secure, ensure privacy of individuals, incorporate fairness, and be accurate.
This article describes how to implement scalable trustworthy AI models in
industry and academia.

With the advent of big data, ML models are being trained to solve many problems
across many problem domains. However, personally identifying information may be
captured in these big data datasets. Therefore, ML models can discriminate
against individuals through this information or be attacked to extract or favor
certain individuals. There is thus an interest in developing privacy-enhanced ML
models to protect individuals while still being able to extract useful
information from the data. The field of defending ML models and systems from
attackers is known as adversarial ML.

Trustworthy ML has to be secure, ensure the privacy of individuals, accurate,
fair, and fault tolerant. This is a new area of research within the ML space.

### Architecture To Support Trustworthy Machine Learning

ML at scale/ cloud hosted is architected in the following sequential manner
(built from the bottom up):

- An infrastructure layer that hosts the data store
- A big data management layer that manages access to the data hosted
- A machine learning layer that performs the inferencing
- An application layer that allows for interfacing with the ML layer or for
  results to be reviewed

Trustworthy ML must involve security, privacy, accuracy, fairness, and fault
tolerance at all levels of the architecture. Depending on the task, different
components of the above requirements might be emphasized more than others.

### Concepts In Trustworthy ML

#### Security

ML models must not access data that is not important to the problem domain or is
specifically not to be trained or inferenced upon. Additionally, ML models must
be resilient to attackers learning the data and bias that the ML model was
trained on. Solutions include adversarial support vector machines. Furthermore,
specifications for testing, verification, and capabilities are being
investigated to ensure that ML models do not contain any malware.

#### Privacy

Personally identifiable information or other sensitive information must be
protected from the ML training process. This has been a field of study for the
past 20 years. Techniques to ensure the privacy of the individuals contained
within the dataset involve removing sensitive information, as well as
randomizing values that shouldn't be trained upon.

#### Fairness

ML models are now being used to make decisions about important life events for
individuals. To ensure that the decisions are fair, fairness metrics and stop
gaps need to be introduced at different levels of the ML pipeline.

First, the data must be fair and non-discriminating/ bias. Next, the ML model
training must be fair which can be implemented with a fairness metric. Finally,
the ML inference must go through post-processing to ensure that the inference is
also fair.

#### Integrity

Integrity refers to the accuracy of the model. This also involves testing many
different models to ensure that the model that is selected for inference is the
best model to choose. Therefore, different features and model variations should
be chosen and documented.

______________________________________________________________________

## Citations
