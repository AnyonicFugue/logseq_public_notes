alias:: [[Lorentz invariance]], [[Lorentz invariant]], [[Lorentz covariant]], [[Lorentz Group]], [[Lorentz Transformation]]

- # The Transformation
	- $$
	  \Lambda=e^{i\left(\theta_i J_i+\beta_i K_i\right)}
	  $$
		- id:: 6539c22c-cdfa-4b6c-8507-83d03de42f4e
		  $$
		  J_1=i\left(\begin{array}{cccc}
		  0 & 0 & 0 & 0 \\
		  0 & 0 & 0 & 0 \\
		  0 & 0 & 0 & -1 \\
		  0 & 0 & 1 & 0
		  \end{array}\right), \quad J_2=i\left(\begin{array}{cccc}
		  0 & 0 & 0 & 0 \\
		  0 & 0 & 0 & 1 \\
		  0 & 0 & 0 & 0 \\
		  0 & -1 & 0 & 0
		  \end{array}\right), \quad J_3=i\left(\begin{array}{cccc}
		  0 & 0 & 0 & 0 \\
		  0 & 0 & -1 & 0 \\
		  0 & 1 & 0 & 0 \\
		  0 & 0 & 0 & 0
		  \end{array}\right)
		  $$
		  $$
		  K_1=i\left(\begin{array}{cccc}
		  0 & -1 & 0 & 0 \\
		  -1 & 0 & 0 & 0 \\
		  0 & 0 & 0 & 0 \\
		  0 & 0 & 0 & 0
		  \end{array}\right), \quad K_2=i\left(\begin{array}{cccc}
		  0 & 0 & -1 & 0 \\
		  0 & 0 & 0 & 0 \\
		  -1 & 0 & 0 & 0 \\
		  0 & 0 & 0 & 0
		  \end{array}\right), \quad K_3=i\left(\begin{array}{cccc}
		  0 & 0 & 0 & -1 \\
		  0 & 0 & 0 & 0 \\
		  0 & 0 & 0 & 0 \\
		  -1 & 0 & 0 & 0
		  \end{array}\right)
		  $$
- # Classification of Representations
	- Write
	  $$
	  J_i^{-} \equiv \frac{1}{2}\left(J_i-i K_i\right), \quad J_i^{+} \equiv \frac{1}{2}\left(J_i+i K_i\right)
	  $$
	  we have
	  $$
	  \begin{aligned}
	  & {\left[J_i^{-}, J_j^{-}\right]=i \epsilon_{i j k} J_k^{-}} \\
	  & {\left[J_i^{+}, J_j^{+}\right]=i \epsilon_{i j k} J_k^{+}} \\
	  & {\left[J_i^{+}, J_j^{-}\right]=0 .}
	  \end{aligned}
	  $$
	- Therefore the (complexified) $\mathfrak{so}(1,3)$ splits into two copies of $\mathfrak{su}(2)$.
	- We may label the representations by (A,B), the spins of the two representations of $\mathfrak{su}(2)$.
	-
	- [[Weyl Spinor]] are $\left(\frac{1}{2}, 0\right)$ and $\left(0, \frac{1}{2}\right)$ representations.
	- Dirac spinor is the direct sum $\left(\frac{1}{2}, 0\right) \oplus\left(0, \frac{1}{2}\right)$.
	- Note that $\left(\frac{1}{2}, 0\right) \oplus\left(0, \frac{1}{2}\right) \neq (\frac 1 2, \frac 1 2)$!
		- In short, the representation $T \otimes T$ of $G \times G$ is irreducible.
		- $$
		  \begin{array}{ccc}
		  (A, B) & \text { field } & \text { spin } \\
		  \hline(0,0) & \text { scalar } & 0 \\
		  \left(\frac{1}{2}, 0\right) & \text { left-handed Weyl spinor } \psi_L & \frac{1}{2} \\
		  \left(0, \frac{1}{2}\right) & \text { right-handed Weyl spinor } \psi_R & \frac{1}{2} \\
		  \left(\frac{1}{2}, \frac{1}{2}\right) & \text { vector } A^\mu & 1 \oplus 0 \\
		  (1,0) & \text { anti-symmetric, self-dual rank-2 tensor } & 1 \\
		  (0,1) & \text { anti-symmetric, anti-self-dual rank-2 tensor } & 1
		  \end{array}
		  $$
-