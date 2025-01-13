# Simon, Condensed Matter Physics (2014) Note
As I found that ashcroft & Mermin's solid state physics is quite hard to follow, I decided [Steve Simon's condensed matter physics lecture, 2015, oxford univ](https://www-thphys.physics.ox.ac.uk/people/SteveSimon/condmat2015/condmat.html). It have materials available on web, both textbook(but 2012 version) and [lecture video - oxford podcast](https://podcasts.ox.ac.uk/03-drude-theory-electrons-metals-sommerfeld-free-electron-theory-electrons-metals) (another [one on youtube](https://www.youtube.com/playlist?list=PLd9hKAUC3AZuo7is-aN45pmfDwJHOqKAj))

## notations
There will be 3 types of items.
1. Summary (default): keyword and summary of the lecture
2. fundamental : Something assumed to be familiar, more fundamental things but I am not sure (So I want to check again), starts with #F: or #Fund:
3. Questions : may have answers as a subitem. starts with #Q:

## Chap 1.
### Heat Capacity
* #Fund: heat capacity $C$, ideal gas $C_v = 3k_B/2$ per atom, Avogadro's number $R$
* Law of Dulong-Petit $C = 3k_B$ per atom or $C = 3R$ : knwon heat capacity for many solids in room temperature in early 19C.
* #Fund: Boltzman model (1896) classical stat. mech. model, agree with $C = 3k_B$

### Einstein's calc.
* #F: Thermal/stat phys
    * eigenstates of a single harmonic oscillator $E_n = \hbar \omega(n+1/2)$, 
        * where $\omega$ is 'Einstein frequency'.
    * (standard notation) $\beta = 1/(k_B T)$
    * Partition function $Z_n = \sum_{n\geq 0}e^{-\beta E_n}$
    * expectations of energy from partition function : $\langle E \rangle = -\frac{1}{Z}\frac{\partial{Z}}{\partial{\beta}}$  
* Then, Expectation of energy is $\hbar \omega [1/2 + 1/(e^{\beta \hbar \omega}-1)]$ or   
    $\langle{E} \rangle_{osc} = \hbar \omega[1/2 + n_B(\beta \hbar \omega)]$, where $n_B(x) = 1/(e^{x}-1)$ (eq 2.1)
    * $n_B$ is Bose occupation factor
    * #Q) interpretation : "the mode $\omega$ is an excitation that is excited on average $n_B$ times or equivalently, there is a boson orbital which is occupied by $n_B$ bosons"
* Then, Heat Capacity is $C = \partial{\langle E \rangle }/\partial T = \frac{\hbar^2 \omega^2}{k_B T^2}(e^{\beta \hbar \omega })/(e^{\beta \hbar \omega}-1)^2$
    * High temperature limit ($k_B T \gg \hbar \omega$), Heat capacity $C/N = k_B$ (cuz expansion of $e^x$ around $x=0$ is $e^x = 1 + x + \frac{x^2}{2!}\dots$)
    * Low temperature limit ($k_B T \ll \hbar \omega$), Heat capacity $C\rightarrow +0$. 
* But low temperature limit is different from the experimental results. 

### Example: Diamond
$w = \sqrt{k/m}$ is extremely large, room temperature is far below the high-temperature limit.

## Chap 2. Debye Model

### Periodic(Born-Von-Karmen) Boundary Condition 
* Instead of 'Box' boundary condition, cuz mathmatically it is simple.
* Let general solution $e^{ikr}$(plane wave), BC gives $e^{ikr} = e^{ik(r+L)}$. Then $k=2\pi n/L $
* In this case, $\sum_k \rightarrow \frac{L}{2\pi}\int_{-\infty}^{\infty}{dk}$. 
* in 3-D, $\sum_{k_x}\sum_{k_y}\sum_{k_z} = (\frac{L}{2\pi})^3 \int dk_x \int dk_y \int dk_z = (\frac{L}{2\pi})^3\int_0^{\infty}4\pi k^2 dk$ 

### Debye's calc. following Planck
* Planck calculated light as quantized wave. Debye did it for soundwave in solid. 
* As an analogy to Einstein's calculation, Debye derived the 'energy of the system' instead of an oscillator (Eventually about soundwave), $\langle{E}\rangle_{tot} = 3\sum_{modes}\hbar \omega_{mode}(1/2 + n_B[\beta\hbar\omega_{mode})]$ 
    * 3 came from the polarization of the soundwave (one longitudinal, two transverse)
    * #Q) Einstein's model에서도 heat capacity를 구하기 위해 결과적으로 불연속적인 $\omega$에 대해 summation을 하지 않았나? ($-\frac{1}{Z}\frac{\partial{Z}}{\partial \beta}$) 여기서 전체 에너지를 구하기 위한 summation의 $\omega_{modes}$랑 그것은 어떤 관계인가? Relation of Einstein frequency and $\omega_{modes}$ here?
        * A) see the interpretation after two equation. Einstein assumed single oscillators so $\omega$ was just an open parameter. Debye introduced 'soundwave' and 'PBC' so $\omega_{modes}$ becomes a group of discrete numbers. (So Simon says ***each excitation mode is a boson of freqeuncy $\omega(\vec{k})$ and it is occupied on average $n_B{\beta \hbar \omega(\vec{k})}$*** )
* It is assumed that velocity is independent to the polarization. So $\omega = vk$
    * Then $\langle{E}\rangle_{tot} = 3\int_{0}^\infty 4\pi k^2 (\frac{L}{2\pi})^3 \hbar \omega [n_B(\beta \hbar \omega)+1/2] dk = 12\pi (\frac{L}{2\pi})^3\int_0^\infty \frac{\omega^2}{v^3} \hbar \omega [n_B(\beta \hbar \omega)+1/2]d\omega$
    * If 'density of state' is $g(\omega)$, $\langle{E}\rangle_{tot} = \int_0^\infty g(w) \langle{E}\rangle{} (\omega)d\omega$  
        where $g(\omega) =  \frac{12\pi L^3 \omega^2}{8\pi^3 v^3}$  
    * Let $nL^3 = N$, then $g(\omega) = N\frac{9\omega^2}{\omega_d^3}$ where debye frequency $\omega_d$ is $\omega_d^3 = 6\pi^2 n v^3$
* Difference from the Planck's result for quantum energy of light waves,
    * replaced $2/c^3$ by $3/v^3$
    * zero point energy of each oscillator, $\hbar\omega/2$
    * This integration diverges. but, If we ignore zero point energy cuz its integration will be independent to temperature T, then  
        $\langle E \rangle = \int_0^\infty N\frac{9\omega^2}{\omega_d^3}\hbar\omega[1/(e^{\beta \hbar \omega}-1)]d\omega + T \text{ independent const.} =\frac{9N\hbar}{\omega_d^3} \int_0^\infty \frac{\omega^3}{(e^{\beta \hbar \omega}-1)}d\omega + T \text{ independent const.} $
        * utilizes $\int_0^\infty \frac{x^3}{e^x-1}dx = 3!\sum_{n=1}^\infty \frac{1}{n^4}$  
    * Then $\langle E \rangle = 9N \frac{(k_B T)^4 \pi^4}{(\hbar \omega_d)^3 15} + T \text{ independent const.}$  
        So heat capacity is $C = \partial{\langle E \rangle}/\partial{T} \sim T^3$

### Debye's "Interpolation"
* #Q)Why? *"Debye understood that the problem with his approximation
is that it allows an infinite number of sound wave modes — up to arbitrarily large k. This would
imply more sound wave modes than there are atoms in the entire system."*
* As $\int_0^\infty d\omega$ yield infinite number of modes, Debye introduced cutoff frequency which satisfies $3N = \int_0^{\omega_{cutoff}} g(\omega)d\omega$
    * with $g(\omega) = N\frac{9\omega^2}{\omega_d^3}$, it becomes $3N = N\frac{3\omega_{cutoff}^3}{\omega_d^3}$, so $\omega_{cutoff}=\omega_d$
* With cutoff frequency,  $\langle E \rangle_{tot} = \int_0^{\omega_D}g(\omega)\hbar \omega [n_B(\beta\hbar\omega)+1/2]d\omega$
    * Low temperature limit : No difference, $k_B T\ll \hbar \omega \rightarrow \beta \hbar \omega \gg 1$. so, $e^{\beta\hbar\omega}$ converges to 0 before it reaches the debye frequency. #Q) really?
    * High temperature limit : $\beta \hbar \omega \ll 1$, so $n_B \rightarrow \frac{k_B T}{\hbar \omega}+1/2$. without T independent term, it gives $\langle E \rangle_{tot} = \int_0^{\omega_D}g(\omega)\hbar \omega n_B(\beta\hbar\omega)d\omega = k_B T\int_0^{\omega_D}g(\omega)d\omega = 3Nk_B T$  
    So $C = \frac{\partial{\langle{E}\rangle_{tot}}}{\partial T} = 3Nk_B$
* It matches well with the experimental results in two limit **without free parameter** (note that Einstein's calculation had a fitting parameter, Einstein frequency.)
* Still wrong cuz...
    * cutoff frequency is AD-HOC (AD-HOC : for this, 특별한 목적을 위해)
    * not exact at intermediate temperature
    * $\omega = vk$ is wrong if k is high(very high frequency) -> 
        * #Q) wavelength become comparable to... what?? core?
    * In the case of Metals, $C = \alpha T^3 + \gamma T$ at low frequency

## Chap 3. Drude Theory
* Kinetic theory of gases on electron within metal.
* Assumptions of Drude theory:
    1. Scattering time $\tau$, probability of collision during $dt$ is $dt/\tau$.
    2. after the scattering event, $\vec{p} = 0$
        * #Q) In Ashcroft & Mermin, it was average momentum $\vec{p}_{avg}=0$? A) See p20, footnote 4.
    3. In between scattering, electron experiences the force $\vec{F}=-e(\vec{E}+\vec{v}\times\vec{B})$ only.
* ***transport equation*** $d\vec{p}/dt = \vec{F} - \vec{p}/\tau$ (eq 3.1)
    * During $dt$, electrons may scatter or not. If not, $\vec{p}(t+dt) = (1-dt/\tau)(\vec{p}(t)+\vec{F}dt)$, If scatter, $\vec{p}_{scattered}(t+dt) \sim (dt/\tau)\vec{F}dt \propto  (dt)^2$ so Ignorable.

### Hall Coefficient
* In steady state, $d\vec{p}/dt = 0$. then $\vec{p}/\tau = -e(\vec{E}+\vec{v}\times\vec{B})$
    * If static E-field (wihtout magnetic field), $m\vec{v}/\tau = -e{E}$. ($m$ is mass of an electron) 
        * Then, from $\vec{j}=n(-e)\vec{v}$ (where $n$ is density of electrons), 
        * current $\vec{j} = \frac{ne^2\tau}{m}\vec{E}$
        * then **conductivity** $\sigma = \frac{ne^2\tau}{m}$ and **resistivity** $\rho = \frac{m}{ne^2\tau}$, now scattering time (relaxation time) can be derived from $\sigma$ or $\rho$.
    * If static electric and magnetic field, 
        * let resistivity $\rho$ is $3\times 3$ matrix. 
        * then $\vec{E} = \frac{1}{ne}\vec{j}\times\vec{B} + \frac{m}{ne^2\tau}\vec{j} = \rho \vec{j}$. 
        * with indices, $E_i = \sum_l\rho_{il}j_l$. 
        * If we assume magnetic field in $\hat{z}$-direction, 
        * $\rho_{xy} =-\rho_{yx} = \frac{B}{ne}$
        * #Q) why he abandoned matrix $\rho$ in 2014 lecture?
    * Hall coefficient $R_H = \frac{\rho_{yx}}{|B|}$ which is $\frac{-1}{ne}$ in the drude theory
        * (Originally $R_H$ is defined as $\vec{E}_{Hall} = R_H\vec{B}\times\vec{j}$)
        * Hall coefficient gives numbers of free electron per atom, $n/\text{[density of atoms]} = \frac{-1}{eR_H}/\text{[density of atoms]}$
        * valence electron (electrons of outermost shell) move, core orbital electrons don't move. 
        * positive Hall coefficient implies that charge of the carrier is positive.
        
### Thermal Conductivity
* #fund)  thermal conductivity $\kappa$(kappa) satisfies $\vec{j}^q = - \kappa\nabla{T}$ where $\vec{j}^q$ is heat flux
* #fund)From Boltzmann's kinetic theory of gases 
    * thermal conductivity of monatomic gas: $\kappa=\frac{1}{3}nc_v\langle v \rangle\lambda$, 
        * where $c_v = C_v/N$, 
        * $\langle v \rangle = \sqrt{\frac{8k_B T}{\pi m}}$.
    * scattering length $\lambda = \langle v \rangle \tau$
    * $c_v = \frac{3}{2} k_B$
* Then $\kappa = \frac{4}{\pi} \frac{n\tau k_B^2 T}{m}$.

#### Thermal conductivity and Lorentz number 
* It gives that Lorentz number $L = \frac{\kappa}{T\sigma}$ is same for all materials and all T
    * Known as Wiedermann - Franz law (experimentally, for metal).
    * two mistakes; specific heat capacity overestimated, $\langle v \rangle$ underestimated
        * However, the two errors canceled each other out, resulting in a fairly accurate outcome. (about 2 times smaller than actual value)

#### Seebeck coefficient
* ***Peltier effect*** 
    * Peltier coefficient $\Pi$ satisfies: $\vec{j}^q = \Pi \vec{j}$
* #fund) from kinetic theory of gases, $\vec{j}^q = \frac{1}{3}(c_v T)n\vec{v}$
    * #Q)why? *$c_v T$ is heat carried by one particle*
    * $\vec{j} = -en\vec{v}$
    * Thus $\Pi = - \frac{c_v T}{3e} = -\frac{k_B T}{2e}$
* ***Seebeck coefficient*** $S = \Pi/T = -k_B/2e$
* this results is about 100 times larger than actual value, because of overestimated $c_v$
* #Q) why it is far from actual value?
    * A) It does not use $v$ from drude model, compensated by current.

## Chap 4. Sommerfeld (free electron) theory
### 4.1. basic Fermi-Dirac statistics
* Fermi factor: $n_F(\beta(E-\mu)) = \frac{1}{e^{\beta (E - \mu)}+1}$. Given a system of free electrons with chemical potential $\mu$ the probability of eigenstate $E$ is occupied.
    * why 'fermi factor' given as this form, function of $\beta(E - \mu)$?
* in the box $V = L^3$, $k = (\frac{2\pi}{L})^3 (n_x, n_y, n_z)$, $\epsilon(\vec{k}) = \frac{\hbar^2 |k|^2}{2m}$
* total electrons in the system $N = 2\sum_{\vec{k}}n_F(\beta(\epsilon(\vec{k})-\mu))N= 2\frac{L^3}{(2\pi)^3}\int_{\vec{k}} n_F(\beta(\epsilon(\vec{k})-\mu))d\vec{k}$ (eq 4.3)
    * '2' from the two possible spin states
* Definition 4.1.1. The Fermi Energy $E_F$ is chemical potential at $T=0$
    * Fermi Wavevector $k_F$ satisfies $E_F = \frac{\hbar^2 k_F^2}{2m}$
    * Fermi velocity $v_F = \frac{\hbar k_F}{m}$
* Fermi energy of metal with $N$ electrons in $V$
    * In this case, $n_F(\beta(\epsilon(\vec{k})-\mu))$ becomes a step function, so $N = 2\frac{V}{(2\pi)^3}\int_0^{k_F}4\pi k^2 dk= 2\frac{V}{(2\pi)^3}\frac{4\pi k_F^3}{3}$ (eq 4.6)
    * Thus $k_F = (3\pi^2 n)^{1/3}$ and $E_F = \frac{\hbar^2 (3\pi^2 n)^{2/3}}{2m}$ (eq 4.7)

### 4.2. Electric Heat Capacity
* Total energy of metal $E_{total} = 2\frac{V}{(2\pi)^3}\int_{\vec{k}}\epsilon(\vec{k})n_F(\beta(\epsilon(\vec{k})-\mu))d\vec{k}$ and Total 
* Let $N = V\int_{\epsilon}g(\epsilon)n_F(\beta(\epsilon-\mu))d\epsilon$ where $g(\omega)$ is density of state per unit volume.
    * from eq 4.3, $N = \int_k \frac{L}{2\pi}^3 4\pi k^2 n_F(\beta(\epsilon(k)-\mu))dk$
    * from $\epsilon(k) = \frac{\hbar^2 k^2}{2m}$, $k = (\frac{2m\epsilon}{\hbar^2})^{1/2} $ and $\frac{dk}{d\epsilon}d\epsilon = (\frac{m}{2\epsilon \hbar^2})^{1/2}d\epsilon$
    * Thus $g(\epsilon) = \frac{(2m)^{3/2}}{2\pi^2 \hbar^3}\epsilon^{1/2}$
        * $g(\epsilon)d\epsilon$ is total number of eigenstate (includes both spin states) with energies between $\epsilon$ and $\epsilon + d\epsilon$
        * with $E_F$ from eq4.7, $g(\epsilon) = \frac{3n}{2E_F}(\frac{\epsilon}{E_F})^{1/2}$ (eq 4.11)
* While $k_B T \ll E_F$ in room temperature, let $\mu = E_F$ (see 31p, footnote 9 and the sentence it is attached to)
    * Then (See Figure 4.1) we can approximate $E(T)$ as $E(T) = E(0) + (\frac{\gamma}{2})[Vg(E_F)(k_B T)](k_B T)$
    * As $g(E_F)(k_B T) \sim \text{number of particles that can be excited per volume}$
    * and Last $k_B T \sim \Delta{E}\text{ of an excited particle}$ 
* Then $C = \partial E/\partial T = \gamma g(E_F)k_B^2 T V$
    * with eq 4.11 and $k_B T_F = E_F$, 
    * $C = \gamma (\frac{3k_B N}{2}) (\frac{T}{T_F})$
    

* #Exercise of chapter 4) 
    * why does the drude theory provide quiet precise heat capacity?
