---
description: Discussion some of simple gates that operate on multiple qubits
---

# Multi-Qubit Gates

Unlike single qubit gates, multi-qubit gates are to complex to be described using the relatively simple Bloch sphere diagram. For these we'll just have their matrix to describe their behaviour.

Something important to note is that all gates must have the [_same number of inputs as there are outputs_](quantum-information.md#reversibility). This is because no information can be lost in quantum systems - whatever goes in must come out again.

## The Controlled Not Gate

This gate is also called the "_CX"_ or the _"controlled X"_ gate. You can guess what this means - it preforms the same operation as the [_Pauli X_](single-qubit-gates.md#pauli-x) gate but controlled by another qubit.

$$
\text{CNOT}=\begin{bmatrix}1&0&0&0\\0&0&0&1\\0&0&1&0\\0&1&0&0\end{bmatrix}
$$

![Symbol for the CX gate](../.gitbook/assets/cx-gate.png)

We pass in two bits - a _control_ bit and a _target_ bit. If the control bit is $$|1\rangle$$, the target bit will flip states. If the control bit is $$|0\rangle$$, nothing happens. The control bit is never affected by this gate.

## Universal Gate Sets

In the section about [_classical models of computation_](classical-models-of-computation.md), we talked a bit about constructing all possible classical logic gates with just one - [_the NAND gate_](classical-models-of-computation.md#universal-gates). The NAND gate is a _universal_ gate because of this special property.

In quantum computing we have the same concept. All possible quantum gates can be a constructed with a selection of one and two qubit gates. Exactly which gates depends - there are multiple possible universal sets of quantum gates. You'll see different resources will rely on different universal sets. For this tutorial what most important is that you understand the concept.

