---
title: Open Closed Complement Relationship
weight: 5
chapter: true
pre: "<b>0e. </b>"
---
# Open Closed Complement Relationship in Metric Spaces

First, the statement of the proposition:  
Let \\( (X,d) \\) be a metric space. A subset \\( F \subset X \\) is closed if and only if \\( F^c = X / F \\) is open.

If you are comfortable with the concept of closed and open in metric spaces this is very trivial to prove. If you are not, this statement probably doesn't make any sense. Let's rectify this with definitions and accompanying intuitive explanations (a lot of real analysis at the introductory level seems to be about converting intuition into formal language; it is highly recommended that you read the intuitive explanation and try to restate it, draw diagrams about what's going on, etc until you can grok it easily).

_Definition:_ The function \\( B: (X, \mathbb{R}^+) \mapsto Y \subset X \\) defined in a metric space \\( (X, d) \\) is \\( B(x, r) := \{ y \in X: d(x,y) < r \} \\). This is an open ball of radius \\(r\\) about \\(x\\).

This is pretty self explanatory. Note that we do not include the boundary of the ball in this definition.

_Definition:_ An element \\( c \in X \\) is a cluster point of \\( S \\) is \\( B(c, \delta) \cap S \\ \{c\} \\) is nonempty for every \\( \delta > 0 \\).

No matter how small we make the radius of the ball excluding the center, There's always something within it. This might be kind of hard to visualize, but I will present a mental model to understand geometrically what a cluster point is using open balls, for metric spaces. Assume \\( c \\) has the properties above. Imagine an open ball of radius \\( \delta \\) in the three dimensional case, excluding the center of the ball (this is an infintesimally small point). No matter how small we shrink \\( \delta \\), we can fit stuff in between \\( \delta \\) and \\( c \\), because the exclusion of \\( c \\) is infintesimally small.

_Definition:_ A subset \\( F \subset X \\) is closed if \\(F\\) contains every cluster point of itself.

Practically all we need to understand to prove the above proposition is that if there exists some point \\( c \in X / F \\) that is a cluster point of \\( F \\), then \\(F\\) is not closed.

Now, lets try to understand the idea of the right direction. Assume \\(F\\) is closed. Then, for any \\(c \in F^c\\), we have that there exists some \\( \delta > 0 \\) such that the open ball of radius \\( \delta \\) about \\(c\\) does not intersect with \\(F\\). Since it does not intersect with \\(F\\), it must be that the open ball is in \\(F^c\\)! But then there exists some \\( \delta > 0 \\) such that \\(B(c, \delta) \subset F^c\\)! That is precisely what it means to be open!

*Proof for right direction:*  
Suppose \\(F\\) is closed. Let \\( x \in F^c \\). Then by definition of closed, we have that there exists \\( \delta > 0 \\) such that \\(B(x, \delta) \not\subset F \\). But since \\(F \cup F^c = X\\), we have that \\(B(x, \delta) \subset F\\). So, for any \\( x \in F^c \\), we have that for some \\( \delta > 0 \\), \\( B(x, \delta) \subset F^c \\). Then \\( F^c \\) is open.

Now, the left direction is very similar. If \\(F^c\\) is open, we have that for any \\(x \in F^c \\), there's some \\( \delta > 0 \\) such that \\(B(x, \delta) \subset F^c\\). But if that ball is in \\(F^c\\), it cannot be in \\(F\\)! So it cannot be a cluster point.

*Proof for the left direction:*  
Assume \\(F^c\\) is open. Let \\( x \in F^c \\). Then, there exists \\( \delta > 0 \\) such that \\( B(x, \delta) \subset F^c \\). Since \\( F \cap F^c = \emptyset \\), we have that \\( B(x, \delta) \not\subset F\\). So, there exists \\( \delta > 0 \\) such that \\(B(x, \delta) \cap F / \{x\} = \emptyset \\). So \\(x\\) is not a cluster point of \\(F\\). So \\(F\\) contains all of its cluster points. So \\(F\\) is closed. This completes the proof.
