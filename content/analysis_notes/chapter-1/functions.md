---
title: Functions
weight: 2
chapter: true
pre: "<b>1b. </b>"
---

# Functions
I will assume you are comfortable with the ideas of the domain of a function, the range of the function, and composition of functions. These do not need to be updated with regard to our high school knowledge.

The first construct I will need is something called the _Cartesian Product_: \\
_Definition:_  Let \\(A\\) and \\(B\\) be functions. The cartiesian product of \\(A\\) and \\(B\\), denoted \\(A \times B \\), is 
$$ A \times B = \{ (a, b) | a \in A, b \in B \}. $$

Now we have all of the tools to state the definition of a function. It might seem a little arcane, but we will see why it must be so soon.  
_Definition:_  A function \\(f: A \mapsto B\\) is a subset \\(f\\) of \\(A \times B\\) such that for each \\( x \in A \\), there is a _unique_ \\( y \in B \\) so that \\( (x, y) \in f \\).

Let's first try to grok this idea; let's try to utilize our intuition from high school math of what a function is, and try to understand how a function comes about. Lets examine the function
$$ f(x) = x^2. $$

Let the domain of \\(f\\) be \\(\mathbb{R}\\). Then, for any \\( x \in \mathbb{R} \\), we have \\( f(x) = y \\) for some \\( y \in \mathbb{R} \\) such that \\( y = x^2 \\). Then, it is plausible that we could encode the idea of \\(f\\) as some kind of mapping, like a dictionary, of \\(x \in \mathbb{R} \\) to \\( y \in \\{a \in \mathbb{R}: a \geq 0\\} \\). In particular, we could define \\(f\\) as \\( f \subset \mathbb{R} \times \mathbb{R} \\), and have \\(f(x)\\) denote the element \\( y \\) such that \\( (x, y) \in f \\). 

Now I have shown that our new definition of a function here is plausible, but I have not shown why it might be necessary. Consider some set of objects \\( A = \\{ a, b, c \\} \\), and \\( B = \\{ d, e, f \\} \\). We would like to define a function \\(f\\) such that \\( f(a) = d, f(b) = d, f\(c\) = f \\). We can no longer do this with algebraic formulas. This is a contrived example, but the point I am trying to illustrate is that we would like to take the yoke of numbers off and deal with functions of any kind of object to any kind of object.

Now that we have moved away from the idea of algebraic formulas and moved towards this set approach, you might be wondering if there is a shorthand for defining a function in terms of a set of objects. We have two main tools for this; _image_ and _inverse image_.  

_Definition:_ Let \\(f: A \mapsto B\\) be a function, and \\( C \subset A \\). The _image_ of \\(C\\) is
$$ f\(C) := \\{ f(x) \in B: x \in C \\}. $$

_Definition:_ Let \\(f: A \mapsto B\\) be a function, and \\( C \subset B \\). The _inverse image_ is
$$ f\(C) := \\{ x \in A: f(x) \in C \\}. $$

Finally, the last little bit of foundation building we have to do is define and explain the ideas of _injectivity_ (one to one) and _surjectivity_ (onto).  

_Definition:_ Let \\(f: A \mapsto B\\) be a function. We say that \\(f\\) is injective if \\(f(x) = f(y)\\) if and only if \\(x = y\\).  

In other words, a function is _injective_ if every element in the range is connected to 1 or 0 elements in the domain.  

_Definition:_ Let \\(f: A \mapsto B\\) be a function. We say that \\(f\\) is surjective if \\(f(A) = B\\). 

In other words, a function is _surjective_ if every element in the range is connected to at least 1 element in the domain. 

Finally, a function \\(f\\) is _bijective_ if \\(f\\) is both surjective and injective. We then say that \\(f\\) is a bijection. 

Here are some important exercises that I think are worth doing. I will try my best to restate where I remembered them from.  
- Restate the definitions of cartesian product, function, image, reverse image, injectivity, and surjectivity.   
- Give examples of functions that are injective. Give examples of functions that are surjective. Give examples of functions that are bijective.  
- Show that there exists functions \\(f, g\\) such that \\(f\\) is surjective but \\(f \circ g \\) is not surjective.  
- Show that if \\(f\\) and \\(g\\) are injective, \\(f \circ g \\) is injective. (Understanding Analysis)  
- Show that there exists functions \\(f, g\\) such that \\(f \circ g\\) is surjective but \\(f\\) or \\(g\\) is not surjective.  
- Suppose \\(f, g\\) are surjective. Show that \\( f \circ g \\) is surjective.  
- Prove that 
$$ f^{-1}(B_1 \cap B_2) = f^{-1}(B_1) \cap f^{-1}(B_2). $$
I recommend that you first sketch out an idea, then try to formalize that idea.
