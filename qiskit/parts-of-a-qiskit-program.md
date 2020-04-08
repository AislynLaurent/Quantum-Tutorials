---
description: >-
  A summary of important parts of a qiskit program, which users may not be
  familiar with already
---

# Parts of a Qiskit Program

## Classical Registers

On a classical system, a register is a storage unit which holds multiple bits. Registers are not used to preform any instructions or math, though instructions may be stored on them. We use classical registers in our quantum program to hold the result when we measure out qubit.

You create a new classical register in qiskit like this:

```text
cr = ClassicalRegister(2)
```

This piece of code creates a classical register holding two bits, and stores it in the variable `cr`.

## Quantum Registers

Quantum registers are like classical ones, except they hold qubits instead of bits. They can hold multiple qubits at a time, and we can operate on each qubit separately.

You create a new quantum register in qiskit like this:

```text
qr = QuantumRegister(2)
```

This creates a quantum register holding two qubits, and stores it in the variable qr.

## Circuits

As previously mentioned, we want to operate on our system using quantum gates. This means we need to create a new quantum circuit. It will behave similarly to the circuit in the[ _circuit composer_](../ibmq/using-quantum-gates-the-circuit-composer.md), but we'll write code to add gates and operations instead of dragging and dropping them.

Just like in the circuit composer, we need to get set up with the number of qubits we want as well as enough classical registers to store the information we measure. You need to have **at least as many classical bits as you have qubits** so that you can store the state of all of them. You can have more if you like, just not less.

We create out circuit like this:

```text
circuit = QuantumCircuit(qr, cr)
```

This circuit include the two qubit quantum registers and the two bit classical register created above.

### Applying Gates

We apply gates to our circuit object by applying the appropriate methods to it. So we apply the [Hadamard gate](../quantum-circuits/single-qubit-gates.md#hadamard-gate) to the first qubit in the system like this:

```text
circuit.h(qr[0])
```

In circuit `circuit`, apply the Hadamard gate `h` to qubit `q[0]` in quantum register `qr`.

For a gate which operates on more than one qubit, we pass in both. Often order will be important:

```text
circuit.cx(qr[0], qr[1])
```

In circuit `circuit`, apply the controlled not gate `cx` to qubits `qr[0], qr[1]` in quantum register `qr`, where `qr[0]` is the control qubit and `qr[1]` is the target qubit.

{% hint style="info" %}
[More information about the _circuit_ object and the gate methods you can apply to it](https://qiskit.org/documentation/stubs/qiskit.circuit.QuantumCircuit.html#qiskit.circuit.QuantumCircuit)
{% endhint %}

## The Backend

### Simulators

Once you're ready to run your qiskit code, you can load a simulator on your local machine to test it. The simulator will give you an idea of whether your circuit is behaving as expected. You can spin up a simulator like this:

```text
simulator = Aer.get_backend('qasm_simulator')
```

Qiskit has a few different components \(which we'll discuss a bit later\) and a few different simulators you can use. Aer is the component that has the different simulators, and the QASM option simulates the quantum assembly language used on IBM systems. Here we've labeled our simulartor `simulator`.

### IBM Quantum Systems

If you've tested your circuit and think the result turned out well, then you can go ahead and run it on an acutaly quantum computer. This requires a few simple steps.

{% hint style="info" %}
The information in this guide is up to date at the time of writing, but it neever hurts to check the [official IBM documentation](https://qiskit.org/documentation/apidoc/ibmq-provider.html) in case something changes \(it's very well maintained\).
{% endhint %}



