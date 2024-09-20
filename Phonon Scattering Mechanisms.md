# Phonon Scattering Mechanisms

[1] Microscale Heat Conduction in Dielectric Thin Films. *-A. Majumdar*

[2] Phonon hydrodynamics and its applications in nanoscale heat transport. *-Guo et al*

#### Classification of Mechanisms
Scattering mechanisms are classified as Normal (N) processes and Resistive (R) processes.
N processes conserve quasi-momentum while R processes do not. Differ from normal scattering mechanisms in that sense that phonon can be created or annihilated by virtue of being virtual particles.
Since phonons can be annihilated or created, we see both N and R type three phonon processes.

![Pasted image 20240919195226](./Images/Pasted%20image%2020240919195226.png)

> **Quasi-momentum** or crystal momentum is a momentum-like vector associated with electrons (in this case, phonons) in a crystal lattice. Defined with associated wave vector.
> 
> $$\mathbf{p}_{crystal} = \hbar \mathbf{k}$$
> 
> Similar in many respects to mechanical momentum.

> **Reciprocal Space/Lattice** is the dual of physical space (lattice) and is the momentum space. The reciprocal lattice exists in the mathematical space of spatial frequencies.


> **First Brillouin Zone** is basically the region within a primitive cell in reciprocal space. Like Bravais lattices are to Wigner-Seitz cells, Reciprocal lattice is to Brillouin zones.
> The first Brillouin zone is the locus of points in reciprocal space that is closest to the lattice point with respect to which the Brillouin zone is defined. 

**Three Phonon Processes**
Propagation of lattice wave creates a local strain field in it's path. When another lattice wave incidents this strain field, it encounters a change in properties and thus scatters. Also known as intrinsic processes as they can occur even in perfect crystals.
When the temperature elevates to a higher value, the combination of two phonons easily goes outside the first Brillouin zone, which falls under R process. Thus R type three phonon processes dominate N type at higher temperatures.

Four phonon processes are only relevant at temperatures higher than the Debye temperature.

#### Resistive Processes (R)
R processes directly introduce thermal resistance by destroying phonon quasi-momentum. They are modelled via effective relaxation times. 

1. Umklapp Process
   *(Berman, 1976)*
   
   $$\tau_{U} = A\frac{T}{\theta_{D}\omega}exp\left(\frac{\theta_{D}}{\gamma T}\right)$$

   where $A$ and $\gamma$ are crystal specific constants and $\theta_{D}$ is the Debye temperature.
   
3. Phonon-Imperfection Scattering
   *(Vincenti and Kruger, 1977)*
   
   $$\tau_{i} = \frac{1}{\alpha \psi \eta v}$$
   
   where $\eta$ is the scattering site density and $\psi$ is the scattering cross-section. $\psi$ is dependent on properties of the scattering site as well as the phonon itself, thus introducing temperature dependence for $\tau_i$.
   
5. Phonon-Boundary Scattering
   Dominates at very low temperatures and in acoustically thin mediums.

**Resistive Processes and Temperature**
At very low temperatures boundary scattering dominates. As the temperature increases, impurity scattering becomes important and a further increase in temperature makes U processes dominant and the N processes negligible. It is in the intermediate range between boundary scattering and U process that N processes play a role.

**Effective Relaxation Time**
As per Matthiessen rule -

$$\frac{1}{\tau_{eff}} = \frac{1}{\tau_{i}} + \frac{1}{\tau_{U}}$$

Akin to adding up resistances posed by each type of process, valid under the assumption that scattering processes are independent of each other.

##### Normal Processes (N)
N processes don't offer a direct resistance to thermal transport as they conserve quasi-momentum. However, they play a role in redistributing the phonon energy across different frequencies.
Other R processes, as seen prior, are dependent on frequency of photons, therefore they are to a certain extent dependent on the N processes too. Due to this indirect nature of influence, it is comparatively more difficult to model the contribution of N processes in something as simple as a component of relaxation time.

##### Energy and Momentum Balance Equations

$$\hbar \omega_{1} + \hbar \omega_{2} = \hbar \omega_{3} $$

$$\hbar \mathbf{k}_ {1} + \hbar \mathbf{k}_ {2} = \hbar \mathbf{k}_{3} + \mathbf{G}$$

where $\mathbf{G}$ is the reciprocal lattice vector, and $\mathbf{G} = 0$ corresponds to N processes.

![Pasted image 20240919233748](./Images/Pasted%20image%2020240919233748.png)

#### Callaway Relaxation Approximation
The collision term for the Boltzmann equation can be approximated using $\tau_{R}$ and $\tau_N$. Both relaxation times are frequency and temperature dependent. The Callaway approximation simplifies the solving the Boltzmann equation due to its linear nature.

$$C(f) = - \frac{f - f_{R}^{eq}}{\tau_R} - \frac{f - f^{eq}_{N}}{\tau_N}$$

