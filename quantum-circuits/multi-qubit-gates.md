---
description: Discussion some of simple gates that operate on multiple qubits
---

# Multi-Qubit Gates

Unlike single qubit gates, multi-qubit gates are to complex to be described using the relatively simple Bloch sphere diagram. For these we'll just have their matrix to describe their behaviour.

Something important to note is that all gates must have the [_same number of inputs as there are outputs_](quantum-information.md#reversibility). This is because no information can be lost in quantum systems - whatever goes in must come out again.

## The Controlled Not Gate

This gate is also called the "_CX"_ or the _"controlled X"_ gate. You can guess what this means - it preforms the same operation as the [_Pauli X_](single-qubit-gates.md#pauli-x) gate but controlled by another qubit.

$$
\text{CNOT}=\begin{bmatrix}1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{bmatrix}
$$

![Symbol for the CX gate](../.gitbook/assets/cx-gate.png)

We pass in two bits - a _control_ bit and a _target_ bit. If the control bit is $$|1\rangle$$, the target bit will flip states. If the control bit is $$|0\rangle$$, nothing happens. The control bit is never affected by this gate.

### Toffoli - Double Control

The Toffoli gate \(_"double control", "CCNOT", "CCX"_ or _"TOFF"_\) does basically the same thing, except this time we have _t_wo _control bits_. If both control bits are $$|1\rangle$$, we flip our target bit. If either of them are $$|0\rangle$$ nothing happens. The control bits are still never effected.

$$
\text{TOFF}=\begin{bmatrix}1&0&0&0&0&0&0&0\\0&1&0&0&0&0&0&0\\0&0&1&0&0&0&0&0\\0&0&0&1&0&0&0&0\\0&0&0&0&1&0&0&0\\0&0&0&0&0&1&0&0\\0&0&0&0&0&0&0&1\\0&0&0&0&0&0&1&0\end{bmatrix}
$$

![Symbol for the TOFF gate](../.gitbook/assets/ccx-gate.png)

{% hint style="success" %}
As we operate on more quits, and end up with more distinguishable states, are matrices get larger. The same as a system with $$n$$ qubits have $$2^n$$ distinguishable states, or matrices will likewise have $$2^n$$ numbers of rows and columns.

So our TOFF gate, which works on 3 qubits, has $$2^3=8$$ distinguishable states, and there for 8 rows and 8 columns in it's matrix.

Notice that this works the same way it would when constructing classical truth tables to describe operations on classical bits. 
{% endhint %}

## The Controlled Z Gate

The controlled Z gate \(_"CZ"_\) works essentially just like the controlled X gate. It's the _Pauli Z_ gate with an extra control bit. When the control bit is $$|1\rangle$$, we preform the Z gate operation. When the control bit is $$|0\rangle$$nothing changes. As before, the control bit is never affected by this operation.

$$
\text{CZ}=\begin{bmatrix}1&0&0&0\\0&1&0&0\\0&0&1&0\\0&0&0&-1\end{bmatrix}
$$

![Symbol for the CZ gate](../.gitbook/assets/cz-gate.png)

## The SWAP Gate

This gate does what is says - it swaps the state of the two bits included in the operation. So if the starting state is:

$$
|a\rangle=|0\rangle, |b\rangle=|1\rangle
$$

The resulting state will be:

$$
|a\rangle=|1\rangle, |b\rangle=|0\rangle
$$

And of course, vice versa.

$$
\text{SWAP}=\begin{bmatrix}1&0&0&0\\0&0&1&0\\0&1&0&0\\0&0&0&1\end{bmatrix}
$$

![Symbol for the SWAP gate](../.gitbook/assets/swap-gate.png)

## Universal Gate Sets

In the section about [_classical models of computation_](classical-models-of-computation.md), we talked a bit about constructing all possible classical logic gates with just one - [_the NAND gate_](classical-models-of-computation.md#universal-gates). The NAND gate is a _universal_ gate because of this special property.

In quantum computing we have the same concept. All possible quantum gates can be a constructed with a selection of one and two qubit gates. Exactly which gates depends - there are multiple possible universal sets of quantum gates. You'll see different resources will rely on different universal sets. For this tutorial what most important is that you understand the concept.

