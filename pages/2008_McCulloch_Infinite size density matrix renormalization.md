- ![2008_McCulloch_Infinite size density matrix renormalization.pdf](file://zotero_link/Physics/Numerical Methods/DMRG/2008_McCulloch_Infinite size density matrix renormalization.pdf)
- # Setup
	- Rotation of the center matrix
		- Move the center to arbitrary positions in the lattice.
		-
		- First, regard $A^s$ as a single $d m \times m$ matrix (or $B^s$ as a $m \times d m$ matrix)
		  $$
		  \begin{aligned}
		  & A=\left[\begin{array}{l}
		  A^1 \\
		  A^2 \\
		  \vdots \\
		  A^d
		  \end{array}\right] \\
		  & B=\left[B^1 B^2 \ldots B^d\right]
		  \end{aligned}
		  $$
		- Then perform SVD $A=U \Lambda V^{\dagger}$, where $\Lambda$ is a $m \times m$ diagonal matrix such that $\Lambda^2$ is the reduced density matrix, and $U, V$ are row-unitary matrices.
		- Upon rewriting $U$ back as a set of $m \times m$ matrices, one obtains $U^s$ as satisfying the orthogonality constraint, with a remainder term $\Lambda V^{\dagger}$ appearing on the right (which we can, for example, incorporate into the neighboring $A$-matrix).
			- The procedure for obtaining the right orthonormalization constraint is similar, now ending up with a remainder matrix appearing on the left.
		-
	- The MPS
		- $$
		  A^{s_1} \ldots A^{s_{n-1}} A^{s_n} \Lambda B^{s_{n+1}} B^{s_{n+2}} \ldots B^{s_L}
		  $$
		- $\Lambda$ is the **central matrix** which is not normalized.
		-
	-
	-
- # Summary of the Idea
	- Add sites iteratively in the center
	- After sufficiently many steps, $A^s$ and $B^p$ converge, which is the desired translational invariant matrix.
	-