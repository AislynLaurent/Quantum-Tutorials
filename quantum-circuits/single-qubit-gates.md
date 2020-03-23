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

And here is how the X gate will be represented on our circuit diagram:

![Symbol for the X gate](../.gitbook/assets/image%20%2812%29.png)

We can track the result on the Bloch sphere:

![An animation showing the rotation of the X gate on the Bloch sphere](../.gitbook/assets/5d908427a5654129b4cf14f53a2f8f26x_bloch.gif)

### Pauli Y

$$
Y=\begin{bmatrix}0&-i\\i&0\end{bmatrix}
$$

![Symbol for the y gate](../.gitbook/assets/image%20%283%29.png)

![An animation showing the rotation of the Y gate on the Bloch sphere](../.gitbook/assets/bc3a4d2390564bc09fe4dab0e6475561y_bloch.gif)

### Pauli Z

$$
Z=\begin{bmatrix}1&0\\0&-1\end{bmatrix}
$$

![Symbol for the Z gate](../.gitbook/assets/image%20%287%29.png)

![An animation showing the rotation of the Z gate on the Bloch sphere](../.gitbook/assets/80823b8202d44bfcbc0ee29058a20929z_bloch.gif)

## Hadamard Gate

The Haramard gate imposes the _unifrom superposition_ on our system. This gate is very important, because often we need to scramble our initial state before we can start computation. The Hadamard gate does this for us in a predicable way.

$$
H=\frac{1}{\sqrt{2}}\begin{bmatrix}1&1\\1&-1\end{bmatrix}
$$

![Symbol for the Hadamard gate](../.gitbook/assets/image%20%282%29.png)

![An animation showing the rotation of the Hadamard gate on the Bloch sphere](../.gitbook/assets/ffbc26fc17d7425e80209112134951ffh_bloch.gif)

## Phase Gate

$$
S=\begin{bmatrix}1&0\\0&i\end{bmatrix}
$$

![Symbol for the phase gate](../.gitbook/assets/image%20%2811%29.png)

![An animation showing the rotation of the phase gate on the Bloch sphere](../.gitbook/assets/29cf0d32dc724cf8bc4cd3a6f2a1866bs_bloch.gif)

