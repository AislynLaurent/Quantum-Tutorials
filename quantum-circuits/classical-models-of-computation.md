---
description: Review of the Turing Machine and the circuit model of classical computation
---

# Classical Models of Computation

## The Turing Machine

The Turing machine is a theoretical computer, originally proposed by Allan Turing. It can compute anything that can be computed by a classical system.

It includes a _finite state machine,_ a machine which has a finite number of possible states, and whose current state relies on the previous state. So if I put in the number 4 now, and the number 4 again next, the results may be different because the current answer depends on the previous result and well as my input.

It's also a _tape_ machine. It has an infinite rope of tape that it can read or write on, but the important thing about the tape is that it can only input _one instruction at a time_. Because the machine includes a finite state machine, the state changes _every time_ a new instruction is read in [_\(Kaye, P - p. 3\)_](quantum-circuit-summary/quantum-circuit-references.md#the-turing-machine).

## The Circuit Model

The Turing machine is the most abstract idea of a computer. We never talk about storage, or time, or wires - only instructions and state. We'll move a bit closer to real life in our discussion of the circuit model of computation.

In the circuit model we have a given number of wires, along which travels a current. As we talked about earlier [_high voltage corresponds to 1 and low voltage corresponds to 0_](../qubits/classical-bits.md#yes-no). Along the path of this wire is some kind of _logic gate_ which affects some change on the state of the system [_\(Kaye, P - p. 3\)_](quantum-circuit-summary/quantum-circuit-references.md#a-circuit-diagram)_:_

![A circuit diagram](../.gitbook/assets/image%20%285%29.png)

You see here on the left a series of inputs, labelled $$i_1 - i_4$$. On the right we have a series of outputs labelled $$o_1 - o_4$$. In the middle we have a few gates, labelled $$G_1 - G_4$$. Some of the gates take in multiple outputs, and produce multiple outputs.

### What are Gates?

A logic gate is an [_operator_](../linear-algebra/transformations.md#operators) that[ _transforms_](../linear-algebra/transformations.md#transformation-matrices) the input into some output. For example, the _transformation matrix_ for a NOT gate would look like this:



