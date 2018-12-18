---
title: Convergent Sequences are Bounded
weight: 6
chapter: true
pre: "<b>0f. </b>"
---
# Convergent Sequences are Bounded

While this is relatively straightforward to prove, it is a foundational theorem and I think it illustrates important proof techniques which help one come up with appropriate proofs for the convergence of arbitrary sequences. Aside from this, it's very practically useful in that it makes a lot of other theorems in introductory real analysis much easier to prove.

The proof will be done for sequences in the reals, then we will extend the result to arbitrary metric spaces.

First, a couple definitions to refresh your memory:

_Definition:_  
Let \\((x_n)\\) be an arbitrary sequence in the reals. We say that \\((x_n)\\) is _convergent_ if for all \\(\epsilon > 0\\) there exists an \\(N \in \mathbb{R}\\) such that \\( |x_n - x| < \epsilon \forall n \geq N \\).

_Definition:_  
Let \\((x_n)\\) be an arbitrary sequence in the reals. We say that \\((x_n)\\) is _bounded_ if there exists an \\(M\\) such that for all \\(n \in \mathbb{N}\\), we have that \\(x_n < M\\).

_Theorem:_  
Let \\((x_n)\\) be a convergent sequence in the reals. If \\((x_n)\\) converges to some \\(x\\) in the reals, we have that \\((x_n)\\) is bounded.

Also, here's an important statement about the absolute value function that will make this theorem very easy to prove:

\\( | x - y| < \epsilon \iff y - \epsilon < x < y + \epsilon. \\)

Lets lay out our plan of attack:  
From the definition of convergence, we kind of get a bound in of itself; \\( |x_n - x| \epsilon \implies x - \epsilon < x_n < x + \epsilon \implies x_n < x + \epsilon \\). So, we know that for some \\( \epsilon > 0 \\), there exists some \\(N \in \mathbb{N}\\) such that for all \\( n \geq N \\), we have that \\( x_n < x + \epsilon\\). But, what about the numbers before \\(N\\)? It's important to note that there's a finite number of these terms in \\((x_n)\\), and it can be shown easily by induction that this finite set admits a maximum (just go over each term, and if you see something bigger, replace it, until you get to the end, which is guaranteed since it's finite). So, we can just take the bound to be the maximum of our \\(\epsilon\\) choice, or the maximum of the terms before the \\(N\\) corresponding to the \\(\epsilon\\). Note that it doesn't really matter which epsilon we pick, so we'll just pick 1.

_Proof:_  
Let \\(\epsilon = 1\\). Then, since \\((x_n)\\) is convergent, we have that there exists an \\(N \in \mathbb{N}\\) such that for all \\(n \geq N\\), we have that \\( |x_n - x| < 1 \implies x_n < 1 + x \\). Let \\( M = max(1, max(\{ x_0, x_1, ..., x\_{n-1} \} )) \\). Let \\(n \in \mathbb{N}\\). Then we have that \\(x_n < M \\). So \\((x_n)\\) is bounded.

Extending this result to metric spaces is very easy, with one insight. First, definitions to refresh your memory:

_Definition:_  
Let \\( (X, d) \\) be a metric space. Let \\( (x_n) \\) be a sequence in \\(X\\). We say that \\( (x_n) \\) is _bounded_ if \\( \{ x_n: n \in \mathbb{N} \} \\) is bounded.

_Definition:_  
Let \\( (X, d) \\) be a metric space. Let \\( (x_n) \\) be a sequence in \\(X\\). We say that \\( (x_n) \\) is _convergent_ if there exists an \\(x \in X\\) such that for all \\( \epsilon > 0\\), we have that \\(d(x_n, x) < \epsilon\\). We say that \\( (x_n) \\) converges to \\(x\\), in this case.

Notice that then, we have that \\( |d(x_n, x) - 0| = d(x_n, x) \\). So, we have that \\( (x_n) \\) converges to \\(x\\) if and only if \\( d(x_n, x) \\) converges to \\(0\\). Now, using this fact, extending the result is easy:

_Theorem:_  
Let \\( (X, d) \\) be a metric space. Let \\( (x_n) \\) be a sequence in \\(X\\). If \\( (x_n) \\) is convergent, we have that \\( (x_n) \\) is bounded.

_Proof:_  
Since \\( (x_n) \\) is convergent, we have that \\( \lim\_{n\to\infty} d(x_n, x) = 0 \\). So we have that \\( \lim\_{n\to\infty} x_n = x \\). Since \\( (x_n) \\) is bounded in the reals, we have that there exists some \\(M\\) such that \\( x_n \leq M \\) for all \\(n \in \mathbb{N}\\). So \\( \{ x_n: n \in \mathbb{N} \\) is bounded.
