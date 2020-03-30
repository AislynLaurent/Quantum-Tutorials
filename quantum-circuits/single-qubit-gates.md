---
description: Discussion some of simple single qubit circuits
---

# Single Qubit Gates

Over the course of this tutorial, we won't be able to go through all possible quantum gates. We will however take time to go through the most important ones, especially ones that we'll use when learning to code later on.

## The Identity Gate

A very simple gate, which doesn't change anything at all. It preserves the state of the system as it is - it gives us the identity of the qubit.

$$
I=\begin{bmatrix}1&0\\0&1\end{bmatrix}
$$

![Symbol for the Identity gate](../.gitbook/assets/image%20%285%29.png)



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

![Symbol for the X gate](../.gitbook/assets/image%20%2813%29.png)

We can track the result on the Bloch sphere:

![An animation showing the rotation of the X gate on the Bloch sphere](../.gitbook/assets/5d908427a5654129b4cf14f53a2f8f26x_bloch.gif)

### Pauli Y

The Pauli Y gate is an interesting machine - we get the same result as the Pauli X gate, but instead of moving through real space we move through imaginary space instead.

$$
Y=\begin{bmatrix}0&-i\\i&0\end{bmatrix}
$$

![Symbol for the y gate](../.gitbook/assets/image%20%283%29.png)

![An animation showing the rotation of the Y gate on the Bloch sphere](../.gitbook/assets/bc3a4d2390564bc09fe4dab0e6475561y_bloch.gif)

By traveling through the imaginary dimension we can change the _spin_ state of our qubit. Most of the time this affects the probabilities in our superposition. In this case we've changed the spin so much that we ended up back where we started.

### Pauli Z



$$
Z=\begin{bmatrix}1&0\\0&-1\end{bmatrix}
$$

![Symbol for the Z gate](../.gitbook/assets/image%20%288%29.png)

![An animation showing the rotation of the Z gate on the Bloch sphere](../.gitbook/assets/80823b8202d44bfcbc0ee29058a20929z_bloch.gif)

## Hadamard Gate

The Hadamard gate imposes the _uniform superposition_ on our system. This gate is very important, because often we need to scramble our initial state before we can start computation. The Hadamard gate does this for us in a predictable way.

$$
H=\frac{1}{\sqrt{2}}\begin{bmatrix}1&1\\1&-1\end{bmatrix}
$$

![Symbol for the Hadamard gate](../.gitbook/assets/image%20%282%29.png)

![An animation showing the rotation of the Hadamard gate on the Bloch sphere](../.gitbook/assets/ffbc26fc17d7425e80209112134951ffh_bloch.gif)

## Phase Gate

$$
S=\begin{bmatrix}1&0\\0&i\end{bmatrix}
$$

![Symbol for the phase gate](../.gitbook/assets/image%20%2812%29.png)

![An animation showing the rotation of the phase gate on the Bloch sphere](../.gitbook/assets/29cf0d32dc724cf8bc4cd3a6f2a1866bs_bloch.gif)

