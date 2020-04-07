---
description: An overview of the circuit composer and a few example using quantum gates
---

# Using Quantum Gates - The Circuit Composer

## How to Use the Circuit Composer

The circuit composer is a very intuitive tool - it's a great way to get started playing around with quantum circuits.

![A screenshot of the circuit composer page](../.gitbook/assets/image%20%2830%29.png)

### Creating a new circuit

You start by selecting the new circuit button:

![The new circuit button on the IBMQ website](../.gitbook/assets/image%20%2828%29.png)

You'll then be taken into the tool itself.

![A screenshot showing the composer](../.gitbook/assets/image%20%2821%29.png)

On the left-hand side you can see a few different options. The first just displays some general information as above.

### Circuit Settings

![The settings tab](../.gitbook/assets/image%20%2831%29.png)

### The Circuit Editor

The second lets you tweak your circuit, including the number of quantum registers \(each of which holds one qubit\) and the number of classical registers \(which is where results will be stored before they're processed and displayed\).

![The code editor tab](../.gitbook/assets/image%20%2813%29.png)

Next is a code editor that lets you directly work on the QASM code. This is the code the runs on the actual quantum computer - we won't discuss it much here because it's out of the scope of this guide.

{% hint style="info" %}
[More information about QASM](https://www.quantum-inspire.com/kbase/qasm/)
{% endhint %}

### The Visualization Tool

![The visualizations tab](../.gitbook/assets/image%20%282%29.png)

Last is the visualization tab which shows you a graph that visualizes your state vector. The state vector shows the probability of finding the whole system in a particular state - it's the combination of all the qubits in your system. Since right now we have no circuit, it doesn't show much at all.

![The visualization tab after adding a Hadamard gate to the circuit](../.gitbook/assets/image%20%2822%29.png)

You can see that when I add a gate to the system, it splits up into all the different possible states, and shows the probability for each.

## Building a circuit

We'll use a simple example circuit as we continue along. 

![An image showing a simple 2 qubit circuit in the composer](../.gitbook/assets/image%20%286%29.png)

As we mentioned before, you can see our two qubits on the left hand side of the circuit. Here they're labeled `q[0]` and `q[1]` . To begin, both qubits are in the $$|0\rangle$$ state. You can see that's labelled just to the right of the qubit labels.

After the labels, we have a straight horizontal line leading from each qubit. This isn't a [_wire like it would be in a classical system_](../quantum-circuits/classical-models-of-computation.md#the-circuit-model) - it's just a visual aid so that we can see which qubits are being acted on by which gates, in order.

Lastly, on the bottom, we have our classical registers. We have two of them, thus, `c2`. This is where we'll store our results.

### Adding Gates

To add gates to your system, we drag them from the pallet onto our circuit. Let's start by imposing our uniform superposition:

![Our quantum circuit with a uniform superposition imposed on it](../.gitbook/assets/image%20%2832%29.png)

Now that we've used a Hadamard gate to each of our qubits, we can see that we have a since tidy superposition - this shows up on the left in our visualizer.

{% hint style="success" %}
The visualizer can only show you what would happen _theoredically_ - that is 
{% endhint %}

