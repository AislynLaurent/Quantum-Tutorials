---
description: A very basic overview of the relevant parts of quantum mechanics
---

# Quantum Mechanics

If you've read this document so far in one sitting, I'll commend you for that. I hope you've felt like it was informative. However... if you haven't yet, this is the moment to take a break. Have some tea, and make sure you've been able to follow along so far. Things are about to get _weird_.

Whereas classical mechanics tells us about medium size stuff \(so just about 100% of the things we interact with\), quantum mechanics deal with the tiniest stuff. The models used are much more complex, because stuff that small is very unpredictable.

You couldn't describe medium sized stuff with the same rules that you describe quantum sized stuff, simply because they don't behave in the same ways. The opposite is also true - the models used for medium sized stuff just aren't detailed enough to use on super small stuff.

## Quantum Systems

### N-Dimensional Space

Previously, we were talking about a mass \(an object\) in a 3-dimensional space. 

When we talk about quantum systems, we're instead talking about a _particle_ \(an object with very little mass\) in an $$N$$-dimensional space. That is to say, in a space without a defined number of dimensions. Which is to say, described by [_vectors_ ](../linear-algebra/vectors.md#vectors)with an undefined number of [_elements_](../linear-algebra/vectors.md#column-vectors).

This is because we can collect more _information_ about these particles than we could about the more simple objects. It's not necessarily simply about the location of these things... _more is happening_ down here in the world of very small things. 

It isn't helpful to attempt to think of the $$N$$-dimensions these particles live in as some kind of physical location. Matrices and vectors are about providing the necessary information to describe the thing they represent. For bigger stuff _where_ it is is enough. Down here, it isn't. Simple as that.

### Complex Numbers

Another thing that's different is the numbers we can use to describe quantum systems. Where before just the regular _real_ numbers were enough, now we'll also include _imaginary_ numbers. This is how we can model such complicated interactions.

#### Imaginary numbers

We use the imaginary number $$i$$ to describe questions we don't have an answer to. Like this:

$$
\sqrt{2} = i \hspace{8pt}\text{or}\hspace{8pt}i^2=-1
$$

$$i$$ is used to describe some imaginary unit, where we don't know the quantity. We extend the real numbers as we know them to include information we don't have a clear description for. We allow ourselves to include this in our calculations so we can describe things beyond our normal understanding.

#### Combinations including imaginary numbers

So if we take some multiple $$b$$ of the imaginary quantity $$i$$ and we combine it with some real quantity $$a$$, we get something like this:

$$
z = a+bi
$$

Where $$z$$ is the result. Even if we gave some values to $$a$$ and $$b$$...

$$
\text{Let}\hspace{6pt} a=4, \hspace{6pt} b=2
$$

$$
z = 4 + 2i
$$

...we wouldn't be able to calculate the value of $$z$$, because we can't separate $$2$$ and $$i$$. We have no idea what $$i$$ is, and so we have no idea what $$2i$$ is. This leaves us with two parts of $$z$$ - the real quantity $$4$$ and the imaginary quantity $$2i$$.

#### Complex numbers

So $$z$$ is a complex number - a combination of a real and imaginary quantity that we can't fully calculate. Some information exists, but we're not able to extract it.

{% hint style="info" %}
[An explanation of complex numbers](https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:complex/x2ec2f6f830c9fb89:complex-num/v/complex-number-intro)
{% endhint %}

### Quantum Vectors

So quantum vectors are:

* Column vectors
* Describe quantum particles
* Have $$N$$ number of elements
* Include elements that are complex numbers

{% hint style="info" %}
[More information about quantum vectors](http://physics.mq.edu.au/~jcresser/Phys301/Chapters/Chapter8.pdf)
{% endhint %}



