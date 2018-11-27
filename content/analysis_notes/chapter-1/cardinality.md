---
title: Cardinality
weight: 4
chapter: true
pre: "<b>1d. </b>"
---

# Cardinality

When dealing with the infinite, we might want to have a way of understanding size. 

_Definition:_ Let \\(A\\) and \\(B\\) be sets. We say that \\(A\\) and \\(B\\) have the same _cardinality_, and write
$$ |A| = |B| $$
when there exists a bijection \\(f: A \mapsto B\\).

Recall that a bijection is a function that is injective and surjective. Recall that a injective function is informally a function that has one unique mapping for every element in its range, and a surjective function is informally a function with at least one mapping for every element in its range. So a bijective function is informally a function with exactly one mapping for every element in its range.

It's worth noting that two finite sets \\(A\\) and \\(B\\) have the same cardinality if and only if they contain the same number of elements. This is easily proven with the Pigeonhole Principle.

A great example of cardinality is the fact that \\( |\mathbb{N} \times \mathbb{N}| = |\mathbb{N}| \\). Suppose there exists a function \\(f\\) such that 
(1, 1) maps to 1, (1, 2) maps to 2, (2, 1) maps to 3, (1, 3) maps to 4, (2, 2) maps to 5, (3, 1) maps to 6, (1, 4) maps to 7, (2, 3) maps to 8, (3, 2) maps to 9, (4, 1) maps to 10...  
Then for all \\(a \in \mathbb{N}\\) there exists \\((n, m) \in \mathbb{N} \times \mathbb{N}\\) such that \\( f((n, m)) = a \\), so \\(f\\) is surjective. \\
Take any \\( (n_1, m_1), (n_2, m_2) \\) such that \\( f((n_1, m_1)) = f((n_2, m_2)) \\). It follows that \\( n_1 = m_1 \\) and \\( n_2 = m_2 \\). So \\(f\\) is injective. So \\(f\\) is a bijection. So \\( |\mathbb{N} \times \mathbb{N}| = |\mathbb{N}| \\).

A piece of notation that's commonly used is as follows:  
let \\(A\\) and \\(B\\) be sets. If there exists an injection from \\(A\\) to \\(B\\), we write \\( |A| \leq |B| \\).  

A useful theorem with a very long proof is the Burnside-Schroder Theorem.  
_Theorem:_ Let \\(A\\) and \\(B\\) be sets. If
$$ |A| \leq |B| \text{ and } |B| \leq |A|, $$
then \\( |A| = |B| \\).

The following theorem validates our intuiton for any finite set being as least as big as the naturals:  

_Proposition:_ If \\(A\\) is an infinite set, then \\( |\mathbb{N}| \leq |A| \\).

_Idea:_ Imagine you have a bag of infinite, but unique, things. We can think of this bag as our infinite set \\(A\\). Pull something out of the bag, which we will denote as \\(a_1\\). Then that is our _first_ element. Our bag is now \\(A / \\{ a_1 \\} \\). Pull something else out of the bag, which we will denote as \\(a_2\\). Notice that this can't be the same element as \\(a_1\\), since we already pulled \\(a_1\\) out of the bag. This is our _second_ element. In general, on the \\(k^{th}\\) pull our bag before is \\( A / \\{ a_1, a_2, ..., a\_{k-1} \\} \\) and our new element is denoted \\(a_k\\). With this, our element corresponding to \\(a_k\\) must be unique, as it is bounded below by what it can't be, and is bounded above by what \\(a\_{k+1}, a\_{k+2}, ... \\) must be.

_Proof:_ Define \\(a_k\\) to be an arbitrary element of \\( A / \\{ a_1, a_2, ..., a\_{k-1} \\} \\). Notice that for any \\( k \in \mathbb{N} \\) we have that \\( A / \\{ a_1, a_2, ..., a\_{k-1} \\} \\) is nonempty since \\(A\\) is infinite. Then \\( f: A \mapsto \mathbb{N} \\) such that for any element \\( \\{ a_k \in A \\} \\) we have that \\( f(a_k) = k \\). Pick any two elements \\( a_n, a_m \in A \\). Assume that 
$$ f(a_n) = f(a_m). $$
Then we have that \\( n = m \\). So \\(f\\) is injective.

Finally, we will finish with the following theorem
