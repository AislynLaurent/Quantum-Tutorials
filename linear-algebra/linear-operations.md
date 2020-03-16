---
description: 'A brief overview of linear combinations, dependence, and independence'
---

# Vector Relationships

## Linear Combinations

Linear combinations logically follow from the matrix operations covered in [_Basics_](vectors.md) - simply put, it's a combination of two vectors, scaled by numbers.

$$ |x\rangle = a |a\rangle + b |b\rangle$$

Here $$ |x\rangle$$is a linear combination of the vector $$|a\rangle$$scaled by the constant $$a$$ and the vector $$|b\rangle$$scaled by the constant $$b$$.

{% hint style="info" %}
[Detailed explanation of linear combinations](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/linear-combinations/v/linear-combinations-and-span)
{% endhint %}

## Linear Dependence

So if we have a set of vectors, how do we define the relationships between those vectors, and what do those relationships tell us about the whole system? Well, in the example above we have a set of three vectors - $$|x\rangle, |a\rangle, |b\rangle$$.

$$|x\rangle$$is dependent on$$|a\rangle$$and$$|b\rangle$$, because $$|x\rangle$$ is defined by$$|a\rangle$$and$$|b\rangle$$. Without them,$$|x\rangle$$could not exist. And since one of the vectors in the set is dependent on one of the other vectors in the set, the whole set can be said to be _linearly dependent_.

## Linear Independence 

So if a set includes a vector which can be described as a linear combination of other vectors in the same set, then the whole set is said to be linearly dependent.

Logically, if this is not the case, and none of the vectors in the set can be described as linear combinations of each other, the whole set is said to be _linearly independent_.

{% hint style="info" %}
[Detailed explanation of linear independence](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/linear-independence/v/linear-algebra-introduction-to-linear-independence)
{% endhint %}

