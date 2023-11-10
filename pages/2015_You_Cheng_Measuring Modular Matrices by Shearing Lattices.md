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
  collapsed:: true
	- To fix the phases of eigenstates, we introduce a reference state and require
	  $$
	  \arg \left\langle\Psi(\lambda) \mid \Psi_{\mathrm{ref}}\right\rangle=0
	  $$
	  i.e. subtract the phase relative to the reference state.
		- It's important to check that $\left|\left\langle\Psi(\lambda) \mid \Psi_{\text {ref }}\right\rangle\right|$ never becomes vanishingly small, otherwise the result would suffer from numerical error.
	- ## Overlap of BCS wavefunctions
		- Notations
			- Write the free-fermion Hamiltonian as
			  $$
			  H(\lambda)=\frac{\mathrm{i}}{2} \sum_{i, j} \gamma_i A_{i j}(\lambda) \gamma_j
			  $$
			- Arrange the eigenvectors of $A$ with negative energies into
			  $$
			  U=\left(\begin{array}{lll}
			  u_1 & \cdots & u_n
			  \end{array}\right)_{E<0}
			  $$
		- Proposition. Eigenstates and eigen-energies can be found via the eigen-equation
		  $$
		  \mathrm{i} A u_n=E_n u_n
		  $$
			- First note that
			  $$a_k^\dagger a_k=\frac {\mathbf 1+i \gamma_{2k-1} \gamma_{2k}}{2}$$
			- Rewritten, it means
			  $$4E_k a_k^\dagger a_k=E_k\left(2 \cdot \mathbf 1+2i \gamma_{2k-1} \gamma_{2k}\right)$$
				- RHS could be written as a constant term plus $E_k i\left(\begin{array}{ c c } 0 & 1\\ -1 & 0 \end{array}\right)$
			- Therefore the eigenvalues of $iA$ are identical with the energies.
			-
			- The eigenstates
				- Note that $i\left(\begin{array}{ c c } 0 & 1\\-1 & 0 \end{array}\right)$ has two eigenstates,
				  $$\begin{align*}
				  u_{+} =|0\rangle -i|1\rangle  & ,\lambda _{+} =1\\
				  u_{-} =|0\rangle +i|1\rangle  & ,\lambda _{-} =-1
				  \end{align*}$$
				- Promote them to operators, we find
				  $$\begin{align*}
				  \frac{\hat{u}_{+}}{2} & =\frac{\gamma _{2k-1} -i\gamma _{2k}}{2} =a_{k}\\
				  \frac{\hat{u}_{-}}{2} & =\frac{\gamma _{2k-1} +i\gamma _{2k}}{2} =a_{k}^{\dagger }
				  \end{align*}$$
				-
		- Theorem.
		  $$
		  \left\langle\Psi\left(\lambda_1\right) \mid \Psi\left(\lambda_2\right)\right\rangle=\operatorname{Pf}\left[U^{\dagger}\left(\lambda_1\right) U\left(\lambda_2\right)\right]
		  $$
			-
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