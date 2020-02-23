---
description: >-
  A brief overview of linear combinations, dependence, independence,
  transformations, inner product, and a few others
---

# Linear Operations

## Linear Combinations

Linear combinations logically follow from the matrix operations covered in "[Basics](vectors.md)" - simply put, it's a combination of two vectors, scaled by numbers.

$$ |x\rangle = a |a\rangle + b |b\rangle$$

Here $$ |x\rangle$$is a linear combination of the vector $$|a\rangle$$scaled by the constant $$a$$ and the vector $$|b\rangle$$scaled by the constant $$b$$.

## Linear Dependence

So if we have a set of vectors, how do we define the relationships between those vectors, and what do those relationships tell us about the whole system? Well, in the example above we have a set of three vectors - $$|x\rangle, |a\rangle, |b\rangle$$.

$$|x\rangle$$is dependent on$$|a\rangle$$and$$|b\rangle$$, because $$|x\rangle$$ is defined by$$|a\rangle$$and$$|b\rangle$$. Without them,$$|x\rangle$$could not exist. And since one of the vectors in the set is dependent on one of the other vectors in the set, the whole set can be said to be _linearly dependent_.

## Linear Independence 

So if a set includes a vector which can be described as a linear combination of other vectors in the same set, then the whole set is said to be linearly dependent.

Logically, if this is not the case, and none of the vectors in the set can be described as linear combinations of each other, the whole set is said to be _linearly independent_.

## Transformations

We can transform a vector to change it into another vector. In general, this vector can be in the same or in a different "vector space" - for example, a vector along one plane could transform into a vector along another plane. 

### Notation

Transformations are described using a matrix, labeled with a letter wearing a little hat - like this: $$\hat{T}$$. To apply the trasnformation, we multiply the vector by the transformation matrix.

So, the expression...

$$
\hat{T}|x\rangle = |y\rangle
$$

...describes $$|y\rangle$$, which is a result of $$|x\rangle$$transformed by $$\hat{T}$$.



