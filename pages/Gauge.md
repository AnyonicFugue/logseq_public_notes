alias:: Gauge Theory

- [What is a gauge? | Teherence Tao](https://terrytao.wordpress.com/2008/09/27/what-is-a-gauge/)
- # Motivations
	- When we try to construct theories like $A^\mu A^\nu \partial_\mu A_\nu$ or $A^4$, we would encounter negative norms.
		- The problem is absent in QED because ((640458fa-7092-47a3-a5db-acb4759ce58a)).
		- This follows from [[Ward identity]], which in turn follows from **gauge invariance**. #Learning-TODO/Course
		- Thus it's natural to consider other theories with some sorts of gauge invariance.
- # Notations
	- $$g=\exp{\{i\alpha^kT_k\}}$$
		- Here the generators are taken to be Hermitian, so $i$ is added in the factor.
	- $$\left[T^a, T^b\right]=i f^{a b c} T^c$$
		- Structure constants
		-
- # Some Lie Algebras
  collapsed:: true
	- $\operatorname{tr}\left[t_r^a t_r^b\right] \equiv D^{a b}$
	- Prop. As long as the generator matrices are Hermitian, the matrix $D^{a b}$ is positive definite. #card
		- Very simple exercise.
		- Abstraction leads to the underlying structure, which points to the path. #[[Thoughts/Math and Physics]]
	- Thus we can select a basis where $D^{ab}$ is diagonal, then $f^{a b c}=-\frac{i}{C(r)} \operatorname{tr}\left\{\left[t_r^a, t_r^b\right] t_r^c\right\}$
		- It is completely antisymmetric.
	- ## Some reps
		- Fundamental representation for $SU(N)$
			- Acting as itself on $C^N$.
			- Prop. This rep is irreducible.
				-
		- Adjoint representation for any simple Lie Algebra
			- $\left(t_G^b\right)_{a c}=i f^{a b c}$
				- Prop. It is indeed a valid rep. #card
	- ## The Casimir Operator
		- Def.
			- $T^2:=\sum_a T^a T^a$
			- Quadratic Casimir operator
				- $t_r^a t_r^a=C_2(r) \cdot \mathbf{1}$, where r labels the irrep.
		- Prop. It commutes with all generators, thus proportional to identity. #card
			- *To be completed*
			- Only holds in the preferred basis or in all bases?
		- For the adjoint representation, it is written as $f^{a c d} f^{b c d}=C_2(G) \delta^{a b}$
		- Prop. $\operatorname{tr}\left(t_{r_1 \otimes r_2}^a\right)^2=\sum C_2\left(r_i\right) d\left(r_i\right)$ #card
			- Note that the definition of tensor product representations is 
			  $$\begin{aligned} \rho_1 \otimes \rho_2: \mathfrak{g} & \rightarrow \mathfrak{g l}\left(V_1 \otimes V_2\right), \\ x & \mapsto\left(v_1 \otimes v_2 \mapsto\left(\rho_1(x)\right)\left(v_1\right) \otimes v_2+v_1 \otimes\left(\rho_2(x)\right)\left(v_2\right)\right)\end{aligned}$$
			- P
			-
		-
- # General Construction
  collapsed:: true
	- See [here](((64115d22-ffe4-4ee4-8a05-79bbe0f520f2))).
	- ## Def
		- Wilson loop #card
			- In the nonabelian case, $U(x,x)$ is not gauge-invariant.
			  So we define $\operatorname{tr} U_P(x, x)$ as the **Wilson loop**.
				-
			-
	- ## Wilson Line
		- $$
		  U_P(z, y)=P\left\{\exp \left[i g \int_0^1 d s \frac{d x^\mu}{d s} A_\mu^a(x(s)) t^a\right]\right\}
		  $$
			- Exercise. Show that it indeed transforms as $U_P\left(z, y, A^V\right)=V(z) U_P(z, y, A) V^{\dagger}(y)$, where $A^V$ is the field after gauge transformation. #card
				- Hint: ((640ad127-cc23-464b-b796-fb5a07f8049a))
				-
		- Notes
			- $P$ is the path-ordering operator. It is introduced since different generators might be non-commutative.
				- Later matrices (greater values of the parameter) is on the left side.
			- The quantity is path-dependent (due to the prescence of curvature)
			- If $x=y$ it is called a Wilson loop in the abelian case.
				- Use [[Stokes Theorem]], 
				  $$
				  U_P(y, y):=\exp \left[-i e \oint_P d x^\mu A_\mu(x)\right]=\exp \left[-i \frac{e}{2} \int_{\Sigma} d \sigma^{\mu \nu} F_{\mu \nu}\right]
				  $$
					- That is, the total amount of holonomy is equal to the flux on the surface.
		-
- # Examples
  collapsed:: true
	- Reconstruct [[QED]] from a viewpoint of gauge invariance
	  collapsed:: true
		- It is striking that the covariant derivative, the field $A^\mu$ and subsequently the interaction term could emerge from such a simple principle!
		-
		- Recall that 
		  $\begin{aligned} \mathcal{L}_{\text {QED }} & =\mathcal{L}_{\text {Dirac }}+\mathcal{L}_{\text {Maxwell }}+\mathcal{L}_{\text {int }} \\ & =\bar{\psi}(i \not \partial-m) \psi-\frac{1}{4} F_{\mu \nu} F^{\mu \nu}-e \bar{\psi} \gamma^\mu \psi A_\mu\end{aligned}$
		- It is invariant under a **global** gauge transformation $\psi(x) \rightarrow e^{i \alpha} \psi(x)$, but **not** under a **local** gauge transformation $\psi(x) \rightarrow e^{i \alpha(x)} \psi(x)$.
			- Obviously the problem is that the derivative isn't covariant. $\partial_\mu \psi(x) \rightarrow \partial_\mu\left[e^{i \alpha(x)} \psi(x)\right]=e^{i \alpha(x)}\left[i \partial_\mu \alpha(x)\right] \psi(x)+e^{i \alpha(x)} \partial_\mu \psi(x)$
		- We need a ((640439cc-078f-40ee-9eee-b9677c4ca2d2)) to write useful derivative terms.
			- In differential geometry, 'covariant' means independent of the specific coordinate system. 
			  Similarly, here it means independent of the specific gauge choice.
			- The transformation law shall be $D_\mu \psi(x) \rightarrow e^{i \alpha(x)} D_\mu \psi(x)$.
		- It can be easily constructed if we have a ((640439c2-364e-4189-bae8-743a984441f4)).
			- That is, some $U(y, x)$ transforming as $U(y, x) \longrightarrow e^{i \alpha(y)} U(y, x) e^{-i \alpha(x)}$
				- Exercise. Examine this transformation law indeed produces a covariant derivative. #card
		- A natural choice is to take the integral curve of $A_\mu$.
			- $U(y, x)=\exp \left[-i e \int_\gamma A_\mu(x) d x^\mu\right]$
			  id:: 6404430c-1c1c-40a7-a9f6-977362c15589
				- Obviously $A_\mu$ must also transform.
				- Exercise. Prove its law of transformation. #card
					- Hint: Examine the infinitesimal behavior.
					- Answer: {{cloze $A^\mu(x) \rightarrow A^\mu(x)-\frac{1}{e} \partial^\mu \alpha$}}
			- This also absorbs the interaction term into the derivative!
		- Conclusion
			- $\mathcal L=-\frac{1}{4} F^{\mu \nu} F_{\mu \nu}+\bar{\psi}\left(i \gamma^\mu D_\mu-m\right) \psi$
			- $D^\mu=\partial_\mu+i e A_\mu$
		- Comments
			- $\left[D_\mu, D_\nu\right]=ieF_{\mu\nu}$ is precisely the ((640439ca-6d19-4064-9b93-f90d6ed0948e))!
			- Generally ((6404430c-1c1c-40a7-a9f6-977362c15589)) may not be path-independent. This is directly related to [[Berry Phase]].
			- Moreover, $A_\mu A^\mu$ **cannot** appear without breaking the gauge invariance.
			- In principle there can also be $\varepsilon^{\alpha \beta \mu \nu} F_{\alpha \beta} F_{\mu \nu},\left(F_{\mu \nu} F^{\mu \nu}\right)^2$, etc. But they violate symmetries like $P$ or $T$, or not renormalizable.
			  id:: 64045b5c-6fea-4ab6-8155-7c5cce369a40
	- [[Strong Interaction]]
	- Doubled Dirac theory with $SU(2)$ gauge group
		- # Setup
		  collapsed:: true
			- The field is a doublet of dirac spinors $\psi=\left(\begin{array}{l}\psi_1(x) \\ \psi_2(x)\end{array}\right)$
			- The gauge group is $SU(2)$, with the transformation analogous to a 2-component spinor, $\psi \rightarrow \exp \left(i \alpha^i(x) \frac{\sigma^i}{2}\right) \psi \equiv V(x)\psi$
				- Note that each 'component' here is a spinor!
		- # Construction of important quantities
		  collapsed:: true
			- Peskin, ((640fe071-b87c-4027-a3f7-0a0c906b8659))
			- ## Parallel transport $U(y,x)$ and Covariant derivative
				- We would like to have $U(y, x) \rightarrow V(y) U(y, x) V^{\dagger}(x)$ (1)
				- Consider the generating vector field $A_\mu$ and an infinitesimal transport:
				  $$U(x+\epsilon n, x)=1+i g\ \epsilon n^\mu A_\mu^i \frac{\sigma_i}{2}+\mathcal{O}\left(\epsilon^2\right)$$
					- $i$ is to ensure Hermicity
					- $\sigma_i$ are generators
				- $$
				  D_\mu=\partial_\mu-i g A_\mu^i \frac{\sigma^i}{2}
				  $$
			- ## Connection $A_\mu$
				- Plug in the transformation rule (1), we have 
				  $$
				  A_\mu^i(x) \frac{\sigma^i}{2} \rightarrow V(x)\left(A_\mu^i(x) \frac{\sigma^i}{2}+\frac{i}{g} \partial_\mu\right) V^{\dagger}(x)
				  $$
					- In principle this is a transformation on $A^i_\mu$, but there is no simple way of writing it.
			- ## Curvature $F_{\mu\nu}$
				- Note that $[D_\mu,D_\nu]$ is a **tensor** rather than a differential operator.
				- By some simple calculation, 
				  $$
				  \begin{gathered}
				  {\left[D_\mu, D_\nu\right]=-i g F_{\mu \nu}^i \frac{\sigma^i}{2},} \\
				  F_{\mu \nu}^i \frac{\sigma^i}{2}=\partial_\mu A_\nu^i \frac{\sigma^i}{2}-\partial_\nu A_\mu^i \frac{\sigma^i}{2}-i g\left[A_\mu^i \frac{\sigma^i}{2}, A_\nu^j \frac{\sigma^j}{2}\right]
				  \end{gathered}
				  $$
					- Plug in the commutation relations of Pauli matrices, $$F_{\mu \nu}^i=\partial_\mu A_\nu^i-\partial_\nu A_\mu^i+g \epsilon^{i j k} A_\mu^j A_\nu^k$$
				- Transformation rule
					- Here's a simple way: Since we know $D_\mu D_\nu \psi$ (thus also $[D_\mu D_\nu]\psi)$ transforms by multiplying $V$ and $[D_\mu D_\nu]$ is a tensor, it must transform by $[D_\mu D_\nu] \to V[D_\mu D_\nu]V^\dag$
		- # Lagrangian
		  collapsed:: true
			- ## Possible terms
				- $\bar\psi \psi, \bar\psi D_\mu \psi$ are covariant.
				- $F_{\mu \nu}$ is **not** covariant, but we can produce a covariant quantity by taking the trace: 
				  $$
				  \mathcal{L}=-\frac{1}{2} \operatorname{tr}\left[\left(F_{\mu \nu}^i \frac{\sigma^i}{2}\right)^2\right]=-\frac{1}{4}\left(F_{\mu \nu}^i F^{\mu\nu}_i\right)
				  $$
					- The second equality follows from $tr(\sigma_i \sigma_j)= 2\delta_{ij}$
			- Yang-Mills Lagrangian
				- $$
				  \mathcal{L}=\bar{\psi}(i \not D) \psi-\frac{1}{4}\left(F_{\mu \nu}^i\right)^2-m \bar{\psi} \psi
				  $$
					- Is $\bar \psi$ acting $\gamma_0$ on two components separately, or exchanging the two components? #Learning-TODO
					  background-color:: red
			- ## EOM #card
				- Dirac fields
					-
				- Vector field
					- $$
					  \partial^\mu F_{\mu \nu}^i+g \epsilon^{i j k} A^{j \mu} F_{\mu \nu}^k=-g \bar{\psi} \gamma_\nu \frac{\sigma^i}{2} \psi
					  $$
					- Don't miss the second term arising from being non-abelian!
					  background-color:: yellow
- # Misc
	- Note that we can freely discard total derivatives when we calculate $\mathcal H$.
		- Integrating over the whole manifold, total derivatives must vanish.