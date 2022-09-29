---
title: A summary of Going deeper with convolutions by Christian Szegedy etal.
description: A summary of Going deeper with convolutions by Christian Szegedy etal.
summary: A summary of Going deeper with convolutions by Christian Szegedy etal.

categories: [summary, computer vision, cv, ml, machine learning, machine learning
      architecture]
citations: [https://doi.org/10.1145/1273445.1273458, https://doi.org/10.48550/arXiv.1409.4842,
  https://doi.org/10.48550/arXiv.1207.0580, https://doi.org/10.48550/arXiv.1312.6229,
  https://doi.org/10.1109/TPAMI.2007.56, https://doi.org/10.48550/arXiv.1312.4400,
  https://doi.org/10.1145/3065386, https://openaccess.thecvf.com/content_cvpr_2014/html/Girshick_Rich_Feature_Hierarchies_2014_CVPR_paper.html,
  https://openaccess.thecvf.com/content_cvpr_2014/html/Erhan_Scalable_Object_Detection_2014_CVPR_paper.html,
  http://proceedings.mlr.press/v32/arora14.pdf, https://doi.org/10.1162/neco.1989.1.4.541,
  https://doi.org/10.1137/0330046, https://doi.org/10.1109/ICCV.2011.6126456, https://doi.org/10.48550/arXiv.1312.5402]

draft: false

date: 2022-09-28T20:07:40-05:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: true
show_reading_time: true
---

# A summary of *Going deeper with convolutions*

> Christian Szegedy etal;
> [https://doi.org/10.48550/arXiv.1409.4842](https://doi.org/10.48550/arXiv.1409.4842)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *Going deeper with convolutions*](#a-summary-of-going-deeper-with-convolutions)
  - [Table of Contents](#table-of-contents)
  - [First Pass](#first-pass)
    - [Category](#category)
    - [Context](#context)
    - [Contributions](#contributions)
  - [Second Pass](#second-pass)
    - [Figures, Diagrams, Illustrations, and Graphs](#figures-diagrams-illustrations-and-graphs)
    - [Clarity](#clarity)
    - [Relevant Work](#relevant-work)
  - [Third Pass](#third-pass)
    - [Author Assumptions](#author-assumptions)
    - [Correctness](#correctness)
    - [Future Directions](#future-directions)
  - [Summary](#summary)
  - [Summarization Technique](#summarization-technique)
  - [Citations](#citations)

______________________________________________________________________

## First Pass

> Discussion about the title, abstract, introduction, section and sub-section
> headings, and conclusion

The paper *Going deeper with convolutions* by Christian Szegedy etal \[1\]
describes a 2014 state of the art computer vision model (on the ImageNet
Large-Scale Visual Recognition Challenge) called GoogLeNet architected based on
Hebbian principles (i.e. neruons that fire together, are wired together)and a
constant computational budget. Their approach relies on creative algorithms and
neuroscience principles and aims to be a more power effiecient model for mobile
devices by limiting the computations during infrencing. Additionally, their
model is deep but not wide and is considered "sparse" by the authors. In other
words, there are as few nodes as possible within the neural network.

Szegedy etal's contributions are a state of the art computer vision model that
provides experimental evidence that, "... Approximating the expected optimal
sparse structure by readily avilible dense building blocks is a viable method
for improving neural networks for computer vision". This means that this model
proves that dense neural networks for computer vision are not necessary in the
author's viewpoint.

### Category

> What type of paper is this work?

This is a computer vision paper describing both a machine learning architecture
and refernce model.

### Context

> What other *types* of papers is the work related to?

This paper is related to other computer vision papers that achieve state of the
art performance values based on the ImageNet Large-Scale Visual Recognition
Challenge.

### Contributions

> What are the author's main contributions?

Szegedy etal's contributions are:

- A computer vision model architecture (Inception) that is both sparse and aims
  to be computationally efficient on mobile (non-server) devices,
- A reference model of the aforementioned computer vision model architecture
- A comparison of previous state of the art work to justify their claims that
  sparser networks are the future of computer vision models.

______________________________________________________________________

## Second Pass

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

All of the tables have proper column labels. However, Table 1 does not provide
default values for blank cells. This is most likely due to the layer type not
performaing a specific operation (as described in the column label). Regardless,
the remaining tables look good.

Additionally, Figure 3 is very clear to read, if a little dense. However, as it
describes all of the layers of GoogLeNet and how they are connected, I find the
size to be appropriate.

### Clarity

> Is the paper well written?

The paper is fairly well written. The only complaints that I have are minor
grammatical mistakes that the author's left in (by accident I assume).
Additionally, that the authors didn't optimize their tables and figures to
better fit on the pages. As tables and figures are stacked on top of one
another, it would be possible to reclaim paper space by rearranging multiple
tables and figures to be next to one another, with the exception of Figure 3 due
to the sheer size of it.

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

- Contrast Normalization
- Max Pooling
- Average Pooling
- Softmax Activation
- Dropout - \[2\]
- Localization Task - \[3\]
- Gabor Filters - \[4\]
- Network in Network - \[5\]
- Rectified Linear Activation - \[6\]
- Regions with Convolutional Neural Networks - \[7\]
- Multi-Box Prediction - \[8\]
- Arora proof - \[9\]
- LeNet 5 - \[10\]
- Fisher vectors
- Polyak Averaging - \[11\]
- Jaccard index
- Selective Search - \[12\]
- Photometric Distortions - \[13\]

______________________________________________________________________

## Third Pass

> This section can only be complete after a virtual re-implementation of the
> paper

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

One assumption that the authors make is that overfitting is more prone to occur
in large models. Additionally, overfitting can occur when there is not enough
labeled examples in a dataset when a large model is training. Furthermore,
increasing the size of a model increases the number of computations that must be
done between layers (e.g. chaining two convulational layers results in
computation cost quadratically increasing) Their solutions relies on moving from
fully connected to sparsely connected architectures including within
convolutional layers. Also, their model architecutre is based on the idea that
computers are inefficent when, "... Computing numerical calculations on
non-uniform sparse data structures".

They assume that 1x1, 3x3, and 5x5 filters are the proper filters to use, but
did not test other size of filters. They also assume that using, "Inception
modules" is only useful at higher levels, whereas the initial levels are
standard convultational levels. However, this was not tested either and was due
to, "infrastructural inefficiences" in the implementation.

Finally, that the model that achieved state of the art performance was the best
model. The authors had been training and testing other models for months prior,
however, it is unclear what the testing methodology was and why a particular
model was choosen to compete in the ImageNet competition.

### Correctness

> Do the assumptions seem valid?

The first paragraph of assumptions seems reasonable and correct. However, the
remaining two paragraphs seem unreasonable. This is due to the lack of testing
that the author's put in when optimizing their model with respect to the filter
sizes and choosing models. Furthermore, if testing did occur to address these
issues, it is not addressed in this paper, thus leaving the reader to wonder why
testing wasn't performed.

### Future Directions

> My own proposed future directions for the work

Based off of Section 3 (Motiviation and High Level Considerations), one
promising area of study would be to perform a network architecture search
utilizing the principles and reasoning of their approach to other machine
learning and computer vision domains.

An enhancement to their work is possible by analyzing what filter sizes most
optimal improve performance. Currently the author's are restricting GoogLeNet to
1x1, 3x3, and 5x5 filter sizes, but this was due to convience and no data was
given to support this.

______________________________________________________________________

## Summary

> A summary of the paper

The paper *Going deeper with convolutions* by Szegedy etal \[1\] introduces a
computer vision model architecture called Inception and a reference model called
GoogLeNet.

Inception is a model architecuture that is both sparse and (attempts to be)
computationally efficent during inferencing with only 1.5 billion multiply-add
operations allowed. Inception models are composed of multiple Inception modules
that are stacked on top of each other. Each Inception module takes in data from
the previous layer and passes it into small convultional filters (i.e. 1x1
typically). There are three of these small filters that are wired to the input
of the Inception module, with one of them connected directly to the output. The
outputs of two of these filters are then passed into larger filters (i.e. 5x5)
to which it is then passed into a DepthConcat function. Additionally, a 3x3
filter is wired to the input of the module and the output of which goes into a
1x1 filter to be passed into the DepthConcat function as well. From there, it is
passed into another Inception module and the process repeats.

**Note:** Depth when referring to two dimensional images refers to the color
channel of the image. As images typically have three color channels (i.e. red,
green, blue), an image would have a depth of 3.

*Example:* A 200 pixel by 200 pixel full color spectrum image would be
represented as 200x200x3.

It is possible for Inception modules to have an additional connection to the
input of the module to perform average pooling for softmax activation.

GoogLeNet achieved SOTA performance in the ImageNet Large-Scale Visual
Recognition Challenge image classification task by having a top-5 error of 6.67%
on both the validation and testing data. This is an improvment of 56.5% in
comparison to 2012's SOTA performer (SuperVision) and 2013's SOTA performer
(Clarifai). Additionally, they achieved SOTA perfomance for the ImageNet
Large-Scale Visual Recognition Challenge detection task with a mean average
precision of 43.9% utilizing an ensemble inference approach. This model was
architected using the Inception architecture with 22 layers. However, not every
layer was an Inception module; the first few layers were standard convulational
layers.

The author's contributions were as follows;

1. The Inception computer vision architecture,
2. The GoogLeNet SOTA computer vision model for classification and object
   detection.

My opinion on this paper is that while it is well written, the author's make
numerous assumptions about the optimal performance of their model's
architecture. They don't test optimal sizes for filters as well as resolving
bugs such as the usage of standard convulational layers early in the model. Both
of which can be solved by performing a neural architecture search.

Future work for this paper would involve optimizing the model architecture via a
neural architecture search. As well as evaluating the performance of the model
by both increasing and decreasing the depth of the model.

______________________________________________________________________

## Summarization Technique

This paper was summarized using the technique proposed by S. Keshav in his work
*How to Read a Paper* \[0\].

## Citations