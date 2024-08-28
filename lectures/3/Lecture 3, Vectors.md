---
tags: [Notebooks/Linear Lectures]
title: 'Lecture 3, Vectors'
created: '2024-08-27T05:33:28.982Z'
modified: '2024-08-28T22:47:52.685Z'
---

# Lecture 3, Vectors

* **Prepared by:** Robert Conde

## Simple Definition of Vectors

Let's start off with *a* definition of a **vector**. We we will discuss what's good and bad about this simple definition.

<dl>
  <dt>Vector</dt>
  <dd>an ordered list of numbers</dd>
</dl>

What's good about this definitions is that we can represent *multi-component* quantities such as
 * force,
 * economic conditions,
 * images, and
 * *more!*

Furthermore, we *can* denote vectors as a (horizontal) list of numbers (e.g. some vector $v \in \mathbb{R}^3$ would be denoted $(a, b, c)$, where $a,b,c \in \mathbb{R}$), but instead often write them as a vertical list of numbers.

$$
\begin{pmatrix}
 a\\ b \\ c
\end{pmatrix}
$$

This will come in helpful when we peform vector operations, some of which are element-wise!

**Note:** The parentheses above just indicate the start and end of their respective list.

Unfortunately, this definition doesn't shed light on what we can do with vectors as we care about vectors & their algebra!

## Abstract Definition of Vectors & their Properties

The following abstract definition provides us with information regarding what we can do with our vectors.

<dl>
  <dt>Vector</dt>
  <dd>an element/member of a <i>vectorspace</i></dd>
  <dt>Vectorspace</dt>
  <dd>a set whose elements (vectors), can be added together and scaled</dd>
</dl>

More formally, a **vectorspace** $V$ over a field $F$ (we will often use $\mathbb{R}$) is a set along with a binary operation, called *vector addition* ($+: V \times V \rightarrow V$), and a binary function, called *scalar multiplication* ($\cdot: F \times V \rightarrow V$), that satisfies the following eight axioms:

1. **Associativity of vector addition:** $\forall \vec{u}, \vec{v}, \vec{w} \in V,\ \vec{u} + (\vec{v} + \vec{w}) = (\vec{u} + \vec{v}) + \vec{w}$
  *So, we can write $\vec{u} + \vec{v} + \vec{w}$ without confusion as no matter which order we evaluate, we get the same result.*

2. **Commutativity of vector addition:** $\forall \vec{u}, \vec{v} \in V,\ \vec{u} + \vec{v} = \vec{v} + \vec{u}$
  *So, we can rearrange additions.*

3. **Identity element of vector addition:** $\exists \vec{0} \in V,\ \forall \vec{v} \in V,\ \vec{v} + \vec{0} = \vec{0}$
  *Notice: $\vec{0}$ is **always** a member of $V$, so $\{\}$ is not a vectorspace and vectorspaces are always non-empty!*

4. **Inverse elements of vector addition:** $\forall \vec{v} \in V,\ \exists -\vec{v} \in V,\ \vec{v} + (-\vec{v}) = \vec{0}$
  *So, we can solve!*
  
5. **Compatibility of scalar multiplication with field multiplication:** $\forall a,b \in F \land \vec{v} \in V,\ a (b \vec{v}) = (a b) \vec{v}$

6. **Identity element of scalar multiplication:** for the multiplicative identity $1 \in F$, $\forall \vec{v} \in V,\ 1 \vec{v} = \vec{v}$
  *This allows us to simplify and defines a (the) "preserving" scalar.*

7. **Distributivity of scalar multiplication with respect to *vector* addition:** $\forall a (\vec{u} + \vec{v}) = a \vec{u} + a \vec{v}$
  *Linear combinations!*

8. **Distributivity of scalar multiplication with respect to *field* addition:** $\forall a,b \in F \land \vec{v} \in V,\ (a + b) \vec{v} = a \vec{v} + b \vec{v}$

**Note:** Vectorspaces are closed under $+$ and $\cdot$ by definition!

This effectively extends a field and makes it play nice with vectors under addition and multiplication.

## Operations on Vectors

Vector addition is an element-wise operation.

**Proof:**
1. Let $\vec{u}, \vec{v} \in V$ be denoted $(u_1, u_2, \ldots, u_n)$ and $(v_1, v_2, \ldots, v_n)$, respectively.
2. $\vec{u} = u_1 \vec{e_1} + u_2 \vec{e_2} + \ldots + u_n \vec{e_n}$
   $\vec{v} = v_1 \vec{e_1} + v_2 \vec{e_2} + \ldots + v_n \vec{e_n}$
   where $\vec{e_1} = (1, 0, 0, \ldots, 0),\ \vec{e_2} = (0, 1, 0, \ldots, 0),\ \ldots, \vec{e_n} = (0, \ldots, 0, 0, 1)$.
3. $\vec{u} + \vec{v} = (u_1 + v_1) \vec{e_1} + \ldots + (u_n + v_n) \vec{e_n}$
4. $\boxed{\vec{u} + \vec{v} = (u_1 + v_1, \ldots, u_n + v_n)}$

Similarly, we can show that scalar multiplication broadcasts (hint: express as linear combination of standard basis vectors).

## Geometric Description

Euclidean space and relations to language models.

> King + (Woman - Man) ≈ Queen

**Related to:** Principal component analysis.

## Linear Combinations

Where $\vec{b} = c_1 \vec{v_1} + c_2 \vec{v_2} + \ldots + c_p \vec{v_p}$, $\vec{b}$ is a **linear combination** of $\vec{v_1}, \vec{v_2}, \ldots, \vec{v_p}$ with weights $c_1, c_2, \ldots, c_p$.

We define the **span** of the set of vectors $\{\vec{v_1}, \ldots, \vec{v_p}\}$ to be set of all linear combinations of the vectors. Think of this *geometrically*! What kind of *space* does the span generate? What does it look like?!

