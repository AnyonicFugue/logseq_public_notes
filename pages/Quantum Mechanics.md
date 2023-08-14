alias:: QM

- # [[Different Pictures of QM]]
- # Density-matrix formulation
  collapsed:: true
	- Evolution
		- $\frac{d}{d t} \rho(t)=\frac{1}{i \hbar}[H, \rho(t)]$
	-
	-
	-
	- Generalized measurement #card
	  card-last-interval:: 26.06
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-02-04T03:02:32.349Z
	  card-last-reviewed:: 2023-01-09T02:02:32.349Z
	  card-last-score:: 5
		- A set of operators $M_i$, which satisfies $\sum_iM_i^\dag M_i=I$ [Projectors for ordinary measurements]
		- The probability to obtain i is $p_i=\left\langle\psi\left|M_i^{\dagger} M_i\right| \psi\right\rangle$
		- After measurement, the state goes to $$\left|\psi_i^{\prime}\right\rangle=\frac{M_i|\psi\rangle}{\sqrt{\left\langle\psi\left|M_i^{\dagger} M_i\right| \psi\right\rangle}}$$
		-
		- Remark: Equivalent to projective measurements with an auxiliary system. [TODO: prove it.]
	-
- # [[Identical Particles]]
- # Perturbation Theory
  id:: 644730bc-03b5-48b5-a75e-c31bdf1e5919
	- ## Time-Independent
		- See [Griffith](((64473628-1f5e-4716-ae6b-39422002886f))) for reference.
		- For degenerate perturbation theory, we need exact diagonalization within the degenerate space.
		- First-order
			- $$E_n^1=\left\langle\psi_n^0\left|H^{\prime}\right| \psi_n^0\right\rangle$$
			- $$
			  \psi_n^1=\sum_{m \neq n} \frac{\left\langle\psi_m^0\left|H^{\prime}\right| \psi_n^0\right\rangle}{\left(E_n^0-E_m^0\right)} \psi_m^0
			  $$
		- Second-order
			- $$
			  E_n^2=\sum_{m \neq n} \frac{\left|\left\langle\psi_m^0\left|H^{\prime}\right| \psi_n^0\right\rangle\right|^2}{E_n^0-E_m^0}
			  $$
	- ## Time-Dependent
		- The strategy is also to expand the coefficients in order and proceed order-by-order.
		- First Order:
		  $$
		  \begin{gathered}
		  \frac{d c_a^{(1)}}{d t}=0 \Rightarrow c_a^{(1)}(t)=1 \\
		  \frac{d c_b^{(1)}}{d t}=-\frac{i}{\hbar} H_{b a}^{\prime} e^{i \omega_0 t} \Rightarrow c_b^{(1)}=-\frac{i}{\hbar} \int_0^t H_{b a}^{\prime}\left(t^{\prime}\right) e^{i \omega_0 t^{\prime}} d t^{\prime}
		  \end{gathered}
		  $$
		- Second Order:
		  $$
		  \begin{aligned}
		  \frac{d c_a^{(2)}}{d t} & =-\frac{i}{\hbar} H_{a b}^{\prime} e^{-i \omega_0 t}\left(-\frac{i}{\hbar}\right) \int_0^t H_{b a}^{\prime}\left(t^{\prime}\right) e^{i \omega_0 t^{\prime}} d t^{\prime} \Rightarrow \\
		  c_a^{(2)}(t) & =1-\frac{1}{\hbar^2} \int_0^t H_{a b}^{\prime}\left(t^{\prime}\right) e^{-i \omega_0 t^{\prime}}\left[\int_0^{t^{\prime}} H_{b a}^{\prime}\left(t^{\prime \prime}\right) e^{i \omega_0 t^{\prime \prime}} d t^{\prime \prime}\right] d t^{\prime},
		  \end{aligned}
		  $$
		  while $c_b$ is unchanged $\left(c_b^{(2)}(t)=c_b^{(1)}(t)\right)$. (Notice that $c_a^{(2)}(t)$ includes the zeroth-order term; the second-order correction would be the integral part alone.)
	- ### Fermi's Golden Rule
		- $$
		  \Gamma_{i \rightarrow f}=\frac{2 \pi}{\hbar}\left|\left\langle f\left|H^{\prime}\right| i\right\rangle\right|^2 \rho\left(E_f\right)
		  $$
		- $\Gamma$ is the transition rate, i.e. transition probability per unit time
		- $\rho(E_f)$ is the state density near the final state. For discrete levels this would be a Dirac delta.
	- Different path: ((64239f9f-7660-4553-ab22-80685caf6f6c)) and effective Hamiltonian
- # Misc
  collapsed:: true
	- Schmidt decomposition of an entangled state #card
	  card-last-score:: 5
	  card-repeats:: 3
	  card-next-schedule:: 2023-06-14T01:19:18.262Z
	  card-last-interval:: 69.6
	  card-ease-factor:: 2.32
	  card-last-reviewed:: 2023-04-05T11:19:18.263Z
		- For a pure state $|\psi\rangle\in V_1\otimes V_2$, we can always decompose it into $|\psi\rangle=\sum_ip_i|e_i\rangle| f_i\rangle$, where $\{e_i\}$ and $\{f_j\}$ are ONBs.
		-
		- Calculation strategy: $T=UDV$, U consists of the normalized eigenvectors of ${T T^\dag}$ (The eigenvectors are the same as the square root), V consists of the eigenvectors of ${T^\dag T}$
		-
		- Purification
			- For some mixed state $\rho$, we can always **add an auxiliary system** to make the whole state a (entangled) **pure** state.