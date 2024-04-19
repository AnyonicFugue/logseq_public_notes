# Setup
	- The system is a spin-1 chain.
	- $$
	  H_{A K L T}=\sum_i \mathbf{S}_i \cdot \mathbf{S}_{i+1}+\frac{1}{3}\left(\mathbf{S}_i \cdot \mathbf{S}_{i+1}\right)^2
	  $$
- # Basic Facts: Hamiltonian, Ground State #card
	- The Hamiltonian is a projection onto the complement of spin-2 states, i.e.
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-25T18:58:37.921Z
	  card-last-reviewed:: 2023-08-25T12:58:37.921Z
	  card-last-score:: 5
	  collapsed:: true
	  $$
	  \frac{1}{3}+\frac{1}{2} \mathbf{S}_x \cdot \mathbf{S}_{x+1}+\frac{1}{6}\left(\mathbf{S}_x \cdot \mathbf{S}_{x+1}\right)^2=P_{x, x+1}^{(2)}
	  $$
		- Recall the define of angular momentum as the Casimir operator:
		  $$\sum (S^\alpha)^2=l(l+1)$$
			- $l=0$ -> $n=0$
			- $l=1$ -> $n=2$
			- $l=2$ -> $n=6$
		- We'd like to construct an orthogonal projector to the space of $l=2$, thus we write down this:
		  $$P^{(2)}=\frac 1 {24} (\vec S_i+\vec S_{i+1})^2[(\vec S_i+\vec S_{i+1})^2-2]$$
			- The first projects out $n=0$ and the second projects out $n=2$.
			- The coefficients grants $P^2=P$.
		- Use $S_i^2=2$ (since it is a spin-1 chain), we obtain the desired result.
	- The Hamiltonian has the spin-rotation invariance.
	- The ground state has a structure of adjacent entangled singlet pairs.
	  card-last-score:: 3
	  card-repeats:: 2
	  card-next-schedule:: 2024-04-26T00:46:17.064Z
	  card-last-interval:: 42
	  card-ease-factor:: 2.46
	  card-last-reviewed:: 2024-03-15T00:46:17.065Z
	  collapsed:: true
		- ((64e51741-d1fa-4a9f-8d9e-c99c745683ec))
		-