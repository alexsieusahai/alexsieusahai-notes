---
title: Lemma 1.3.8
weight: 2
chapter: true
pre: "<b>0a. </b>"
---

# Lemma 1.3.8 - Understanding Analysis
### Alternative Proof

The phrasing of the statement in my notes is as follows:  
Suppose \\(M\\) is an upper bound for a non-empty set \\(E \subset \mathbb{R}\\). Then \\( M = supE \\) if and only if for every \\( \epsilon > 0 \\), there exists \\( x \in E \\) such that \\( x > M - \epsilon \\).

Before presenting the proof I'd like to talk about the main ideas behind the proof. This seems like an easy lemma to prove so there might not be very much to talk about, but nevertheless if you cannot grok the idea it will make proving it much harder.

The cornerstone here is that \\(M\\) is the least upper bound, so shifting M down even a little more should intuitively violate the fact that \\(M\\) is the least upper bound; if we could shift \\(M\\) down a little more and get another lower bound, that would then be the supremum, and not \\(M\\). That is the main idea of the forward direction. Similarly, if we assume that we have some upper bound \\(M\\) such that if we shift it down even a little bit, we find some element bigger than it. So, if we take an upper bound of \\(E\\) even a tiny \\(\epsilon\\) smaller than \\(M\\), we violate the fact the aforementioned element is an upper bound. This is the cornerstone of the backward direction.

**Proof:**  
\\( (\rightarrow) \\) Suppose \\( M = sup E \\). Then, suppose there exists \\( \epsilon > 0 \\) such that \\( \forall x \in E, x \leq M - \epsilon \\). But then \\( M - \epsilon \\) is an upper bound for \\(E\\), and \\( M - \epsilon < M \\). But \\( M = sup E \\), which is a contradiction.  \\
\\( (\leftarrow) \\) Suppose that \\( \forall \epsilon > 0, \exists x \in E \\) such that \\( x > M - \epsilon \\). Suppose there exists \\( M' \in \mathbb{R} \\), such that \\( M' < M \\) and \\( M' \\) is an upper bound for \\(E\\). 
Since \\( M' < M, \exists \epsilon' > 0 \\) such that \\( M - \epsilon' = M' \\). By the first statement, there exists \\( x \in E \\) such that \\( x > M - \epsilon' = M' \\). So \\( x > M'\\). But \\(M'\\) is an upper bound for \\(E\\). This is a contradiction. So \\(M = supE \\). 
