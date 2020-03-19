---
description: A basic overview of the relevant portions of classical mechanics
---

# Classical Mechanics

In physics we use mathematical models to describe the world around us. Classical mechanics includes models for medium sized stuff.

## Measuring Physical Systems

### Mass

Each object contains a certain amount of matter - what we could call it's _mass_. This is a more fundamental property than it's weight, which depends on how much gravity is a applied to it.

By knowing how _massive_ an object is we can calculate how much energy it will take to make some change to the position of that object.

### Position

Let's start with a static mass \(an object in this case - let's imagine a ball\) at a given position. We know _exactly_ where this object is, because we can go ahead and measured it directly.

![The position of our object in meters at 1 second - showing a single dot on a graph](../.gitbook/assets/image.png)

When measuring the position of our object, we decide where to "origin" is - where our 0 will be.

### Time

Everything occurs over a finite amount of time in our system. Similarly to the position, we measure time from some origin which we decide on. Everything that happens, happens _after_ some arbitrary point in the past that we designate as time 0.

As forces act on our object, it's position changes over time. if we kick the ball, we might construct a graph of it's movement that looks like this:

![The graph of the position of a ball over time - showing an upside down parabola](../.gitbook/assets/image%20%281%29.png)

First the ball goes up, and after a while it comes down.

{% hint style="info" %}
[More information about position vs. time graphs and how they're used](https://www.khanacademy.org/science/physics/one-dimensional-motion/displacement-velocity-time/a/position-vs-time-graphs)
{% endhint %}

### Force

Nobody is going anywhere unless we can affect some change on the system. _Forces_ are how we do that - they offer some quantifiable change to the _state_ of a given object.

#### State

The state of a system, or an object, is the collection of all the information we know about it. 

So, we might say that the state of our cat this that he is _at rest_ - he's sleeping, and going nowhere. The state of a system can be more complex - because systems are collections of multiple objects, there might be a lot of information that describes it's current state. The state of the cat cafe system may also be at rest - all of the cats are sleeping, and nobody is moving.

#### Types of Forces

There are a bunch of different types of forces - magnetic, nuclear, gravity. We won't discuss much about specific forces and how to calculate them. What's important for this tutorial is that you understand the concept [_\(Wikipedia - 2020\)_](../physics-references.md#representation-of-forces-image). 

![A few images illustrating forces](../.gitbook/assets/480px-force_examples.svg.png)

## Notation

An object in 3-D space can be described using a [_vector_](../linear-algebra/vectors.md#vectors), like we talked about in our discussion of [_space_](../linear-algebra/space-dimension-and-span.md#space).

Matrices are just says for us to store and manipulate information, and so we store the important information about our object in a column matrix. At any given moment in time, the relevant information about our object is it's position, and so our vector is a position vector.

So the vector $$|x\rangle$$ represents the position of our object, called $$x$$.

### Position and Time Together

Let's add some information to our position vector. The vector is _changing_. Changing how? Changing with respect to the _time._ How do we describe the change in position of object $$x$$ over some amount of \(with _respect_ to\) time $$t$$?

$$
|x(t)\rangle
$$

## Measuring Change



