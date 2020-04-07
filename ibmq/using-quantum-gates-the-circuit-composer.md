---
description: An overview of the circuit composer and a few example using quantum gates
---

# Using Quantum Gates - The Circuit Composer

## How to Use the Circuit Composer

The circuit composer is a very intuitive tool. You start out looking at a summary of all your circuits with some basic information about them listed.

### Creating a new circuit

You start by selecting the new circuit button:

![The new circuit button on the IBMQ website](../.gitbook/assets/image%20%2826%29.png)

You'll then be taken into the tool itself.

![A screenshot showing the composer](../.gitbook/assets/image%20%2819%29.png)

On the left-hand side you can see a few different options. The first just displays some general information as above.

![The settings tab](../.gitbook/assets/image%20%2829%29.png)

The second lets you tweak your circuit, including the number of quantum registers \(each of which holds one qubit\) and the number of classical registers \(which is where results will be stored before they're ready and displayed\).

![The code editor tab](../.gitbook/assets/image%20%2811%29.png)

Next is a code editor that lets you directly work on the QASM code. This is the code the runs on the actual quantum computer - we won't dicuss it much here because it's out of the scope of this guide.

{% hint style="info" %}
[More information about QASM](https://www.quantum-inspire.com/kbase/qasm/)
{% endhint %}

![The visualizations tab](../.gitbook/assets/image%20%282%29.png)

Last is the visualization tab which shows you a graph that visualizes your state vector. The state vector shows the probability of finding the whole system in a particular state - it's the combination of all the qubits in your system. Since right now we have no circuit, it doesn't show much at all.

![The visualization tab after adding a Hadamard gate to the circuit](../.gitbook/assets/image%20%2820%29.png)

You can see that when I add a gate to the system, it splits up into all the different possible states, and show the probability for each.

### Building a circuit

We'll use a simple example circuit as we continue along. 

To add gates to your system, you simply drag them from the pallet onto your circuit.

