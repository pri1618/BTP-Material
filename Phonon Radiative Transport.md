# Phonon Radiative Transport

[1] Microscale Heat Conduction in Dielectric Thin Films -A. Majumdar

#### Equation of Phonon Radiative Transport

Heat transfer in dielectric crystalline materials is predominantly by atomic or crystal vibrations which travel within solids as waves. Energy of these waves are quantized as **phonons**.
Phonons in dielectric materials are scattered by boundaries, impurities, defects, and other phonons.

**Fourier's Law** accurately models heat transfer in macroscale.
$$q = -\lambda \nabla T$$
However, the law breaks down at smaller length scales as mean free path becomes almost equal to the length scale.
Thermal conductivity depends on the existence of a local temperature gradient, which stops having a physical sense when the points are separated by less than the mean free path. 

![Pasted image 20240731190555](./Images/Pasted%20image%2020240731190555.png)

>At lower temperatures, even thicker films would fall in the microscale regime as the mean free path increases as temperature decreases.

In the limiting case with no phonon scattering within the thin film, heat flux would be given similar to radiative transfer.
$$q = \sigma (T_{1}^{4} - T_{2}^{4})$$
A boundary that thermalizes phonons can be considered black in the sense of phonon radiation.
In physics, **thermalization** is the process of physical bodies reaching thermal equilibrium through mutual interaction.

**Casimir limit** for which thermal conductivity cannot be defined is reached when the two length scales (film thickness and mean free path) are almost comparable.

From one limiting case to the other ($l \lt\lt L$ to $l \sim L$), the heat conduction changes from diffusive to ballistic transport.

#### Phonon Transport

Statistics of phonons in thermodynamic equilibrium follows the Bose-Einstein statistics.
Transport of phonons leads to the transport of heat in dielectric solids.

**Semiclassical Boltzmann Equation**

$$\frac{\partial f}{\partial t} + v \cdot \nabla f + a\cdot \frac{\partial f}{\partial v} = \left(\frac{\partial f}{\partial t}\right)_{scatt}$$

$a$ is the particle acceleration and $f(r, v, t)$ is the distribution function.

For phonon heat transport, the third term is ignored. Phonons dominant in heat transport travel at the speed of sound. The speed of sound doesn't appreciably change with frequency. 
Ergo, $f(r,v,t)$ becomes akin to $f(r,t)$ as $v$ is pretty much constant for our concerns. 
Alternatively, the third term can be ignored by assuming a lack of external forces on the system.

> In a thin film, Fourier law may be valid for heat conduction in the plane of the film but will break down for heat conduction across the film.

$f$ is a function of position and time.
Simplification - $f$ varies only in the $x$ direction
Simplification - scattering term is simplified by the relaxation-time approximation. 

$$\frac{\partial f_{\omega}}{\partial t} + v_{x}\frac{\partial f_{\omega}}{\partial x} = \frac{f^{0}_ {w} - f_{w}}{\tau}$$

where $f_{\omega}$ is the distribution function as a function of phonon frequency $\omega$.
$f^{0}_{\omega}$ is the equilibrium phonon distribution, following Bose-Einstein Distribution.
${\tau}$ is the mean free time between scattering.


**Fourier's Law** (again)

On solving for heat flux we arrive at an expression similar to Fourier's Law - 

$$q_{x} = -\frac{dT}{dx} \int\tau v_{x}^{2}\frac{df^{0}_{\omega}}{dT}\hbar \omega \mathcal{D}(\omega)d\omega$$

under the assumption that phonon distribution at some point is equal to the equilibrium distribution. Naturally, since we arrive at the same Fourier's law, for applicability in the microscale regime we need to abandon the assumption.


**Phonon Radiative Transfer**

The idea behind phonon radiative transfer is presented by making a connection between phonons and photons and subsequently modifying the Boltzmann Transport Equation to arrive at a equation form similar to the Equation of Radiative Transfer.

Phonon intensity can be defined as - 

$$I_{\omega}(\theta, \phi, x, t) = \sum_{p}v(\theta, \phi)f_{\omega}(x, t)h\omega\mathcal{D}(\omega)$$

Intensity is the flux of energy per unit time, per unit area, per unit solid angle in the direction of phonon propagation, $v(\theta, \phi)$. 

The Boltzmann Equation is transformed to a one dimensional Equation of Phonon Radiative Transfer -

$$\frac{1}{v}\frac{\partial I_{\omega}}{\partial t} + \mu \frac{\partial I_{\omega}}{\partial x} = \frac{I^{0}_ {\omega}(T(x)) - I_{\omega}}{v\tau(\omega, T)}$$

$\mu$ is the direction cosine along the $x$ direction and $I^{0}_{\omega}$ is the equilibrium intensity corresponding to a blackbody (for temperatures below the Debye temperature).
After solving for intensity, the heat flux can be obtained as - 

$$q(x) = \int_{\Omega = 4\pi} \int_{0}^{\omega_{D}} \mu I_{\omega}(x, \omega, \Omega) d\omega d\Omega$$

EPRT does not account for phonon-phonon interactions. Moreover, since phase of lattice waves are not considered, interference effects are also not considered. Relevance of phase reduces if the thermalizing surfaces are diffuse.

>**Acoustic Thickness** - Ratio of mean free path to the physical thickness or principal geometric dimension of the medium.
>
>$$\xi_{L} = \frac{L}{v \tau(\omega, T)}$$
>
>where an acoustically thin medium has $\xi_{L} << 1$.  

In the limit of acoustically thick mediums, where the mean free path is much smaller than a geometric dimension of the medium. Under this limit, $q(x)$ resolves back to a form of Fourier's Law, hence attesting to the validity of EPRT.

In the limit of acoustically thin mediums, the expression for $q(x)$ is resolved to a form similar to photon radiation. 


**Simplification under Radiative Equilibrium** (and otherwise)

Assuming the condition for phonon radiative equilibrium, i.e., there are no sources or sinks, $\nabla \cdot q = 0$, we can arrive at an expression for $I^{0}_ {\omega}(T)$ can be obtained. A further assumption that there is radiative equilibrium at every frequency is imposed. The latter assumption is unphysical as the $\nabla \cdot q = 0$ condition only guarantees overall equilibrium.

$$I^{0}_ {\omega}(T) = \frac{1}{2}\int^{1}_ {-1} I_{\omega}d\mu$$

$$\frac{1}{v}\frac{\partial I_{\omega}}{\partial t} + \mu \frac{\partial I_{\omega}}{\partial x} = \frac{\left (\frac{1}{2}\int^{1}_ {-1} I_{\omega}d\mu\right ) - I_{\omega}}{v\tau(\omega, T)}$$

This equation is actually a general equation for radiative transport as even in the transient case the integral approximation for $I^{0}_ {\omega}(T)$ can be employed.

$$\frac{\partial U}{\partial t} + \nabla \cdot \pmb{q} = 2\int_{0}^{\omega_{D}} \frac{I^{0}_ {\omega_D}(T)}{v\tau} d\omega -\int_{-1}^{1}\int_{0}^{\omega_D}\frac{I_{\omega}}{v\tau} d\omega d\mu$$

LHS evaluates to 0 as per the first law of thermodynamics, which results in a similar simplification as presented for the steady case.

##### Additional Notes
1. The Hyperbolic Heat Equation can be derived from the transient form of EPRT by making the assumption that relaxation time is independent of frequency and that phonon distribution at some point is equal to the equilibrium distribution.
2. EPRT becomes a bit tricky to use when modelling processes where heat flux may vary along more than one dimension. For instance, case of a nanowire where heat flux may be $q(r,z)$.
3. EPRT does not suitably model phonon-phonon interactions. Accounts for scatterings ([Phonon Scattering Mechanisms](Phonon%20Scattering%20Mechanisms.md)) via equivalent relaxation time.
