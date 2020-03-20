---
description: A very brief review of how classical bits work
---

# Classical Bits

## Information on Computers

Computers require information to be passed to them in a very specific format. We must include _explicit_ instructions about what to do next, for every single step of the process. Bits are the basic units of information on a computer system - they provide the basis for all instructions and decisions made on the system.

### Yes, No

Bits contain exactly one piece of information each - 1 \(for yes, true, on\), or 0 \(for no, false, off\). For non-theoretical systems, this means "high" voltage for 1 and "low" voltage for 0. The bit is a _physical_ quantity - we can measure it any time we like, but it needs to be stored [_\(Vahid, F. & Givargis, T. - 2002\)_](qubits-summary/qubit-references.md#diagram-of-serial-waveforms).

![Serial Waveforms](../.gitbook/assets/image.png)

You can see in the image above a voltage graph that illustrates this - the low portions are our 0 bits and the high portions are our 1 bits.

### Doing Work

In this situation we can tell two things for sure:

 First, a classical bit can only exist in one state at a time - it's either on or off. We can look at any time we like... it'll always be doing the same thing. We could even figure out the state of a bit indirectly - other information could lead us to the fact of what state that bit is in.

Second, a single bit isn't particularly useful... we can't do very much work with it. It's the combination of bits \(preferably a whole bunch of them\) that makes them useful. 

## Classical Error

### Electricity

Because a classic bit is a property of voltage, electricity going through a wire, there is potential for noise in our information.

We purposefully put a relatively wide gap between what we consider to be on and what we consider to be off. If the difference in _voltage_ between the two states is too close together, we get a mushy answer. This is because electricity is electrons traveling along the wire - we're never in a place where there are no electrons traveling along the wire at all. So technically the wire is never "all the way off".

### Fault Detection

How does the computer know if some kind of problem has occurred? Not a "dead stick of RAM" problem, nor a "my code won't compile" problem. A _fundamental_ problem.

Each "wire" gets measured by the system... each bit "self reports" about the state that it's in. How do we know that it's telling the truth?

In a regular computer system we do this through some clever math. We force the computer to check it's work and prove that the answer we got really is the answer the system arrived at. This allows us to rely on these fundamental, irreducible answers. The result is correct, the noise levels in our information remain at acceptable levels.

{% hint style="success" %}
This concept will become important later on. We need to understand the _clarity_ of the information we're looking at. How much precision can we expect?
{% endhint %}

