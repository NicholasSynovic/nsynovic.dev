---
title: A summary of The Random Subspace Method for Constructing Decision Forests by
  Tin Kam Ho
description: Posted in the IEEE TRANSACTIONS ON PATTERN ANALYSIS AND MACHINE INTELLIGENCE,
  1998
summary: Posted in the IEEE TRANSACTIONS ON PATTERN ANALYSIS AND MACHINE INTELLIGENCE,
  1998

categories: [summary, 1998, Pattern recognition, decision tree, decision forest, stochastic
      discrimination, decision combination, classifier combination, multiple-classifier
      system, bootstrapping]
citations: [https://doi.org/10.1145/1273445.1273458, https://doi.org/10.1109/34.709601,
  https://doi.org/10.1109/34.632990, https://doi.org/10.1002/widm.8, https://doi.org/10.1613/jair.63,
  https://doi.org/10.1109/ICDAR.1995.598994, https://doi.org/10.1109/ICPR.1998.711201]

draft: false

date: 2022-11-09T15:17:53-06:00
featured_image: ''
include_toc: true
markup: md
outputs: []
show_comments: false
toc: false
show_reading_time: true
---

# A summary of *The Random Subspace Method for Constructing Decision Forests*

> Tin Kam Ho, IEEE TRANSACTIONS ON PATTERN ANALYSIS AND MACHINE INTELLIGENCE,
> 1998 [DOI](https://doi.org/10.1109/34.709601)

For the summary of the paper, go to the [Summary](#summary) section of this
article.

## Table of Contents

- [A summary of *The Random Subspace Method for Constructing Decision Forests*](#a-summary-of-the-random-subspace-method-for-constructing-decision-forests)
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

This paper addresses the problem of decision tree forest construction.

### Motivation

> Why should we care about this paper?

We should care about this paper as it compares eight forest construction
algorithms against the author's algorithm on publicly available datasets. This
allows the reader to understand the pros and cons of using a particular
algorithm over another as well as validating the author's claims. Furthermore,
this algorithm can monotonically increase in generalization accuracy while
preserving perfect accuracy.

### Category

> What type of paper is this work?

This is an algorithms paper.

### Context

> What other *types* of papers is the work related to?

This paper is related to papers that present ways of constructing random
forests.

### Contributions

> What are the author's main contributions?

Her main contributions were:

- An efficient algorithm for generating decision trees
- A comparison of 8 forest construction algorithms on publicly available
  datasets

______________________________________________________________________

## Second Pass

> A proper read through of the paper is required to answer this

### Background Work

> What has been done prior to this paper?

Work has been done before to describe what decision trees are, as well as how to
generate many of them for the purposes of classification.

### Figures, Diagrams, Illustrations, and Graphs

> Are the axes properly labeled? Are results shown with error bars, so that
> conclusions are statistically significant?

All of the tables are clear and easy to read. However, all of the line charts
are difficult to read as each line is the same color in my copy of the paper.
Additionally, figure 1 is difficult to tell what is supposed to represented.

### Clarity

> Is the paper well written?

I found this work hard to follow. I think that this is due to me not
understanding the problem domain, rather than her explanations.

### Relevant Work

> Mark relevant work for review

The following relevant work can be found in the [Citations](#citations) section
of this article.

2. Y. Amit, D. Geman, and K. Wilder, “*Joint Induction of Shape Features and
   Tree Classifiers*,” IEEE Trans. Pattern Analysis and Machine Intelligence,
   vol. 19, no. 11, pp. 1,300-1,305, Nov. 1997
3. L. Breiman, J.H. Friedman, R.A. Olshen, and C.J. Stone, *Classification and
   Regression Trees*. Belmont, Calif.: Wadsworth, 1984
4. D. Heath, S. Kasif, and S. Salzberg, “*Induction of Oblique Decision Trees*,”
   Proc. 13th Int’l Joint Conf. Artificial Intelligence, vol. 2, pp.
   1,002-1,007, Chambery, France, 28 Aug.-3 Sept. 1993.
5. T.K. Ho, “*Random Decision Forests*,” Proc. Third Int’l Conf. Document
   Analysis and Recognition, pp. 278-282, Montreal, Canada, 14-18 Aug. 1995.
6. T.K. Ho, “*C4.5 Decision Forests*,” Proc. 14th Int’l Conf. Pattern
   Recognition, Brisbane, Australia, 17-20 Aug. 1998.

### Methodology

> What methodology did the author's use to validate their contributions?

The author compared the performance of different forest generation methods
against her own generation method. The different forest generation methods were:

- Single feature split with best gain ratio
- Distribution mapping
- Class centroids
- Unsupervised clustering
- Supervised clustering
- Central axis projection
- Perceptron
- Support Vector Machine

### Author Assumptions

> What assumptions does the author(s) make? Are they justified assumptions?

The author assumes that the reader has worked with decision trees prior to
reading.

#### Correctness

> Do the assumptions seem valid?

Yes.

### Future Directions

> My own proposed future directions for the work

I'd like to learn more about decision trees and compare them against Deep
Learning models.

### Open Questions

> What open questions do I have about the work?

When would I ever use a decision tree over a SVM or DL model?

### Author Feedback

> What feedback would I give to the authors?

I'd appreciate the usage of color to separate different lines on the figures.
Additionally (and this could be due to the limited available citation), please
reduce the number of self-citations in future works.

______________________________________________________________________

## Summary

> A summary of the paper

The paper *The Random Subspace Method for Constructing Decision Forests* by Tin
Kam Ho \[1\] discusses a method of generating many decision trees efficiently
without affecting accuracy. She validates this method by comparing it against
eight other forest construction methods, all on publicly available datasets. The
benefits of her work is that it is parallelized; meaning that with some tuning
to the algorithm, it can run on multiple CPU cores or threads (potentially even
faster on GPU cores).

______________________________________________________________________

## Summarization Technique

This paper was summarized using a modified technique proposed by S. Keshav in
his work *How to Read a Paper* \[0\].

## Citations
