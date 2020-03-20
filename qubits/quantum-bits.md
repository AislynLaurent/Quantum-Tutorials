---
description: An introduction to quantum bits
---

# Quantum Bits

## Quantum Information

In the section about [_quantum mechanics_](../physics/quantum-mechanics.md), we talked about the idea of [_superposition_](../physics/quantum-mechanics.md#superposition), where more than one [_state_](../physics/classical-mechanics.md#state) is overlapped over top of each other. The system is in [_multiple distinguishable states_](../physics/quantum-mechanics.md#distinguishable-states) at the same time - the information is _superimposed._ We don't know what going on in there, we can only talk in [_probabilities_ ](../physics/quantum-mechanics.md#probability)- what state are we likely to see if we measure \(or observe\) the system at a particular moment?

### The Single Qubit System

A single quantum bit is the basic unit of quantum computation, but it's also the smallest \(non-trivial\) quantum system. Unlike a classical system, where a single bit can't do much at all, in the quantum system the individual bits can be used to do work alone.

### Distinguishable States

Like a classical bit, the quantum bit has two distinguishable states - 0 and 1. We'll use them the same way we use them there - 0 for false, and 1 for true. The difference here is very simple. In the quantum system, we have the potential for superposition.

A quantum bit can be 1 _and_ 0, at the _same time_. We measure this in between zone by talking about the [_probability_ ](../physics/quantum-mechanics.md#probability)of finding the qubit in a particular state _when we measure_ it.

### Notation

A single qubit is represented as a 2-dimensional [_quantum vector_](../physics/quantum-mechanics.md#quantum-vectors). Recall that a quantum vector has as many dimensions as there are distinguishable states, so it makes sense that a single qubit system has 2 elements. Like any quantum vector, we represent a qubit in an unknown state like this:

$$
|\psi\rangle
$$

The different states, like this:

$$
|0\rangle = \begin{bmatrix}1\\0\end{bmatrix}, |1\rangle=\begin{bmatrix}0\\1\end{bmatrix}
$$

As our system gets more complex and begins to contain more numbers, we can expand on this:

$$
|00\rangle=\begin{bmatrix}1\\0\\0\\0\end{bmatrix},|01\rangle=\begin{bmatrix}0\\1\\0\\0\end{bmatrix},|10\rangle=\begin{bmatrix}0\\0\\1\\0\end{bmatrix},|11\rangle=\begin{bmatrix}0\\0\\0\\1\end{bmatrix}
$$

You can imagine that if we have a whole bunch of qubits, this could get very confusing very quickly. So we might use the decimal version of these binary numbers streamline things:

$$
|0\rangle=\begin{bmatrix}1\\0\\0\\0\end{bmatrix},|1\rangle=\begin{bmatrix}0\\1\\0\\0\end{bmatrix},|2\rangle=\begin{bmatrix}0\\0\\1\\0\end{bmatrix},|3\rangle=\begin{bmatrix}0\\0\\0\\1\end{bmatrix}
$$

{% hint style="info" %}
[Binary number review](https://www.khanacademy.org/math/algebra-home/alg-intro-to-algebra/algebra-alternate-number-bases/v/number-systems-introduction)
{% endhint %}

