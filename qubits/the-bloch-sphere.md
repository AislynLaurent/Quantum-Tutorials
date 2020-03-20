---
description: Operations on multi-qubit systems
---

# Multi-Qubit Systems

## The Number of States

In a[ _classical system_ ](untitled.md#yes-no)we have two possible pieces of information - true or false. That's still the case here - we [_still work in binary_](quantum-bits.md#distinguishable-states) on quantum systems. So for multi-qubit systems, how do we decide the number of distinguishable states?

We take the number of possible pieces of information \(so 2 - 0 or 1\) and we take it to the power of the number of qubits in the system, $$n$$. So for a single qubit system:

$$
n=1, \hspace{8pt} 2^n = 2^1 = 2
$$

### A 2 Qubit System

Let's take the a 2 qubit system as an example. First let's determine the number of [_distinguishable states_](../physics/quantum-mechanics.md#distinguishable-states):

$$
n=2, \hspace{8pt}2^n=2^2=4
$$

Our [_basis vectors_](../linear-algebra/space-dimension-and-span.md#basis) will have the same number of [_dimensions_](../linear-algebra/space-dimension-and-span.md#dimensions) as we have distinguishable states. If $$N$$ is the number of dimensions, we can say that $$N=4$$.

For a system in 4 dimensions, we need 4 basis vectors which each have 4 elements. If the basis vectors for a [_single qubit system_](quantum-bits.md#the-single-qubit-system) look like this:

$$
|0\rangle = \begin{bmatrix}1\\0\end{bmatrix}, |1\rangle=\begin{bmatrix}0\\1\end{bmatrix}
$$

Then we can extend this idea for the basis vectors of our two qubit system [_\(Nielsen, M. - p. 16\)_](qubits-summary/qubit-references.md#states-for-a-2-qubit-system):

$$
|00\rangle=\begin{bmatrix}1\\0\\0\\0\end{bmatrix},|01\rangle=\begin{bmatrix}0\\1\\0\\0\end{bmatrix},|10\rangle=\begin{bmatrix}0\\0\\1\\0\end{bmatrix},|11\rangle=\begin{bmatrix}0\\0\\0\\1\end{bmatrix}
$$

This makes sense - it's also true for a classical system. If we had two classical bits, we could arrange the following combinations:

* $$00$$, Both are 0
* $$01$$, The first is 0 and the second is 1
* $$10$$, The first is 1 and the second is 0
* $$11$$, Both are 1

## Calculating the Probability of States

We already know that the probability of all possible states has to add up to 1. So, if we combine all our possible states like this:

$$
|\psi\rangle=a_{00}|00\rangle+a_{01}|01\rangle+a_{10}|10\rangle+a_{11}|11\rangle
$$

Where $$a_{00} - a_{11}$$ are complex numbers representing the probability of each of the states being observed respectively, the probability of any specific state $$x$$ being observed is:

$$
|a_x|^2
$$

{% hint style="success" %}
Recall that [_complex numbers_](../physics/quantum-mechanics.md#complex-numbers-1) are based on [_imaginary numbers_](../physics/quantum-mechanics.md#imaginary-numbers), which become real when they're squared.
{% endhint %}

After we measure it, the qubit in question will collapse to a specific state $$|x\rangle$$ [_\(Nielsen, M. - p. 16\)_](qubits-summary/qubit-references.md#math-for-the-probability-of-observing-a-qubit-in-a-particular-state)_._

### Measuring Probabilities

Consider the following system:

$$
|\psi\rangle=\frac{1}{\sqrt{2}}*(|00\rangle+|01\rangle)
$$

Here we're considering the possible states for the _first_ qubit in this system. Why just the first? Because we read multi-qubit systems from [_right to left_](quantum-bits.md#notation), and the last qubit isn't changing:

$$
|\psi\rangle=\frac{1}{\sqrt{2}
}*(|\textcolor{red}{0}0\rangle+|\textcolor{red}{0}1\rangle)
$$

We're only changing the possible states for the first qubit:

$$
|\psi\rangle=\frac{1}{\sqrt{2}}*(|0\textcolor{red}{0}\rangle+|0\textcolor{red}{1}\rangle)
$$

So let's calculate the probabilities in this situation:

$$
|\psi\rangle =\frac{1}{\sqrt{2}}|00\rangle + \frac{1}{\sqrt{2}}|01\rangle = a_{00}|00\rangle+a_{01}|01\rangle
$$

$$
P|x\rangle=|a_x|^2
$$

$$
\text{When}\hspace{6pt} |x\rangle=|00\rangle, \hspace{6pt} a_x=a_{00}=\frac{1}{\sqrt{2}} \hspace{6pt} \& \hspace{6pt} |x\rangle=|01\rangle, \hspace{6pt} a_x=a_{01}=\frac{1}{\sqrt{2}}
$$

$$
\text{So...}\hspace{6pt} P|00\rangle=|a_{00}|^2= (\frac{1}{\sqrt{2}})^2=\frac{1}{2}\hspace{6pt} \& \hspace{6pt} P|01\rangle=|a_{01}|^2= (\frac{1}{\sqrt{2}})^2=\frac{1}{2}
$$

$$
P|00\rangle=\frac{1}{2}, \hspace{6pt} P|01\rangle=\frac{1}{2}
$$

For this system, the probabilities for the first qubit are equal - if we measure enough times we'll get 0 50% of the time and 1 50% of the time. The last qubit will _always_ be 0.

Why do I say _if we measure enough times_? Because this is a probability distribution - nothing is guaranteed. If you measure this system an infinite number of times, you'll get a perfect 50/50 spread. Any less than that, and you'll get some noise - your measurement won't be perfect.

## Notation for Systems with _n_ Qubits

In a system with $$n$$ qubits, we label each state with the number represented by the [_decimal version_](quantum-bits.md#notation) of their binary identifier:

$$
|0\rangle, |1\rangle,|2\rangle,|3\rangle, ... , |2^n-1\rangle
$$

Where in the $$|0\rangle$$ state, all the qubits in the system are 0, and for the $$|2^n-1\rangle$$ state, all the qubits in the system are 1.

Recall also from our previous discussions on _dot product_, and _basis_ that the inner product of any two of these basis vectors \(labelled here $$|x\rangle$$ and $$|y\rangle$$\) is 0, and that the inner product of any of these basis vectors with itself is 1:

$$
\langle x|y \rangle=0, \langle x | x \rangle=1
$$

## Uniform Superposition

A special state for the $$n$$ qubit system is the _uniform superposition_, where the system is equally likely to collapse to any of the possible distinguishable states.

### Notation

We label the uniform superposition with the vector:

$$
|S\rangle
$$

So for a single qubit system:

$$
|S\rangle=\frac{1}{\sqrt{2}}*(|0\rangle+|1\rangle)
$$

For a 2 qubit system:

$$
|S\rangle=\frac{1}{\sqrt{2}}*(|0\rangle+|1\rangle)
$$





