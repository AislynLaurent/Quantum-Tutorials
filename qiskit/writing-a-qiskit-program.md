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
from qiskit.tools.monitor import job_monitor

%matplotlib inline
```

The line `%matplotlib inline` is used to make matplotlib graphs show up correctly in the jupyter notebook. You won't need this if you're using a different tool.

### Connecting your IBMQ account

Next, we need to connect your IBM account so that you can access their quantum systems. You'll need to log into your IBM account and grab your API token. Each token is different, and you shouldn't share it with anyone \(that would pose a security risk to your account\). To find your token log into your IBM account, and head to the account page:

![A screenshot show where the account page can be found](../.gitbook/assets/image%20%2833%29.png)

Once you're there, you'll see the where you can copy your token:

![A screenshot showing where the copy token button can be found](../.gitbook/assets/image%20%2849%29.png)

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

![A visualization of our empty circuit](../.gitbook/assets/image%20%2840%29.png)

### Applying Gates

Let's apply a Hadamard gate to the first qubit and a controlled not gate to both - afterward we'll measure the result.

```python
circuit.h(qr[0])
circuit.cx(qr[0], qr[1])

circuit.measure(qr, cr)

circuit.draw(output='mpl')
```

![A visualization of our circuit after applying gates and measuring](../.gitbook/assets/image%20%2810%29.png)

## Running your Circuit

### Testing on the simulator

Now that we have our little circuit set up, we're ready to test it. The first thing we'll need to do it load up our simulator. Once it's loaded, we'll execute it and display the results.

```python
simulator = Aer.get_backend('qasm_simulator')
result = execute(circuit, backend = simulator).result()

plot_histogram(result.get_counts(circuit))
```

![The graph showing which states were measured in our simulation](../.gitbook/assets/index.png)

We can see that the results make sense - the Hadamard gate imposed a uniform superposition on the control bit, and the controlled not gate depends on the state of the control bit. Therefore what we should see is about half $$|00\rangle$$ and about half $$|11\rangle$$ - that is, half of the time both qubits are in state $$|0\rangle$$ and half the time both qubits are in state $$|1\rangle$$.

### Running on a real quantum system

Since our test was successful, we're ready to run our code on an actual system. This means we need to load up the quantum system and prepare our job.

```python
provider = IBMQ.get_provider('ibm-q')
qcomp = provider.get_backend('ibmq_16_melbourne')
job = execute(circuit, backend=qcomp)

job_monitor(job)
```

When we submit our job, we'll see a few different messages:

![The message indicating our job is 6th in the queue](../.gitbook/assets/image%20%289%29.png)

![The message indicating the job is running](../.gitbook/assets/image%20%2841%29.png)

![The message indicating the job has been successfully run](../.gitbook/assets/image%20%2821%29.png)

This way we can track where we are in the queue and if our job is finished.

## Results

### Getting our results

Let's check what we got from the real quantum system:

```python
result = job.result()
plot_histogram(result.get_counts(circuit))
```

![The graph showing which states were measured in our job](../.gitbook/assets/index%20%281%29.png)

### Error

How strange - we're expecting about half $$|00\rangle$$ and about half $$|11\rangle$$... where are $$|01\rangle$$ and $$|10\rangle$$ coming from?

They come from inaccuracies in our quantum system. In the section about [_classical bits_](../qubits/classical-bits.md) we talked about [_sources of error and noise_](../qubits/classical-bits.md#fault-detection) __in typical systems. Because quantum systems are so much more complex, we have more potential sources of noise, and therefore end up with more potential for error. Sometimes, our _qubits_ end up where they shouldn't, and sometimes our _measurements_ are wrong.

As quantum systems get better, we'll get more accurate result. They'll start to be able to check their own work - the noise in the system will be reduced. For now, we'll always end up with a little bit of what we didn't expect, and we'll need to be careful to recognize that when we analyze our results.

