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
%matplotlib inline
```

The line is used to make matplotlib graphs show up correctly in the jupyter notebook. You won't need this if you're using a different tool.

### Connecting your IBMQ account

Next, we need to connect your IBM account so that you can access their quantum systems. You'll need to log into your IBM account and grab your API token. Each token is different, and you shouldn't share it with anyone \(that would pose a security risk to your accont\). To find your token log into your IBM account, and head to the account page:

![A screenshot show where the account page can be found](../.gitbook/assets/image%20%2829%29.png)

Once you're there, you'll see the where you can copy your token:

![A screenshot showing where the copy token button can be found](../.gitbook/assets/image%20%2843%29.png)

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



