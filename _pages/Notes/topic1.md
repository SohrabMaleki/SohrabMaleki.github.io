---
layout: archive
title: 'From Probabilistic Mechanics to Quantum Theory'
permalink: /notes/topic1/
---

## Description

In this paper, I dive into the evolution of the probability distribution of a mechanical system. If you've studied classical mechanics, you probably know that once we nail down the initial conditions (like position and velocity), we can solve Hamilton's equations to get a clear, deterministic picture of the system at any future time $t$.

But here's a twist: what if those initial conditions aren't set in stone? What if we're dealing with a <i>probability distribution</i> instead? This paper tackles that intriguing question and works out the <i>equation of motion</i> for the probability distribution itself. It's a pretty cool way to think about mechanics beyond the usual deterministic approach!

## [Download Paper in English](http://sohrabmaleki.github.io/files/From%20Probabilistic%20Mechanics%20to%20Quantum%20Theory.pdf)
## [Download Paper in Persian](http://sohrabmaleki.github.io/files/ProbClassicalMech-Fa.pdf)

## Results
The equation of motion for a general mechanical system is derived through this paper as

$$\frac{\partial f}{\partial t} = \sum_{i=1}^{3N} -\frac{\partial f}{\partial q_i} \frac{\partial\mathcal{H}}{\partial p_i} + \frac{\partial f}{\partial p_i} \frac{\partial\mathcal{H}}{\partial q_i}$$

This equation, as explained in paper, reduces for a one-dimensional particle to: 

$$-\frac{\partial f}{\partial t}=\frac{y}{m}\frac{\partial f}{\partial x}+F(x)\frac{\partial f}{\partial y}$$

where $y$ is momentum, $x$ is position and $F(x)=-\partial U/\partial x$ is the force field. 

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

### Periodic Potential

Particle with gaussian initial distribution arounnd zero (for position and momentum) in a periodic potential $U(x)=\cos(x)$:
<video width="640" height="360" controls>
  <source src="../../files/Cosine.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>