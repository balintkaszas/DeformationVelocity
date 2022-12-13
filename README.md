# The Objective Deformation component of a Velocity field


In this notebook, we present explicit calculations with the deformation velocity $\mathbf{v}_d$ associated to a given velocity field $\mathbf{v}$. 

This is defined following a decomposition of the original velocity field into two components

$$
\begin{equation}
\label{eq1}
\mathbf{v} = \mathbf{v}_{RB} + \mathbf{v}_{d},
\end{equation}
$$

where $\mathbf{v}_{RB}$ is the rigid body-component of the velocity field and $\mathbf{v}_d$ comes from deformations. 
We propose three criteria for defining $\mathbf{v}_{RB}$

- It should be a rigid body velocity field that is closest to the original velocity field in a physically relevant norm.

- The deformation component, which we get by subtracting $\mathbf{v}_{RB}$ from the original velocity field should be objective (or frame indifferent) in order to capture
intrinsic features of the fluid (see Truesdell & Noll (2004)),

- The deformation component should be observable: an appropriately chosen, single observer of the fluid flow should be able to measure this deformation velocity field over the whole domain.


Our approach is based on looking for the $\mathbf{v}_{RB}$ as the $L^{2}$ closest velocity field to the input velocity field $\mathbf{v}$. Without loss of generality, the rigid-body velocity field $\mathbf{v}_{RB}$ can be written as 

$$
\begin{equation}
\label{eq2}
\mathbf{v}_{RB} = \bar{\mathbf{v}} + \boldsymbol{\omega} \times (\mathbf{x} - \bar{\mathbf{x}}),
\end{equation}
$$

where the overbar denotes spatial averaging over a chosen domain $U \in \mathbb{R}^{3}$. We then minimize the functional defined as 

$$
L_{1}(\boldsymbol{\Omega},t) = \frac{1}{M}\int_{U}\left\{ \left|\mathbf{v}(\mathbf{\mathbf{x}},t)-\dot{\mathbf{x}}_{A}(t)-\boldsymbol{\Omega}(t)\left(\mathbf{x}-\mathbf{x}_{A}(t)\right)\right|^{2}\right\}\rho(\mathbf{x},t)dV,
$$

where M is the total mass contained in the volume $U$ and $\rho(\mathbf{x},t)$ is the density.

A unique minimizing angular velocity exists and can be written as
$$
\boldsymbol{\omega}=M\boldsymbol{\Theta}^{-1}\overline{(\mathbf{x}-\bar{\mathbf{x}})\times(\mathbf{v}-\bar{\mathbf{v}})},
$$

with the moment of inertia tensor defined as 

$$
\boldsymbol{\Theta} = M\overline{\left(\left|\mathbf{x}-\bar{\mathbf{x}}\right|^{2}\right)\mathbf{I}-(\mathbf{x}-\bar{\mathbf{x}})\otimes(\mathbf{x}-\bar{\mathbf{x}})}.
$$

In the following sections, we calculate the minimizing $\boldsymbol{\omega}$ and through it, the deformation velocity $$
\begin{equation}
\label{eq3}
\mathbf{v}_d = \mathbf{v} - \bar{\mathbf{v}} - \boldsymbol{\omega} \times (\mathbf{x} - \bar{\mathbf{x}}).
\end{equation}
$$

As shown in Kaszás, Pedergnana, & Haller (2022), the deformation velocity field defined in (3) is objective. This means, that an observer in the rotating $\mathbf{y}-$ frame will measure the velocity to be 

$$
\hat{\mathbf{v}} = \mathbf{Q}^T(t)\mathbf{v},
$$

if the (stationary) $\mathbf{x}-$ and (rotating and translating) $\mathbf{y}-$ frames are related by

$$
\mathbf{x} = \mathbf{Q}(t)\mathbf{y} + \mathbf{b}(t).
$$

