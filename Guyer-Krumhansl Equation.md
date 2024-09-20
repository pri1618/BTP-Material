[1] Phonon hydrodynamics and its applications in nanoscale heat transport. *-Guo et al*

$$
\tau_R \frac{\partial \mathbf{q}}{\partial t} + \mathbf{q} + \lambda\nabla T = \frac{1}{5}v_{g}^{2}\tau_R \tau_N\left[\nabla^{2}\mathbf{q} + 2\nabla(\nabla \cdot \mathbf{q})\right]
$$
$\tau_R$ and $\tau_N$ are the empirically obtained [relaxation times](Phonon%20Scattering%20Mechanisms.md) for the R processes and the N processes respectively.
$\lambda$ is the bulk thermal conductivity and $\mathbf{q}$ is the heat flux vector.

This form of the G-K Equation is very similar to the Navier-Stokes equation, the very similarity which lays a mathematical foundation for Phonon Hydrodynamics. The notable difference is the absence of a highly non-linear advection-like term $\left(\mathbf{v}\cdot\nabla\right)\mathbf{v}$ in the G-K equation.

##### Eigenvalue Analysis Method
For a phonon distribution function $f$ -
$$
\mathbf{D^{*}}f = (\mathbf{R^{*}} + \mathbf{N^{*}})f
$$
where the drift operator $\mathbf{D^{*}}$ contains the transient and advection terms while $\mathbf{R^{*}}$ and $\mathbf{N^{*}}$ are the collision operators for R and N type processes respectively.
In the limit of extremely temperatures, $\mathbf{R^{*}} << \mathbf{N^{*}}$, so only eigenvectors of the $\mathbf{N^{*}}$ operator are considered.

> [!info] G-K equation neglects the contribution of R type processes, while EPRT neglects the contribution N type processes. However there is still the appearance of a $\tau_R$ term in G-K equation.

##### Chapman-Enskog Method
The Chapman-Enskog method is used derive hydrodynamics equations (Navier-Stokes, Euler) from the basic Boltzmann Transport Equation. The fundamental idea behind the method is to asymptotically expand the phonon distribution function as -
$$
f = f_0 + \epsilon f_1 + \epsilon^{2}f_2 + \epsilon^3 f_3 + \cdot \cdot \cdot
$$
In hydrodynamic derivations, the factor $\epsilon$ is usually taken to be the *Kn* number. But in the case of phonon scatterings, the idea of mean free path becomes ambiguous due to the two types of scatterings, hence the parameter is assumed to be -
$$
\epsilon = \frac{\tau_N}{\tau_R}
$$
As the macroscopic variables are all various moments of the distribution function, any macroscopic variable $\mathbf{X}$ is expanded as -
$$
\mathbf{X} = \mathbf{X}_{0} + \epsilon \mathbf{X}_1 + \epsilon^2 \mathbf{X}_2 + \cdot \cdot \cdot
$$

These macroscopic variables such as energy density, momentum density, heat flux and flux of heat flux can be solved using the proposed multiscale expansion along with known conservations equations.