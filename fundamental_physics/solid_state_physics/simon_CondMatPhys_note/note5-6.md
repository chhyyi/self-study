# Chapter 5
## General considerations on Bonding
* H or Nucleus charge Z and 1 electron
    * Eigen state of the electron: indexed by quantum numbers
        * principal quantum numbers n: 1,2,3...
        * Angular momentum quantum number l = 0,1,2,3,4,...,n-1
        * magnetic quantum number m = -l, ... , +l
        * spin quantum number $\sigma = \pm 1/2$ 
        * $E_n = -\frac{\text{Ry}}{n^2}Z^2 + \text{small}$
* Aufbau Principle : Fill by shell,
    * [Madelung's Rule (at wikipedia)](https://en.wikipedia.org/wiki/Aufbau_principle#Madelung_energy_ordering_rule)
    * Why 4s then 3d: because $V(\vec{r})\not \propto\frac{1}{r}$

## Ionic Bonds
* $Na + Cl \rightarrow Na^+ +Cl^- \rightarrow NaCl$: electron transferred
* $\Delta E = E_{ION} - E_{AFF} - E_{COH}$
    * $E_{ionization} = E_{(Na^+ +e^-)}-E_{Na}$
    * $E_{affinity} = E_{(Cl+e^-)} - E_{Cl^-}$
    * $E_{cohesive} = E_{(Na^+ + Cl^-)}-E_{NaCl}$
    * In some books $\Delta E$ is defined as a cohesive energy
    * Cohesive energy is $\frac{1}{2}\sum_{i\neq j}\frac{q_i q_j}{4\pi \epsilon_0 |\vec{r}|}$
    * $E_{ion}, E_{aff}$: 
        * to the left of periodic table: small ionization energy
        * to the right of periodic table: large electron affinity 

## Covalent Bonds
* Particle in a box :
    * $H + H \rightarrow H_2$ because $\frac{\hbar^2 \pi^2}{2mL^2} + \frac{\hbar^2 \pi^2}{2mL^2} > 2\frac{\hbar^2 \pi^2}{2m(2L)^2}$
    * No $\text{He}_2$ because anti-bonding orbital will be occupied
* Molecular Orbital Theory or Thight Bingding Theory : $\text{H}_2^+$ example
    * consider 2 nuclei and 1 electron only
    * let two nuclei are fixed (Born-Openheimer Approximation)
        * Born-Openheimer Approximation : Wavefunctions of atomic nuclei and electrons in a molecule can be treated separately based on the fact that nuclei are much heavier than the electrons.
    * $H = \frac{\vec{P}}{2m} + V(\vec{r}-\vec{R_1}) + V(\vec{r} - \vec{R_2}) = K + V_1 + V_2$
        * where $R_1, R_2$ are displacements of each nuclei
        * Atomic orbital / Tight Binding Orbital (of the electron) $|1\rangle$, $|2\rangle$ 
            * $(K+V_1)|1\rangle = \epsilon_0|1\rangle$ and $(K+V_2)|2\rangle = \epsilon_0|2\rangle$
        * assume variational trial wavefunction (LCAO) $|\psi \rangle = \phi_1|1\rangle + \phi_2|2\rangle$
        * Then $\sum_j H_{ij} \phi_j = E\phi_i$ where $H$ is $\langle{i|H|j}\rangle$ ($2\times 2$ matrix).
            * #Q) why - footnote 13 on page 50. where $E = \frac{\langle \psi|H|\psi\rangle}{\langle{\psi|\psi}\rangle}$, From $\frac{\partial{E}}{\partial{\phi_1^*}}$ and $\frac{\partial{E}}{\partial{\phi_2^*}}$.
        * Rough(or bad) assumption; $\langle i | j \rangle = \delta_{ij}$
    * Then $H_{ij} = \langle{i|H|j}\rangle$ is
        * $\langle{1|H|1}\rangle = \langle{1|K+V_1|1}\rangle + \langle{1|V_2|1}\rangle = \epsilon_0 + V_{cross}$
        * $\langle{2|H|2}\rangle = \langle{2|K+V_2|2}\rangle + \langle{2|V_1|2}\rangle = \epsilon_0 + V_{cross}$
        * $\langle{1|H|2}\rangle = \langle{1|V_1|2}\rangle = -t$
        * $\langle{2|H|1}\rangle = -t^*$
    * solution of this eigenvalue equation (When t positive)
        * $E_\pm = \epsilon_0 + V_{cross} \pm |t|$
        * bonding $(\phi_1, \phi_2) = (\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}})$
        * anti-bonding $(\phi_1, \phi_2) = (\frac{1}{\sqrt{2}}, -\frac{1}{\sqrt{2}})$
