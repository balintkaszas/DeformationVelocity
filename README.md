# The Objective Deformation Component of a Velocity Field


In this notebook, we present explicit calculations with the deformation velocity $\mathbf{v}_d$ associated to a given velocity field $\mathbf{v}$. 

This is defined following a decomposition of the original velocity field into two components

$$
\begin{equation}
\label{eq1}
\mathbf{v} = \mathbf{v}_{RB} + \mathbf{v}_{d},
\end{equation}
$$

where $\mathbf{v}_{RB}$ is the rigid body-component of the velocity field and the remaining part comes from deformations. 
We propose three criteria for defining the rigid body velocity field

- It should be a rigid body velocity field that is closest to the original velocity field in a physically relevant norm.

- The deformation component, which we get by subtracting $\mathbf{v}_{RB}$ from the original velocity field should be objective (or frame indifferent) in order to capture
intrinsic features of the fluid (see Truesdell & Noll (2004)),

- The deformation component should be observable: an appropriately chosen, single observer of the fluid flow should be able to measure this deformation velocity field over the whole domain.

This repository contains the implementation of the method proposed by B. Kaszás, T. Pedergnana and G. Haller (2022).



B. Kaszás, T. Pedergnana and G. Haller,_The Objective Deformation Component of a Velocity Field_, _European Journal of Mechanics - B/Fluids_ (in press 2022)
