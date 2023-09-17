- ![Kitaev honeycomb tensor networks.pdf](file://zotero_link/Research/Entanglement/2017_Schmoll_Orus_Kitaev honeycomb tensor networks.pdf)
  id:: 64cbbde2-2685-4e08-96b6-b18c7f6e7874
- # Questions and Problems
  collapsed:: true
	- Is it bosonic or fermionic?
		- In both cases the model is local!
	- ## Understanding the Paper
		- ((64cbf6c7-040f-44f7-9b00-950565b151bf))
		- ((64cbf93e-77a8-4e2d-84a4-9fd96ee3cf4e))
- # Setup
	- ((64cbbe59-bfff-4709-b692-c82b8d99b52a))
	  id:: 64f3d976-e784-4432-bdf6-561919bda8f9
	- JW transformation
	  collapsed:: true
		- $$
		  \begin{aligned}
		  & \hat{\sigma}_{i, j}^{+}=2\left(\prod_{j^{\prime}<j} \prod_{i^{\prime}} \hat{\sigma}_{i^{\prime}, j^{\prime}}^z\right)\left(\prod_{i^{\prime}<i} \hat{\sigma}_{i^{\prime}, j}^z\right) \hat{a}_{i, j}^{\dagger} \\
		  & \hat{\sigma}_{i, j}^{-}=2\left(\prod_{j^{\prime}<j} \prod_{i^{\prime}} \hat{\sigma}_{i^{\prime}, j^{\prime}}^z\right)\left(\prod_{i^{\prime}<i} \hat{\sigma}_{i^{\prime}, j}^z\right) \hat{a}_{i, j} \\
		  & \hat{\sigma}_{i, j}^z=2 \hat{a}_{i, j}^{\dagger} \hat{a}_{i, j}-1 .
		  \end{aligned}
		  $$
			- i.e. Order the sites in an j-first, i-second manner.
		- $$
		  \hat{\sigma}^{ \pm}=\left(\hat{\sigma}^x \pm i \hat{\sigma}^y\right)
		  $$
		- $$
		  \begin{aligned}
		  & \hat{\sigma}_{i, j}^x \hat{\sigma}_{i+1, j}^x=-\left(\hat{a}_{i, j}^{\dagger}-\hat{a}_{i, j}\right)\left(\hat{a}_{i+1, j}^{\dagger}+\hat{a}_{i+1, j}\right) \\
		  & \hat{\sigma}_{i-1, j}^y \hat{\sigma}_{i, j}^y=\left(\hat{a}_{i-1, j}^{\dagger}+\hat{a}_{i-1, j}\right)\left(\hat{a}_{i, j}^{\dagger}-\hat{a}_{i, j}\right) \\
		  & \hat{\sigma}_{i, j}^z \hat{\sigma}_{i, j+1}^z=\left(2 \hat{a}_{i, j}^{\dagger} \hat{a}_{i, j}-1\right)\left(2 \hat{a}_{i, j+1}^{\dagger} \hat{a}_{i, j+1}-1\right)
		  \end{aligned}
		  $$
			- Proof
				- $$\begin{aligned}
				  \hat{\sigma }_{i,j}^{x}\hat{\sigma }_{i+1,j}^{x} & =\hat{\sigma }_{i,j}^{z}\left(\frac{\hat{\sigma }_{i,j}^{+} +\hat{\sigma }_{i,j}^{-}}{2}\right)\left(\frac{\hat{\sigma }_{i+1,j}^{+} +\hat{\sigma }_{i+1,j}^{-}}{2}\right)\\
				   & =\left( 2\hat{a}_{i,j}^{\dagger }\hat{a}_{i,j} -1\right)\left(\hat{a}_{i,j}^{\dagger } +\hat{a}_{i,j}\right)\left(\hat{a}_{i+1,j}^{\dagger } +\hat{a}_{i+1,j}\right)\\
				   & =\left(\hat{a}_{i,j}^{\dagger } -\hat{a}_{i,j}\right)\left(\hat{a}_{i+1,j}^{\dagger } +\hat{a}_{i+1,j}\right)
				  \end{aligned}$$
				- Similar for y.
				- z is obvious.
			-
	- Majorana Operators
		- $$
		  \begin{array}{lll}
		  \hat{c}_{i, j}=i\left(\hat{a}_{i, j}^{\dagger}-\hat{a}_{i, j}\right) & \hat{d}_{i, j}=\hat{a}_{i, j}^{\dagger}+\hat{a}_{i, j} & i+j \text { even } \equiv \circ \\
		  \hat{c}_{i, j}=\hat{a}_{i, j}^{\dagger}+\hat{a}_{i, j} & \hat{d}_{i, j}=i\left(\hat{a}_{i, j}^{\dagger}-\hat{a}_{i, j}\right) & i+j \text { odd } \equiv \bullet
		  \end{array}
		  $$
		- Now there are two for each site.
	- The Hamiltonian
		- collapsed:: true
		  $$
		  \begin{aligned}
		  \hat{H}= & +J_x \sum_{\mathrm{x}-\text { links }}\left(\hat{a}_{i, j}^{\dagger}-\hat{a}_{i, j}\right)\left(\hat{a}_{i+1, j}^{\dagger}+\hat{a}_{i+1, j}\right) \\
		  & -J_y \sum_{\mathrm{y}-\mathrm{links}}\left(\hat{a}_{i-1, j}^{\dagger}+\hat{a}_{i-1, j}\right)\left(\hat{a}_{i, j}^{\dagger}-\hat{a}_{i, j}\right) \\
		  & -J_z \sum_{\mathrm{z}-\mathrm{links}}\left(2 \hat{a}_{i, j}^{\dagger} \hat{a}_{i, j}-1\right)\left(2 \hat{a}_{i, j+1}^{\dagger} \hat{a}_{i, j+1}-1\right)
		  \end{aligned}
		  $$
			- x and y are quadratic while z is quadruple. z would be simplified by conserved quantities.
		- $$
		  \hat{H}=-i J_x \sum_{\mathrm{x} \text {-links }} \hat{c}_{\mathrm{o}} \hat{c}_{\bullet}+i J_y \sum_{\mathrm{y} \text {-links }} \hat{c}_{\bullet} \hat{c}_{\mathrm{o}}-i J_z \sum_{\mathrm{z} \text {-links }}\left(i \hat{d}_{\bullet} \hat{d}_{\circ}\right) \hat{c}_{\bullet} \hat{c}_{\circ}
		  $$
		- $$
		  \hat{H}=i \sum_{\vec{r}}\left(J_x \hat{c}_{\bullet}, \vec{r} \hat{c}_{\mathrm{o}, \vec{r}+\vec{r}_1}+J_y \hat{c}_{\bullet}, \vec{r} \hat{c}_{\mathrm{o}, \vec{r}+\vec{r}_2}-J_z \hat{\alpha}_{\vec{r}} \hat{C}_{\bullet}, \vec{r} \hat{c}_{\mathrm{o}}, \vec{r}\right)
		  $$
			- Note that the vectors are displacements between **unit cells**, which consist of one odd site and one even site each.
			- $$
			  \hat{\alpha}_{\vec{r}}=\left(i \hat{d}_{\bullet, \vec{r}} \hat{d}_{\circ, \vec{r}}\right)
			  $$
			- ((64cbc9cb-0306-41d9-9402-6fa5ce307141))
			-
- # Solution
  id:: 64cbc95f-3878-4633-9f23-c3ae9a407a7e
	- Here $$\hat{\alpha}_{\vec{r}}=\left(i \hat{d}_{\bullet, \vec{r}} \hat{d}_{\circ, \vec{r}}\right)$$ commute with the Hamiltonian and are good quantum numbers, thus we could decompose the Hilbert space.
		- The eigenvalues of it could be regarded as the **Z2 gauge field**.
	- The following procedure is completely analogous to the original paper: Quasi-diagonalize the Hamiltonian by performing Fourier transformations.
		- We obtain a ((64cbec00-ab00-4267-a1a9-e3ad3915dbca)) Hamiltonian:
		  $$
		  \hat{H}=\sum_{\vec{k}} \frac{1}{2}\left(\begin{array}{ll}
		  \hat{d}_{\vec{k}}^{\dagger} & \hat{d}_{-\vec{k}}
		  \end{array}\right)\left(\begin{array}{cc}
		  \varepsilon_{\vec{k}} & i \Delta_{\vec{k}} \\
		  -i \Delta_{\vec{k}}^* & -\varepsilon_{\vec{k}}
		  \end{array}\right)\left(\begin{array}{c}
		  \hat{d}_{\vec{k}} \\
		  \hat{d}_{-\vec{k}}^{\dagger}
		  \end{array}\right)
		  $$
			- $$
			  \begin{gathered}
			  \varepsilon_{\vec{k}}=2\left(J_z-J_x \cos \left(k_1\right)-J_y \cos \left(k_2\right)\right) \\
			  \Delta_{\vec{k}}=2\left(J_x \sin \left(k_1\right)+J_y \sin \left(k_2\right)\right) .
			  \end{gathered}
			  $$
		- By Bogoliubov transformations we obtain the solution
		  $$
		  E_{\vec{k}}=\sqrt{\varepsilon_{\vec{k}}^2+\Delta_{\vec{k}}^2}
		  $$
	- The phase is gapless when we can find some $k$ such that $\varepsilon_{\vec{k}}=\Delta_{\vec{k}}=0$, which leads to our familiar phase diagram.
- # Construct the TN
  collapsed:: true
	- The TN is taken to be **fermionic** until the JW transformation to map fermionic operators to Paulis.
	  collapsed:: true
		- It is claimed there are some extra requirements:
		  ((64cbf25b-8e84-404a-98e4-18889954611e)) and ((64cbf263-f0ae-4f55-8be3-d9e3c9ae355c)).
	- Step 1. Unentangled quantum states in momentum state
	  collapsed:: true
		- The values of the physical index correspond to the fermionic occupation number of Bogoliubov (free) momentum modes.
		  collapsed:: true
			- This means that if the physical index is 0 then the corresponding mode is unoccupied, whereas it is occupied if the value of the physical index is 1
		- Obviously the ground state is the Bogoliubov vacuum, i.e. all occupation numbers are zero.
	- Step 2. Perform the reverse Bogoliubov transformation to obtain the coupled modes.
	  collapsed:: true
		- ((64cbf5bf-ee36-4a7d-93d1-93b5552b1eaf))
		  collapsed:: true
			- Modes along the black arrow are coupled to the ones on the right hand side with opposite momenta, following the ordering indicated by the arrow.
		- After the transformation the entanglement structure becomes
		  ((64cbf655-3540-48ae-800e-2704781e7014))
		  which indicates a 3D structure is necessary (though only constant layers in the extra dimension).
		-
	- Step 3. Perform the reverse FT to go back to real space.
		- Is it that the tensors do not have physical indices, but merely serve as quantum gates?
		  background-color:: red
		  id:: 64cbf6c7-040f-44f7-9b00-950565b151bf
	- Step 4. Majorana braiding TN
		- Why do we need to braid the majorana fermions?
		  background-color:: red
		  id:: 64cbf93e-77a8-4e2d-84a4-9fd96ee3cf4e
	- Step 5. Perform JW transformation to restore Pauli matrices
		- By some miracle we do not need to worry about extra -1 phases since they all cancel!
- # Physical Quantities Calculated
	- Ground state fidelity
	- Thermo fidelity
	- 2-point correlations