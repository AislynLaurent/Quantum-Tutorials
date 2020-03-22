---
description: Introduction to quantum models of information
---

# Quantum Information

In this section, we'll combine many of the concepts we've discussion in the tutorial so far. This means that if anything so far has confused you or if you feel like you need more information on anything, this would be the time to review.

## Reversible Computing

Simply put, quantum calculations need to be reversible. During the process of quantum computation, _information_ should not be destroyed. 

In a classical system this isn't a concern - as long as we get the result we're looking for, we don't have any problem. For our [_Turing machine_](classical-models-of-computation.md#the-turing-machine), the state of the system changes with every instruction. We're not so concern with remembering the _previous_ state, as long as the _current_ state conforms to our expectations.

### Reversibility

> A computation is _reversible_ if it is always possible to uniquely recover the input, given the output. For example, the NOT operation is reversible, because if the output bit is 0, you know the input bit must have been 1, and vice versa. On the other hand, the AND operation is not reversible. [_\(Kaye, P. - p.12\)_](quantum-circuit-summary/quantum-circuit-references.md#reversibility)\_\_

It's important to fully understand what this means. If I provide to you only the resulting state of some quantum computation, it must be true that you can figure out where I started from. 

### Converting Classical Gates

While most classical gates are not reversible, we can change them so that they are. This requires adding more wires, used only to keep the information we put in [_\(Kaye, P. - p.12\)_](quantum-circuit-summary/quantum-circuit-references.md#diagram-of-the-reversible-and-gate)_:_

![The reversible AND gate keeps a copy of the inputs](../.gitbook/assets/image%20%282%29.png)

### Measuring

The one non-reversible action we take in quantum computation is [_measuring_ ](../physics/quantum-mechanics.md#measuring-quantum-systems)\(or observation\).

When we measure a qubit, it [_collapses_ ](../qubits/quantum-bits.md#measuring-qubits)into a particular state. It's forced to reveal what it had been doing this whole time - like our [_cat in the box_](../physics/quantum-mechanics.md#superposition), we know if it where alive or not.

This means we need to measure at the end whenever possible, so that we preserve reversibility until we have no choice.

## The Bloch Sphere

![A diagram of the Bloch sphere](../.gitbook/assets/bloch_sphere.svg)

The Bloch sphere can be used to describe the behaviour of single qubit systems. Here we see that we have a [_3-dimensional space_](../linear-algebra/space-dimension-and-span.md#space), and like all quantum system we're able to[ _range across the complex numbers_ ](../physics/quantum-mechanics.md#quantum-vectors)as well as the real numbers.

### What the Diagram Shows Us

Let's explore some of the things labelled on this diagram:

* $$x, y , z$$ are our three axis for 3-dimentional space
  * Note that the sphere has a radius of exactly _one unit_ 
* $$|0\rangle$$ and $$|1\rangle$$ are our two distinguishable states
  * See that these two are opposite each other on the diagram
* $$|\psi\rangle$$ is our vector in an unknown state - the single qubit we're describing
  * Our qubit projects a _shadow_ - this is the dotted line we see
  * When we draw a line between the shadow and our vector, we get a right angle triangle
* $$\theta$$ is the angle between the vector for our qubit $$|\psi\rangle$$ and the $$z$$ axis
* $$\varphi$$ is the angle between the shadow of our qubit and the $$x$$ axis

The sphere shows us all of the possible states our qubit can be in. Not just $$|0\rangle$$and $$|1\rangle$$, but the infinite combinations in between. By measuring the angle the vector $$|\psi\rangle$$ and it's shadow make with respect to the $$x$$, $$y$$and $$z$$ axis, we can derive the probability of finding our qubit in a particular state when we measure it.

