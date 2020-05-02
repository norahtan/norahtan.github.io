---
title: Sequences, Metric Spaces, and Continuity
date: 2020-04-10 20:11:07
category: 
    - Mathematics
tags: 
    - topology
    - analysis
mathjax: true
---
> "The events in our lives happen in a sequence in time, but in their significance to ourselves they find their own order, a timetable not necessarily - perhaps not possibly - chronological. The time as we know it subjectively is often the chronology that stories and novels follow: it is the continuous thread of revelation." –– Eudora Welty, *On Writing*

Before I officially learned the definition to continuous functions in my first college real analysis class, I thought I would comprehend it easily since I had got some experience with the $\delta, \epsilon$ style of definitions in high school. So, I skimmed through the sequential definitions to both continuous functions and limit points, but, apparently, only to find my mind completely blank when reading the homework questions. 

It was not until then when I realized that I have been overestimating myself. So I went back to the famous textbook written by Rudin and all of accessible class materials. This article summarizes what I found the most critical and interesting in understanding sequences, metric spaces, and continuous functions and their relations.

The concept of sequences is helpful or even essential in understanding the metric topology, continuity, and later on the function space. So, we will start from here. 

---

## Perceive metric spaces through sequences

### On sequences themselves

<center>Convergence &#8594 Cauchyness &#8594 Completeness </center>

- Convergence: the sequence *converges to an element* in X.
- Cauchyness: an *intrinsic* understanding of convergence of the sequence.
- Completeness: a property ascribed to the space when *all Cauchy sequences converge*. 

The definition to a sequence {$x_n$}$_n$ in a metric space $(X, d)$ is simple, as every member in the sequence can be listed out in order. One vivid observation is to see sequences as a depiction of **\<distance\>**. For example, if we see that "elements in the sequence are getting closer and closer to a point in $X$", it means that the sequence converges to that element (point). Or, a "diminishing fluctuation among elements" implies an intrinsic convergence possessed by Cauchy sequences. 

### Sequential definitions

If every sequence in a metric space admits some properties, then it is natural to postulate that the space itself must adopt some *structural* features such that this is possible. Therefore, we have sequential definitions to many topology concepts, as \<metric\> enables a sense of "closeness" that is equivalent to the idea of neighborhood in the general topology. 

For example,

- If every sequence has convergent subsequences (i.e., sequentially compact), then the metric space is **compact**.
- If every Cauchy sequence converges, then the space is **complete**.
- If every convergent sequence converges to an element in the space, then the space is **closed**.

There are some other important concepts and theorems in metric spaces that are closely related to or can be understood from this sequential point view. For instance, total boundedness, the Bolzano-Weierstrass theorem, the Heine-Borel theorem, and the Characterization of compactness. 

One of my favorite proofs just comes from a statement in the Characterization of compactness. It claims that if a metric space $X$ is complete and totally bounded, then $X$ is sequentially compact. The proof starts with assuming towards contradiction that there exists a sequence that has no convergent subsequence. Then it proceeds to disapprove compactness with a brilliant utilization of Cantor diagonalization argument: a construction of open balls with certain radius. 

In case there are any interested readers, the following link provides a detailed illustration of the proof. But of course, you can always find other versions online as it is very classic. 

[https://www.colorado.edu/amath/sites/default/files/attached-files/compact_sequential.pdf](https://www.colorado.edu/amath/sites/default/files/attached-files/compact_sequential.pdf) 

---

## Perceive continuous functions through sequences

> **Theorem (Characterization of continuity)**: Let $(X, d_X)$ and $(Y, d_Y)$ be two metric spaces. Then the following are equivalent:
> 1. $f$ is continuous at with respect to the metric topology;
> 2. $f$ is continuous at every $p\in X$: i.e., for every $p\in X$, every $\epsilon > 0$, there exists $\delta > 0$ such that $d_Y(f(x), f(p))<\epsilon$ whenever $d_X(x, p) < \delta$.
> 3. For every $p\in X$ and a sequence {$x_n$} with $x_n\to p$, we have $\lim_{n\to\infty} f(x_n) = f(p)$, i.e., $f(x_n)\to f(p)$.

This sequential definition to continuous functions is not hard to comprehend now after we have gone through the basics for sequences and metric spaces. It is just a process of unfolding $x\to p$ as into $x_n\to p$. 

Within the context of distance set up by the sequential definition in metric spaces, we are able to perceive continuity as preserving everything locally. More specifically, everything that is in a small neighborhood (i.e., $B_{\delta}(x)$ with respect to metric $d_X$) of a point $x\in X$ will still be in a small neighborhood (i.e., $B_{\epsilon}(f(x))$ with respect to metric $d_Y$) of the point $f(x)\in Y$ after the continuous mapping. 

For more general topological spaces, we can easily generalize the neighborhood of "open balls" into general open sets. As every open set is preserved by mapping "continuously", then local structure will be preserved which further enables the preservation of the entire topological structure. 

---

## How continuity preserves the structure of spaces

As we mentioned above, continuity preserves the structure of topological spaces. More precisely, in the theory of topology, the continuous functions are those maps between two topological spaces that preserve neighborhood via the pullback of their preimages. Therefore, basic properties of the space, such as compactness and connectedness, are passed into the continuously projected space too. 

### Extreme value theorem and compactness

The extreme value theorem is a consequence of the preservation of compactness. We start with the basic theorem saying that if $X$ is compact and function $f:X\to Y$ is continuous, then the image $f(X)$ is compact in $Y$. Then, consider the case when $Y = \mathbb{R}$. According to the Heine-Borel theorem, a subset of $\mathbb{}R$ is compact if and only if it is closed and bounded. Therefore, there must exist a minimizer and a maximizer on $f(X)$. 

### Intermediate value theorem and connectedness

The intermediate value theorem is a consequence of the reservation of connectedness. Similarly, we have the basic theorem that if $X$ is connected and function $f:X\to Y$ is continuous, then the image $f(X)$ is also connected in $Y$. Still consider the special case when $Y = \mathbb{R}$ with addition to $X = [a, b]\in \mathbb{R}$. 

By the lemma that subset on $\mathbb{R}$ is connected if and only if it is an interval, we can conclude that both $[a, b]$ and $f([a, b])$ are connected and being two intervals. Naturally following from that, for every $y$ that falls in between $f(a)$ and $f(b)$ on $\mathbb{R}$, it also falls into the range of the function.

---