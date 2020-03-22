---
description: Review of the Turing Machine and the circuit model of classical computation
---

# Classical Models of Computation

## The Turing Machine

The Turing machine is a theoretical computer, originally proposed by Allan Turing. It can compute anything that is possible on a classical system.

It includes a _finite state machine,_ a machine which has a finite number of possible states, and whose current state relies on the previous state. So if I put in the number 4 now, and the number 4 again next, the results may be different because the current answer depends on the previous result and well as my input.

It's also a _tape_ machine. It has an infinite rope of tape that it can read from or write on, but the important thing about the tape is that it can only input _one instruction at a time_. Because the machine includes a finite state machine, the state changes _every time_ a new instruction is read in [_\(Kaye, P - p. 3\)_](quantum-circuit-summary/quantum-circuit-references.md#the-turing-machine).

## The Circuit Model

The Turing machine is the most abstract idea of a computer. We never talk about storage, or time, or wires - only instructions and state. We'll move a bit closer to real life in our discussion of the circuit model of computation.

In the circuit model we have a given number of wires, along which travels a current. As we talked about earlier [_high voltage corresponds to 1 and low voltage corresponds to 0_](../qubits/classical-bits.md#yes-no). Along the path of this wire is some kind of _logic gate_ which affects some change of state on the system [_\(Kaye, P - p. 3\)_](quantum-circuit-summary/quantum-circuit-references.md#a-circuit-diagram)_:_

![A circuit diagram](../.gitbook/assets/image%20%286%29.png)

You see here on the left a series of inputs, labelled $$i_1 - i_4$$. On the right we have a series of outputs labelled $$o_1 - o_4$$. In the middle we have a few gates, labelled $$G_1 - G_4$$. Some of the gates take in multiple outputs, and produce multiple outputs.

### Using Gates

A logic gate is an [_operator_](../linear-algebra/transformations.md#operators) that[ _transforms_](../linear-algebra/transformations.md#transformation-matrices) the input into some output. These may preform [_fundamental boolean operations_](../qubits/classical-bits.md#boolean-operations) or more complex instructions.

For example, the [_transformation matrix_](../linear-algebra/transformations.md#transformation-matrices) for a NOT gate looks like this:

$$
\text{NOT}=\begin{bmatrix}0&1\\1&0\end{bmatrix}
$$

Let's do an example. We'll start by defining the matrices for our classical bits:

$$
0=\begin{bmatrix}1\\0\end{bmatrix}, \hspace{6pt} 1=\begin{bmatrix}0\\1\end{bmatrix}
$$

Looks familiar I'm sure. We'll multiply the 0 vector by the NOT transformation matrix:

$$
\begin{bmatrix}0&1\\1&0\end{bmatrix}\begin{bmatrix}1\\0\end{bmatrix}=\begin{bmatrix}0\\1\end{bmatrix}
$$

You can see that the result is the 1 matrix.

Classical gates are flexible. We can take multiple bits as input, and we can produce multiple bits as output. We can combine them and use them to construct larger and more complex operations.

{% hint style="info" %}
[More information on classical logic gates](https://www.khanacademy.org/computing/ap-computer-science-principles/computers-101/logic-gates-and-circuits/a/logic-gates)
{% endhint %}

### Universal Gates

We can also define _universal gates_ - gates which can be used to define all other gate operations. For example the NAND gate \(NOT/AND\) is an example of a universal gate.

{% hint style="info" %}
[More about universal gates](https://www.electronics-tutorials.ws/logic/universal-gates.html)
{% endhint %}

## Classical Systems and Information

During this entire tutorial, we've focused heavily on _information_.

How is information represented? How is information processed? How is information preserved? How is information changed?

We can see that in both these models of computation, information can be destroyed. The original state of the wire may not be retrievable after certain gate operations. We've gained something, but we've also lost something.

Quantum mechanics doesn't allow for this possibility. All information must be preserved. This means all of our quantum operations must be _reversible_.

