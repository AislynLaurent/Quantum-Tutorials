---
description: Discussion of simple single qubit circuits
---

# Single Qubit Gates

Over the course of this tutorial, we won't be able to go through all of possible quantum gates. We will however take time to go through the most important ones, especially ones that we'll use when learning to code later on.

## Pauli Gates

These gates work by changing the direction of the vector $$|\psi\rangle$$ in either the $$x$$, $$y$$ or $$z$$ direction.

{% hint style="info" %}
[More about the Pauli matrices and where they come from](https://en.wikiversity.org/wiki/Pauli_matrices)
{% endhint %}

### Pauli X

The Pauli X gate is exactly the classical NOT gate as we described earlier:

$$
X = \begin{bmatrix}0&1\\1&0\end{bmatrix}
$$

$$
|0\rangle \rightarrow |1\rangle, |1\rangle \rightarrow|0\rangle
$$

And here is the X gate represented on our circuit diagram:

![A circuit diagram showing the X gate](../.gitbook/assets/circuit.svg)

We can track the result on the Bloch sphere:

![An animation showing the rotation of the X gate on the Bloch sphere](../.gitbook/assets/5d908427a5654129b4cf14f53a2f8f26x_bloch.gif)

### Palui Y

$$
Y=\begin{bmatrix}0&-i\\i&0\end{bmatrix}
$$

![A circuit diagram showing the Y gate](../.gitbook/assets/circuit-4.svg)

![An animation showing the rotation of the Y gate on the Bloch sphere](../.gitbook/assets/bc3a4d2390564bc09fe4dab0e6475561y_bloch.gif)

### Pauli Z

![A circuit diagram showing the Z gate](../.gitbook/assets/circuit-5.svg)

![An animation showing the rotation of the Z gate on the Bloch sphere](../.gitbook/assets/80823b8202d44bfcbc0ee29058a20929z_bloch.gif)



