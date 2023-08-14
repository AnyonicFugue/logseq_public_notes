- ![2010_Jagannathan_On generalized Clifford algebras and their.pdf](file://zotero_link/Mathematics/Algebra/Linear Algebra/2010_Jagannathan_On generalized Clifford algebras and their.pdf)
- [[Generalized Clifford Algebra]]
	- # Motivation
		- ((64d93fd7-f3bf-42d9-a6fe-966c02a074d6))
		- In short, the projective representations of a finite abelian group precisely defines a GCA.
	- Definition
		- GCA
		  collapsed:: true
			- $$
			  \begin{aligned}
			  e_j e_k & =\omega_{j k} e_k e_j, \quad \omega_{j k} e_l=e_l \omega_{j k}, \quad \omega_{j k} \omega_{l m}=\omega_{l m} \omega_{j k} \\
			  e_j^{N_j} & =1, \quad \omega_{j k}^{N_j}=\omega_{j k}^{N_k}=1, \quad \forall j, k, l, m=1,2, \ldots, n .
			  \end{aligned}
			  $$
				- Note that the exchange phase could depend on the site.
			- Equivalently,
			  $$
			  \begin{gathered}
			  \omega_{j k}=e^{2 \pi i t_{j k} / \hat{N}}, \quad t_{k j}=-t_{j k}, \quad \hat{N}=1 \cdot \operatorname{c} \cdot \mathrm{m}\left[N_{j k}\right] \\
			  j, k=1,2, \ldots, n .
			  \end{gathered}
			  $$
			- Thus, any GCA can be characterized by an integer $\hat{N}$ and an antisymmetric integer matrix
			  $$
			  T=\left(\begin{array}{ccccc}
			  0 & t_{12} & t_{13} & \ldots & t_{1 n} \\
			  -t_{12} & 0 & t_{23} & \ldots & t_{2 n} \\
			  -t_{13} & -t_{23} & 0 & \ldots & t_{3 n} \\
			  \vdots & \vdots & \vdots & \ddots & \vdots \\
			  -t_{1 n} & -t_{2 n} & -t_{3 n} & \ldots & 0
			  \end{array}\right)
			  $$
		- Uniform GCA $C(p,n)$
			- $$\begin{aligned}
			  e_j e_k & =\omega e_k e_j, \quad \omega=e^{2 \pi i / p}, \quad \forall j<k \\
			  e_j^N & =1, \quad j, k=1,2, \ldots, n .
			  \end{aligned}$$
		- Skew-normal form
		  collapsed:: true
			- \begin{aligned}
			  \mathcal{T} & =\left(\begin{array}{cc}
			  0 & t_1 \\
			  -t_1 & 0
			  \end{array}\right) \oplus \cdots \oplus\left(\begin{array}{cc}
			  0 & t_s \\
			  -t_s & 0
			  \end{array}\right) \oplus \mathrm{O}_{n-2 s} \\
			  T & =U \mathcal{T} \tilde{U}( \pm \bmod . \hat{N})
			  \end{aligned}
				- 'mod N$ arises from $\omega^N=1$.
			- i.e. A JW transformation to disentangle the pairs
		- Sylvester Matrices
			- Shift matrix 
			  $$
			  B=\left[\begin{array}{cccccc}
			  0 & 0 & 0 & \cdots & 0 & 1 \\
			  1 & 0 & 0 & \cdots & 0 & 0 \\
			  0 & 1 & 0 & \cdots & 0 & 0 \\
			  0 & 0 & 1 & \cdots & 0 & 0 \\
			  \vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\
			  0 & 0 & 0 & \cdots & 1 & 0
			  \end{array}\right]
			  $$
				- $|n\rangle \mapsto |n+1 \mod p\rangle$
			- Clock matrix
			  $$
			  A=\left[\begin{array}{ccccc}
			  1 & 0 & 0 & \cdots & 0 \\
			  0 & \omega & 0 & \cdots & 0 \\
			  0 & 0 & \omega^2 & \cdots & 0 \\
			  \vdots & \vdots & \vdots & \ddots & \vdots \\
			  0 & 0 & 0 & \cdots & \omega^{d-1}
			  \end{array}\right]
			  $$
				- $|n\rangle \mapsto \omega^{n}|n\rangle$
			- Obviously $AB = \omega BA$
			  id:: 64d93795-d2f0-47c6-9ade-1001aad4282d
			-
	- Basic Facts
		- The T-matrix of a GCA could always be made into a Skew-normal form by a similarity transformation.
			- It implies that we need only to study the representations of $AB=\omega BA$.
			  The whole GCA follows by a JW transformation.
		- Theorem. The Sylvester matrices is the only irreducible representation of $AB=\omega BA$.
			-