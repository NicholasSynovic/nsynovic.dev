---
title: A summary of ImageNet Classification with Deep Convolutional Neural Networks
  by Krizhevsky et al.
description: Published in the 60th volume, number 6 Communications of the ACM in 2017
summary: Published in the 60th volume, number 6 Communications of the ACM in 2017

categories: [summary, deep learning, computer vision, ImageNet, GPU, 2017, Communications
      of the ACM]
citations: [https://doi.org/10.1145/1273445.1273458, https://doi.org/10.1145/3065386]

draft: false

date: 2022-09-29T14:33:01-05:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *ImageNet Classification with Deep Convolutional Neural Networks*

> Krizhevsky et al.;
> [https://doi.org/10.1145/3065386](https://doi.org/10.1145/3065386)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *ImageNet Classification with Deep Convolutional Neural Networks*](#a-summary-of-imagenet-classification-with-deep-convolutional-neural-networks)
  - [Table of Contents](#table-of-contents)
  - [First Pass](#first-pass)
    - [Category](#category)
    - [Context](#context)
    - [Contributions](#contributions)
  - [Second Pass](#second-pass)
    - [Background Work](#background-work)
    - [Motivation](#motivation)
    - [Figures, Diagrams, Illustrations, and Graphs](#figures-diagrams-illustrations-and-graphs)
    - [Clarity](#clarity)
    - [Relevant Work](#relevant-work)
    - [Author Assumptions](#author-assumptions)
      - [Correctness](#correctness)
    - [Discussion of the Proofs](#discussion-of-the-proofs)
    - [Future Directions](#future-directions)
  - [Summary](#summary)
  - [Summarization Technique](#summarization-technique)
  - [Citations](#citations)

______________________________________________________________________

## First Pass

> Discussion about the title, abstract, introduction, section and sub-section
> headings, and conclusion

The paper *ImageNet Classification with Deep Convolutional Neural Networks* by
Krizhevsky et al. discusses the AlexNet model and its architecture as well as
its SOTA achievements in the 2012 ImageNet Challenge. The difference between
AlexNet and other contestants was that the model relies on GPU training to train
the convolutional neural network model. By utilizing the GPU, training time can
be accelerated significantly more than what was previously possible. Their major
contributions is that a large, deep convolutional neural network is capable of
achieving record-breaking results via supervised learning. They did not utilize
unsupervised pre-training, but the authors suspect that it would improve the
accuracy of the model.

### Category

> What type of paper is this work?

This is a computer vision model evaluation and architecture paper.

### Context

> What other *types* of papers is the work related to?

This paper is similar to others that have published about SOTA results from the
ImageNet Challenge.

### Contributions

> What are the author's main contributions?

Their main contributions were that training on GPUs allows for accelerated
training, that large and deep convolutional neural networks are effective at
classifying images, and that removing layers does decrease the performance of
models. Therefore, a larger, deeper model is applicable. It should be noted that
AlexNet was the largest model ever at the time of publication.

______________________________________________________________________

## Second Pass

### Background Work

> What has been done prior to this paper?

Previous work on designing convolutional neural networks and architectures.
However, they were bounded by not being particularly deep.

### Motivation

> Why should we care about this paper?

Because it is one of the key papers that demonstrates that large, deep,
convolutional neural networks are effective for image classification. As well as
providing evidence that training on GPUs is not only effective but recommended
for optimal performance. Additionally it provides empirical evidence that
removing a layer from a convolutional neural network is detrimental to the
performance of the model. In other words, the more layers you add, the more
potential there is for improvement.

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

Nearly all of the figures are designed well, with the exception of Figure 2.
Figure 2 is the model architecture of AlexNet. This figure suffers from
information density and a three dimensional design which makes it hard to
determine what is going on and in what dimension are images being manipulated.

### Clarity

> Is the paper well written?

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

They assume that it is because of the larger compute devices and data sets that
make these deep convolutional neural networks possible.

#### Correctness

> Do the assumptions seem valid?

While true, [Szegedy et al.](going-deeper-with-convolutions.md) designed their
own architecture using unique algorithms not prevalent in existing convolutional
neural networks.

### Discussion of the Proofs

Their training involved both dropout and data augmentation.

Dropout involves not using the outputs of neurons whose activation is less than
0.5.

Data augmentation involves manipulating the input images such that 5 244 x 244
images are derived from one 256 x 256 image (e.g., the four corners and one
centered). Additionally, PCA was done on the RGB channels of all of the images
in the ImageNet 2010 and 2012 data sets. These eigenvectors were then added to
each of the images respective color channels.

### Future Directions

> My own proposed future directions for the work

A reimplementation of the work would be interesting, with particular respect to
bench marking training time, as the authors were limited by their GPU compute
units' performance.

______________________________________________________________________

## Summary

> A summary of the paper

*Taken from [First Pass](#first-pass)*

The paper *ImageNet Classification with Deep Convolutional Neural Networks* by
Krizhevsky et al. \[1\] discusses the AlexNet model and its architecture as well
as its SOTA achievements in the 2012 ImageNet Challenge. The difference between
AlexNet and other contestants was that the model relies on GPU training to train
the convolutional neural network model as well as being a deep convolutional
neural network.

By utilizing the GPU, training time can be accelerated significantly more than
what was previously possible. The benefits of being a deep convolutional neural
network is that the classification of images builds off of the features found in
the previous images. The result of this is that their top 1% and top 5% error
were the lowest ever in the competition.

They trained their model by utilizing both dropout, where neurons that activated
with a value less than 0.5 are not inputted into the next layer, and by
augmenting the Imagenet 2010 and 2012 data sets to increase the amount of data
that they can throw at the model.

Their work is important as it kicked off the usage of both deep convolutional
neural networks and the usage of GPUs to reduce training time.

______________________________________________________________________

## Summarization Technique

This paper was summarized using a modified technique proposed by S. Keshav in
his work *How to Read a Paper* \[0\].

## Citations
