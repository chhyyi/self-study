# Chapter 7, 8
Lecture 6. Monatomic Harmonic Chain
## One-Dimensional Monatomic Chain
* Taylor Expansion of Potential of One-Dimensional Model: $V(x) = V_{eq}+\frac{\kappa}{2}(x-x_{eq})^2+\frac{\kappa_3}{6}(x-x_{eq})^3+...$
* Near equililibrium, potential of chain $V_{tot} = \sum_i V(x_i - x_{i+1}) = V_{eq} + \sum_i \frac{\kappa}{2}(\delta x_i-\delta x_{i+1})^2$ where $\delta x_n = x_n - x_n^{eq}$
* force on atom $n$ is $F_n = \kappa(\delta x_{n+1} - \delta x_n) + \kappa(\delta x_{n-1} - \delta x_n)$
* $m(\delta \ddot{x}_n) = \kappa(\delta x_{n+1} + \delta x_{n-1} - 2\delta x_n)$ where m is the mass of an atom.
* Let $\delta x_n = Ae^{i\omega t - ikx_n^{eq}} = Ae^{i\omega t - ikna}$ where $a$ is lattice constant, 
    * only consider $\omega\geq0$, because we will take only real parts.
* Then $-\omega^2 m = \kappa(e^{-ika} + e^{ika}-2)=2\kappa(\cos{ka}-1) = -4\kappa \sin^2{\frac{ka}{2}}$
* So $\omega = 2\sqrt{\frac{\kappa}{m}}|\sin\frac{ka}{2}|$ (eq 8.3)

### Dispersion Relation and Periodicity
* Dispersion relation $\omega(k)$ is shown in Figure 8.1.
* Brilluin Zone
* Reciprocal Space : periodic in $k\rightarrow k + 2\pi/a$
* Reciprocal Lattice $k_p = 2\pi p/a$ with $p$ an integer
    * direct lattice (real-space lattice) $x_n = na$
    * $e^{iG_mx_n}=1$ where $G_m$ is a member of reciprocal lattice

## Sound Waves
* In the low-$k$ limit, from eq 8.3, $v_{sound} = \omega/k = a\sqrt{\frac{\kappa}{m}}$
* This is same with eq7.3. In Chapter 7, it is predicted from compressibility and speed of soundwave of isotropic compressible fluid.
    * compressibility $\beta$ is $\beta = -\frac{1}{V}\frac{\partial{V}}{\partial{P}}$. In 1-dim,
    * In one dimensional case, $\beta = -\frac{1}{L}\frac{\partial{L}}{\partial{F}} = \frac{1}{\kappa x_{eq}} = \frac{1}{\kappa a}$ 
    * #Fund) from fluid course, $v_{soundwave} = \sqrt{\frac{B}{\rho}} = \sqrt{\frac{1}{\beta \rho}}$, where $$

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
