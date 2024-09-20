[1] Phonon hydrodynamics and its applications in nanoscale heat transport. *-Guo et al*
[2] Geometrical dependence of thermal conductivity in elliptical and rectangular nanowires *-Sellitto et al*
[3] Second law of thermodynamics and phonon-boundary conditions in nanowires *-Sellitto et al* 

Following a similar treatment for nanowires as with [thin films](Thermal%20Transport%20in%20Thin%20Films.md), we use the [G-K equation](Guyer-Krumhansl%20Equation.md) to estimate the heat flux across the cross-section. Note the use of cylindrical coordinates and the subsequent appearance of cylindrical Bessel functions of the first kind.

For nanoscale regime, we can ignore the heat flux as it would be negligible compared to the Laplacian term. For microscale we will proceed with the heat flux term as is. Under steady state conditions, we can say that $\mathbf{q}$ is a function of only radial distance, $q(r)$.
$$
q = -\lambda \nabla_zT + l^2\nabla^2q
$$
For the current derivation we assume that $\nabla_z T$ is constant in each transversal section. The bulk term is assumed to vanish near the boundary $\left(q_b(R) = 0\right)$ and the boundary term is then added to it in to account for nonlocal effects.
$$
q_b(r) = \lambda \left[1 - \frac{J_0(ir/l)}{J_0(iR/l)}\right]\frac{\Delta T}{L}
$$
$$
q_w(r) = -Cl\frac{\partial q_b}{\partial r}\bigg\rvert_{r = R} = -\lambda\left(C\left[\frac{iJ_1(iR/l)}{J_0^2(iR/l)}\right]J_0(iR/l)\right)\frac{\Delta T}{L} 
$$
Combining both to calculate total heat flux and obtain the effective thermal conductivity in terms of *Kn* as -
$$
\lambda_{eff} = \lambda \left(1 - 2\text{Kn}\left[\frac{J_1(i/\text{Kn})}{J_0(i/\text{Kn})}\right]^2\left[\frac{J_0(i/\text{Kn})}{iJ_1(i/\text{Kn})} + C\right]\right)
$$
where the cylindrical Bessel function of the first kind is of the form -
$$
J_n(z) = \left(\frac{z}{2}\right)^n \sum_{t = 0}^{\infty}\frac{(-1)^t\left(\frac{z}{2}\right)^{2t}}{t!(t+n)!}
$$

The same has been fully hand derived by me [here](Nanowire%20Derivation.pdf).
>[!info] Slight mismatch in the effective thermal conductivity expression, currently verifying the same with Mathematica.

However, the validity of simply adding needs the wall contribution and bulk contribution needs to be questioned.

Quotation from [3]
>In the linear approach used in G-K Equation and boundary condition for slip heat flux, the full local heat flow will be the sum of the bulk contribution plus the wall contribution. From the physical perspective, one could imagine more complicated situations where simple addition would no longer be valid; for instance, for some forms of the wall profile, the phonons could have a strong component normal to the wall after colliding with it, and their collisions with the phonons of the main flow could lead to a reduction in the total heat flow. However, a situation like this one would be nonlinear in the heat flow, as it would involve effects of the collisions of the wall flow with the bulk flow, which are not considered here.

