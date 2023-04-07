alias:: GR

- # Principles
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
  collapsed:: true
	- Christoffel symbol #card
		- $$\Gamma_{a b}^c=\frac{1}{2} g^{c d}\left\{\partial_a g_{b d}+\partial_b g_{a d}-\partial_d g_{a b}\right\}$$
		- Quick memorization: Two plus and a minus, raised by a metric, symmetric positive at the two lower indices
	- Geodesic equation #card
		- Covariant form:
		  $$
		  u^a \nabla_a u^b=0
		  $$
			- The tangent vector is parallel transported!
		- Written in coordinates:
		  $$
		  \frac{d^2 x^\mu}{d t^2}+ \Gamma_{\sigma \nu}^\mu \frac{d x^\sigma}{d t} \frac{d x^\nu}{d t}=0
		  $$
			- Note that this only holds for an affine parameter. For a different parameter $\lambda'$ we have instead $\left(\ddot{x}^\mu+\Gamma_{v \rho}^\mu \dot{x}^\nu \dot{x}^\rho\right)\left(\frac{d \lambda^{\prime}}{d \lambda}\right)^2=-\dot{x}^\mu \frac{d^2 \lambda^{\prime}}{d \lambda^2}$. (Exercise)
		- Can be derived from minimizing $S=\frac{1}{2} m \int_{\gamma} g_{ab}(x) \dot{x}^a \dot{x}^b d t$ and writing down the EL equation
	- Derivative operator
		- Def
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
			  $$\nabla_a \omega_b=\tilde{\nabla}_a \omega_b-C_{a b}^c \omega_c$$
				- Exercise. $\nabla_a t^b=\tilde{\nabla}_a t^b+C_{a c}^b t^c$ #card
			- Note that we must use the trick: If $\omega_b^{\prime}-\omega_b$ vanishes at $p$ we can find smooth functions, $f_{(\alpha)}$, which vanish at $p$ and smooth dual vector fields, $\mu_b^{(\alpha)}$, such that
			  $$
			  \omega_b^{\prime}-\omega_b=\sum_{\alpha=1}^n f_{(\alpha)} \mu_b^{(\alpha)}
			  $$
			  and invoke the fact that all derivative operators agree on scalar fields
		- Covariant derivative #card
			- We hope that $\nabla_a g_{bc}=0$. Moreover, it only differs from the partial derivative by a tensor denoted as $\Gamma$
			- From $\nabla_a t^b=\partial_a t^b+\Gamma_{a c}^b t^c$, we can derive $$\Gamma_{a b}^c=\frac{1}{2} g^{c d}\left\{\partial_a g_{b d}+\partial_b g_{a d}-\partial_d g_{a b}\right\}$$
				- Put $a,b,c$ at the derivative index respectively
				- Invoke symmetricity at the lower indices of $\Gamma_{a b}^c$ (Exercise: Derive it from the property that the derivative operators are torsion-free)
				- Sum two then minus one
		- Parallel Transport #card
			- We say a vector field $v^b$ is parallel transported along $t^a$ if
			  $$
			  t^a \nabla_a v^b=0
			  $$
			- Note that it is curve-dependent, so we can only say that vectors on the same curve are parallel.
			  In general we **cannot** say two vectors at different points are parallel or not.
	- Riemann curvature tensor
		- Def #card
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-05T00:25:43.264Z
		  card-last-reviewed:: 2023-04-05T00:25:43.265Z
		  card-last-score:: 5
			- $$
			  \nabla_a \nabla_b \omega_c-\nabla_b \nabla_a \omega_c:=R_{a b c}{ }^d \omega_d
			  $$
				- Exercise: Show that LHS could indeed be expressed by a tensor, i.e. only depending on the value of $\omega_c$ at a **single point**
			- Ricci tensor
				- $$
				  R_{a c}:=R_{a b c}{}^b
				  $$
			- Scalar curvature
				- $$R := R_a{}^a$$
		- Properties #card
			- 1. $R_{a b c}{ }^d=-R_{b a c}{ }^d$.
			- 2. (First Bianchi Identity) $R_{[a b c]}{}^d=0$.
			- 3. For the derivative operator $\nabla_a$ naturally associated with the metric, $\nabla_a g_{b c}=0$, we have
			  $$
			  R_{a b c d}=-R_{a b d c}
			  $$
			- 4. The (second) Bianchi identity:
			  $$
			  \nabla_{[a} R_{b c] d}{}^e=0
			  $$
			- Note that they can all be proved in the dirty way, i.e. comparing to partial derivatives and writing Christoffel symbols
				- This is actually rather reasonable, since 'manifold' means a structure of $\mathbb R^n$ and partial derivatives commute.
		- Corollary. $\nabla_\mu G^{\mu \nu}=0$ #card
			- Note that $G^{ab}=R^{ab}-\frac 1 2 Rg^{ab}$
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
				- Write $g_{a b}=\eta_{a b}+\gamma_{a b}$ and expand all quantities to first order of $\gamma_{ab}$
				- Fix the gauge to obtain a beautiful equation
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