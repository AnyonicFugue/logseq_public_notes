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
	- ## Overlap of BCS wavefunctions
		-