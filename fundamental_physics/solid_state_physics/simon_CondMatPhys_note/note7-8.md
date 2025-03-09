
# Chapter 7, 8  
**Lecture 6: Monatomic Harmonic Chain**
(Revised by OpenAI o3-mini-high)

## One-Dimensional Monatomic Chain

- **Taylor Expansion of the Potential (1D Model):**  
  $
  V(x) = V_{\text{eq}} + \frac{\kappa}{2}(x - x_{\text{eq}})^2 + \frac{\kappa_3}{6}(x - x_{\text{eq}})^3 + \cdots
  $

- **Near Equilibrium:**  
  The total potential of the chain is given by  
  $
  V_{\text{tot}} = \sum_i V(x_i - x_{i+1}) = V_{\text{eq}} + \sum_i \frac{\kappa}{2}\bigl(\delta x_i - \delta x_{i+1}\bigr)^2,
  $
  where $\delta x_n = x_n - x_n^{\text{eq}}$.

- **Force on Atom $n$:**  
  $
  F_n = \kappa\bigl(\delta x_{n+1} - \delta x_n\bigr) + \kappa\bigl(\delta x_{n-1} - \delta x_n\bigr).
  $

- **Equation of Motion:**  
  $
  m\,\delta \ddot{x}_n = \kappa\bigl(\delta x_{n+1} + \delta x_{n-1} - 2\delta x_n\bigr),
  $
  where $m$ is the mass of an atom.

- **Assuming a Wave-Like Solution:**  
  Let
  $
  \delta x_n = A e^{i\omega t - ikx_n^{\text{eq}}} = A e^{i\omega t - ikna},
  $
  where $a$ is the lattice constant.  
  - **Note:** Only $\omega \ge 0$ is considered because we take only the real part of the solution.

- **Derivation of the Dispersion Relation:**  
  Substituting the wave-like solution into the equation of motion gives
  $
  -\omega^2 m = \kappa\left(e^{-ika} + e^{ika} - 2\right) = 2\kappa\bigl(\cos(ka) - 1\bigr) = -4\kappa \sin^2\left(\frac{ka}{2}\right).
  $
  Therefore,  
  $
  \omega = 2\sqrt{\frac{\kappa}{m}} \left|\sin\left(\frac{ka}{2}\right)\right| \quad \text{(eq. 8.3)}.
  $

- **aliasing:**
  $e^{ikna} = e^{ik(n+N)a}$
  
---

### Dispersion Relation and Periodicity

- The dispersion relation $\omega(k)$ is shown in Figure 8.1.
- **Brillouin Zone:**  
  Reciprocal space is periodic with  
  $
  k \rightarrow k + \frac{2\pi}{a}.
  $
- **Reciprocal Lattice:**  
  The reciprocal lattice vectors are given by (note that $\mathbb{Z}$ is integers)  
  $
  k_p = \frac{2\pi p}{a}, \quad \text{with } p \in \mathbb{Z}.
  $

  For the direct (real-space) lattice,
  $
  x_n = na.
  $
  Also, note that
  $
  e^{iG_m x_n} = 1,
  $
  where $G_m$ is a member of the reciprocal lattice.

---

## Sound Waves

- **Low-$k$ Limit:**  
  In the low-$k$ limit, from eq. (8.3),
  $
  v_{\text{sound}} = \frac{\omega}{k} = a\sqrt{\frac{\kappa}{m}}.
  $
  
- **Comparison with Chapter 7:**  
  This result is the same as that in eq. (7.3). In Chapter 7, the speed of sound in an isotropic compressible fluid is derived from its compressibility.
  - **Compressibility:**  
    The compressibility $\beta$ is defined as
    $
    \beta = -\frac{1}{V}\frac{\partial V}{\partial P}.
    $
    In one dimension,
    $
    \beta = -\frac{1}{L}\frac{\partial L}{\partial F} = \frac{1}{\kappa x_{\text{eq}}} = \frac{1}{\kappa a}.
    $
  - **Fundamental Result from Fluid Mechanics:**  
    $
    v_{\text{sound}} = \sqrt{\frac{B}{\rho}} = \sqrt{\frac{1}{\beta \rho}},
    $
    where $B$ is the bulk modulus and $\beta$ is the (adiabatic) compressibility.  
    From $\beta = 1/\kappa a$ and $\rho = \frac{m}{a}$ (1D), $v_{sound} = \sqrt{\frac{\kappa a^2}{m}}$

- **Group velocity and phase velocity**
  - #Q) I don't know why it is mentioned here.
  - **Group velocity** $\frac{d\omega}{dk}$  
    Group velocity is 0 where $k = \pm \frac{\pi}{a}$ (dispersion is flat)  
  - **Phase Velocity** $\frac{\omega}{k}$  
    #Q) *These two match in the case of a linear dispersion*

## Counting Normal Modes
- **Normal Modes:**  
  Every atom osciallate with same frequency
- **Assumption:**  
if there is N atom forming a big circle
- **Counting Normal Modes**  
  $e^{i\omega t - ikna} = e^{i\omega t - ikna - ikNa}$  
  $1 = e^{-ikNa}$  
  $k = \frac{2\pi p}{Na}$, where p is integer satisfies $-\pi/a \leq k \leq \pi/a$. In other words, spacing between neighboring k in k-space is $\frac{2\pi}{Na}$  
- **number of normal modes**  
  $(\frac{2\pi}{a})/(\frac{2\pi}{Na}) = N$ , **This is what Debye predicted**  
### Quantum Modes: Phonon
- **energy states of the model**  
  $E_n = \hbar\omega(n+1/2)$ 
### Crystal Momentum 

- **Modulo**
