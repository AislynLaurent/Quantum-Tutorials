---
description: Describing and manipulating vectors using bra-ket notation.
---

# Basics

## Vectors

You may be used to thinking of vectors as having a magnitude and a direction. This is a pretty classical way of doing things - usually we're talking about vectors in a physics context, and therefore we're usually using them to describe where something is going.

Here we want to think of vectors in a more abstract way. Our vectors here are not really _going_ anywhere in particular. 

## Bra-Ket Notation

For quantum systems, we'll describe vectors using [Bra-Ket notation](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation). Once you get the hang of it, it's simple enough, but for the uninitiated it might be a bit weird.

The basic idea is that vectors can be labeled with what looks like a line **\( \| \)** on one side and an angle bracket **\( &lt; , &gt; \)** on the other. 

So, for the vector _**x**,_ the label would look like this: $$ |x \rangle$$. 

Actually, this is a "**ket**" vector. A "**bra**" vector looks like this: $$ \langle x| $$. You'll see later that we use this to our advantage when describing the inner product of two vectors: $$ \langle x|y \rangle$$, but that's another tutorial.

You can describe different things about a vector this way, too. So, for the vector _**x**_ over time _**t**_ we might write:

$$
|x (t) \rangle
$$

Easy enough.

## Column Vectors

The vectors we're describing are the sort of column vectors you're likely already very familiar with.

$$
|x\rangle = \begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix}
$$

Obviously this kind of vector is just a one column matrix, and as such we can preform all of the matrix operations you would expect.

## Matrix Operations

For our purpose the only important kinds of matrix operations are addition and multiplication.

### Addition

Adding two matrices together requires that they both have the same dimensions - that is to say the same number of rows and columns. As you might expect, you just add the respective entries together: 

$$ |x\rangle = \begin{bmatrix} 1 \\ 1 \\ \end{bmatrix}$$

$$ |y\rangle = \begin{bmatrix} 2 \\ 2 \\ \end{bmatrix}$$

$$ |x\rangle + |y\rangle = \begin{bmatrix} 3 \\ 3 \\ \end{bmatrix}$$

Simple enough. You should note that subtraction is just a sort of special case of addition, where you started by multiplying the second matrix by -1.

### Multiplication

There are two relevant types of multiplication: 

#### Scalar Multiplication

Where we multiply each entry in the matrix by a number:

$$ |x\rangle = \begin{bmatrix} 1 \\ 1 \\ \end{bmatrix}$$

$$ 2 * |x\rangle = \begin{bmatrix} 2 \\ 2 \\ \end{bmatrix}$$

As you would expect, you could also multiply the matrix by a variable.

#### Matrix Multiplication

The second type is regular old matrix multiplication. If you're already well familiar with linear algebra then you know how this works, and why. If not this will seem very strange, and the rules will seem a little obtuse.

Let's start by reviewing the rules:

* Multiplication goes **row** by **column**
* Multiply the first entry of the first row of the first matrix by the first entry in the first row of the second matrix
* Add this to the result of the next entries, respectively
* Continue until there are no more entries

As you can see, this means that the **number of entries in the rows** of the first matrix have to be equal to the **number of entries in the columns** of the second matrix.

Here I'll include a lovely graphic that should clear things up significantly [_\(image source\)_](https://hadrienj.github.io/posts/Deep-Learning-Book-Series-2.2-Multiplying-Matrices-and-Vectors/):

![Matrix multiplication](../.gitbook/assets/dot-product.png)

There, much better. You should be able to see that you'll end up with a single column matrix at the end.



