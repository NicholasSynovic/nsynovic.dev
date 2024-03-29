---
title: A summary of A Convolutional Neural Network Cascade for Face Detection by Haoxiang
  Li et al.
description: Posted in CVPR, 2015
summary: Posted in in CVPR, 2015

categories: [summary]
citations: [https://doi.org/10.1145/1273445.1273458, https://doi.org/10.1109/CVPR.2015.7299170]

draft: false

date: 2022-12-04T21:43:17-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *A Convolutional Neural Network Cascade for Face Detection*

> Haoxiang Li et al. CVPR, 2015 [DOI](https://doi.org/10.1109/CVPR.2015.7299170)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *A Convolutional Neural Network Cascade for Face Detection*](#a-summary-of-a-convolutional-neural-network-cascade-for-face-detection)
  - [Table of Contents](#table-of-contents)
  - [First Pass](#first-pass)
    - [Problem](#problem)
    - [Motivation](#motivation)
    - [Category](#category)
    - [Context](#context)
    - [Contributions](#contributions)
  - [Second Pass](#second-pass)
    - [Background Work](#background-work)
    - [Figures, Diagrams, Illustrations, and Graphs](#figures-diagrams-illustrations-and-graphs)
    - [Clarity](#clarity)
    - [Relevant Work](#relevant-work)
    - [Methodology](#methodology)
    - [Author Assumptions](#author-assumptions)
      - [Correctness](#correctness)
    - [Future Directions](#future-directions)
    - [Open Questions](#open-questions)
    - [Author Feedback](#author-feedback)
  - [Summary](#summary)
  - [Summarization Technique](#summarization-technique)
  - [Citations](#citations)

______________________________________________________________________

## First Pass

> Read the title, abstract, introduction, section and sub-section headings, and
> conclusion

### Problem

> What is the problem addressed in the paper?

The problem addressed in this paper is that previous works relied on Haar
features which work for when faces are looking at the camera head on. However,
these features are not enough to capture faces at angles and are hand crafted.

### Motivation

> Why should we care about this paper?

This paper proposes a model architecture for face detection that relies on a
cascade of CNNs to detect not only if there is a face, but also where a face is
within an image.

### Category

> What type of paper is this work?

This paper is a face detection and model architecture paper.

### Context

> What other *types* of papers is the work related to?

This paper is most closely related to work that involves face detection.

### Contributions

> What are the author's main contributions?

The authors contributions are a CNN cascade for fast face detection, a bounding
box calibration method for fine tuning the localization of the model, a
multi-resolution CNN architecture for face detection, and a SOTA model
implementation of the architecture for face detection.

______________________________________________________________________

## Second Pass

> A proper read through of the paper is required to answer this

### Background Work

> What has been done prior to this paper?

Work has been done previously to use neural networks for face detection.

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

All of the figures, charts, and tables are clear and easy to read.

### Clarity

> Is the paper well written?

This paper is well written.

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

### Methodology

> What methodology did the author's use to validate their contributions?

The authors measured the recall of their model and others on the Annotated Face
(Landmarks) in the Wild datasets.

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

The major assumption that the authors made was that a cascade of CNNs could
learn face detection better than an end to end model.

#### Correctness

> Do the assumptions seem valid?

Not really. As more and more modern literature is released about computer
vision, the trend is to train a model end to end on a particular task, rather
than use a cascade of models.

### Future Directions

> My own proposed future directions for the work

I think a reimplementation would be cool to do. However, I'd like to compare
this model to end to end solutions as well.

### Open Questions

> What open questions do I have about the work?

Why were VGA sized images (800 x 600 pixels) used instead of transforming the
images into smaller inputs such as 224 x 224?

### Author Feedback

> What feedback would I give to the authors?

This is a good paper. However, I would encourage the authors to explore
implementing this model on mobile or low powered systems if it is that efficient
to run on a CPU or GPU.

______________________________________________________________________

## Summary

> A summary of the paper

The paper *A Convolutional Neural Network Cascade for Face Detection* by
Haoxiang Li et al. \[1\] presents a CNN based solution for face detection. Their
solutions aims to be robust against faces that are not looking directly at the
camera. Their model architecture involves a cascade of 6 CNNs that aim to first
identify if a first is in the image using dense features (first 3 CNNs), then
isolate and locate faces within the scene (last 3 CNNs). The general
architecture of the solution is: 12 layers, 12 layers + calibration, 24 layers,
24 layers + calibration, 48 layers, 48 layers + calibration. This architecture
was able to achieve SOTA performance on the Annotated Face (Landmarks) in the
Wild datasets.

______________________________________________________________________

## Summarization Technique

This paper was summarized using a modified technique proposed by S. Keshav in
his work *How to Read a Paper* \[0\].

## Citations
