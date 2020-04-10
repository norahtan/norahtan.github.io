---
title: Sequences (TBD)
date: 2020-04-10 20:11:07
category: 
    - Mathematics
tags: 
    - topology
    - analysis
mathjax: true
---
> "The events in our lives happen in a sequence in time, but in their significance to ourselves they find their own order, a timetable not necessarily - perhaps not possibly - chronological. The time as we know it subjectively is often the chronology that stories and novels follow: it is the continuous thread of revelation." –– Eudora Welty, *On Writing*

The concept of sequences is helpful or even essential in understanding the metric topology, continuity, and later on the function space. 

## Perceive metric spaces through sequences

### On sequences themselves

<center>Convergence &#8594 Cauchyness &#8594 Completeness </center>

- Convergence: the sequence *converges to an element* in X.
- Cauchyness: an *intrinsic* understanding of convergence of the sequence.
- Completeness: a property ascribed to the space when *all Cauchy sequences converge*. 

The definition to a sequence $\{x_n\}_n$ in a metric space $(X, d)$ is simple, as every member in the sequence can be listed out in order. One vivid observation is to see sequences as a depiction of **\<distance\>**. For example, if we see that "elements in the sequence are getting closer and closer to a point in $X$", it means that the sequence converges that element (point). Or, a "diminishing fluctuation among elements" implies an intrinsic convergence possessed by Cauchy sequences. 

### Sequential definitions

If every sequence in a metric space admits some properties, then it is natural to postulate that the space itself must adopt some *structural* features such that this is possible. Therefore, we have sequential definitions to many topology concepts, as \<metric\> enables a sense of "closeness" that is equivalent to the idea of neighborhood in the general topology. 

For example,

- If every sequence has convergent subsequences (i.e., sequentially compact), then the metric space is **compact**.
- If every Cauchy sequence converges, then the space is **complete**.
- If every convergent sequence converges to an element in the space, then the space is **closed**.

There are some other important concepts and theorems in metric spaces that are closely related to or can be understood from this sequential point view. For instance, total boundedness, the Bolzano-Weierstrass theorem, the Heine-Borel theorem, and the Characterization of compactness. One of my favorite proofs just comes from one of statements in the Characterization of compactness. It claims that if a metric space $X$ is complete and totally bounded, then $X$ is sequentially compact. I have included this proof at the end of this article, in case there are any interested readers. 

## Perceive functions through sequences

## A proof for one statement in the Characterization compactness