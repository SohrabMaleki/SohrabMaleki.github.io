---
layout: archive
title: 'Probabilistic Mechanics'
permalink: /notes/ProbMech/
---

## Description

This paper discusses the evolution of probability distribution of a mechanical system. If you have studied classical mechanics, you probably know that if we specify initial conditions (initial position and velocity), solving the Hamilton's equations we obtain a unique and deterministic solution for state of the system in desired moment <i>t</i>.

But, have you thought about "What if the initial condition is not deterministic --i.e probability distribution"? This paper delves into this problem, find the equation of motion for the <i>"probability distribution"</i>.

[Download Paper](http://sohrabmaleki.github.io/files/ProbClassicalMech.pdf)
----

The equation of motion for a one-dimensional particle is derived through this paper as

$$\frac{\partial f}{\partial t} = \sum_{i=1}^{3N} -\frac{\partial f}{\partial q_i} \frac{\partial\mathcal{H}}{\partial p_i} + \frac{\partial f}{\partial p_i} \frac{\partial\mathcal{H}}{\partial q_i}$$

where $y$ is momentum and $x$ is position. This equation, as explained in paper, reduces to 

$$-\frac{\partial f}{\partial t}=\frac{y}{m}\frac{\partial f}{\partial x}+F(x)\frac{\partial f}{\partial y}$$

Stationary distributions must satisfy 

$$ f(x,y)=\frac{1}{Z}\exp\left[-\frac{\mathcal{H}(x,y)}{k_B T}\right]\quad,\quad Z\equiv\iint\exp\left[-\frac{\mathcal{H}(x,y)}{k_B T}\right]\;dx\;dy $$

which is highly similar to Boltzmann's distribution.

## Numerical Solutions

There are some numerical solutions to the given equations evaluated using Python.

### Harmonic Oscillator

Harmonic oscillator with momentum error much less than position error ($\sigma_p<<\sigma_x$):
<video width="640" height="360" controls>
  <source src="../../files/Harmonic.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

Harmonic oscillator stationary distribution (verifying the derived solution from paper):
<video width="640" height="360" controls>
  <source src="../../files/Harmonic - Stationary.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Free particle

Free particle with gaussian initial distribution around zero (for position and momentum)
<video width="640" height="360" controls>
  <source src="../../files/Free Particle.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Cosine Potential

Particle with gaussian initial distribution arounnd zero (for position and momentum) in a periodic potential $U(x)=\cos(x)$:
<video width="640" height="360" controls>
  <source src="../../files/Cosine.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>