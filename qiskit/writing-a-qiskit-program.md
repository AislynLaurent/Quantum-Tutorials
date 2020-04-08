---
description: An example of a qiskit program from start to finish
---

# Writing a Qiskit Program

As mentioned before, this tutorial is being written in a jupyter notebook \(_version 4.6.1_\) with Anaconda \(_version 4.6.14_\) and qiskit \(_version 0.11.1_\) installed, running python \(_version 3.7.3_\).

## Set-up

### Imports

First we need to go through and import all our libraries and set up our IBM account.

```python
from qiskit import **
from qiskit.tools.visualization import plot_histogram
%matplotlib inline
```

The line `%matplotlib inline` is used to make matplotlib graphs show up correctly in the jupyter notebook. You won't need this if you're using a different tool.

### Connecting your IBMQ account

Next, we need to connect your IBM account so that you can access their quantum systems. You'll need to log into your IBM account and grab your API token. Each token is different, and you shouldn't share it with anyone \(that would pose a security risk to your accont\). To find your token log into your IBM account, and head to the account page:

![A screenshot show where the account page can be found](../.gitbook/assets/image%20%2831%29.png)

Once you're there, you'll see the where you can copy your token:

![A screenshot showing where the copy token button can be found](../.gitbook/assets/image%20%2846%29.png)

Then we can save the token on our local system:

```python
IBMQ.save_account('example_API_token-replace_me')
IBMQ.load_account()
```

Now you'll be able to run jobs on IBM's system when you're ready.

{% hint style="info" %}
[More detailed instructions for finding your API token](https://qiskit.org/documentation/install.html#access-ibm-quantum-systems)
{% endhint %}

## Your Quantum Circuit

### Circuit set-up

We'll be working with two qubits, so we'll need two classical and two quantum registers:

```python
qr = QuantumRegister(2)
cr = ClassicalRegister(2)
```

Our circuit will include both of those:

```python
circuit = QuantumCircuit(qr, cr)
circuit.draw(output='mpl')
```

And our output:

![A visualization of our empty circuit](../.gitbook/assets/image%20%2838%29.png)

### Applying Gates

Let's apply a Hadamard gate to the first qubit and a controlled not gate to both - afterward we'll measure the result.

```python
circuit.h(qr[0])
circuit.cx(qr[0], qr[1])

circuit.measure(qr, cr)

circuit.draw(output='mpl')
```

![A visualization of our circuit after applying gates and measuring](../.gitbook/assets/image%20%289%29.png)

## Running your Circuit

### Testing on the simulator

Now that we have our little circuit set up, we're ready to test it. The first thing we'll need to do it load up our simulator. Once it's loaded, we'll execute it and display the results.

```python
simulator = Aer.get_backend('qasm_simulator')
result = execute(circuit, backend = simulator).result()

```

