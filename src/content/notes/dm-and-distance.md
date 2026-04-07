---
title: "Why Does DM Tell Us How Far the Source Is?"
date: 2026-04-07
tags: ["astrophysics", "radio", "plasma", "dm"]
summary: "A note on why dispersion measure can be used as an indicator of propagation distance in a plasma medium."
---

# Why Does DM Tell Us How Far the Source Is?

## Dispersion relation in plasma

The dispersion relation in plasma is different from the one in vacuum. This is because plasma is an ionized medium containing a high density of free electrons. These electrons respond to the electric field, generate a current, and modify the electromagnetic wave.

We begin with the electron equation of motion:

$$
m_e \frac{d\mathbf{v}}{dt} = -e \mathbf{E}.
$$

Hence,

$$
\frac{d\mathbf{v}}{dt} = -\frac{e}{m_e}\mathbf{E}.
$$

We know that the current density is

$$
\mathbf{J} = -n_0 e \mathbf{v},
$$

so differentiating with respect to time gives

$$
\frac{d\mathbf{J}}{dt}
= -n_0 e \frac{d\mathbf{v}}{dt}
= -n_0 e \left(-\frac{e}{m_e}\mathbf{E}\right)
= \frac{n_0 e^2}{m_e}\mathbf{E}.
$$

Now use Maxwell's equations in Gaussian units:

$$
\begin{aligned}
\nabla \times \mathbf{E} &= -\frac{1}{c}\frac{\partial \mathbf{B}}{\partial t}, \\
\nabla \times \mathbf{B} &= \frac{1}{c}\frac{\partial \mathbf{E}}{\partial t} + \frac{4\pi}{c}\mathbf{J}.
\end{aligned}
$$

We would like to eliminate $\mathbf{B}$.

So take the curl of Faraday's law:

$$
\nabla \times (\nabla \times \mathbf{E})
= -\frac{1}{c}\frac{\partial}{\partial t}(\nabla \times \mathbf{B}).
$$

Substituting Ampère's law,

$$
\begin{aligned}
\nabla \times (\nabla \times \mathbf{E})
&= -\frac{1}{c}\frac{\partial}{\partial t}
\left(
\frac{1}{c}\frac{\partial \mathbf{E}}{\partial t}
+ \frac{4\pi}{c}\mathbf{J}
\right) \\
&= -\frac{1}{c^2}\frac{\partial^2 \mathbf{E}}{\partial t^2}
- \frac{4\pi}{c^2}\frac{\partial \mathbf{J}}{\partial t}.
\end{aligned}
$$

Using the vector identity discussed in the appendix,

$$
\nabla \times (\nabla \times \mathbf{E})
= \nabla(\nabla \cdot \mathbf{E}) - \nabla^2 \mathbf{E},
$$

and for a neutral plasma wave we take

$$
\nabla \cdot \mathbf{E} = 0,
$$

so that

$$
-\nabla^2 \mathbf{E}
= -\frac{1}{c^2}\frac{\partial^2 \mathbf{E}}{\partial t^2}
- \frac{4\pi}{c^2}\frac{\partial \mathbf{J}}{\partial t}.
$$

Therefore,

$$
\nabla^2 \mathbf{E}
= \frac{1}{c^2}\frac{\partial^2 \mathbf{E}}{\partial t^2}
+ \frac{4\pi}{c^2}\frac{\partial \mathbf{J}}{\partial t}.
$$

Substituting

$$
\frac{\partial \mathbf{J}}{\partial t} = \frac{n_0 e^2}{m_e}\mathbf{E},
$$

we obtain

$$
\nabla^2 \mathbf{E}
= \frac{1}{c^2}\frac{\partial^2 \mathbf{E}}{\partial t^2}
+ \frac{4\pi n_0 e^2}{m_e c^2}\mathbf{E}.
$$

Define the plasma frequency by

$$
\omega_p^2 = \frac{4\pi n_0 e^2}{m_e}.
$$

Then the wave equation becomes

$$
\nabla^2 \mathbf{E}
- \frac{1}{c^2}\frac{\partial^2 \mathbf{E}}{\partial t^2}
- \frac{\omega_p^2}{c^2}\mathbf{E} = 0.
$$

Assume a plane-wave solution

$$
\mathbf{E} = \mathbf{E}_0 e^{i(\mathbf{k}\cdot\mathbf{r} - \omega t)}.
$$

Then

$$
\begin{aligned}
\nabla^2 \mathbf{E} &= -k^2 \mathbf{E}, \\
\frac{\partial^2 \mathbf{E}}{\partial t^2} &= -\omega^2 \mathbf{E}.
\end{aligned}
$$

Substituting into the wave equation gives

$$
-k^2 \mathbf{E}
- \frac{1}{c^2}(-\omega^2 \mathbf{E})
- \frac{\omega_p^2}{c^2}\mathbf{E} = 0,
$$

hence

$$
-k^2 + \frac{\omega^2}{c^2} - \frac{\omega_p^2}{c^2} = 0.
$$

Therefore the dispersion relation is

$$
\omega^2 = \omega_p^2 + c^2 k^2.
$$

## Phase velocity

The phase velocity is

$$
v_{\mathrm{ph}} = \frac{\omega}{k}.
$$

Using the dispersion relation,

$$
\begin{aligned}
v_{\mathrm{ph}}
&= \frac{\omega c}{\sqrt{\omega^2 - \omega_p^2}} \\
&= c \sqrt{\frac{\omega^2}{\omega^2 - \omega_p^2}} \\
&= \frac{c}{\sqrt{1 - \omega_p^2/\omega^2}}.
\end{aligned}
$$

## Group velocity

The group velocity is

$$
v_g = \frac{d\omega}{dk}.
$$

From

$$
\omega^2 = \omega_p^2 + c^2 k^2,
$$

differentiate with respect to $k$:

$$
2\omega \, d\omega = 2c^2 k \, dk.
$$

So,

$$
\frac{d\omega}{dk} = \frac{c^2 k}{\omega}.
$$

Now use

$$
k = \frac{\sqrt{\omega^2 - \omega_p^2}}{c},
$$

to get

$$
\begin{aligned}
v_g
&= \frac{c^2}{\omega}\frac{\sqrt{\omega^2 - \omega_p^2}}{c} \\
&= c\sqrt{1 - \frac{\omega_p^2}{\omega^2}}.
\end{aligned}
$$

For radio waves with $\omega \gg \omega_p$, we expand:

$$
v_g \approx c\left(1 - \frac{1}{2}\frac{\omega_p^2}{\omega^2}\right).
$$

And also

$$
\frac{1}{v_g}
= \frac{1}{c}\left(1 - \frac{\omega_p^2}{\omega^2}\right)^{-1/2}
\approx \frac{1}{c}\left(1 + \frac{1}{2}\frac{\omega_p^2}{\omega^2}\right).
$$

One useful relation in plasma is

$$
v_g v_{\mathrm{ph}} = c^2.
$$

## Time delay and dispersion measure

The travel time through a path element $dl$ is

$$
dt = \frac{dl}{v_g}
\approx \frac{dl}{c} + \frac{1}{2c}\frac{\omega_p^2}{\omega^2}dl.
$$

Thus the delay is

$$
\Delta t
= \int \frac{1}{2c}\frac{\omega_p^2}{\omega^2}dl.
$$

Using

$$
\omega_p^2 = \frac{4\pi n_e e^2}{m_e},
$$

we obtain

$$
\begin{aligned}
\Delta t
&= \int \frac{1}{2c}\frac{4\pi n_e e^2}{m_e \omega^2}dl \\
&= \frac{2\pi e^2}{m_e c \omega^2}\int n_e \, dl.
\end{aligned}
$$

Now use

$$
\omega = 2\pi \nu,
$$

so that

$$
\omega^2 = 4\pi^2 \nu^2.
$$

Therefore,

$$
\begin{aligned}
\Delta t
&= \frac{2\pi e^2}{m_e c (4\pi^2 \nu^2)}\int n_e \, dl \\
&= \frac{e^2}{2\pi m_e c}\frac{1}{\nu^2}\int n_e \, dl.
\end{aligned}
$$

Finally, introducing the dispersion measure

$$
\mathrm{DM} = \int n_e \, dl,
$$

the delay can be written as

$$
\Delta t
= \frac{e^2}{2\pi m_e c}\frac{\mathrm{DM}}{\nu^2}.
$$

This indicates that the time delay measured at different frequencies tells us how many electrons the signal encountered along the way. If the electron density along the path is approximately uniform on average, then a larger DM generally suggests a larger propagation distance.

## Appendix: Proof of the vector identity

### Proof of $\nabla \times (\nabla \times \mathbf{E}) = \nabla(\nabla \cdot \mathbf{E}) - \nabla^2 \mathbf{E}$

Using index notation, the $i$-th component of the left-hand side is

$$
\begin{aligned}
\left[\nabla \times (\nabla \times \mathbf{E})\right]_i
&= \epsilon_{ijk}\,\partial_j (\nabla \times \mathbf{E})_k \\
&= \epsilon_{ijk}\,\partial_j \left(\epsilon_{klm}\,\partial_l E_m\right).
\end{aligned}
$$

Now use the Levi-Civita contraction identity

$$
\epsilon_{ijk}\epsilon_{klm}
= \delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}.
$$

Therefore,

$$
\begin{aligned}
\left[\nabla \times (\nabla \times \mathbf{E})\right]_i
&= (\delta_{il}\delta_{jm} - \delta_{im}\delta_{jl})\,\partial_j \partial_l E_m \\
&= \partial_i \partial_m E_m - \partial_l \partial_l E_i.
\end{aligned}
$$

Recognizing the two terms,

$$
\begin{aligned}
\partial_i \partial_m E_m &= \left[\nabla(\nabla \cdot \mathbf{E})\right]_i, \\
\partial_l \partial_l E_i &= (\nabla^2 \mathbf{E})_i,
\end{aligned}
$$

we obtain

$$
\left[\nabla \times (\nabla \times \mathbf{E})\right]_i
= \left[\nabla(\nabla \cdot \mathbf{E})\right]_i - (\nabla^2 \mathbf{E})_i.
$$

So

$$
\nabla \times (\nabla \times \mathbf{E})
= \nabla(\nabla \cdot \mathbf{E}) - \nabla^2 \mathbf{E}.
$$
