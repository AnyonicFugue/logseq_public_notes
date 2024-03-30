# Free Electrons
id:: 65f4fd67-9f37-484c-8080-04a14d598bc3
	- ((65503243-b09d-4b95-a43a-bc95ef69d5ac))
		- Note that to study $\omega_p$ and resonance we need to study the effective AC dielectric constant, not only the conductance!
	- Classical Hall effect under Drude Model
	  collapsed:: true
		- Setup
		  collapsed:: true
			- ![image.png](../assets/image_1710557578624_0.png)
			- Without the magnetic field, there is $E_y$ but **NO CURRENT**.
		- Definition. Hall resistance
		  collapsed:: true
			- $$
			  R_H=\frac{E_y}{j_x B}
			  $$
		- Proposition.
		  collapsed:: true
		  $$
		  R_H=-\frac{1}{n e}
		  $$
			- Derivation
			  collapsed:: true
				- $$
				  \frac{d \boldsymbol{p}}{d t}=\boldsymbol{F}-\frac{\boldsymbol{p}}{\tau}=-e\left(\boldsymbol{E}+\frac{\boldsymbol{p} \times \boldsymbol{B}}{m}\right)-\frac{\boldsymbol{p}}{\tau}=0
				  $$
				- Rewritten as components,
				  collapsed:: true
				  $$
				  \begin{aligned}
				  & -e E_x-\frac{e B}{m} p_y-\frac{1}{\tau} p_x=0 \\
				  & -e E_y+\frac{e B}{m} p_x-\frac{1}{\tau} p_y=0
				  \end{aligned}
				  $$
					- Note that $E_x$ would become non-zero at equilibrium.
				- At equilibrium: $j_y=0$. Consider only the second equation above, we see that
				  collapsed:: true
				  $$
				  E_y =-\frac{1}{n e} j_x B
				  $$
					-
	- Heat transport
	  collapsed:: true
		- Wiedemann-Franz law: $\frac{\kappa}{\sigma T}$ is approximately a constant across different materials.
		  collapsed:: true
			- Classical (wrong) derivation
				- Consider a virtual boundary, with
				  $$
				  \Delta x=\left\langle v_x\right\rangle \cdot 2 \tau
				  $$
				- The net heat current flowing from the high-T side to the low-T side is
				  $$
				  j_q=\frac{1}{2} n \times \frac{3}{2} k_B\left(T_1-T_2\right) \times\left\langle |v_x|\right\rangle
				  $$
				- Ignore the difference between $\left\langle v_x^2\right\rangle$ and $\left\langle |v_x|\right\rangle^2$, we see that
				  $$
				  \kappa=\frac{1}{3} c_v\left\langle v^2\right\rangle \tau
				  $$
					- $c_v=\frac 3 2 k_B n$
				- Finally,
				  $$
				  \frac{\kappa}{\sigma T}=\frac{1}{3} c_v\left\langle v^2\right\rangle \tau \frac{m}{n e^2 \tau} \frac{1}{T}=\frac{3}{2}\left(\frac{k_B}{e}\right)^2
				  $$
				  which is **half** the real value.
				- Actually it is irreparably erroneous. We really need quantum derivations here.
	- Sommerfeld Theory
		- Notes
			- Treat electrons as free fermions, thus satisfying the Fermi-Dirac distribution.
			- Near room temperature, $T_F \gg T$, thus we could almost ignore $T$.
		- Definitions
			- Fermi temperature
				- $$
				  T_F=\frac{\epsilon_F}{k_B}
				  $$
			- Fermi velocity
				- $$
				  v_F=\frac{\hbar k_F}{m}
				  $$
			- Electron **mode** density distribution function $g(\varepsilon)$
			  $$
			  n_{mode}=\frac{N_{mode}}{V}=\int_0^{\epsilon_F} d \epsilon \cdot g(\epsilon)
			  $$
				- Independent of temperature, only the density of available electron modes!
				- Note that in 3D, 
				  $$
				  g(\varepsilon)=\frac{(2 m)^{3 / 2}}{2 \pi^2 \hbar^3} \epsilon^{1 / 2}
				  $$
			- Bohr radius
			  $$
			  a_0=\hbar^2 / m e^2=0.529 \times 10^{-8} \mathrm{~cm}
			  $$
		- Proposition. 
		  collapsed:: true
		  $$
		  k_F=\left(\frac{9 \pi}{4}\right)^{1 / 3} \frac{1}{r_s}
		  $$
		  where $r_s$ is the effective distance between electrons.
			- Consider a material with the shape of a cube.
			- Step 1. Eigenstates and number of particles
				- Each eigenstate takes volume $\left(\frac{2 \pi}{L}\right)^3$ in momentum space.
				- Therefore, the total number of particles is 
				  $$N=2 \times (\frac {2\pi} L)^{-3} \frac 4 3 \pi k_F^3=\frac{V k_F^3}{3 \pi^2}$$
					- The first 2 accounts for the spin.
			- Step 2. Compare to the effective distance
			  $$
			  n=\frac{N}{V}=\frac{k_F^3}{3 \pi^2}=\left(\frac{4 \pi}{3} r_s^3\right)^{-1}
			  $$
			- Thus we directly obtain the result.
		- Proposition. The average energy at zero temperature is
		  collapsed:: true
		  $$
		  \frac{E}{N}=\frac{3}{5} \frac{\hbar^2 k_F^2}{2 m}=\frac{3}{5} \epsilon_F
		  $$
			- Essentially
			  $$(\int_0^1 r^2 dr) \big / (\int_0^1 r^4 dr)$$
			-
		- The Sommerfeld expansion
			- Statement. At low temperature,
			  $$
			  \int_{-\infty}^{\infty} \frac{H(\varepsilon)}{e^{\beta(\varepsilon-\mu)}+1} \mathrm{~d} \varepsilon=\int_{-\infty}^\mu H(\varepsilon) \mathrm{d} \varepsilon+\frac{\pi^2}{6}\left(\frac{1}{\beta}\right)^2 H^{\prime}(\mu)+O\left(\frac{1}{\beta \mu}\right)^4
			  $$
			- Key idea
				- For $f(\varepsilon)=(e^{\beta(\varepsilon-\mu)}+1)^{-1}$, $df/d\varepsilon$ has a **strong** peak near $\varepsilon=\mu$.
				- Thus we can first perform integration by part, then perform Taylor expansion at $\mu$.
		- Specific heat
			- Use the Sommerfeld expansion, we find
			-
		- Re-examine the Wiedemann-Franz law
		  collapsed:: true
			- Use $c_v=\frac{\pi^2}{2}\left(\frac{k_B T}{\varepsilon_F}\right) n k_B$ and use $v_F$ instead of $v_0$
			- We obtain $2.44 \times 10^{-8} \mathrm{~W} \Omega / \mathrm{K}^2$, much closer to experiment.
		- Re-examine the Seeback effect
		  collapsed:: true
			- $$
			  v_Q+v_E=0 \Rightarrow Q=-\left(\frac{1}{3 e}\right) \frac{d}{d T}\left(\frac{m v^2}{2}\right)=-\frac{c_v}{3 n e}
			  $$
			- Similarly, use $c_v$ of fermions to obtain
			  $$
			  Q=-\frac{\pi^2}{6} \frac{k_B}{e}\left(\frac{k_B T}{\epsilon_F}\right)
			  $$
		-
-