---
title: Nested Interval Property
weight: 3
chapter: true
pre: "<b>0b. </b>"
---
# Explanation of Nested Interval Property

The statement of Nested Interval Property is as follows:

Suppose \\( I\_n = [a_n, b_n] \\) are closed intervals for \\( n \in \mathbb{N} \\) such that \\( I\_{n+1} \subset I_n \\) for all \\( n \in \mathbb{N} \\). Then
$$ \cap\_{n=1}^\infty I_n \neq \emptyset. $$

The most illuminating thing I think we can notice about this statement (in terms of aiding our ability to prove it) is that for any \\(n, m \in \mathbb{N}\\), \\(a_n \leq b_m \\). This is due to the fact that \\( I\_{n+1} \subset I_n \\). So, what if we were to look at or just beyond the tip of every single \\( a_n \\) for every \\( n \in \mathbb{N} \\)? Does that element sit inside of every single interval? 

Well, we can cleverly use the definitions which we have established to do this. Notice that for any \\( n \in \mathbb{N}\\), we have that \\(b_n \geq a_m \forall m \in \mathbb{N} \\). So, thankfully, we have that any \\( b_n \\) is a upper bound for \\( \\{ a_n: n \in \mathbb{N} \\} \\). Now, we have all of the ideas to write up a clean and tight proof.

**Proof:** Let \\( A = \\{ a_n: n \in \mathbb{N} \\} \\). Let \\(x = supA \\). Then we have that \\( x \geq a_n \forall n \in \mathbb{N} \\). Since \\( \forall n, m \in \mathbb{N}, a_n \leq b_m \\), we have that \\( b_n \\) is an upper bound for \\( A \\). But \\( x \\) is the least upper bound, so we have that \\( x \leq b_n \forall n \in \mathbb{N} \\). So, we have that 
$$ a_n \leq x \leq b_n, \forall n \in \mathbb{N}. $$
So \\( x \in \cap\_{n=1}^\infty I_n. \\)
