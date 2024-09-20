[1] Microscale Heat Conduction in Dielectric Thin Films. *-A. Majumdar*
[2] Phonon hydrodynamics and its applications in nanoscale heat transport. *-Guo et al*

#### EPRT Treatment

![Pasted image 20240920133729](Pasted%20image%2020240920133729.png)

The analysis of heat transport across the thin film depends on the nature of boundaries. Specular reflection at boundaries conserve momentum and can be treated as phonon images being transmitted through the boundary. Hence in the case of perfect specularity, the film can be modelled as a plane-parallel medium.
On the other hand, diffuse scattering poses a resistance to phonon transport and needs to be accounted for in the mean free path/relaxation time calculations. Let the diffusivity of the boundary be denoted by $d$, diffuse scattering probability. An increase in diffuse scattering probability essentially decreases the phonon mean free path.

**Heat Transport across Diamond Thin Films**
Once the relevant scattering contributions are analyzed and an effective relaxation time is obtained (as described [here](Phonon%20Scattering%20Mechanisms.md)), the [EPRT](Phonon%20Radiative%20Transport.md) can be solved with the intensity integral being approximated by Gaussian quadrature.
$$
\int_{-1}^{1}I(\mu) d\mu = \sum_{j = 1}^{2N}I(\mu_{j})w_{j}
$$
With the obtained intensities, the heat flux along the length of the thin film can be obtained as a function of non-dimensional length.
$$
q(\xi/\xi_L) = 2\pi\sum_{j=1}^{2N}\mu_j \,I_{j}(\xi/\xi_L)\,w_j
$$
where $\xi_L = L/l$  with $l$ being the mean free path for the particular impurity concentration.

Heat flux predicted by EPRT -
$$
\frac{q_E}{\sigma\left(T_{1}^{4} - T_{2}^{4}\right)} = \frac{1}{3/4\,\,\xi_L + 1}
$$
$$
q_{E} = \frac{4\sigma T^{3} \Delta T}{\frac{3}{4}\left(\frac{L}{l}\right) + 1}
$$
With effective thermal conductivity evaluating to be -
$$
\lambda = \frac{4\sigma T^{3} L}{\frac{3}{4}\left(\frac{L}{l}\right) + 1} = \frac{1}{3} Cv\left[\frac{l}{1 + \frac{4}{3}\left(\frac{l}{L}\right)}\right]
$$
as opposed to the thermal conductivity obtained from kinetic theory $\lambda = \frac{1}{3}Cvl$ (Ziman, 1960).
The study by Majumdar considered three different length scales and impurity concentrations, and concluded the following - 
1. As expected, at higher temperatures and larger film sizes purely diffusive transport was observed. While for lower temperatures and thinner films pure ballistic transport was noted.
2. Unless acoustic thickness is large, temperature jumps occur at boundaries. The magnitude of temperature jumps on the other hand is largely dependent on the crystal temperature.
3. Change in impurity concentration by a whole order of magnitude did not have as much an impact for the considered film sizes and temperature.
   When transport is purely ballistic or diffusive, impurity concentration has minimal impact.
4. The independence of temperature with respect to impurity concentration at low temperatures and acoustic thickness suggests the dominance of boundary scattering.

>[!info] The EPRT treatment essentially offers a modification to Fourier's Law that has better agreement with experimental data than the kinetic theory approximation of thermal conductivity.


#### Phonon Hydrodynamic Treatment
The EPRT assumes a constant heat flux profile across the cross-section. In a sense of speaking, the integration of boundary scattering to the relaxation time term provides average heat flux as the result. However in low Knudsen regimes, the value of heat flux at boundaries is lower than the center plane value.
The hydrodynamic analogy compares this boundary decay profile to the velocity profile in a microfluidic channel, where a slip is seen at the walls in non-continuum regimes.

A more rigorous and complete method for estimating heat flux in a thin film is by using the [Guyer-Krumhansl Equation](Guyer-Krumhansl%20Equation.md).
$$
\tau_R \frac{\partial \mathbf{q}}{\partial t} + \mathbf{q} + \lambda\nabla T = l^2\left[\nabla^{2}\mathbf{q} + 2\nabla(\nabla \cdot \mathbf{q})\right]
$$
*Slightly different but dimensionally consistent. The coefficient of RHS is replaced with the square of mean free path.*

![Pasted image 20240920175121](Pasted%20image%2020240920175121.png)

Under steady state conditions, the time derivative term on the LHS and the divergence term on the RHS vanish. The heat flux term is negligible in comparison to the Laplacian of heat flux in nanostructures. G-K equation thus reduces to -
$$
\lambda \nabla T = l^2 \nabla^2 \mathbf{q}
$$
The heat flux is assumed to consist of two parts, the bulk term $\mathbf{q}_b$ and the boundary term $\mathbf{q}_w$. The bulk term is the solution to the G-K equation presented above with conventional boundary conditions, while the boundary term arises due to nonlocal effects at the wall.
$$
\mathbf{q}_b = \frac{\lambda \Delta T}{2l^2L} \left(\frac{h^2}{4} - y^2\right)
$$
$$
\mathbf{q}_w = -Cl \frac{\partial \mathbf{q}_b}{\partial y} = C \frac{h \lambda \Delta T}{2lL}
$$
$$
\mathbf{q} = \mathbf{q}_b + \mathbf{q}_w = \frac{\lambda \Delta T}{2l^2L} \left(\frac{h^2}{4} - y^2\right) +  C\frac{h \lambda \Delta T}{2lL}
$$
Integrating over the channel cross-section yields the total heat flowrate and subsequently the effective thermal conductivity as -
$$
\lambda_{eff} = \frac{\lambda h^2}{12l^2}\left( 1 + \frac{6l}{h}C\right)
$$
However, in the microscale regime, the heat flux term cannot be considered negligible. Solving the resulting second order ODE gives the new effective thermal conductivity as -
$$
\lambda_{eff} = \lambda\left[1 - \frac{2l}{h}\tanh\left(\frac{h}{2l}\right)+C\tanh\left(\frac{h}{2l}\right)\right]
$$

Both results exhibit a size dependence and a reduction of effective thermal conductivity with reducing thickness of film. The heat flux boundary coefficient $C$ will depend on properties of the boundary (such as probability of diffuse scattering, as seen in the EPRT treatment).