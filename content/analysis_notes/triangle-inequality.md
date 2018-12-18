---
title: Triangle Inequality
weight: 6
chapter: true
pre: "<b>0g. </b>"
---

# Triangle Inequality
### A very simple proof I found

The statement of triangle inequality is as follows:  
Let \\(x, y \in \mathbb{R}\\). Then \\(|x-y| \leq |x| + |y|\\).  

I've only ever seen the case by case proof for triangle inequality, which I find inelegant. This proof is quite simple, 
it just hinges on the fact that \\( |x|^2 = x^2 \forall x \in \mathbb{R}\\). One thing I am not a fan of is that
this proof is by contradiction when there exists a direct proof; it might be that there's an even simpler proof without it.

Suppose \\(|x-y| > |x| + |y|\\). Then \\(|x-y|^2 > (|x| + |y|)(|x-y|) > (|x|+|y|)^2\\). Notice \\( |x-y|^2 = (x-y)^2\\).  
We then have that
\\(x^2 - 2xy + y^2 > |x|^2 + 2|x||y| + |y|^2. \\)  
Notice that \\(|x|^2 = x^2, |y|^2 = y^2\\), so we have that  
\\( -2xy > 2|x||y| \\),  
which is a contradiction. So the triangle inequality is true.
