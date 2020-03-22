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



