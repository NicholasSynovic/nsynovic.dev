---
title: A summary of Deep Learning by Yann LeCun et al,
description: Posted in Nature, 2015
summary: Posted in Nature, 2015

categories: [summary, Nature, 2015]
citations: [https://doi.org/10.1145/1273445.1273458, https://doi.org/10.1038/nature14539,
  https://doi.org/10.1145/3065386, https://doi.org/10.1109/MSP.2012.2205597, 
      https://proceedings.neurips.cc/paper/2014/hash/a14ac55a4f27472c5d894ec1c3c743d2-Abstract.html,
  https://proceedings.mlr.press/v15/glorot11a.html, https://doi.org/10.1162/neco.2006.18.7.1527,
  https://proceedings.neurips.cc/paper/2006/hash/5da713a690c067105aeb2fae32403405-Abstract.html,
  https://proceedings.neurips.cc/paper/1989/hash/53c3bce66e43be4f209556518c2fcb54-Abstract.html,
  https://doi.org/10.1109/5.726791, https://doi.org/10.1162/neco.1997.9.8.1735]

draft: false

date: 2022-11-08T12:55:10-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *Deep Learning*

> Yann LeCunn et al, Nature, 2015 [DOI](https://doi.org/10.1038/nature14539)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *Deep Learning*](#a-summary-of-deep-learning)
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

This paper discusses the usage of deep learning (DL) models and how they have
led to improvements in speech recognition, visual object recognition, object
detection, drug discovery, and genomics. It talks about how these models are
created, what type of models are typically applied to what domains, and the
usage of the backpropagation algorithm to train the model. Additionally, a
discussion about the usage of Recurrent Neural Networks (RNNs) and their
benefits is had.

### Motivation

> Why should we care about this paper?

We should care about this paper as it is a review of different DL techniques for
different problem domains.

### Category

> What type of paper is this work?

This paper is a literary review paper.

### Context

> What other *types* of papers is the work related to?

It is closest related to papers that summarize a body of literature for the
purposes of understanding what the current SOTA techniques for a problem are.

### Contributions

> What are the author's main contributions?

Their main contribution is a discussion of DL, its usages, RNNs, and a general
summary of the SOTA DL techniques for different problem domains.

______________________________________________________________________

## Second Pass

> A proper read through of the paper is required to answer this

### Background Work

> What has been done prior to this paper?

Work has been done to develop DL and RNN techniques.

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

All of the figures are clear and easy to understand.

### Clarity

> Is the paper well written?

This paper is well written.

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

02. Krizhevsky, A., Sutskever, I. & Hinton, G. *ImageNet classification with
    deep convolutional neural networks.* In Proc. Advances in Neural Information
    Processing Systems 25 1090–1098 (2012).
03. Hinton, G. et al. *Deep neural networks for acoustic modeling in speech*
    recognition. IEEE Signal Processing Magazine 29, 82–97 (2012).
04. Sutskever, I. Vinyals, O. & Le. Q. V. *Sequence to sequence learning with
    neural* networks. In Proc. Advances in Neural Information Processing Systems
    27 3104–3112 (2014)
05. Glorot, X., Bordes, A. & Bengio. Y. *Deep sparse rectifier neural networks.*
    In Proc. 14th International Conference on Artificial Intelligence and
    Statistics 315–323 (2011).
06. Hinton, G. E., Osindero, S. & Teh, Y.-W. *A fast learning algorithm for deep
    belief nets*. Neural Comp. 18, 1527–1554 (2006).
07. Bengio, Y., Lamblin, P., Popovici, D. & Larochelle, H. *Greedy layer-wise
    training of deep networks.* In Proc. Advances in Neural Information
    Processing Systems 19 153–160 (2006).
08. LeCun, Y. et al. *Handwritten digit recognition with a back-propagation
    network.* In Proc. Advances in Neural Information Processing Systems 396–404
    (1990).
09. LeCun, Y., Bottou, L., Bengio, Y. & Haffner, P. G*radient-based learning
    applied to document recognition*. Proc. IEEE 86, 2278–2324 (1998).
10. Hochreiter, S. & Schmidhuber, J. *Long short-term memory*. Neural Comput. 9,
    1735–1780 (1997).

### Methodology

> What methodology did the author's use to validate their contributions?

The author's of this paper reviewed literary sources for examples and usage of
DL and RNN techniques applied to different problem domains.

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

The author's assume that unsupervised learning will become far more important in
the future than supervised learning.

#### Correctness

> Do the assumptions seem valid?

Potentially. Unsupervised learning presents problems and challenges not explored
in this paper, and is therefore treated as the next logical evolution of
techniques, rather than a series of unknowns and problems that need to be solved
first.

### Future Directions

> My own proposed future directions for the work

I'd like to implement the different DL techniques to the suggested problem
domains presented in this paper.

### Open Questions

> What open questions do I have about the work?

Why wasn't a discussion about Generative Adversarial Networks (GANs) not had in
this work? What are the performance differences of the presented loss functions?

### Author Feedback

> What feedback would I give to the authors?

Overall, a pretty good paper. A follow up paper on unsupervised learning would
be nice to read.

______________________________________________________________________

## Summary

> A summary of the paper

The review paper *Deep Learning* by Yann LeCun et al \[1\]. discusses the
advances and advantages of deep learning (DL) techniques made up to 2015. The
authors discuss what is DL, how and where it is applied, commercial and academic
usages of DL, the advantages of merging two different architectures together to
solve challenging tasks, and the usage of Recurrent Neural Networks (RNNs) for
handling natural language processing and speech recognition tasks. As their
paper is purely a listing of work that others have done prior to them, their
contributions were mostly the synthesis of such information into a digestible
document. With that said, each section of their work can be summarized, which is
what I have done here.

DL allows for machine learning to surpass its previous limitations of having to
manually represent data in a suitable internal representation (through feature
extraction) by learning the representation itself. Current DL models are
typically trained using labeled datasets in what is known as supervised
learning. A sub-set of the data is used for training, which when ran through the
model, adjusts the hidden weights. These weights are adjusted using a technique
called stochastic gradient descent (SGD). SGD is accomplished by working
backwards through the model and taking the derivative of each weight which is
then used to adjust the hidden weights. Algorithms to do this include `tanh(x)`
and `ReLU`. `ReLU` is the most popular algorithm for this task which is more
commonly known as backpropagation.

Convolutional neural networks (ConvNets) are useful for analyzing data
structured as a series of multi-dimensional arrays. A typical application of
ConvNets are for analyzing images. RNNs are useful for analyzing data that is
dependent upon prior understanding. Chat bots, speech recognition, and answering
questions about data (i.e.,, where is a character in a book?) are all problems
that are reliant upon the model having some sort of "memory". Memory solutions
include `long short-term memory` which has been useful for accomplishing these
tasks.

______________________________________________________________________

## Summarization Technique

This paper was summarized using a modified technique proposed by S. Keshav in
his work *How to Read a Paper* \[0\].

## Citations
