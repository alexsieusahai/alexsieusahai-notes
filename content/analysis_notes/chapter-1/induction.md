---
title: Induction
weight: 3
chapter: true
pre: "<b>1c. </b>"
---

# Induction

First, we will need the axiom known as the _Well Ordering Property of the naturals._

_Well Ordering Property of \\(\mathbb{N}\\):_ Every nonempty subset of \\(\mathbb{N}\\) has a smallest element. 

_Theorem:_ (Principle of Induction)  
Let \\(P(n)\\) be a statement depending on a natural number \\(n\\). Suppose that

(i) \\(P(1)\\) is true, and  
(ii) if \\(P(n)\\) is true, then \\(P(n+1)\\) is true.

Then \\(P(n)\\) is true for all \\(n \in \mathbb{N}.\\)

The cornerstone of why this statement is true is (i); it's the beginning of the chain of true statements. Then 2 is true, and since 2 is true, 3 is true, and since 3 is true, 4 is true, ... What if there's a false element in this list? Well, it can't be 1, since we know 1 is true by (i). So it must be something bigger than 1. Let's call this element \\(x\\). Let's consider \\(x-1\\). What if \\(x-1\\) is false too? Well, lets consider \\(x-1-1=x-2\\). If \\(x-2\\) is also false, keep looking farther down until you either hit a true statement, or you hit 1, which we know must be true. Instead of recursively looking down and down, lets just take the smallest element before 1 that's false, and use this above logic. Lets formalize this idea in a proof now.


**Proof:** Assume (i) and (ii) are true. Suppose that there exists some \\(n \in \mathbb{N}\\) such that \\(P(n)\\) is false. Then, the set \\( A = \\{n \in \mathbb{N}: P(n) \text{ is false}\\} \\) is nonempty. By the well ordering property, there exists a smallest element \\(a \in A\\) such that \\(P(a)\\) is false. Since \\(P(1)\\) is true, we know that \\(a > 1\\). Consider \\(a-1\\). Since \\(a\\) is the smallest element in \\(A\\), we know that \\(a-1 \not\in A\\) and therefore \\P(a-1)\\) is true. By (ii), \\(P(a)\\) is true. So then \\(a \not\in A\\). But then \\(a \in A\\) and \\(a \not\in A\\), which is a contradiction. So, \\(A\\) is empty. So for all \\(n \in \mathbb{N}\\), we have that \\(P(n)\\) is true. This completes the proof.

My only exercise I suggest for you is to try to reproduce the proof on paper, knowing the main idea. Make sure that you understand the main idea of the proof, which will make reproducing it a matter of mechanics and comfort with proof writing. For practice, there is a wealth of good problems on induction in any discrete mathematics book or introductory text in analysis, which would probably be more illuminating than anything I can remember right now.
