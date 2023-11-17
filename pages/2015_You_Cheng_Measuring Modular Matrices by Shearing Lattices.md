- ![2015_You_Cheng_Measuring Modular Matrices by Shearing Lattices.pdf](file://zotero_link/Research/Anyon Data from Microscopic Data/2015_You_Cheng_Measuring Modular Matrices by Shearing Lattices.pdf)
- # Key Ideas of the Algorithm
  collapsed:: true
	- Adiabatically strengthen diagonal bonds and weaken original bonds to perform Dehn twists.
		- ((652d0276-dc37-4d39-b974-c121123d6d91))
		- Note that for a $L_x \times L_y$ torus, we need $L_y$ steps of adiabatic transformation to return to the original state.
	- Plot $\Theta$ vs $N$ to obtain the universal subleading term.
	-
- # Flux Removal
  collapsed:: true
	- Problem
		- After a full cycle, different flux configuration might be swapped.
	- Solution
		- Before the twisting starts, add/remove the flux in advance.
- # Details
	- To fix the phases of eigenstates, we introduce a reference state and require
	  $$
	  \arg \left\langle\Psi(\lambda) \mid \Psi_{\mathrm{ref}}\right\rangle=0
	  $$
	  i.e. subtract the phase relative to the reference state.
		- It's important to check that $\left|\left\langle\Psi(\lambda) \mid \Psi_{\text {ref }}\right\rangle\right|$ never becomes vanishingly small, otherwise the result would suffer from numerical error.
	- ## Dehn Twist in Momentum Space
	  collapsed:: true
		- Idea
			- Brute-force diagonalization of the real-space Hamiltonian is very slow.
			- On the other hand, it can be much more efficient after Fourier transformation (to the momentum space).
		- $$
		  \left\langle\boldsymbol{k}, u_{\boldsymbol{k}} \mid \boldsymbol{k}^{\prime}, u_{\boldsymbol{k}^{\prime}}\right\rangle=\frac{\sin \left[\frac{1}{2}\left(\boldsymbol{k}-\boldsymbol{k}^{\prime}\right) L\right]}{L \sin \left[\frac{1}{2}\left(\boldsymbol{k}-\boldsymbol{k}^{\prime}\right)\right]} u_{\boldsymbol{k}}^{\dagger} u_{\boldsymbol{k}^{\prime}}
		  $$
			- The computation could be much faster than before.
			-
		-
	- ((654078c3-2991-4e2d-85cf-b6ac916ed1cb))
	- ## Represent the square Hamiltonian by majoranas
		-