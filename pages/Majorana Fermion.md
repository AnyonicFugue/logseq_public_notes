alias:: Majorana Representation

- ((63bcd4e3-9a17-4ac4-b17a-cb562564925d))
-
- ((63bcd4f9-083f-4212-b48b-0ddf3f607684)).
  collapsed:: true
	- In fact, it is not even a particle. It is a property of a particle, just like the mass is a property of a particle
	- ((63bcd53a-5198-40fd-ad60-ade9ff7350c6))
-
- # Majorana Representation of Fermionic Modes #card
  id:: 64b442f1-bf2d-40cd-926a-9629bc86763d
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-08-25T18:59:31.213Z
  card-last-reviewed:: 2023-07-25T12:59:31.213Z
  card-last-score:: 5
	- What's behind the formalism? Any general math picture?
	  background-color:: red
	- Comments
		- Another formalism is always good.
		- This might be viewed as 'real fermions'. The commutation relations are neater.
	- The Transformation
	  $$
	  \gamma_{2 k-1}=a_k+a_k^{\dagger}, \quad \gamma_{2 k}=\frac{a_k-a_k^{\dagger}}{i}
	  $$
		- For each fermion there are two majorana modes.
	- Inverse Transformation
		- $$a_k=\frac {\gamma_{2k-1}+i \gamma_{2k}}{2}, a_k^\dagger=\frac {\gamma_{2k-1}-i \gamma_{2k}}{2}$$
		-
		-
	-
- # Basic Properties
	- Commutation Relations
		- $$
		  \gamma_j^2=1, \quad \gamma_j \gamma_l=-\gamma_l \gamma_j \text { if } j \neq l
		  $$
			- Similar to 'generalized Pauli operators'.
		- Note that all majorana operators can be treated on an equal basis, regardless of odd or even.
	- $\gamma_j$ is hermitian.
	- id:: 65430d84-a1db-400d-b05f-0578198574b5
	  $$a_k^\dagger a_k=\frac {\mathbf 1+i \gamma_{2k-1} \gamma_{2k}}{2}$$
	- Eigenvalues of $c_j$ are $\pm 1$, thus they're invertible.
	  collapsed:: true
	  Moreover, the positive and negative multiplicities are equal.
		- Note that if $|\psi\rangle$ is an +1 eigenvector of $c_j$, $c_k|\psi\rangle$ is an -1 eigenvector (and vice versa)
		- Since each $c_k$ is invertible, the +1 and $-1$ eigenvectors have a 1-1 correspondence.