---
title: A summary of Fully Convolutional Networks for Semantic Segmentation by Jonathan
  Long et al.
description: Posted in arXiv, 2015
summary: Posted in arXiv, 2015

categories: [summary]
citations: [https://doi.org/10.1145/1273445.1273458, http://arxiv.org/abs/1411.4038,
  https://doi.org/10.1109/TIP.2005.852470, https://doi.org/10.1109/TPAMI.2012.231,
  https://proceedings.mlr.press/v32/pinheiro14.html]

draft: false

date: 2022-12-03T14:24:59-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *Fully Convolutional Networks for Semantic Segmentation*

> Jonathan Long et al. arXiv, 2015 [DOI](http://arxiv.org/abs/1411.4038)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *Fully Convolutional Networks for Semantic Segmentation*](#a-summary-of-fully-convolutional-networks-for-semantic-segmentation)
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

That previous SOTA models for semantic segmentation did not utilize fully
convolutional neural networks.

### Motivation

> Why should we care about this paper?

Because it presents a methodology for using existing SOTA convolutional neural
networks for semantic segmentation.

### Category

> What type of paper is this work?

This is a deep learning computer vision semantic segmentation paper.

### Context

> What other *types* of papers is the work related to?

This paper is related to works that involve the development of semantic
segmentation techniques.

### Contributions

> What are the author's main contributions?

Their main contribution is an analysis of the usage of fully convolutional
neural networks for the purposes of semantic segmentation.

______________________________________________________________________

## Second Pass

> A proper read through of the paper is required to answer this

### Background Work

> What has been done prior to this paper?

Work has been done to develop semantic segmentation models as well as developing
convolutional neural networks for the purposes of image classification.

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

The charts and figures are clear and easy to read.

### Clarity

> Is the paper well written?

The paper is well written.

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

2. F. Ning, D. Delhomme, Y. LeCun, F. Piano, L. Bottou, and P. E. Barbano.
   Toward automatic phenotyping of developing embryos from videos. Image
   Processing, IEEE Transactions on, 14(9):1360–1371, 2005.
3. C. Farabet, C. Couprie, L. Najman, and Y. LeCun. Learning hierarchical
   features for scene labeling. Pattern Analysis and Machine Intelligence, IEEE
   Transactions on, 2013.
4. P. H. Pinheiro and R. Collobert. Recurrent convolutional neural networks for
   scene labeling. In ICML, 2014.

### Methodology

> What methodology did the author's use to validate their contributions?

The authors compared a variety of semantic segmentation model using VGG,
GoogLeNet, and ResNet on several different datasets. These datasets include
NYUDv2, PASCAL VOC, and SIFT Flow. The metrics captured were pixel accuracy,
mean accuracy, mean IU, and frequency weighted IU.

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

The authors are reliant upon image classification models that have fully
connected layers for the purposes of classification. This is because these fully
connected layers are converted into fully convolutional layers.

#### Correctness

> Do the assumptions seem valid?

This reliance seems valid as most SOTA models for image classification (that I'm
aware of) utilize fully connected layers for the purposes of classification.
However, the method that the authors propose may not be transferable to present
or future convolutional networks that no longer rely on fully connected layers
for the purposes of classification.

### Future Directions

> My own proposed future directions for the work

I'd like to take the ideas and methodology proposed in this paper and apply them
to one shot object detection models to see if it is possible to create something
like a YOLO-Segmentation model.

### Open Questions

> What open questions do I have about the work?

Is it possible to incorporate a fully connected layer for the purposes of
classification and additionally convolutional layers for the purposes of
semantic segmentation within the same layer by using a complicated branching
architecture (in the vein of GoogLeNet)?

### Author Feedback

> What feedback would I give to the authors?

This is a good paper. I am concerned that the methodology presented may not be
transferable to models of the future that may not rely upon fully convolutional
layers to accomplish image classification.

______________________________________________________________________

## Summary

> A summary of the paper

The paper *Fully Convolutional Networks for Semantic Segmentation* by Jonathan
Long et al. \[1\] describes a methodology for converting an existing image
classification network into a semantic segmentation network. This is done by
replacing the fully connected layers at the head of the classification network
with one or more convolutional layers. This thereby makes semantic segmentation
networks full convolutional in terms of architecture design.

However, not all models rely on this pattern and different architectures need to
be tested for each model conversion. For example, GoogLeNet has a different
architecture for semantic segmentation than VGG.

______________________________________________________________________

## Summarization Technique

This paper was summarized using a modified technique proposed by S. Keshav in
his work *How to Read a Paper* \[0\].

## Citations
