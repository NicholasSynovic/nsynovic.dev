---
title: A summary of Focal Loss for Dense Object Detection by Tsung-Yi Lin et al.
description: Posted in arXiv, 2018
summary: Posted in arXiv, 2018

categories: [summary, arXiv, 2018]
citations: [https://doi.org/10.1145/1273445.1273458, http://arxiv.org/abs/1708.02002,
  http://dx.doi.org/10.5244/C.23.91, https://doi.org/10.1109/CVPR.2010.5539906, https://doi.org/10.1007/978-0-387-21606-5,
  https://doi.org/10.1007/978-3-319-46448-0_2]

draft: false

date: 2022-12-03T12:01:03-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *Focal Loss for Dense Object Detection*

> Tsung-yi Lin et al. arXiv, 2018 [DOI](http://arxiv.org/abs/1708.02002)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *Focal Loss for Dense Object Detection*](#a-summary-of-focal-loss-for-dense-object-detection)
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

This paper aims to address the problem that one stage object detectors (i.e.,
YOLO, SSD) face when trying to match the performance of SOTA two stage object
detectors which is class imbalance.

### Motivation

> Why should we care about this paper?

Because it introduces a new loss function that addresses the issue of class
imbalance when training dense, one stage object detectors. Additionally, the
authors released an example model implementing this loss known as Detectron/
RetinaNet.

### Category

> What type of paper is this work?

This is an algorithms and CV object detection paper.

### Context

> What other *types* of papers is the work related to?

This paper is related to papers demonstrating or working on one stage object
detection models.

### Contributions

> What are the author's main contributions?

The author's main contribution is a new loss function aimed at training one
stage object detection models that reduces the problem of class imbalance
between identifying objects in the foreground and background. Furthermore, the
authors have released an example model that was trained on this loss function
known as Detectron/RetinaNet.

______________________________________________________________________

## Second Pass

> A proper read through of the paper is required to answer this

### Background Work

> What has been done prior to this paper?

Work has been done in developing classic object detectors, one and two stage
detectors, reducing class imbalance, and robust estimation techniques.

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

The figures are clear and understandable

### Clarity

> Is the paper well written?

This paper is well written and is dense with technical information.

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

2. P. Doll ́ ar, Z. Tu, P. Perona, and S. Belongie. Integral channel features.
   In BMVC, 2009.
3. P. F. Felzenszwalb, R. B. Girshick, and D. McAllester. Cascade object
   detection with deformable part models. In CVPR, 2010.
4. T. Hastie, R. Tibshirani, and J. Friedman. The elements of statistical
   learning. Springer series in statistics Springer, Berlin, 2008.
5. W. Liu, D. Anguelov, D. Erhan, C. Szegedy, and S. Reed. SSD: Single shot
   multibox detector. In ECCV, 2016.

### Methodology

> What methodology did the author's use to validate their contributions?

They compared their RetinaNet model against other SOTA object detectors on the
COCO dataset. Additionally, they compare the performance of models trained using
their Focal Loss and the Online Hard Example Mining (OHEM) technique.

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

Their assumption is that one stage object detectors are the future.

#### Correctness

> Do the assumptions seem valid?

While having more options as to what type of object detector to choose from (one
or two stage), it is important to keep in mind that inference speed, accuracy,
recall, other metrics, and domain need all play an important role in what model
is selected for a particular task.

### Future Directions

> My own proposed future directions for the work

I'd like to implement Focal Loss in both a traditional YOLO network and a YOLO
network following the MobileNet architecture.

### Open Questions

> What open questions do I have about the work?

Why was the COCO dataset chosen and not the ImageNet or Pascal VOC dataset for
training?

### Author Feedback

> What feedback would I give to the authors?

This is a good paper. I would say that the size of the network is certainly
larger than previous one stage object detectors such as YOLO. Could it be
possible to reduce the size of the network to be comparable to these smaller
networks while maintaining the accuracy or achieving a better accuracy?

______________________________________________________________________

## Summary

> A summary of the paper

The paper *Focal Loss for Dense Object Detection* by Tsung-Yi Lin et al. \[1\]
describes a new loss function aimed at improving the performance of one shot
object detection models that rely on region proposals. The problem that one shot
object detection models face compared against traditional two stage models that
utilize region proposals and object detection is that of class imbalance. Class
imbalance is simply that the region proposal network detects too many regions
where an object might be. This affects the performance of the object detection
component of the model as it might infer that an object is in a location that it
isn't.

To reduce this error, the authors of this paper propose the Focal Loss function,
a loss function aimed at reducing class imbalance. The function is
`FL(pt) = −(1 − pt)^γ log(pt)` where `γ >= 0` They then trained a model
(RetinaNet) with this loss function on the COCO dataset and found that it
performed better than other on stage methods with respect to average precision.

______________________________________________________________________

## Summarization Technique

This paper was summarized using a modified technique proposed by S. Keshav in
his work *How to Read a Paper* \[0\].

## Citations
