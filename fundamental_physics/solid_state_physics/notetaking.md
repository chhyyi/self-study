# Simon, Condensed Matter Physics (2015) Note
As I found that ashcroft & Mermin's solid state physics is quite hard to follow, I decided [Steve Simon's condensed matter physics lecture, 2015, oxford univ](https://www-thphys.physics.ox.ac.uk/people/SteveSimon/condmat2015/condmat.html). It have materials available on web, both textbook(but 2012 version) and lecture video ([one on youtube](https://www.youtube.com/playlist?list=PLd9hKAUC3AZuo7is-aN45pmfDwJHOqKAj))

## notations
There will be 3 types of items.
1. Summary (default): keyword and summary of the lecture
2. fundamental : Something assumed to be familiar, more fundamental things but I am not sure (So I want to check again), starts with #F: or #Fund:
3. Questions : may have answers as a subitem. starts with #Q:

## Lecture 1.
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
    * expectations of energy from partition function : $<E> = -\frac{1}{Z}\frac{\partial{Z}}{\partial{\beta}}$  
* Then, Expectation of energy is $\hbar \omega [1/2 + 1/(e^{\beta \hbar \omega}-1)]$ or $\hbar \omega[1/2 + n_B(\beta \hbar \omega)]$, where $n_B(x) = 1/(e^{x}-1)$
    * $n_B$ is Bose occupation factor
    * #Q) interpretation : "the mode $\omega$ is an excitation that is excited on average $n_B$ times or equivalently, there is a corresponding boson orbital which is occupied by n bosons"
* Then, Heat Capacity is $C = \partial{\langle E \rangle }/\partial T = \frac{\hbar^2 \omega^2}{k_B T^2}(e^{\beta \hbar \omega })/(e^{\beta \hbar \omega}-1)^2$
    * High temperature limit ($k_B T \gg \hbar \omega$), Heat capacity $C/N = k_B$ (cuz expansion of $e^x$ around $x=0$ is $e^x = 1 + x + \frac{x^2}{2!}\dots$)
    * Low temperature limit ($k_B T \ll \hbar \omega$), Heat capacity $C\rightarrow +0$

## Lecture 2. Debye Model