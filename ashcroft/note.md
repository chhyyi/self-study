# Ashcroft Mermin, solid state physics (1978)
 * 이 문서는 내가 2024년 겨울에 이 책(교재) 공부하면서 노트필기 식으로 정리하는 것이다.
 * 이 책은 gaussian systems of units를 쓰고 있다. 이에 대해 다음 자료를 참고하자. [Robert G. LittleJohn, Physics 221A Appendix A, Fall 2020](https://bohr.physics.berkeley.edu/classes/221/1112/notes/emunits.pdf)  
 * 이 문서에서 Figure나 식의 번호는 모두 ashcroft & mermin, Solid State Physics (1978)의 것을 따른다.

## Chapter 1. Drude Model
챕터1은 drude model은 금속의 내부를 free electron의 ideal gas로 본 classical한 모델이다. Free electron들은 이온(원자핵 + core electron)과 충돌하는 상호작용만 한다고 가정된다. Drude모델 자체와 더불어 1챕터에서는 다양한 물리량이 처음으로 등장한다. Relaxation time $\tau$는 메탈 내의 전자가 이온에 충돌하는 평균적인 시간이다. 
### DC electrical conductivity of a metal
#### relaxation time and resistivity
$\tau$와 $\vec{F} = -e\vec{E}$에서 전자의 평균적인 속도를 $\vec{v}_{avg}=-\frac{e\vec{E}\tau}{m}$ 라고 하자. Resistivity $\rho$는 $\vec{E}=\rho\vec{j}$, conductivity $\sigma$는 $\rho =1/{\sigma}$ 으로 주어진다. 또 $\vec{j} = -ne\vec{v}$ 이다. 이 때 $n$은 전자의 밀도이다. 이들을 이용하면 relaxation time, conductivity, resistivity에 대한 다음 식들을 얻을 수 있다.  
$\sigma = ne^2\tau/m$ (eq 1.6)  
$\tau = \frac{m}{\rho n e^2}$ (eq 1.7)   
#### momentum after infinitesimal time
infinitesimal time $t$와 $t+dt$ 사이에 충돌이 일어날 확률은 $\frac{dt}{\tau}$이므로 충돌이 일어나지 않을 확률은 $1-\frac{dt}{\tau}$이다. 충돌이 일어나지 않은 전자에 대해서만 따져보면 $\vec{p}(t+dt) = (1 - \frac{dt}{\tau})[\vec{p}(t)+\vec{f}(t)dt+O(dt)^2] = \vec{p}(t) - \frac{dt}{\tau}\vec{p}(t) + \vec{f}(t)dt + O(dt)^2$이다. 여기에서 $dt \to 0$ 이면 미분의 정의에서  
 $\frac{d\vec{P}}{dt} = -\frac{\vec{p}(t)}{\tau}+\vec{f}(t)$ (eq 1.12)  
 가 성립한다. 충돌이 일어나는 전하에 대해서는 모든 항이 $O(dt)^2$에 해당한다. (충돌할 확률과 힘이 작용하는 시간 양쪽에 dt가 있고 이들이 곱해지기 때문이다.) 또 Drude Model의 전자는 충돌후 속도는 임의 방향이므로 평균에서 상쇄된다.   
 식(1.12)는 damping 항이 추가된 전자의 운동방정식이기도 하다. 1장의 나머지 부분에서 이를 Hall effect와 금속의 AC electrical conductivity, Thermal conductivity에 적용시켜 보도록 한다.

### Hall effect and Magnetoresistance
Hall effect에 대해 따져보면 전류를 만드는 입자가 어떤 전하를 가지고 있는지 알 수 있다. (Figure 1.3을 보라) 이동하는 전하가 자기장에게 받는 힘은 Lorentz force에서 $\vec{F} = \frac{q}{c} \vec{v} \times \vec{H}$ 이므로, 음전하를 가지는 전자는 $-y$ 방향으로 이동하고, 도선 내의 $E_y$는 음의 방향으로 형성된다. 한편 양전하가 전류를 형성한다면 같은 방식에서 $E_y$는 양의 방향으로 형성된다.  
Hall은 이런 상황에서 자기장에 따라 저항이 커질 것이라는 가설하에 실험하였으므로, (transverse) magnetoresistance $\rho(H) = E_x/j_x$ 가 중요한 측정값이지만, 자기장과 저항은 independent하였다. 대신 Lorentz Force를 상쇄시키도록 전자가 도선 양쪽에 축적되어 전기장을 형성하는데, 이를 Hall coefficient $R_H$로 나타낸다.
$R_H = E_y / (j_x H)$   
식 (1.12)를 한 전자가 lorentz force를 받는 상황에 대해 정리하면 다음과 같다.  
$\frac{d\vec{P}}{dt} = -e(\vec{E} + \frac{1}{c}\vec{v}\times\vec{H})-\frac{1}{\tau}\vec{p}(t)$ (eq 1.16)  
Hall coefficient를 구하기 위해 $E_y$ 를 $j_x H$에 대한 식으로 나타내보자. 먼저 전류가 static하게 흐르고 있고, y방향의 전류는 없으므로,  $0 = -e[E_y - (1/c)v_x H]$ 이다. 또 $\vec{j} = -ne\vec{v}$ 를 이용하면 $e E_y = (e/c)v_x H = -(1/nc)j_x H$ 이므로,
$R_H = -(1/nec)$ (eq 1.21) 이 된다.  
 같은 방식으로 $E_x$에 대해 풀어보면 저항이 자기장에 의해 변하지 않는다는 것도 확인할 수 있다. $v_y=0$이므로, $e E_x = -p_x/\tau$ 이다. 이 식의 양변에 $ne\tau/m$ 을 곱하면, 좌변의 경우 $(ne^2 \tau/m) E_x = \sigma_0 E_x$가 되고 우변은 $(-m v_x/\tau)(ne\tau/m) = -nev_x = j_x$ 이다. 이 때 $\sigma_0 = (ne^2\tau/m)$으로 식 1.6에서 구한 drude 모델 DC conductivity이다. 둘을 합치면 $\sigma_0 E_x = j_x$ 으로 

### AC electrical conductivity of a metal
time-dependent electric field가 $\vec{E}(t) = \vec{E}(w)e^{-iwt}$ 이와 같은 꼴로 주어져 있고, 그에 대한 해가 $\vec{p}(t) = \vec{p}(w)e^{-iwt}$ 의 꼴로 주어진다고 가정하자. 이를 식 1.12에 대입하면, $\vec{f}=-e\vec{E}$ 이므로, time-independent term들을 이와 같이 정리할 수 있다.  
$-iw\vec{p}(w) = -\vec{p}(w)/\tau - e\vec{E}(w)$ (eq 1.26)   
또 AC conductivity $\sigma(w)$가 $\vec{j}(w) = \sigma(w)\vec{E}(w)$ 의 관계를 가진다고 하고, $\vec{j}=-ne\vec{p}/m$ 임을 이용하면, $\vec{j}(w) = \frac{ne^2\tau}{m}\frac{1}{1-iw\tau}\vec{E}(w)$ 이다. 따라서 $\sigma(w)$  는 다음과 같다.  
$\sigma(w) = \sigma_0/(1-iwt)$, $\sigma_0 = ne^2\tau/m$ (eq 1.29)   
#### Wave propagation and Complications
책에서는 이 결과의 가장 중요한 application이 메탈에서의 EM wave의 propagation이라고 하면서, 그에 관한 2개의 문제를 이야기하고 있다. 첫 번째는 magnetic field가 유도된다는 것이다. 하지만 Lorentz force에서 두 항의 크기를 비교하면 $v/c$ 가 곱해지기 때문에 무시할 수 있다고 한다. 두 번째는 eq 1.12가 모든 전자에 같은 E-field가 작용했을 때의 결론이라는 것이다. 하지만 이 경우 $\vec{r}$에서의 전류는 마지막 충돌 이후에 전기장이 전자에 한 일에 dependent하므로, EM wave가 전파하면서 전기장의 세기가 $\vec{r}$에 따라 변화하는 상황과 다르다는 것이다. 이 경우 가시광선 영역까지는 wavelength $\lambda$ 가 mean free path보다 충분히 커서 $\vec{j}(\vec{r}, w) = \sigma(w) \vec{E}(\vec{r}, w)$ 가 유효하다고 한다. 그러니까 collision이 일어난 범위부터의 E-field를 다 고려하지 않고 $\vec{E}(\vec{r})$만으로 계산해도 된다는 것이다. 

#### Dielectric constant
complication에 대한 설명을 마치고 교재는 em wave의 propagation에 대해 더 깊이 다룬다. Maxwell Equation(M.E.)에서 시작해 wave equation을 유도하고, 'complex dielectric constant' $\epsilon$을 도입하여 설명하고 있다. 이를 이해하기 위해 macroscopic한 경우를 포함해 M.E.를 알고 넘어가야 할 필요가 있다. 이것은 다시 gaussian unit 문제와도 얽혀 있다. 하지만 일단 책에 있는, net charge가 없는 경우의 M.E. (eq 1.31)에서 시작해보자.   
$\nabla \cdot \vec{E} = 0$  
$\nabla \cdot \vec{H} = 0$  
$\nabla \times \vec{E} = -\frac{1}{c}(\partial\vec{H}/\partial t)$  
$\nabla \times \vec{H} = \frac{4\pi}{c}\vec{j}+\frac{1}{c}(\partial\vec{E}/\partial t)$ (eq 1.31)  
M.E.는 curl of curl에서 wave equation과 같은 꼴이 된다. 이를 계산하면,   
$\nabla \times (\nabla \times \vec{E}) = -\nabla^2\vec{E} = \frac{iw}{c}\nabla\times\vec{H}=\frac{iw}{c}(\frac{4\pi}{c}\vec{j}-\frac{iw}{c}\vec{E})$  
여기에서 $\vec{j} = \sigma \vec{E}$ 을 적용하여 정리하면 다음과 같다.  
$-\nabla^2\vec{E} = \frac{w^2}{c^2}(1+\frac{4\pi i\sigma}{w})\vec{E}$ (eq 1.33)  
이것은 $-\nabla^2\vec{E} = \frac{w^2}{c^2}\epsilon(w)\vec{E}$ 이와 같은 wavefunction으로 볼 수 있고, 이 때 $\epsilon(w) = 1+4\pi i \sigma/w$ 이다.

#### plasma frequency and charge density wave
plasma frequency에 대해 따지기 위해 교재에서는 만약 propagation의 frequency가 충분히 높다면, $1 \ll w\tau$ 가 성립함을 가정하고 있다. 위에서 electronic mean free path보다 wavelength가 충분히 크다고 했는데, 이와 양립 가능한 상황인지 따져보자. $l \sim v_{avg}\tau$ 이고, $v_{avg} \ll c$ 일 것이다. 따라서 $l = \tau v$ 와 $\lambda = cT$를 비교할 때 $\tau \sim T$ 이어도 $l \ll \lambda$ 일 수 있다.