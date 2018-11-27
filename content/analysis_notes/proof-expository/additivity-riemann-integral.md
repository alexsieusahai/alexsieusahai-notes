---
title: Additivity of Riemann Integrals
weight: 4
chapter: true
pre: "<b>0d. </b>"
---
# Addivitiy of Riemann Integrals

This is an alternative proof than what was presented in my lecture, so it could be wrong.

First, we will formally state the proposition:  

Let \\(a < b < c\\). A function \\(f: [a,c] \mapsto \mathscr{R} \\) if and only if
\\(f\\) is Riemann integrable on \\([a,b]\\) and \\([b,c]\\). If \\(f\\) is Riemann integrable,
then \\( \int\_a^c f = \int\_a^b f + \int\_b^c f\\).

The idea behind the proof is quite basic; we take the parition that we get when we apply a common theorem that shows up a lot in proving stuff about Riemann integrals that states:

\\(f \in \mathscr{R} [a,b] \iff \forall \epsilon > 0 \exists P | U(P, f) - L(P, f) < \epsilon.\\)

Then, all we have to do is break \\(P\\) into two partitions on \\(b\\), then we use the fact that the functions \\(L, U\\) evaluate to real numbers to use the left-to-right part of the above theorem to prove that \\(f\\) is Riemann integrable on \\([a,b]\\), and similarly for \\([b,c]\\). Then, the result is true.

**Proof:**  
Let \\(\epsilon > 0\\). Then we have that there exists a partition \\(P = \\{x_0, x_1, ..., x_n\\}\\) where \\(x_0 = a, x_n = b\\), such that \\( U(P, f) - L(P, f) < \epsilon' \\). 

Let \\( P' = P \cup \\{b\\}\\). Then we have that \\( U(P', f) - L(P', f) < \epsilon' \\).  
This follows from the fact that \\(P'\\) is a refinement of \\(P\\).

Let \\(P_1 = P' \cap [a, b], P_2 = P' \cap (b, c]\\). Then we have that \\(P_1 \cup P_2 = P'\\).   
So, we have that  
\\( U(P_1, f) + U(P_2, f) - (L(P_1, f) + L(P_2, f)) = U(P', f) - L(P', f). \\)
Let \\( \epsilon = \epsilon' + U(P_2, f) - L(P_2, f) \\). Then we have that 
\\( U(P_1, f) - L(P_1, f) < \epsilon \\), as required. So \\(f \in \mathscr{R}[a,b]. \\)  
Similarly, it can be proven that \\(f \in \mathscr{R}[b, c]. \\)  
This completes the proof.
