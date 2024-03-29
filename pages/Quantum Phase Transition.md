- # Setting
	- $H(g)=H_0+g H_1$, where $H_0$ and $H_1$ commute.
	- At $T=0$, we may change the parameter $g$ (or generally, a set of parameters $\{g_j\}$) to obtain a critical point.
		- There may be a level-crossing / splitting at $g=g_c$.
- # Basics
	- Defs
		- Quantum phase transition
			- ((63940007-697b-452b-a112-4ca2a6b53d5f))
				- This definition suits the zero temperature, where only the ground state accounts.
				- However, we need the description of nonzero temperatures
		- Second-order phase transition
			- ((63940062-91a3-4846-b259-720a2df5d8c9))
				- $\Delta \sim J\left|g-g_c\right|^{z v}$
			- ((6394286c-f118-4cc8-b890-7e38017f4459))
				- $\xi^{-1} \sim \Lambda\left|g-g_c\right|^v$
	- ## General analysis
		- Proposition. Inhomogeneity won't affect the universality class. #card
		  card-last-interval:: 84
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-07-28T12:03:32.234Z
		  card-last-reviewed:: 2023-05-05T12:03:32.235Z
		  card-last-score:: 5
			- In short, we can always **rescale** the coordinates to eliminate the inhomogeneity.
			- eg. Inhomogeneity between space and time
				- $\mathcal L=K_1(\nabla \phi)^2+K_2\left(\partial_\tau \phi\right)^2+\frac{r}{2} \phi^2+\frac{y}{4} \phi^4$
				- $x \rightarrow \sqrt{K_1} x, \quad \tau \rightarrow \sqrt{K_2} \tau$
			- Q: Are there things, similar to [[Curvature]], that are unable to eliminate by coordinate transformations?
		- Compare the values of $\Delta$ and $k_B T$
			- ((63942988-c4ea-4da9-b66c-ff2bd4b2f692))
				- This is a diagram of crossovers, not phase transitions.
		- We may also expand the effective action to obtain something similar to Ginzburg-Landau theory.
			- However there are differences from the classical Ginzburg-Landau theory.
				- $\phi=\phi(r,\tau)$ is now time-dependent.
				- Time derivatives are now present in the action.
					- Yet another hint that $Nd$ classical <-> $(N+1)d$ quantum!
- # Dynamical Exponent
	- In classical phase transitions, there are only **two** independent critical exponents.
	- In the quantum case, however, there is one more...
	- Def. Dynamical Exponent $z$
		- $[\omega]=z \neq 1$
		- Correspondingly, $[t]=-z$.
- # Density Wave and [[Mean-Field Theory]]
	- Def. Density wave
		- In short, a density wave some order parameter which has a **periodic** spatial dependence.
		- For example, in the anti ferromagnetic phase the spin depends on the location in an $Z_2$ manner.
		- Examples
			- Spin density wave (SDW)
			- Charge density wave (CDW)
			- Paring density wave (PDW) [Used in superconductors]
	- Example: Anti-ferromagnetic phase on 2D square lattice
		- Intuition
			- AFM -> Adjacent spins tend to be anti-parallel
		- Setting
			- $$H=\sum _{k\alpha }( E_{k} -\mu ) c_{k\alpha }^{\dagger } c_{k\alpha } +J\sum _{< ij> }\overrightarrow{S_{i}} \cdot \vec{S}_{j}$$
				- $J>0$ means AFM. If $J<0$ this would be FM.
			- Perform a mean-field calculation to the $J\sum _{< ij> }\overrightarrow{S_{i}} \cdot \vec{S}_{j}$ term in the Hamiltonian.
			- The order parameter is
			  $$\vec{\phi } :=( -1)^{i}< \vec{S}_{i}> $$
				- Quite reasonable. 'Divide the graph into two subsets by parity'.
		- We can diagonalize the Hamiltonian and see that the coupling terms open a gap in the mean-field Hamiltonian.
			- Key points in diagonalization:
			  1. Fourier transformation
			  2. write the Hamiltonian as 
			  $$\sum _{k\alpha }\left(\begin{array}{ c c }
			  c_{k\alpha }^{\dagger } & c_{k+Q,\alpha }^{\dagger }
			  \end{array}\right)\left(\begin{array}{ c c }
			  E_{k} -\mu  & -\alpha \Delta \\
			  -\alpha \Delta  & E_{k+Q} -\mu 
			  \end{array}\right)\left(\begin{array}{ l }
			  c_{k\alpha }\\
			  c_{k+Q,\alpha }
			  \end{array}\right)$$
			  and diagonalize the matrix (similar to the [[Bogoliubov Transformation]])
				- $\vec Q=(\pi,\pi)$
			- The result is
			  $$
			  \xi_k=\frac{E_k+E_{k+Q}}{2}-\mu \pm \sqrt{\left(\frac{E_k-E_{k+Q}}{2}\right)^2+\Delta^2}
			  $$
		- Hotspot and Folding of Brillioune zone
			- ![Image(1).png](../assets/Image(1)_1685493563397_0.png){:height 529, :width 770}
				- The orange lines are the original BZ translated by $(\pi,\pi)$
				- The red points (hotspots) are the intersections of the new BZ with the old BZ.
				  They satisfy $E_k=E_{k+q}$, thus a **gap** is opened at them.
					- Recall
					  $$
					  \xi_k=\frac{E_k+E_{k+Q}}{2}-\mu \pm \sqrt{\left(\frac{E_k-E_{k+Q}}{2}\right)^2+\Delta^2}
					  $$
			- New Fermi Surface
				- ![image.png](../assets/image_1685493879670_0.png){:height 440, :width 413}
				  $\vec Q=(\pi,\pi)$
					- (a) Fermi surface without SDW order
					- (b) The original Fermi surface along with the Fermi surface shifted by wavevector $(\pi, \pi)$. These intersect at the hot spots shown by the filled circles.
					- (c) With the onset of a nonzero spin density wave order with $\left\langle\phi_\alpha\right\rangle \neq 0$, gaps open at the hot spots leading to electron (thin lines) and hole (thick lines) pockets.
					- (d) With increasing $\left|\left\langle\phi_\alpha\right\rangle\right|$ the electron pockets shrink to zero for the hole-doped case, leaving only hole pockets. In the electron-doped case, the hole pockets shrink to zero, leaving only electron pockets (this is not shown). Finally, in the half-filled case, the electron and hole pockets shrink to zero simultaneously.
				- ![image.png](../assets/image_1685494085531_0.png)
				  $\vec Q=(\pi,0)$
					- The last step is always restoring translation symmetry of the new BZ.
		-
- # Examples
	- ## General Strategy
		- Examine different limits of the parameters (eg $g \to 0$ and $g \to \infty$) to see different phases.
		- Assuming that the behavior (or the phase) depends continuously on the parameters, we conclude that there must be critical points.
	- Quantum [[Ising model]]
		- $H_I=-J g \sum_i \hat{\sigma}_i^x-J \sum_{\langle i j\rangle} \hat{\sigma}_i^z \hat{\sigma}_j^z$
		- Argue that criticality exists
			- When $g<<0$: Ferromagnetic.
				- $$\lim _{\left|x_i-x_j\right| \rightarrow \infty}\left\langle 0\left|\hat{\sigma}_i^z 
				   \hat{\sigma}_j^z\right| 0\right\rangle=m_0^2$$
				- There is spontaneous symmetry breaking
			- When $g>>1$: Paramagnetic
				- The spins are all in the eigenstate of $\sigma_x$, that is, $|0\rangle=\prod_i|\rightarrow\rangle_i$
				- $\sigma_z$ are short-range correlated, i.e. $\left\langle 0\left|\hat{\sigma}_i^z \hat{\sigma}_j^z\right| 0\right\rangle \sim e^{-\left|x_i-x_j\right| / \xi}$
				- No spontaneous symmetry breaking
		- Summary
			- FM phase for small h
			- PM phase for large h
			- QCP is similar to 3D Ising
	- [[Quantum Rotors]]
		- Similarly, FM when $\frac 1 {2IJ} \to 0$ (dominated by coupling) and PM when $\frac 1 {2IJ} \to \infty$ (dominated by rotation)