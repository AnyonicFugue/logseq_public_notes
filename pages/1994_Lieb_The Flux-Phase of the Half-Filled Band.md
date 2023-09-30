- ![1994_Lieb_The Flux-Phase of the Half-Filled Band.pdf](file://zotero_link/Research/TO in Kitaev Honeycomb/1994_Lieb_The Flux-Phase of the Half-Filled Band.pdf)
- # Statement of the Problem
	- We have a general finite graph $\Lambda$, which is a collection of $|\Lambda|$ sites and certain bonds denoted by $x y$ with $x$ and $y$ in $\Lambda$ and $x \neq y$.
	- A positive weight $\left|t_{x y}\right|=\left|t_{y x}\right|$ is specified in advance for each bond. By convention $t_{x x}=0$. The hopping amplitude is then $t_{x y}=\left|t_{x y}\right| \exp [i \phi(x, y)]$, with $\phi(x, y)=-\phi(y, x)$ for hermiticity.
	- The problem is to find the phases $\phi(x, y)$ that minimize the total electronic ground state energy (when $\beta=1 / k T=\infty$ ) or free energy (when $\beta<\infty$ ).
- # Definition
	- Circuit
		- A sequence of points $x_1, x_2, \ldots, x_n, x_1$ with $t_{x_i x_{i+1}} \neq 0$
	- Flux
		- $$
		  \sum_{i=1}^n \phi\left(x_i, x_{i+1}\right)(\bmod 2 \pi)
		  $$
- # Main Result
	- [Theorem](((651182d6-ad9b-44d2-b5c8-17501d6d00ad))) The spectrum only depends on the fluxes, not specific values of $\phi_{ij}$.
		- Various additional conditions are needed (e.g. finite temperature). [[2020_Chulliparambil_Tu_Microscopic models for Kitaev's sixteenfold way]] actually used the difference of ground state energy of different phase configurations to extract data.
	- Theorem. When $H=K, N=|\Lambda|$ and $\Lambda$ is planar the optimum choice of fluxes is $\pi$ in every circuit containing $0 \ (\bmod 4)$ sites and 0 in circuits with $2 \ (\bmod 4)$ sites.
	-