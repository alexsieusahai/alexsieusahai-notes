---
title: Cantor's Theorem
weight: 4
chapter: true
pre: "<b>0c. </b>"
---
# Explanation of Proof of Cantor's Theorem

First, the statement:  
\\( \mathbb{R} \\) is uncountable. 

Let's first remind ourselves of what it means for a set \\(S\\) to be uncountable. A set \\(S\\) is uncountable if there does not exist a bijection \\( f: S \mapsto \mathbb{N} \\). 

Similarly, let's remind ourselves of the following definitions:

A function \\(f\\) is a bijection if \\(f\\) is an injection and \\(f\\) is a surjection.

 A function \\(f\\) is a surjection if for every element \\(y\\) in the range of \\(f\\), there exists an \\(x\\) in the domain of \\(f\\) such that \\(f(x)) = y \\). 

A function \\(f\\) is an injection if for any \\(x, y \in R(f) \\), where \\(R\\) denotes the range of \\(f\\), if \\( f(x) = f(y) \\) then \\( x = y \\).

It is imperative that we have no ambiguity about what these terms mean, which is why I stated them. 

_Idea:_ We know from the nested interval property that if you arbitrarily take nested intervals of any starting interval on a real number line, the intersection of all of those nested intervals is nonempty. What does this mean for the countability of \\( \mathbb{R} \\)? We can have some kind of endless duel, where on the \\(n^{th}\\) round, the bijection picks some number \\(f(n)\\), and the interval shrinks to avoid that number. Since we know that we can't get all of the numbers by the Nested Interval Property, then we know that \\(f\\) is not a bijection. Since \\(f\\) was arbitrary, we know that there does not exist a bijection from the reals to the naturals.

One piece of ground we have to cover is that given any \\(x, a, b \in \mathbb{R}\\), where \\(a < b\\), we have to show that we can pick some \\( a', b' \in [a, b]\\) such that \\(a' < b'\\) and \\(x \not \in [a', b'] \\). We will make quick work of this:

**Lemma:** Suppose \\(a, b, x \in \mathbb{R}\\) and \\(a < b.\\) There exists \\(a', b' \in [a, b]\\) such that \\(a' < b'\\) and \\( x \not\in [a', b'] \\).

_Idea:_ If \\(x\\) is not in \\( [a, b] \\), our work is simple. Otherwise, we want to pick some kind of midpoint between \\(x\\) and \\(b\\), and take the left hand side. Notice that if \\(x = b \\), our midpoint idea fails, so we have to account for a seperate case for that.

**Proof:**
If \\( x \not \in [a, b]\\), pick \\(a' = a, b' = b\\). Then \\(x \not\in [a', b']\\). \\
If \\( x = b \\), pick \\(a' = a, b' = b/2\\). Then \\( x \not\in [a', b'] \\). \\
If \\( x \in [a, b) \\), pick \\( a' = \frac{x + b}{2}, b' = b \\). Then \\( x \not\in [a', b'] \\).

Now, we can finally produce a nice, easy to understand, slick proof of Cantor's Theorem:

**Proof:** Suppose that \\(\mathbb{R}\\) is countable. Then, there exists a function \\(f: \mathbb{R} \mapsto \mathbb{N} \\) such that \\(f\\) is a bijection. Let \\( a_1 = f(1) + 1, b_1 = f(1) + 2 \\). Then \\( f(1) \not\in [a_1, b_1] \\). Now, for all \\( k \in \mathbb{N} / \\{1\\} \\), pick \\
- \\( a_k > a\_{k-1}, b_k < b\_{k-1} \\),  \\
- \\( a_k < b_k \\), and  \\
- \\( f(k) \not\in [a_k, b_k] \\), which exists by the above lemma. \\
Then, by the nested interval property, there exists an \\(x \in \mathbb{R} \\) such that 
$$ x \in \cap\_{n=1}^\infty [a_n, b_n]. $$
Then \\(x\\) is not in the range of \\(f\\). So \\(f\\) is not a surjection. So \\(f\\) is not a bijection. This is a contraction. So \\( \mathbb{R} \\) is uncountable.
