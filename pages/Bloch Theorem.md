- Theorem. $\psi_k(r)=e^{ikr}u_k(r)$ in a periodic potential. #card
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-09-25T19:07:47.553Z
  card-last-reviewed:: 2023-08-25T13:07:47.553Z
  card-last-score:: 5
	- Notes
		- The wavefunction **cannot be normalized** when the system is infinite.
		- The potential possesses **discrete** translation invariance while $k$ could take **continuous** values.
			- $k$ is only quantized when we take a finite lattice with certain boundary conditions.
	- Proof
		- In a periodic potential, the Hamiltonian $H$ commutes with the period-translation operator $T$. Thus we may find their common eigenvectors.
	-
- Notation
	- $$
	  \psi_{n \vec{k}}(\vec{r})=e^{i \vec{k} \cdot \vec{r}} u_{n \vec{k}}(\vec{r})
	  $$
		- The n^th level of Bloch wavevector $k$
	- Normalization
		- $$
		  \left\langle\psi_{n_1 k_1} \mid \psi_{n_2 k_2}\right\rangle=\frac{1}{V} \delta_{n_1 n_2} \delta^3\left(\vec{k}_1-\vec{k}_2\right)
		  $$
		- Note: $\frac{1}{V}$ is regarded to cancel $\delta^3(0)$.