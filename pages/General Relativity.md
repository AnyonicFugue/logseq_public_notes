alias:: GR

- # Principles
  collapsed:: true
	- General Covariance #card
		- The metric of space is the only quantity pertaining to space that can appear in the laws of physics.
		- Specifically, there are no preferred vector fields or preferred bases of vector fields pertaining only to the structure of space which appear in any law of physics.
			- As a consequence, the (undifferentiated) Christoffel symbol cannot appear in physical laws since it implies a preferred frame.
		- Rephrased, laws of physics are the same in all reference frames (with only the metric dependent on the frame)
		- See ((64267a67-8dfa-44a6-a52c-4f86ebc81214))
	- Special Covariance #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-05-06T17:28:22.039Z
	  card-last-reviewed:: 2023-04-05T11:28:22.039Z
	  card-last-score:: 5
		- All physical measurements are equally possible in different inertial frames and all physical laws are the same.
- # Special Relativity
  collapsed:: true
	- Lorentz transformation #card
		- $$
		  \left\|\Lambda_x{ }^\mu{ }_\nu\right\|=\left(\begin{array}{cccc}
		  \gamma & -\gamma & 0 & 0 \\
		  -\gamma \beta & \gamma & 0 & 0 \\
		  0 & 0 & 1 & 0 \\
		  0 & 0 & 0 & 1
		  \end{array}\right)
		  $$
		- A quick way to rederive it: Take $\tilde t=ict$, then the metric becomes Euclidean.
		  We can first write down a rotation in the Euclidean space, then insert $i$ back.
- # Elements of Differential Geometry
	- Christoffel symbol #card
	  collapsed:: true
		- $$\Gamma_{a b}^c=\frac{1}{2} g^{c d}\left\{\partial_a g_{b d}+\partial_b g_{a d}-\partial_d g_{a b}\right\}$$
		- Quick memorization: Two plus and a minus, raised by a metric, symmetric positive at the two lower indices
	- Geodesic equation #card
	  id:: 64268b1f-18f1-4eb8-a851-d33728ebfa9c
	  collapsed:: true
		- Covariant form:
		  collapsed:: true
		  $$
		  u^a \nabla_a u^b=0
		  $$
			- The tangent vector is parallel transported!
		- Written in coordinates:
		  collapsed:: true
		  $$
		  \frac{d^2 x^\mu}{d t^2}+ \Gamma_{\sigma \nu}^\mu \frac{d x^\sigma}{d t} \frac{d x^\nu}{d t}=0
		  $$
			- Note that this only holds for an affine parameter. For a different parameter $\lambda'$ we have instead $\left(\ddot{x}^\mu+\Gamma_{v \rho}^\mu \dot{x}^\nu \dot{x}^\rho\right)\left(\frac{d \lambda^{\prime}}{d \lambda}\right)^2=-\dot{x}^\mu \frac{d^2 \lambda^{\prime}}{d \lambda^2}$. (Exercise)
		- Can be derived from minimizing $S=\frac{1}{2} m \int_{\gamma} g_{ab}(x) \dot{x}^a \dot{x}^b d t$ and writing down the EL equation
	- Derivative operator
	  collapsed:: true
		- Def
		  collapsed:: true
			- 1. Linearity: For all $A, B \in \mathscr{T}(k, l)$ and $\alpha, \beta \in R$,
			  $$
			  \begin{aligned}
			  \nabla_c\left(\alpha A^{a_1 \cdots a_{k_k} \cdots b_l}+\right. & \left.\beta B^{a_1 \cdots a_{k_1} \cdots b_1 \cdots b_l}\right) \\
			  & =\alpha \nabla_c A^{a_1 \cdots a_{k^{\prime}} \cdots b_l}+\beta \nabla_c B^{a_1 \cdots a_{k_k}} b_1 \cdots b_l
			  \end{aligned}
			  $$
			- 2. Leibnitz rule: For all $A \in \mathscr{T}(k, l), B \in \mathscr{T}\left(k^{\prime}, l^{\prime}\right)$,
			  $$
			  
			  \nabla_e\left[A^{a_1 \cdots a_{k_k} \cdots b_l} B^{c_1 \cdots c_{k^{\prime}}} d_1 \cdots d_{l^{\prime}}\right] =\left[\nabla_e A^{a_1 \cdots a_{k^{\prime}}} b_{b_1 \cdots b_l}\right] B^{c_1 \cdots c_{k^{\prime}} d_1 \cdots d_l} +A^{a_1 \cdots a_{k_k} \cdots b_l}\left[\nabla_e B^{c_1 \cdots c_{k^{\prime}}} d_1 \cdots d_l\right]
			  
			  $$
			- 3. Commutativity with contraction: For all $A \in \mathscr{T}(k, l)$,
			  $$\nabla _{d}\left( A^{a_{1} \cdots c}{}_{a_{k_{1}} \cdots c\cdots b_{l}}\right) =\nabla _{d} A^{a_{1} \cdots c}{}_{a_{k_{1}} \cdots c\cdots b_{l}}$$
			- 4. Consistency with the notion of tangent vectors as directional derivatives on scalar fields: For all $f \in \mathscr{F}$ and all $t^a \in V_p$
			  $$
			  t(f)=t^a \nabla_a f .
			  $$
			- 5. Torsion free: For all $f \in \mathscr{F}$,
			  $$
			  \nabla_a \nabla_b f=\nabla_b \nabla_a f .
			  $$
		- How could they possibly differ?
		  collapsed:: true
			- There must be a tensor $C$ s.t. 
			  collapsed:: true
			  $$\nabla_a \omega_b=\tilde{\nabla}_a \omega_b-C_{a b}^c \omega_c$$
				- Exercise. $\nabla_a t^b=\tilde{\nabla}_a t^b+C_{a c}^b t^c$ #card
				  card-last-interval:: 30
				  card-repeats:: 1
				  card-ease-factor:: 2.6
				  card-next-schedule:: 2023-05-13T01:25:55.498Z
				  card-last-reviewed:: 2023-04-13T01:25:55.498Z
				  card-last-score:: 5
					- Different derivative operators must agree on scalar fields.
			- Note that we must use the trick: If $\omega_b^{\prime}-\omega_b$ vanishes at $p$ we can find smooth functions, $f_{(\alpha)}$, which vanish at $p$ and smooth dual vector fields, $\mu_b^{(\alpha)}$, such that
			  $$
			  \omega_b^{\prime}-\omega_b=\sum_{\alpha=1}^n f_{(\alpha)} \mu_b^{(\alpha)}
			  $$
			  and invoke the fact that all derivative operators agree on scalar fields
		- Covariant derivative #card
		  collapsed:: true
			- We hope that $\nabla_a g_{bc}=0$. Moreover, it only differs from the partial derivative by a tensor denoted as $\Gamma$
			- From $\nabla_a t^b=\partial_a t^b+\Gamma_{a c}^b t^c$, we can derive $$\Gamma_{a b}^c=\frac{1}{2} g^{c d}\left\{\partial_a g_{b d}+\partial_b g_{a d}-\partial_d g_{a b}\right\}$$
			  collapsed:: true
				- Put $a,b,c$ at the derivative index respectively
				- Invoke symmetricity at the lower indices of $\Gamma_{a b}^c$ (Exercise: Derive it from the property that the derivative operators are torsion-free)
				- Sum two then minus one
		- Parallel Transport #card
		  collapsed:: true
			- We say a vector field $v^b$ is parallel transported along $t^a$ if
			  $$
			  t^a \nabla_a v^b=0
			  $$
			- Note that it is curve-dependent, so we can only say that vectors on the same curve are parallel.
			  In general we **cannot** say two vectors at different points are parallel or not.
	- Riemann curvature tensor
	  collapsed:: true
		- Def #card
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-05T00:25:43.264Z
		  card-last-reviewed:: 2023-04-05T00:25:43.265Z
		  card-last-score:: 5
		  collapsed:: true
			- collapsed:: true
			  $$
			  \nabla_a \nabla_b \omega_c-\nabla_b \nabla_a \omega_c:=R_{a b c}{ }^d \omega_d
			  $$
				- Exercise: Show that LHS could indeed be expressed by a tensor, i.e. only depending on the value of $\omega_c$ at a **single point**
			- Ricci tensor
			  collapsed:: true
				- $$
				  R_{a c}:=R_{a b c}{}^b
				  $$
			- Scalar curvature
			  collapsed:: true
				- $$R := R_a{}^a$$
		- Properties #card
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-12T00:41:15.410Z
		  card-last-reviewed:: 2023-04-12T00:41:15.411Z
		  card-last-score:: 5
			- 1. $R_{a b c}{ }^d=-R_{b a c}{ }^d$.
			- 2. 
			  $$
			  R_{a b c d}=-R_{a b d c}
			  $$
			- 3. (First Bianchi Identity) $R_{[a b c]}{}^d=0$.
			- 4. The (second) Bianchi identity:
			  $$
			  \nabla_{[a} R_{b c] d}{}^e=0
			  $$
			- Note that they can all be proved in the dirty way, i.e. comparing to partial derivatives and writing Christoffel symbols
			  collapsed:: true
				- This is actually rather reasonable, since 'manifold' means a structure of $\mathbb R^n$ and partial derivatives commute.
		- Corollary. $\nabla_\mu G^{\mu \nu}=0$ #card
			- Note that $G^{ab}=R^{ab}-\frac 1 2 Rg^{ab}$
			- First invoke the (second) Bianchi identity:
			  $$
			  \nabla_{[a} R_{b c] d}{}^e=0
			  $$
			- First contract $a$ and $e$, then contract $b$ and $d$.
			- Note that $R_{abcd}$ is anti-symmetric both in $ab$ and in $cd$.
	-
	- ## Pushforward and Pullback
	  collapsed:: true
		- Motivation
			- From the categorical view, it's natural to examine the induced maps.
			- From the geometrical view, $(\phi_*)_x$ is the **best linear approximation** (i.e. Jacobian) of $\phi$ at $x$.
		- Def #card
			- Let $M$ and $N$ be manifolds (not necessarily of the same dimension) and let $\phi: M \rightarrow N$ be a $C^{\infty}$ map.
			- First, $(\phi^*f)(x):=f(\phi(x))$, which is the case for $(0,0)$ tensors.
			- For $(1,0)$ tensors (vectors) we have $\phi_*(v)(f):=v(\phi^*f)==v(f\circ \phi)$
				- $f$ is a scalar field on $N$, $f \circ \phi$ is a scalar field on $M$, i.e. $f\circ \phi: M \to \mathbb R$
			- For $(0,1)$ tensors (1-forms) we define $\phi^*\omega(v):=\omega(\phi_*v)$
			-
			- For all $(k,0)$ and $(0,l)$ tensors we have
			  $$
			  \left(\phi_* T\right)_{a_1 \cdots a_l}\left(v_1\right)^{a_1} \cdots\left(v_l\right)^{a_l}=T_{a_1 \cdots a_l}\left(\phi^* v_1\right)^{a_1} \cdots\left(\phi^* v_l\right)^{a_l}
			  $$
			  $$
			  \left(\phi^* T\right)^{b_1 \cdots b_k}\left(\mu_1\right)_{b_1} \cdots\left(\mu_k\right)_{b_k}=T^{b_1 \cdots b_k}\left(\phi_* \mu_1\right)_{b_1} \cdots\left(\phi_* \mu_k\right)_{b_k}
			  $$
			  since tensors are defined as multi-linear forms.
			-
			- Generally we **do not** know how to do for mixed tensors.
			  However, if $\phi$ is a diffeomorphism, we can use $\phi^{-1}$ to define pushforward and pullback for mixed tensors (exercise).
		- ### Link with Symmetry
			- Isometry #card
				- If $\phi: M \rightarrow M$ is a diffeomorphism, $T$ is a tensor field on $M$ and $\phi^* T=T$, $\phi$ is a symmetry transformation for the tensor field $T$.
				- In the case of the metric $g_{a b}$, a symmetry transformation, or a diffeomorphism $\phi$ such that $\left(\phi^* g\right)_{a b}=g_{a b}$, is called an isometry.
				- Notes
					- Explicitly, 'symmetry' means 'operations which leave the field invariant'.
					- Isometries are the gauge freedoms of general relativity.
	- ## Lie Derivative
	  collapsed:: true
		- Def #card
			- $$
			  \mathcal L_v T^{a_1 \cdots a_{k}}_{b_1 \cdots b_l}=\lim _{t \rightarrow 0}\left\{\frac{\phi_{-t}^* T^{a_1 \cdots a_{k}}_{b_1 \cdots b_l}-T^{a_1 \cdots a_k}_{b_1 \cdots b_l}}{t}\right\}
			  $$
			  where $\phi(t)$ is the 1-parameter family of diffeomorphisms generated by the integral curves of $v^a$.
			- Exercise. It indeed satisfies linearity, the Leibniz law and $\mathcal L_v f=v(f)$
		- Now we try to determine its behavior in coordinate systems.
			- Proposition. $$\mathcal L_v w^a=[v, w]^a$$ #card
				- Note that $[v,w](f):=v(w(f))-w(v(f))$
				- In the coordinate where $v^a=e_1^a$, $\mathcal L_v T^{a_1 \cdots a_{k}}_{b_1 \cdots b_l}=\frac {\partial} {\partial x_1} T^{a_1 \cdots a_{k}}_{b_1 \cdots b_l}$. It's easy to verify the equality in this coordinate.
				- Since both sides are tensorial, this tensorial equation holds.
				-
		- Subsequently, all behaviors are determined by the Leibniz rule!
			- For example,
			  $$
			  \mathcal L_v\left(\mu_a w^a\right)=w^a \mathcal L_v \mu_a+\mu_a[v, w]^a
			  $$
			  $$
			  \begin{aligned}
			  \mathcal L_v g_{a b} & =v^c \nabla_c g_{a b}+g_{c b} \nabla_a v^c+g_{a c} \nabla_b v^c \\
			  & =\nabla_a v_b+\nabla_b v_a
			  \end{aligned}
			  $$
			- Note that $v(f)=v^a \nabla_a f$, so Leibniz rule also applies.
		-
	- ## Killing Vector
	  id:: 6433cc8f-9fd7-4848-a229-d5b4372356d2
		- Def #card
			- A vector field $\xi^a$ which generates an 1-para family of isometries, i.e. $\mathcal L_\xi g_{ab}=0$
			- Exercise. The above definition is equivalent to $\nabla_a \xi_b+\nabla_b \xi_a=0$.
		- ((6433cd3d-fc1f-48f5-966e-e2f1fd234ef2)) Let $\xi^a$ be a Killing vector field and let $\gamma$ be a geodesic with tangent $u^a$. Then $\xi_a u^a$ is constant along $\gamma$. #card
		  id:: 6433ccd0-93c5-4ea3-965d-4aba75f860ac
			- A simple exercise to recall the ((64268b1f-18f1-4eb8-a851-d33728ebfa9c)) and the Killing equation.
			- Physically, this means that every 1-para family of isometries gives rise to a conserved quantity.
		- Degrees of freedom
			- See [Wald](((6433ce90-e3c9-4031-95f6-d7b06c8ac6fc)))
			- Note that
			  $$
			  \nabla_a \nabla_b \xi_c=-R_{b c a}{ }^d \xi_d
			  $$
			  so $\xi^a$ is completely determined by its value and first-order derivative at some point (as boundary conditions).
				- Immediately we see that there are at most $n+n(n-1) / 2=n(n+1) / 2$ linear independent Killing fields. #card
					- *Reminder.
					- $n(n-1)/2$ arises from $\nabla_a \xi_b+\nabla_b \xi_a=0$, i.e. antisymmetricity.
- # Tricks in Calculation
  collapsed:: true
	- Local flatness
		- The goal is to find a coordinate where
		  $$
		  g_{\alpha^{\prime} \beta^{\prime}}(P)=\eta_{\alpha^{\prime} \beta^{\prime}}, \quad \Gamma_{\beta^{\prime} \gamma^{\prime}}^{\alpha^{\prime}}(P)=0
		  $$
		- The first can be achieved since $g_{ab}$ is symmetric, thus diagonalizable.
		- It can be shown that 
		  $$
		  x^\mu \rightarrow x^{\prime \mu}=x^\mu+\frac{1}{2} \Gamma_{\rho \sigma}^\mu(0) x^\rho x^\sigma
		  $$
		  satisfies the second condition.
			- It is easy to remember: 
			  $$\frac{\partial ^{2} x^{\prime \mu }}{\partial x^{\rho } \partial x^{\sigma }} =\Gamma ^{\mu }{}_{\rho \sigma }$$
		- Problem: Try to calculate the transformation law of $\partial_c g_{ab}$ and find $$\frac{\partial ^{2} x^{\prime \mu }}{\partial x^{\rho } \partial x^{\sigma }}$$ to make $\tilde \partial_c \tilde g_{ab}=0$. #card
			- Are there enough d.o.f. ?
				- Answer: $T_{(ab)c}$ isn't completely symmetric even if it is symmetric under exchanging b and c.
			- Note: To obtain the transformation rule of $g_{ab}$, first derive the rule of $w_a$. Higher-rank tensors follow.
- # Einstein Equation
  collapsed:: true
	- $$
	  G_{a b} \equiv R_{a b}-\frac{1}{2} R g_{a b}=8 \pi T_{a b}
	  $$
		- Exercise. There's an equivalent form $R_{a b}=8 \pi\left(T_{a b}-\frac{1}{2} g_{a b} T\right)$. #card
			- The two forms can derive each other by taking trace.
	- ## Lagrangian Formulation
		- The total action is a sum of gravitational term and matter term, $S=S_{G}+S_M$
		- $$S_{G}=\frac{c^3}{16 \pi G} \int R \sqrt{-g} \ d^4 x$$
		  $$S_{\mathrm{M}}=\frac{1}{c} \int \mathscr{L}_{\mathrm{M}} \sqrt{-g} d^4 x$$
			- Exercise. The variation indeed gives the correct EOM. #card
				- Useful relations
					- Palatini identity
					  $$
					  \delta R_{\mu \nu}=\nabla_\rho\left(\delta \Gamma_{\mu \nu}^\rho\right)-\nabla_\nu\left(\delta \Gamma_{\mu \rho}^\rho\right)
					  $$
					- id:: 642a29c9-fa99-45de-bd78-1947029aaeb0
					  $$
					  \frac{\partial g}{\partial g_{\mu \nu}}=\tilde{g}_{\mu \nu}=g g^{\mu \nu}
					  $$
						- This is an elementary result in (matrix-wise) linear algebra.
					- $$
					  \begin{aligned}
					  \nabla_\mu A^\mu & =\frac{\partial A^\mu}{\partial x^\mu}+\Gamma_{\sigma \mu}^\mu A^\sigma=\frac{\partial A^\mu}{\partial x^\mu}+A^\sigma \frac{\partial}{\partial x^\sigma} \ln \sqrt{-g} \\
					  & =\frac{1}{\sqrt{-g}} \frac{\partial}{\partial x^\mu}\left(A^\mu \sqrt{-g}\right) .
					  \end{aligned}
					  $$
						- In other words, the covariant divergence is also a coordinate divergence, which **vanishes** upon integrating over the manifold.
						- The would be used to show that $\delta R_{\mu\nu} g^{\mu \nu}$ is a total derivative and vanishes.
				- Note that $g_{ab}\delta g^{ab}=-g^{ab} \delta g_{ab}$
					- The indices **cannot** be raised and lowered arbitrarily in variations!
- # The Schwarzchild Solution
	- $$
	  d s^2=-\left(1-\frac{2 M}{r}\right) d t^2+\left(1-\frac{2 M}{r}\right)^{-1} d r^2+r^2 d \Omega^2
	  $$
		- For easy referencing
	- It is the solution of the external gravitational field of a static and spherically symmetric body.
	  But what is exactly static and spherically symmetric?
	- ## Def
	  collapsed:: true
		- Stationary #card
			- There exists a timelike ((6433cc8f-9fd7-4848-a229-d5b4372356d2)) field.
			- Intuitively, this means that the spacetime has some sort of time-translation symmetry.
		- Static #card
			- The spacetime is stationary and there exists a (spacelike) hypersurface $\Sigma$ which is orthogonal to the orbits of the isometry.
			- By Frobenius's theorem (see appendix B) this is equivalent to the requirement that the timelike Killing vector field $\xi^a$ satisfy
			  $$
			  \xi_{[a} \nabla_b \xi_{c]}=0
			  $$
			- Question: What does it mean that a spacetime is stationary but not static?
				- The timelike Killing vector field is 'rotating'?
		- Spherically symmetric
			- A spacetime is said to be spherically symmetric if its isometry group contains a subgroup isomorphic to the group $S O(3)$, and the orbits of this subgroup (i.e., the collection of points resulting from the action of the subgroup on a given point) are two-dimensional spheres.
			- The $S O(3)$ isometries may then be interpreted physically as rotations.
	- ## Basic facts
	  collapsed:: true
		- If a spacetime is static, then we can push $\Sigma$ to $\Sigma_t$ by the induced diffeomorphism of the Killing field.
			- Therefore there's an orthogonal hypersurface everywhere.
			- Moreover, we may install a coordinate such that 
			  $$
			  d s^2=-V^2\left(x^1, x^2, x^3\right) d t^2+\sum_{\mu, \nu=1}^3 h_{\mu \nu}\left(x^1, x^2, x^3\right) d x^\mu d x^\nu
			  $$
				- Note that if the spacetime is only stationary but not static, we would have cross terms $dtdx^a$.
		- For a spherically symmetric spacetime, the induced metric on each orbit 2-sphere must be uniform (since by definition the rotation is an isometry).
			- However, in a curved space, a sphere need not have a center (e.g., the manifold structure could be, say, $\mathbb{R} \times S^2$, rather than $\mathbb{R}^3$ ); and even if it does, $r$ need not bear any relation to the distance to the center.
		- If a spacetime is both static and spherically symmetric, and if the static Killing field $\xi^a$ is unique (as we shall assume), then $\xi^a$ must be orthogonal to the orbit 2-spheres.
			- Namely, if $\xi^a$ is unique, it must be invariant under all the rotational isometries (since isometries can compose).
			- However, this requires its projection onto any orbit sphere to vanish, since a nonvanishing vector field on a sphere cannot be invariant under all rotations.
		- We may install a convenient coordinate
		  $$
		  d s^2=-f(r) d t^2+h(r) d r^2+r^2\left(d \theta^2+\sin ^2 \theta d \phi^2\right)
		  $$
		   in the spacetime.
			- First, being static grants the existence of hypersurfaces $\Sigma_t$. Moreover the orbit 2-spheres are within the hypersurfaces.
			- Different 2-spheres can be linked by geodesics orthogonal to the 2-spheres. The affine parameter is called $r$.
				- Geodesics are always valid, but the radius may not be!
			- However this coordinate can break down, when $\nabla_a r=0$ or $\xi^a=0$ or $\xi^a$ is colinear with $\nabla_a r$.
			  background-color:: red
		- id:: 64377e9f-224e-4111-b5a5-be9afb161ede
		-
	- ## The Solution
	  collapsed:: true
		- Solve $$d s^2=-f(r) d t^2+h(r) d r^2+r^2\left(d \theta^2+\sin ^2 \theta d \phi^2\right)$$ by brute force, we obtain
		  $$
		  d s^2=-\left(1+\frac{C}{r}\right) d t^2+\left(1+\frac{C}{r}\right)^{-1} d r^2+r^2 d \Omega^2
		  $$
			- Obviously this is asymptotically flat.
		- Comparing with the Newtonian solution (in a proper gauge) we obtain $M=-C/2$, thus
		  $$
		  d s^2=-\left(1-\frac{2 M}{r}\right) d t^2+\left(1-\frac{2 M}{r}\right)^{-1} d r^2+r^2 d \Omega^2
		  $$ #card
			- *Complete the comparison!
		-
	- ## Birkhoff's Theorem
	  collapsed:: true
		- Statement
			- The only spherically symmetric solution of the vacuum Einstein equations is the Schwarzschild metric.
			- That is, static or asymptotic flatness need not be assumed a priori.
		- Generalization
			- Any spherically symmetric and asymptotically flat solution of the Einstein/Maxwell field equations (with no cosmological constant), must be static, so the exterior geometry of a spherically symmetric charged star must be given by the Reissner–Nordström electrovacuum.
		- Proof
			- Bambi started by writing the metric as $d s^2=-f(t, r) c^2 d t^2+g(t, r) d r^2+r^2\left(d \theta^2+\sin ^2 \theta d \phi^2\right)$ and did a brute-force calculation to plug in the Einstein field equation.
				- However it is somewhat unrigorous, since the form of the metric asserts something more than spherical symmetry.
			- It can be proven in a mathematically elegant and rigorous way as [willemvanoosterhout_bscthesis_2019.pdf (wordpress.com)](https://annegretburtscher.files.wordpress.com/2019/11/willemvanoosterhout_bscthesis_2019.pdf)
	- ## Geodesics and Motions
		- It will be used a lot that ((6433ccd0-93c5-4ea3-965d-4aba75f860ac))
		- ### Gravitational Redshift #card
			- Statement of the problem: Light emitted by one static observer is received by another one. How does the frequency differ?
			- Setup
				- The 4-velocities $u^a$ of the observers are tangent to the Killing field $\xi^a$
				  collapsed:: true
					- Note that $u^a:=\frac{dx^a}{d\tau}$, so it is properly normalized.
				- The frequency measured at $P_1$ is
				  $$
				  \omega_1=-\left.\left(k_a u_1^a\right)\right|_{P_1}
				  $$
					- Each observer has his locally Minkowski frame, where $k^a=(E_p,\vec p)$
				- Light goes along a Schwarzschild geodesic.
			- Solution
				- Note that $\xi^a k_a$ remains a constant, $u^a$ is proportional to $\xi^a$ and $u^a u_a=-1$, so we only need to calculate how $\xi^a \xi_a$ changes.
				- Prop. $$\xi^b \xi_b=g_{t t}=-(1-2 M / r)$$.
					-
				- Therefore
				  $$
				  \frac{\omega_1}{\omega_2}=\frac{\left.\left(-\xi^b \xi_b\right)^{1 / 2}\right|_{P_2}}{\left.\left(-\xi^b \xi_b\right)^{1 / 2}\right|_{P_1}}=\frac{\left(1-2 M / r_2\right)^{1 / 2}}{\left(1-2 M / r_1\right)^{1 / 2}}
				  $$
					- This is reasonable since light has redshift when it climbs up the gravitation.
	- ## Interior Solution
	  collapsed:: true
		- Motivation: We're interested in what happens inside a massive body.
		- Setup
			- Model the matter as perfect fluid,
			  $$
			  T_{a b}=\rho u_a u_b+P\left(g_{a b}+u_a u_b\right)
			  $$
				- Note that in order to be compatible with the time-translating symmetry, 
				  $$
				  u^a=-\left(e_0\right)^a=-f^{1 / 2}(d t)^a
				  $$
		- Writing down the equations
		  collapsed:: true
			- $$
			  d s^2=-f(r) d t^2+h(r) d r^2+r^2\left(d \theta^2+\sin ^2 \theta d \phi^2\right)
			  $$
			- $$
			  \begin{aligned}
			  8 \pi T_{00}=8 \pi \rho=G_{00}= & R_{00}+\frac{1}{2}\left(R_0^0+R_1{ }^1+R_2{ }^2+R_3{ }^3\right) \\
			  = & \left(r h^2\right)^{-1} h^{\prime}+r^{-2}\left(1-h^{-1}\right), \\
			  8 \pi T_{11}=8 \pi P=G_{11}= & R_{11}-\frac{1}{2}\left(R_0^0+R_1{ }^1+R_2{ }^2+R_3{ }^3\right) \\
			  = & (r f h)^{-1} f^{\prime}-r^{-2}\left(1-h^{-1}\right), \\
			  8 \pi T_{22}=8 \pi P=G_{22}= & \frac{1}{2}(f h)^{-1 / 2} \frac{d}{d r}\left[(f h)^{-1 / 2} f^{\prime}\right] \\
			  & +\frac{1}{2}(r f h)^{-1} f^{\prime}-\frac{1}{2}\left(r h^2\right)^{-1} h^{\prime} .
			  \end{aligned}
			  $$
		- Solutions
		  collapsed:: true
			- $$
			  \begin{gathered}
			  h(r)=\left[1-\frac{2 m(r)}{r}\right]^{-1} \\
			  m(r)=4 \pi \int_0^r \rho\left(r^{\prime}\right) r^{\prime 2} d r^{\prime}
			  \end{gathered}
			  $$
				- It seems like the Newtonian gravitational field in a ball, but the volume element is **different** since $h(r) \neq 1$.
			- Let $f=e^{2\phi}$, we find
			  $$
			  \frac{d \phi}{d r}=\frac{m(r)+4 \pi r^3 P}{r[r-2 m(r)]}
			  $$
				- Note that $P$ still depends on $r$, so we have to use the last equation.
			- $$
			  \frac{d P}{d r}=-(P+\rho) \frac{m(r)+4 \pi r^3 P}{r[r-2 m(r)]}
			  $$
			- Summing those up, we obtain
			  $$
			  d s^2=-e^{2 \phi} d t^2+\left(1-\frac{2 m(r)}{r}\right)^{-1} d r^2+r^2 d \Omega^2
			  $$
		- Remarks
			- For the solution to be non-singular, we must have $r > 2m(r)$.
			- The pressure needed in general relativity to obtain equilibrium is always larger than in Newtonian graviry.
				- $$
				  P(r)=\rho_0\left[\frac{(1-2 M / R)^{1 / 2}-\left(1-2 M r^2 / R^3\right)^{1 / 2}}{\left(1-2 M r^2 / R^3\right)^{1 / 2}-3(1-2 M / R)^{1 / 2}}\right]
				  $$
				  (Wald ((6437aad2-3d97-4484-9f01-ccf5d4d0b667)))
					- The boundary condition is $\rho=P=0$ at $r=R$.
				- Thus when $R=9M/4$ the pressure needed at $r=0$ becomes **infinite**.
					- The existence of such upper bound is quite interesting: It strongly suggests that heavy stars might undergo a gravitational collapse. #card
						- *Reminder.
						- Would QG prevent a total collapse?
				- The upper bound can be derived by other ways, eg. non-singularity of the metric and $\xi^a$ being timelike.
			-
- # Theories in Curved Spacetime
  collapsed:: true
	- Principle of minimal substitution
		- Substitute $\eta_{ab}$ by $g_{ab}$ and substitute partial derivatives by covariant derivatives.
			- See [Wald](((6428f77e-b46f-426d-b11d-1b15a9e38ab1))) for reference.
		- However, the rule isn't free from ambiguity and different ways of substitution may be possible.
	- ## Electromagnetism
		- $$
		  \begin{gathered}
		  \nabla^a F_{a b}=-4 \pi j_b \\
		  \nabla_{[a} F_{b c]}=0
		  \end{gathered}
		  $$
		- Ricci tensor would naturally emerge in EOM of $A^\mu$ (In Lorentz gauge). See [Wald](((6428f95a-63d8-4f02-8ef3-864bb4438d87))).
			- This suggests the substitution isn't unique. If we minimally 'GRize' the EOM of $A^\mu$ we'd obtain a different form.
	- ## [[Klein-Gordon Theory]]
		- The most natural is
		  $$
		  \nabla^a \nabla_a \phi-m^2 \phi=0
		  $$
		- However, we may equally write
		  $$
		  \nabla^a \nabla_a \phi-m^2 \phi-\alpha R \phi=0
		  $$
		-
- # Physical Interpretations
  collapsed:: true
	- Is gravity still a force? How to define the gravity of the earth? #card
		- First, **what is a force**?
			- If a particle accelerates with respect to an inertial observer, we claim that a force $F:=ma$ is acting on the particle.
			- However, in GR there's no notion of inertial observers (or natural reference frames).
		- Therefore, we can't talk about absolute gravitational force since there's no natural reference frame.
			- However, we can always talk about tidal forces (relative acceleration of two observers).
		- The earth is a special case: We have the earth as a natural reference frame, or we have a natural notion of time-translation symmetry (standing on the surface of the earth)
	- Calculate time measured by an observer #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-05-08T17:25:33.918Z
	  card-last-reviewed:: 2023-04-07T11:25:33.919Z
	  card-last-score:: 5
		- What is an observer?
			- A trajectory in the spacetime, with a locally Minkowski reference frame
		- What is the time he measured?
			- Difference of proper time (i.e. time in the observer's frame)
		- Special case: Static observer
			- Take $g_{ab}=\eta_{ab}$ at infinity (no gravity at infinity)
			- $d\tau^2=-g_{tt}dt^2$
				- Generally $|g_{tt}|<1$, so time measured by the observer would be slower than the coordinate time, i.e. time felt at infinity.
			- Example. Schwarzschild solution
				- $$
				  d \tau=\sqrt{1-\frac{2 G_{\mathrm{N}} M}{c^2 r}} d t<d t
				  $$
	- ## Examples
		- Time difference between GPS satellites and receivers #card
			- Outline
				- Take the same coordinate time and calculate the difference in proper times (which is measured)
					- We don't need to go to the respective frames. Just calculate $g_{ab}dx^a dx^b$.
				- As a weak-gravity approximation, use the Newtonian solution and calculate special- and general-relativity effects separately.
	- ## Weak-Gravity limit
		- Linearized gravity
			- Summary #card
				- Write $g_{a b}=\eta_{a b}+\gamma_{a b}$ and expand all quantities to first order of $\gamma_{ab}$.
				- Fix the gauge to obtain a beautiful equation
					- Consider the perturbation $\gamma_{ab}$ as the derivative $\frac {dg_{ab}(\lambda)}{d\lambda}|_{\lambda=0}$ and a family of diffeomorphisms $\phi_\lambda$. Then $\gamma_{a b}=d g_{a b} /\left.d \lambda\right|_{\lambda=0}$ and $\gamma_{a b}^{\prime}=d\left(\phi_\lambda^* g_{a b}\right) /\left.d \lambda\right|_{\lambda=0}$, which shall represent the same physical spacetime.
					- Prove that $\gamma_{a b}^{\prime}=\gamma_{a b}-\mathcal L_v g_{a b}$, where $v$ is the generating vector field of $\phi_\lambda$. This is the gauge freedom of the perturbation.
				- The final result is $\partial^c \partial_c \bar{\gamma}_{a b}=-16 \pi T_{a b}$, where $\bar{\gamma}_{a b}=\gamma_{a b}-\frac{1}{2} \eta_{a b} \gamma$
					- Note that we can obtain $\gamma_{ab}$ back by taking trace.
		- Restore Newtonian gravity
			- Summary #card
				- *Simplified way
					- Derive $h_{t t}=-\frac{2 \Phi}{c^2}$ from the geodesic equation, which should recover EOM in Newtonian gravity
					- Plug the above expression to the Einstein equation and recover the Poisson equation.
				- Find a suitable coordinate where $T_{a b} \approx \rho t_a t_b$, where $t$ is the time direction of the coordinate (almost inertial)
				- The equation becomes $\nabla^2 \bar{\gamma}_{00}=-16 \pi \rho$, where $\phi \equiv-\frac{1}{4} \bar{\gamma}_{00}$ satisfies Poisson's equation,
				  $$
				  \nabla^2 \phi=4 \pi \rho
				  $$
					- Just the Newtonian gravity!
				- The final task is to verify the geodesic equation.
					- For slow motions, we may approximate $d x^\alpha / d \tau \approx (1,0,0,0)$, thus the geodesic equation writes
					  $$\frac{d^2 x^\mu}{d t^2}=-\Gamma^\mu{ }_{00}$$
					- Plug in the expression of Christoffel symbols, we obtain
					  $$\Gamma_{00}^\mu=-\frac{1}{2} \frac{\partial \gamma_{00}}{\partial x^\mu}=\frac{\partial \phi}{\partial x^\mu}$$
					-