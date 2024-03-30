alias:: CFT

- Refs
	- [[2016_Qualls_Lectures on Conformal Field Theory]]
	- ![2009_Blumenhagen_Plauschinn_Introduction to Conformal Field Theory.pdf](file://zotero_link/Physics/CFT/2009_Blumenhagen_Plauschinn_Introduction to Conformal Field Theory.pdf)
	- ![1997_Di Francesco_Mathieu_Sénéchal_Conformal field theory.pdf](file://zotero_link/Physics/CFT/1997_Di Francesco_Mathieu_Sénéchal_Conformal field theory.pdf)
	-
- # Examples and Models
  collapsed:: true
	- The free boson
	  $$
	  S=\int d^d x\left(-\frac{1}{2} \partial_\mu \phi \partial^\mu \phi\right)
	  $$
- # Setup
  collapsed:: true
	- Notations
	  collapsed:: true
		- $$
		  \begin{aligned}
		  z & =z^0+i z^1 & z^0 & =\frac{1}{2}(z+\bar{z}) \\
		  \bar{z} & =z^0-i z^1 & z^1 & =\frac{1}{2 i}(z-\bar{z}) \\
		  \partial_z & =\frac{1}{2}\left(\partial_0-i \partial_1\right) & \partial_0 & =\partial_z+\partial_{\bar{z}} \\
		  \partial_{\bar{z}} & =\frac{1}{2}\left(\partial_0+i \partial_1\right) & \partial_1 & =i\left(\partial_z-\partial_{\bar{z}}\right)
		  \end{aligned}
		  $$
	- Definitions
	  collapsed:: true
		- Chiral (=holomorphic), (Quasi-) primary
		  collapsed:: true
			- Chiral (holomorphic) and anti-chiral (anti-holomorphic) fields
			  collapsed:: true
				- Holomorphic fields only depend on $z$ and anti-holomorphic fields only depend on $\bar z$.
				- To be more precise, there can be two viewpoints:
				  collapsed:: true
					- Define $\partial_z$ and $\partial_{\bar z}$ as in the notations. '$\phi$ does not depend on $z$' means $\partial_z \phi=0$.
					- Complexify $\mathbb R^2$ to $\mathbb C^2$
		- Conformal dimension
			- If a field $\phi(z, \bar{z})$ transforms under scalings $z \mapsto \lambda z$ according to
			  $$
			  \phi(z, \bar{z}) \mapsto \phi^{\prime}(z, \bar{z})=\lambda^h \bar{\lambda}^{\bar{h}} \phi(\lambda z, \bar{\lambda} \bar{z}),
			  $$
			  it is said to have conformal dimensions $(h, \bar{h})$.
			- Why are not they scale invariant?
			  background-color:: yellow
				- The correct viewpoint is that fields transform under certain representations of the conformal group (as spinor fields transform under certain reps of the Lorentz group), then we use the fields to form conformal invariant quantities.
			- Relationship to coordinate transformation
				- Coordinate transformations (passive viewpoint) induce operators on field configurations (active viewpoint).
				- However, (1) the operators does **not** act on the metric, which should change under coordinate transformations (2) The operator has an extra effect of multiplying by $\lambda^d$ when acting on a field.
			-
			- Compare to the classical scaling dimension:
				- The $\phi^4$ theory has a symmetry under $x^\mu \rightarrow \frac{1}{\lambda} x^\mu, \partial_\mu \rightarrow \lambda \partial_\mu, m \rightarrow \lambda m, g \rightarrow g$ and $\phi \rightarrow \lambda \phi$.
					- This operation is called dilatation and denoted by $\mathcal{D}$.
					- In the active viewpoint, it is a transformation of field configurations **without** affecting the integration measure or the derivative.
				- Thus,
				  $$
				  \mathcal{D}: \phi \rightarrow \lambda^{d_0} \phi .
				  $$
				- The $d_0$ is called the classical or canonical scaling dimension.
		- Primary field and quasi-primary field
		  collapsed:: true
			- If a field transforms under **local** conformal transformations $z \mapsto f(z)$ according to
			  $$
			  \phi(z, \bar{z}) \mapsto \phi^{\prime}(z, \bar{z})=\left(\frac{\partial f}{\partial z}\right)^h\left(\frac{\partial \bar{f}}{\partial \bar{z}}\right)^{\bar{h}} \phi(f(z), \bar{f}(\bar{z})),
			  $$
			  it is called a **primary field** of conformal dimension $(h, \bar{h})$.
			- If it holds only for $f \in S L(2, \mathbb{C}) / \mathbb{Z}_2$, i.e. only for **global** conformal transformations, then $\phi$ is called a **quasi-primary field**.
			-
			- Note that a primary field is always quasi-primary but the reverse is not true.
			- Furthermore, not all fields in a CFT are primary or quasi-primary. Those fields are called **secondary fields**.
- # Conformal Transformations
  collapsed:: true
	- Conformal transformations and the conformal group: Definition, conditions, $d \geq 3$, $d=2$ #card
		- Definitions
		  collapsed:: true
			- Conformal transformation
				- Plain English
					- Preserve angles, or metric up to a constant
				- A map $\varphi: U \to V$ (generally on different manifolds M and M') is called a conformal transformation, if the metric tensor satisfies $\varphi^* g^{\prime}=\Lambda g$.
				- Denoting $x^{\prime}=\varphi(x)$ with $x \in U$, we can express this condition in the following way:
				  $$
				  g_{\rho \sigma}^{\prime}\left(x^{\prime}\right) \frac{\partial x^{\prime \rho}}{\partial x^\mu} \frac{\partial x^{\prime \sigma}}{\partial x^\nu}=\Lambda(x) g_{\mu \nu}(x)
				  $$
					- Usually we take $M'=M, g=\eta$, therefore
					  $$
					  \eta_{\rho \sigma} \frac{\partial x^{\prime \rho}}{\partial x^\mu} \frac{\partial x^{\prime \sigma}}{\partial x^\nu}=\Lambda(x) \eta_{\mu \nu}
					  $$
			- The conformal group
				- The group consisting of **globally** defined, invertible and finite conformal transformations (or more concretely, conformal diffeomorphisms).
				- Note that SCT in Euclidean spaces are **not** in the conformal group!
				  background-color:: red
			- The conformal algebra
				- The Lie algebra corresponding to the conformal group.
				- Note  the algebra consisting of generators of inﬁnitesimal conformal transformations contains the conformal algebra as a subalgebra, but it is **larger in general**.
		- Conditions for conformal invariance
		  collapsed:: true
			- Takeaway message
				- #+BEGIN_WARNING
				  Infinitesimal transformations are often easy to deal with, but they only contain information about the **connected component**.
				  Always be careful that whether there are disconnected components (maybe by investigating the general global form)!
				  #+END_WARNING
			- The full condition:
			  $$
			  \partial_\mu \epsilon_v+\partial_\nu \epsilon_\mu=\frac{2}{d}(\partial \cdot \epsilon) \eta_{\mu \nu}
			  $$
				- Derivation
					- Consider an infinitesimal transformation, $x^{\prime \rho}=x^\rho+\epsilon^\rho(x)+\mathcal{O}\left(\epsilon^2\right)$
					- Then
					  $$
					  \eta_{\rho \sigma} \frac{\partial x^{\prime \rho}}{\partial x^\mu} \frac{\partial x^{\prime \sigma}}{\partial x^\nu} = \eta_{\mu \nu}+\left(\frac{\partial \epsilon_\mu}{\partial x^\nu}+\frac{\partial \epsilon_\nu}{\partial x^\mu}\right)+\mathcal{O}\left(\epsilon^2\right)
					  $$
					- Compare to the definition, we see that
					  $$
					  \partial_\mu \epsilon_\nu+\partial_\nu \epsilon_\mu=K(x) \eta_{\mu \nu}
					  $$
					- Contracting with $\eta ^{\mu \nu}$, we obtain
					  $$
					  2 \partial^\mu \epsilon_\mu=K(x) d
					  $$
					- Plugging in $K$, we arrive at the full condition.
			- ((65e7e4b7-482e-4ba7-8c0c-27c104f72d5f))
				- $$
				  (d-2) \partial_\mu \partial_\nu(\partial \cdot \epsilon)=0 \quad (1)
				  $$
					- First we derive
					  $$
					  (d-1) \square(\partial \cdot \epsilon)=0
					  $$
						- Apply two derivatives, symmetrize over indices, then contract.
					- Then we plug it into the equation
					  $$
					  \left(\eta_{\mu \nu} \square+(d-2) \partial_\mu \partial_\nu\right)(\partial \cdot \epsilon)=0
					  $$
				- $$
				  2 \partial_\mu \partial_\nu \epsilon_\rho=\frac{2}{d}\left(-\eta_{\mu \nu} \partial_\rho+\eta_{\rho \mu} \partial_\nu+\eta_{\nu \rho} \partial_\mu\right)(\partial \cdot \epsilon) \quad (2)
				  $$
					- Essentially the same trick with ((654072b3-9f3f-49b5-afb1-2046a138b115)): Apply one more derivative, permute indices, then $a+b-c$ to cancel unwanted terms.
					-
		-
		- Conformal transformations in $d \geq 3$
		  collapsed:: true
			- Takeaway message
			  collapsed:: true
				- The ((65e7eb45-5b1c-48d7-9919-f23aa59d8e6d))
				  $$
				  \begin{array}{|c|c|c|}
				  \hline \text { Names } & \text { Transformations } & \text { Generators} \\
				  \hline \text { translation } & x^{\prime \mu}=x^\mu+a^\mu & P_\mu=-i \partial_\mu \\
				  \hline \text { dilation } & x^{\prime \mu}=\alpha x^\mu & D=-i x^\mu \partial_\mu \\
				  \hline \text { rotation }   & x^{\prime \mu}=M_v^\mu x^\nu & L_{\mu \nu}=i\left(x_\mu \partial_\nu-x_\nu \partial_\mu\right) \\
				  \hline \mathrm{SCT} & x^{\prime \mu}=\frac{x^\mu-(x \cdot x) b^\mu}{1-2(b \cdot x)+(b \cdot b)(x \cdot x)} & K_\mu=-i\left(2 x_\mu x^\nu \partial_\nu-(x \cdot x) \partial_\mu\right) \\
				  \hline
				  \end{array}
				  $$
					- Comment: The SCT is **not globally well-defined**, since there is a point $x^\mu=\frac{1}{b \cdot b} b^\mu$ such that
					  $$
					  1-2(b \cdot x)+(b \cdot b)(x \cdot x)=0
					  $$
						- We need conformal compactification to correct this.
						- Note that if $b \cdot b = 0$, then any $x \propto b$ is mapped to infinity.
				- ((65eab6eb-316d-4940-baf7-fa1a485fef27))
			- Key observation
				- $$
				  \epsilon_\mu=a_\mu+b_{\mu \nu} x^\nu+c_{\mu \nu \rho} x^\nu x^\rho
				  $$
				- Perform a series expansion of $\epsilon(x)$.
				- Note that relation (1) implies that $(\partial \cdot \epsilon)$ is at most linear in $x^\mu$, so we can make the ansatz.
			- The rest is just perform analysis to each term.
				- The constant term is obviously translation.
				- The linear term
					- Plug in the full condition, we see that
					  $$
					  b_{\nu \mu}+b_{\mu \nu}=\frac{2}{d}\left(\eta^{\rho \sigma} b_{\sigma \rho}\right) \eta_{\mu \nu}
					  $$
					- Then we can separate $b$ into the symmetric part and the anti-symmetric part,
					  $$
					  b_{\mu \nu}=\alpha \eta_{\mu \nu}+m_{\mu \nu}
					  $$
					- The symmetric is dilation and the anti-symmetric is rotation.
				- The quadratic term
					- Plug in the full condition, we see that 
					  $$c_{\mu \nu \alpha} + c_{\nu \mu \alpha} = \frac 1 d c^\gamma _{\gamma \alpha} \eta_{\mu \nu}$$
					- Perform the Christoffel symbol trick, we see that
					  $$
					  c_{\mu \nu \rho}=\eta_{\mu \rho} q_\nu+\eta_{\mu \nu} q_\rho-\eta_{\nu \rho} q_\mu \quad \text { with } \quad q_\mu=\frac{1}{d} c^\rho{ }_{\rho \mu}
					  $$
						- Note that $q_\mu$ could be an arbitrary vector!
					- The full transformation could be obtained following a lengthy integration.
			- How to obtain generators from the infinitesimal form?
			  background-color:: yellow
			  collapsed:: true
				- Note that we cannot add spacetime points, so we need find something that can be added!
				- The natural choice is **fields** defined on the manifold! Therefore, we identify *the transformation of spacetime points* and *the transformation of scalar fields*.
				-
				- Exercise. The infinitesimal transformation $x^\mu \mapsto x^\mu+ a^\mu$ induces the finite transformation $P=-i a^\mu \partial_\mu$.
			- Determine the type of the conformal algebra
			  collapsed:: true
				- The commutation relations are
				  $$\begin{aligned}
				  [ D,P_{\mu }] & =iP_{\mu }\\
				  [ D,K_{\mu }] & =-iK_{\mu }\\
				  [ K_{\mu } ,P_{\nu }] & =2i( \eta _{\mu \nu } D-M_{\mu \nu })\\
				  [ K_{\rho } ,M_{\mu \nu }] & =i( \eta _{\rho \mu } K_{\nu } -\eta _{\rho \nu } K_{\mu })\\
				  [ P_{\rho } ,M_{\mu \nu }] & =i( \eta _{\rho \mu } P_{\nu } -\eta _{\rho \nu } P_{\mu })\\
				  [ L_{\mu \nu } ,M_{\rho \sigma }] & =i( \eta _{\nu \rho } M_{\mu \sigma } +\eta _{\mu \sigma } M_{\nu \rho } -\eta _{\mu \rho } M_{\nu \sigma } -\eta _{\nu \sigma } M_{\mu \rho })
				  \end{aligned}$$
				- Claim. For the case of dimensions $d=p+q \geq 3$, the conformal algebra of $\mathbb{R}^{p, q}$ is $\mathfrak{so}(p+1, q+1)$.
				  id:: 65eab6eb-316d-4940-baf7-fa1a485fef27
					- By a transformation 
					  $$
					  \begin{array}{ll}
					  J_{\mu, \nu}=L_{\mu \nu}, & J_{-1, \mu}=\frac{1}{2}\left(P_\mu-K_\mu\right) \\
					  J_{-1,0}=D, & J_{0, \mu}=\frac{1}{2}\left(P_\mu+K_\mu\right)
					  \end{array}
					  $$
					  we find
					  $$
					  \left[J_{m n}, J_{r s}\right]=i\left(\eta_{m s} J_{n r}+\eta_{n r} J_{m s}-\eta_{m r} J_{n s}-\eta_{n s} J_{m r}\right)
					  $$
					  which is isomorphic to $\mathfrak{so}(p+1,q+1)$.
					- Is the Lie group is completely determined by the Lie algebra?
					  background-color:: red
						- Seems dubious. Even the connected component cannot be guaranteed.
					-
		- Conformal transformations in $d=2$
			- Note that we only investigate the Euclidean case here.
			- Takeaway message
				- Holomorphic or anti-holomorphic
				- The algebra is two commuting copies (corresponding to holomorphic or anti-holomorphic) of the Witt algebra
				- $\mathrm{Conf}(S^2) \simeq \mathrm{SL}(2,\mathbb C) / \mathbb Z_2$.
					- Though the derivation is dubious, the conclusion is correct.
				- #+BEGIN_WARNING
				  The full story is very tricky, since
				  (1) holomorphic functions are generally not invertible and do not form a group 
				  (2) We can encounter difficulties to extend infinitesimal transformations into global ones 
				  (3) The conformal group isn't connected, particularly the anti-holomorphic part is not.
				  #+END_WARNING
			- Partial solution: Infinitesimal transformations
			  background-color:: gray
			  collapsed:: true
				- The anti-holomorphic part would be missed!
				  background-color:: red
				- Now the useful relation (1) holds identically. So we shall investigate the full condition.
				  It turns out to be
				  $$
				  \partial_0 \epsilon_0=+\partial_1 \epsilon_1, \quad \partial_0 \epsilon_1=-\partial_1 \epsilon_0
				  $$
					- The familiar Cauchy-Riemann equations!
				- #+BEGIN_NOTE
				  Being holomorphic is stronger than CR equations.
				  However, it is reasonable to assume that the transformations are smooth, under which CR equations implies holomorphic.
				  #+END_NOTE
			- Full solution: Finite conformal mappings
			  collapsed:: true
				- Under a change of coordinate system $z^\mu \rightarrow w^\mu(x)$, the metric tensor transforms as
				  $$
				  g^{\mu \nu} \rightarrow\left(\frac{\partial w^\mu}{\partial z^\alpha}\right)\left(\frac{\partial w^\nu}{\partial z^\beta}\right) g^{\alpha \beta}
				  $$
				- The condition that defines a conformal transformation is $g_{\mu \nu}^{\prime}(w) \propto g_{\mu \nu}(z)$ or, explicitly,
				  $$
				  \begin{gathered}
				  \left(\frac{\partial w^0}{\partial z^0}\right)^2+\left(\frac{\partial w^0}{\partial z^1}\right)^2=\left(\frac{\partial w^1}{\partial z^0}\right)^2+\left(\frac{\partial w^1}{\partial z^1}\right)^2 \\
				  \frac{\partial w^0}{\partial z^0} \frac{\partial w^1}{\partial z^0}+\frac{\partial w^0}{\partial z^1} \frac{\partial w^1}{\partial z^1}=0
				  \end{gathered}
				  $$
				- We have two solutions to the conditions:
				  Holomorphic
				  $$
				  \frac{\partial w^1}{\partial z^0}=\frac{\partial w^0}{\partial z^1} \text { and } \frac{\partial w^0}{\partial z^0}=-\frac{\partial w^1}{\partial z^1}
				  $$
				  or anti-holomorphic
				  $$
				  \frac{\partial w^1}{\partial z^0}=-\frac{\partial w^0}{\partial z^1} \text { and } \quad \frac{\partial w^0}{\partial z^0}=\frac{\partial w^1}{\partial z^1}
				  $$
					- The conditions can be written as
					  $$a_{00}^{2} +a_{01}^{2} =a_{10}^{2} +a_{11}^{2} \iff\ a_{00}^{2} -a_{10}^{2} =a_{11}^{2} -a_{01}^{2} \\ a_{00} a_{10} +a_{01} a_{11} =0$$
					- Then we complete the square
					  $$a_{00}^{2} -a_{10}^{2} +2ia_{00} a_{10} =a_{11}^{2} -a_{01}^{2} -2ia_{01} a_{11} \\ ( a_{00} +ia_{10})^{2} =( a_{11} -ia_{01})^{2}
					  $$
					- The two solutions correspond to plus and minus respectively.
					-
			- Ref. [The big yellow book](((65ec5fd9-6512-4a10-96fd-415c6fb97a61)))
			-
			- The conformal algebra: Copies of Witt Algebra
				- For holomorphic conformal transformations:
					- Consider the Laurent expansion of a **meromorphic** function:
					  $$
					  z^{\prime}=z+\epsilon(z)=z+\sum_{n \in \mathbb{Z}} \epsilon_n\left(-z^{n+1}\right)
					  $$
					- Some points could be mapped to infinity.
					- Therefore, the corresponding generators are
					  $$
					  l_n=-z^{n+1} \partial_z
					  $$
					  with commutation relations
					  $$
					  \left[{l}_m, {l}_n\right]=(m-n) {l}_{m+n}
					  $$
					- This is precisely the **Witt algebra**.
				- Similarly, we can expand anti-meromorphic functions:
					- $$
					  \bar{l}_n=-\bar{z}^{n+1} \partial_{\bar{z}} \\
					  \left[\bar{l}_m, \bar{l}_n\right]=(m-n) \bar{l}_{m+n}
					  $$
					-
				- Note that
				  $$
				  \left[l_m, \bar{l}_n\right]=0
				  $$
				-
			- The conformal group on the Riemann sphere
				- background-color:: red
				- Allowed elements of the algebra
					- First, we require the transformations to be well-defined at $z=0$, which requires 
					  $$n \geq -1$$
					- Also, we require them to be well-defined at $z=\infty$. After a change of variables $w= \frac 1 z$, we find 
					  $$n \leq 1$$
					- Therefore, the algebra consists of three elements $\{l_{-1}, l_0, l_1\}$.
				- The (connected component of) the conformal group
					- In the Laurent expansion we allow poles. Why don't we allow them here?
					  background-color:: red
					- We can exponentiate the three generators to see their finite forms.
						- As it is clear from its definition, the operator $l_{-1}$ generates translations $z \mapsto z+b$.
						- For the operator $l_0$, let us recall that $l_0=-z \partial_z$. Therefore, $l_0$ generates transformations $z \mapsto a z$ with $a \in \mathbb{C}$.
						- Finally, the operator $l_{+1}$ corresponds to Special Conformal Transformations which are translations for the variable $w=-\frac{1}{z}$, $z \mapsto \frac {z}{cz+1}$.
						- #+BEGIN_NOTE
						  The derivation for anti-holomorphic transformations is completely analogous. 
						  However, note that they reverse the orientation.
						  #+END_NOTE
					- Therefore, a general conformal transformation is in the form
					  $$
					  z \mapsto \frac{a z+b}{c z+d} \quad \text { with } \quad a, b, c, d \in \mathbb{C}
					  $$
					- But there are more restrictions.
						- For this transformation to be invertible, we have to require that $a d-b c$ is nonzero.
						- Then we can scale the constants $a, b, c, d$ such that $a d-b c=$ 1.
						- Furthermore, note that the expression above is invariant under $(a, b, c, d) \mapsto$ $(-a,-b,-c,-d)$.
					- Therefore, the final result is $\mathrm{Conf}(S^2) \simeq \mathrm{SL}(2,\mathbb C) / \mathbb Z_2$.
				-
	- Representations of the conformal algebra and conformal group in $d \geq 3$
	  collapsed:: true
		- Ref. ((65ee9e89-d3d9-46d1-8570-8297e120fada))
		- Key technique
			- Study the subalgebra leaving $x=0$ invariant (i.e. excluding translations).
				- Then the representation is a finite-dimensional linear representation on the components of the field **at the origin**, $\phi(0)$.
			- Then we use BCH formula to obtain transformation at other points,
			  $$
			  e^{-A} B e^A=B+[B, A]+\frac{1}{2 !}[[B, A], A]+\frac{1}{3 !}[[[B, A], A], A]+\cdots
			  $$
		- Denote by $S_{\mu \nu}, \tilde{\Delta}$, and $\kappa_\mu$ the respective values of the generators $L_{\mu \nu}, D$, and $K_\mu$ at $x=0$.
		- Derivation
		  collapsed:: true
			- The subalgebra is
			  $$
			  \begin{aligned}
			  {\left[\tilde{\Delta}, S_{\mu \nu}\right] } & =0 \\
			  {\left[\tilde{\Delta}, \kappa_\mu\right] } & =-i \kappa_\mu \\
			  {\left[\kappa_\nu, \kappa_\mu\right] } & =0 \\
			  {\left[\kappa_\rho, S_{\mu \nu}\right] } & =i\left(\eta_{\rho \mu} \kappa_\nu-\eta_{\rho v} \kappa_\mu\right) \\
			  {\left[S_{\mu \nu}, S_{\rho \sigma}\right] } & =i\left(\eta_{\nu \rho} S_{\mu \sigma}+\eta_{\mu \sigma} S_{\nu \rho}-\eta_{\mu \rho} S_{v \sigma}-\eta_{\nu \sigma} S_{\mu \rho}\right)
			  \end{aligned}
			  $$
			- The last line is the Lorentz algebra, so the representation of the subalgebra is determined by the spin of the field.
			- If we demand that the field $\Phi(x)$ belong to an irreducible representation of the Lorentz group:
				- By Schur's lemma $\tilde{\Delta}$ is a multiple of the identity, or a number.
				- All the matrices $\kappa_\mu$ must vanish.
			- Use BCH formula, we obtain the general rule
			  $$
			  \begin{aligned}
			  D \Phi(x) & =\left(-i x^\nu \partial_\nu+\tilde{\Delta}\right) \Phi(x) \\
			  K_\mu \Phi(x) & =\left\{\kappa_\mu+2 x_\mu \tilde{\Delta}-x^\nu S_{\mu \nu}-2 i x_\mu x^\nu \partial_\nu+i x^2 \partial_\mu\right\} \Phi(x)
			  \end{aligned}
			  $$
		- Result
			- We shall give the result only for spinless fields $\left(S_{\mu \nu}=0\right)$.
			- Under a conformal transformation $x \rightarrow x^{\prime}$, a **spinless** field $\phi(x)$ transforms as
			  $$
			  \phi(x) \rightarrow \phi^{\prime}\left(x^{\prime}\right)=\left|\frac{\partial x^{\prime}}{\partial x}\right|^{-\Delta / d} \phi(x)
			  $$
			  where $\left|\partial x^{\prime} / \partial x\right|$ is the Jacobian of the conformal transformation of the coordinates, related to the scale factor $\Lambda(x)$ by
			  $$
			  \left|\frac{\partial x^{\prime}}{\partial x}\right|=\Lambda(x)^{-d / 2}
			  $$
			- A field transforming like this is called quasi-primary.
	-
- # Basics
	- Infinitesimal conformal transformation of primary fields
	  id:: 65ee7bec-5960-462a-b50c-ec8de7eb7908
	  collapsed:: true
		- Takeaway message
			- $$
			  \delta_{\epsilon, \bar{\epsilon}} \phi(z, \bar{z})=\left(h \partial_z \epsilon+\epsilon \partial_z+\bar{h} \partial_{\bar{z}} \bar{\epsilon}+\bar{\epsilon} \partial_{\bar{z}}\right) \phi(z, \bar{z}) .
			  $$
		- Consider the map $f(z)=z+\epsilon(z)$ with $\epsilon(z) \ll 1$ and compute the following quantities up to first order in $\epsilon(z)$ :
		  $$
		  \begin{aligned}
		  \left(\frac{\partial f}{\partial z}\right)^h & =1+h \partial_z \epsilon(z)+\mathcal{O}\left(\epsilon^2\right), \\
		  \phi(z+\epsilon(z)) & =\phi(z)+\epsilon(z) \partial_z \phi(z, \bar{z})+ \bar\epsilon(z) \partial_{\bar z} \phi(z, \bar{z})+ \mathcal{O}\left(\epsilon^2\right) .
		  \end{aligned}
		  $$
			- Note that $z$ here is the **coordinate** in $\mathbb R^2$, not a specific **direction**.
		- Using these two expressions in the definition of a primary field, we obtain
		  $$
		  \phi(z, \bar{z}) \mapsto \phi(z, \bar{z})+\left(h \partial_z \epsilon+\epsilon \partial_z+\bar{h} \partial_{\bar{z}} \bar{\epsilon}+\bar{\epsilon} \partial_{\bar{z}}\right) \phi(z, \bar{z}),
		  $$
	- Energy-Momentum tensor
		- Theorem. Tracelessness of the EM tensor implies the invariance of action.
		  collapsed:: true
			- $$\begin{aligned}
			  \delta S & =\int d^d x T^{\mu \nu} \partial_\mu \epsilon_\nu \\
			  & =\frac{1}{2} \int d^d x T^{\mu \nu}\left(\partial_\mu \epsilon_\nu+\partial_\nu \epsilon_\mu\right)
			  \end{aligned}$$
			- Plug into the full condition for conformal transformations, we obtain
			  $$\delta S=\frac{1}{d} \int d^d x T_{\ \mu}^\mu (\partial_\rho \epsilon^\rho)$$
			-
			-
		- Theorem. In the coordinate $(z, \bar z)$, the two nonzero components of the ES tensor are chiral and anti-chiral respectively.
		  collapsed:: true
			- Key idea
				- Show that 
				  $$
				  \partial_z T_{\bar z \bar z}=0, \quad \partial_{\bar z} T_{zz}=0
				  $$
				  which should be the **definition** of chiral and anti-chiral.
			- Ref. [Intro](((65ee7d6f-dc98-42c8-8ac2-4d73af60d219)))
		- Theorem. The spacetime conformal transformations are generated by Laurent modes of the EM tensor,
		  $$L_n=\frac{1}{2 \pi i} \oint dz \  z^{n+1} T(z)$$
			- Conversely,
			  $$
			  T(z)=\sum_{n \in \mathbb{Z}} z^{-n-2} L_n
			  $$
	- Infinitesimal conformal transformation of EM tensor
	  id:: 65fd3214-419c-40b0-bb24-e8c523d1a1f7
	  collapsed:: true
		- Theorem. Under conformal transformations $f(z)$, the energy-momentum tensor behaves as
		  $$
		  T^{\prime}(z)=\left(\frac{\partial f}{\partial z}\right)^2 T(f(z))+\frac{c}{12} S(f(z), z),
		  $$
			- $S(w, z)$ is the Schwarzian derivative
			  $$
			  S(f, z)=\frac{1}{\left(\partial_z f\right)^2}\left(\left(\partial_z f\right)\left(\partial_z^3 f\right)-\frac{3}{2}\left(\partial_z^2 f\right)^2\right)
			  $$
		- Proof.
			- The Yellow Book derived it from the conformal Ward identity
		- Note
			- The Schwarzian derivative vanishes for global conformal transformations, thus {{cloze T is a quasi-primary field with conformal dimension 2}}.
	- Radial quantization
	  collapsed:: true
		- Setup
			- Notation
				- $x^0$ is the time direction on the cylinder, and $x^1$ is the space direction
				- $z$ is the coordinate for the plane.
			- We assume that there is a unique vacuum $|0 \rangle$.
				- Recall that in QFT, the vacuum is annihilated by all positive-frequency annihilation operators.
		- Compactification and coordinate transformation
		  collapsed:: true
			- First, we compactify the space direction $x^1$ to a sphere with radius $1$.
			- The map to the plane is
			  $$
			  z=e^w=e^{x^0} \cdot e^{i x^1}
			  $$
				- Note that the point $z=0$ is singular: It corresponds to $t \to -\infty$ and arbitrary $x^1$.
		- Asymptotic state
			- Promote the asymptotic field to an operator,
			  $$
			  \left|\phi_{\text {in }}\right\rangle=\lim _{z, \bar{z} \rightarrow 0} \phi(z, \bar{z})|0\rangle
			  $$
				- Note that on the cylinder, it is $t \to -\infty$.
			- Argument
				- We now consider a field $\phi(z, \bar{z})$ with conformal dimensions $(h, \bar{h})$, for which we can perform a Laurent expansion around $z_0=\bar{z}_0=0$
				  $$
				  \phi(z, \bar{z})=\sum_{n, \bar{m} \in \mathbb{Z}} z^{-n-h} \bar{z}^{-\bar{m}-\bar{h}} \phi_{n, \bar{m}}
				  $$
				- Then we promote the Laurent modes $\phi_{n, \bar{m}}$ to **operators**.
				-
	- Fixing 2-pt and 3-pt correlation functions for primary and quasi-primary fields #card
	  collapsed:: true
		- Primary fields
		  collapsed:: true
			- Results
				- $$
				  \left\langle\phi_1\left(x_1\right) \phi_2\left(x_2\right)\right\rangle=\left\{\begin{array}{lll}
				  \frac{C_{12}}{\left|x_1-x_2\right|^{2 \Delta_1}} & \text { if } & \Delta_1=\Delta_2 \\
				  0 & \text { if } & \Delta_1 \neq \Delta_2
				  \end{array}\right.
				  $$
				- $$
				  \left\langle\phi_1\left(x_1\right) \phi_2\left(x_2\right) \phi_3\left(x_3\right)\right\rangle=\frac{C_{123}}{x_{12}^{\Delta_1+\Delta_2-\Delta_3} x_{23}^{\Delta_2+\Delta_3-\Delta_1} x_{13}^{\Delta_3+\Delta_1-\Delta_2}}
				  $$
			- Analysis
				- Rotation invariance -> The function could only depend on $|x_i-x_j|$ (since all side lengths fix the triangle)
				- Scaling invariance -> Fix the exponents
					- For example, $f(x)=\lambda^{\Delta_1+\Delta_2} f(\lambda x)$ requires
					  $$
					  \left\langle\phi_1\left(x_1\right) \phi_2\left(x_2\right)\right\rangle=\frac{C_{12}}{\left|x_1-x_2\right|^{\Delta_1+\Delta_2}}
					  $$
				- SCT -> Gives relations between scaling dimensions of fields
		- Quasi-primary fields
			- #+BEGIN_NOTE
			  This analysis only allows using **global** conformal transformations, thus the results are weaker.
			  #+END_NOTE
			- Results
				- The two-point function must be
				  $$
				  \left\langle\phi_i(z) \phi_j(w)\right\rangle=\frac{d_{i j} \delta_{h_i, h_j}}{(z-w)^{2 h_i}}
				  $$
					-
				- The three-point function must be
				  $$
				  f\left(z_{12}, z_{23}, z_{13}\right)=\frac{C_{123}}{z_{12}^a z_{23}^b z_{13}^c}
				  $$
				  with
				  $$
				  a=h_1+h_2-h_3, \quad b=h_2+h_3-h_1, \quad c=h_1+h_3-h_2
				  $$
			- Analysis
			  collapsed:: true
				- First, translation invariance ($l_0$) requires that the functions only depend on $z_{12}:=z_1 - z_2$ (and $z_{23}, z_{31}$).
				- 2-pt
					- The scaling invariance ($l_1$) imposes
					  $$
					  \left\langle\phi_1(z) \phi_2(w)\right\rangle \rightarrow\left\langle\lambda^{h_1} \phi_1(\lambda z) \lambda^{h_2} \phi_2(\lambda w)\right\rangle=\lambda^{h_1+h_2} g(\lambda(z-w)) \stackrel{!}{=} g(z-w)
					  $$
					  which fixes the form
					  $$
					  g(z-w)=\frac{d_{12}}{(z-w)^{h_1+h_2}}
					  $$
					- The remaining symmetry $l_{-1}$ could be generated by $z \mapsto -1/z$, which leads to
					  $$h_1=h_2$$
				- 3-pt
					- Completely analogous.
		- For $n \geq 4$, the analysis doesn't suffice to fix correlation functions.
		  background-color:: red
		  collapsed:: true
			- For instance, the four-point function may take the following form:
			  $$
			  \left\langle\phi_1\left(x_1\right) \ldots \phi_4\left(x_4\right)\right\rangle=f\left(\frac{x_{12} x_{34}}{x_{13} x_{24}}, \frac{x_{12} x_{34}}{x_{23} x_{14}}\right) \prod_{i<j}^4 x_{i j}^{\Delta / 3-\Delta_i-\Delta_i}
			  $$
				- $\Delta:=\sum_{i=1}^4 \Delta_i$
	- Conformal Ward identity
	  collapsed:: true
		- Statement
			- $$
			  \begin{aligned}
			  & \left\langle T(z) \phi_1\left(w_1, \bar{w}_1\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle \\
			  & \quad=\sum_{i=1}^N\left(\frac{h_i}{\left(z-w_i\right)^2}+\frac{1}{z-w_i} \partial_{w_i}\right)\left\langle\phi_1\left(w_1, \bar{w}_1\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle
			  \end{aligned}
			  $$
		- Takeaway message
			- Since we have OPE for a primary field, we can try to obtain OPE for the product of multiple primary fields.
			- The conformal Ward identity is essentially the sum of OPE 'distributed' over multiple fields by deforming the integration contour.
		- Proof
			- Start from the integral
			  $$
			  I=\left\langle\oint \frac{d z}{2 \pi i} \epsilon(z) T(z) \phi_1\left(w_1, \bar{w}_1\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle
			  $$
			- Deform the contour
			  ((66022b92-6d30-4492-aaa9-060a16f31918))
			- Then the integral becomes
			  $$
			  \begin{aligned}
			  I & =\sum_{i=1}^N\left\langle\phi_1\left(w_1, \bar{w}_1\right) \ldots\left(\oint_{\mathcal{C}\left(w_i\right)} \frac{d z}{2 \pi i} \epsilon(z) T(z) \phi_i\left(w_i, \bar{w}_i\right)\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle \\
			  & =\sum_{i=1}^N\left\langle\phi_1\left(w_1, \bar{w}_1\right) \ldots\left(h_i \partial \epsilon\left(w_i\right)+\epsilon\left(w_i\right) \partial_{w_i}\right) \phi_i\left(w_i, \bar{w}_i\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle
			  \end{aligned}
			  $$
			- Employ OPE, we find
			  $$
			  \begin{aligned}
			  0=I-I=\oint \frac{d z}{2 \pi i} \epsilon(z)[ & \left\langle T(z) \phi_1\left(w_1, \bar{w}_1\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle \\
			  & \left.-\sum_{i=1}^N\left(\frac{h_i}{\left(z-w_i\right)^2}+\frac{1}{z-w_i} \partial_{w_i}\right)\left\langle\phi_1\left(w_1, \bar{w}_1\right) \ldots \phi_N\left(w_N, \bar{w}_N\right)\right\rangle\right]
			  \end{aligned}
			  $$
			- Since RHS must vanish for any $\epsilon(z)=-z^{n+1}$, the integrand (which has Laurent expansions) must vanish identically.
			  Thus we arrive at the result.
- # [[Operator Product Expansion]]
- # The Hilbert Space and Descendants
	- Outline
	  collapsed:: true
		- We will use two relations repeatedly.
		- The first is the relation between EM tensor and spacetime conformal generators,
		  $$
		  \begin{array}{ll}
		  T(z)=\sum_{n \in \mathbf{Z}} z^{-n-2} L_n & L_n=\frac{1}{2 \pi i} \oint d z z^{n+1} T(z) \\
		  \bar{T}(\bar{z})=\sum_{n \in \mathbf{Z}} \bar{z}^{-n-2} \bar{L}_n & \bar{L}_n=\frac{1}{2 \pi i} \oint d \bar{z} \bar{z}^{n+1} \bar{T}(\bar{z})
		  \end{array}
		  $$
		- The second is OPE.
	- Setup
	  collapsed:: true
		- Convention. The two-point functions are diagonalized and set to identity, i.e. $C_{\alpha \beta}=\delta_{\alpha \beta}$ in
		  $$
		  \left\langle\phi_\alpha(w, \bar{w}) \phi_\beta(z, \bar{z})\right\rangle=\frac{C_{\alpha \beta}}{(w-z)^{2 h}(\bar{w}-\bar{z})^{2 \bar{h}}}
		  $$
			- The coefficients $C_{\alpha \beta}$ are symmetric
		- Definition. Descents of the asymptotic state $|h\rangle$
		  collapsed:: true
			- $$
			  L_{-k_1} L_{-k_2} \cdots L_{-k_n}|h\rangle \quad\left(1 \leq k_1 \leq \cdots \leq k_n\right)
			  $$
			- Note that the number of distinct, linearly independent states at level $N=k_1+...+k_n$ is simply the number $p(N)$ of partitions of the integer $N$.
				- Rephrased, each different way to lift the asymptotic state up the ladder leads to a different state.
		- Definition. The operator algebra is the multiplication rules of general fields, i.e. OPE of general quasi-primary fields and descendants.
			- $$
			  \phi_a(z, \bar{z}) \phi_b(0,0)=\sum_p \sum_{\{k, \bar{k}\}} C_{ab}^{p\{k, \bar{k}\}} z^{h_p-h_a-h_b+K} \bar{z}^{\bar{h}_p-\bar{h}_a-\bar{h}_b+\bar{K}} \phi_p^{(k, \bar{k}\}}(0,0)
			  $$
			- Note that the expansion can be factored into primary part (ancestor), holomorphic part and anti-holomorphic part,
			  $$
			  C_{12}^{p(k, \bar{k})}=C_{12}^p \beta_{12}^{p\{k\}} \bar{\beta}_{12}^{p\{\bar{k}\}}
			  $$
				- Here $p\{k\}$ labels the partition of $k$, **not** the number of partitions!
			- By convention we set $\beta_{i j}^{p(0)}=1$.
	- collapsed:: true
	  #+BEGIN_PINNED
	  Once we know the OPE, any n-pt function can be calculated by using OPE repeatedly -- the theory is solved!
	  #+END_PINNED
		- The only necessary inputs are the central charge $c$, the conformal dimensions of the primary fields, and the three-point function coefficient $C_{pnm}$.
		- Of course, the coefficients $C_{pnm}$ must be obtained from another source, for instance through the conformal bootstrap.
	- ## Properties of energy eigenstates #card
	  collapsed:: true
		- Prop. $T(z)|0\rangle$ and $\bar{T}(\bar{z})|0\rangle$ are well-defined as $z, \bar{z} \rightarrow 0$ implies
		  collapsed:: true
		  $$
		  \begin{aligned}
		  & L_n|0\rangle=0 \\
		  & \bar{L}_n|0\rangle=0
		  \end{aligned} \quad \text{for }n \geq-1
		  $$
			- Use
			  $$T(z)=\sum_{n \in \mathbf{Z}} z^{-n-2} L_n$$
			- Since $T(z) |0\rangle$ is non-singular, it follows that all $n+2 >0$ ($n \geq -1$) terms should vanish.
		- Prop. The asymptotic states $|h, \stackrel{\rightharpoonup}{h}\rangle \equiv \phi(0,0)|0\rangle$ satisfy 
		  collapsed:: true
		  $$
		  L_0|h, \bar{h}\rangle=h|h, \bar{h}\rangle \quad \bar{L}_0|h, \bar{h}\rangle=\bar{h}|h, \bar{h}\rangle
		  $$
		  which implies that they are eigenstates of the Hamiltonian $H=L_0 + \bar L_0$. Also,
		  $$
		  \begin{aligned}
		  & L_n|h, \bar{h}\rangle=0 \\
		  & \bar{L}_n|h, \bar{h}\rangle=0
		  \end{aligned} \quad \text {for } n>0
		  $$
			- Use OPE,
			  $$
			  \begin{aligned}
			  {\left[L_n, \phi(w, \bar{w})\right] } & =\frac{1}{2 \pi i} \oint_w d z z^{n+1} T(z) \phi(w, \bar{w}) \\
			  & =\frac{1}{2 \pi i} \oint_w d z z^{n+1}\left[\frac{h \phi(w, \bar{w})}{(z-w)^2}+\frac{\partial \phi(w, \bar{w})}{z-w}+\mathrm{reg} .\right] \\
			  & =h(n+1) w^n \phi(w, \bar{w})+w^{n+1} \partial \phi(w, \bar{w}) \quad(n \geq-1)
			  \end{aligned}
			  $$
			- As $w$ tends to zero, $w^{1}=0$ while $w^{0}=1$. Therefore,
			  $$
			  {\left[L_0, \phi(w, \bar{w})\right] } =h(n+1) \phi(w, \bar{w})
			  $$
			- The relation for anti-holomorphic generators are completely analogous.
		- Prop. For Laurent modes of primary fields,
		  collapsed:: true
		  $$
		  \left[L_n, \phi_m\right]=[n(h-1)-m] \phi_{n+m}
		  $$
			- Note that
			  $$
			  \begin{aligned}
			  \phi(z) & =\sum_{m \in \mathbf{Z}} z^{-m-h} \phi_m \\
			  \phi_m & =\frac{1}{2 \pi i} \oint d z z^{m+h-1} \phi(z)
			  \end{aligned}
			  $$
			- Verified using OPE.
			- In particular,
			  $$
			  \left[L_0, \phi_m\right]=-m \phi_n
			  $$
			  thus $\phi_m$ can be used as ladder operators.
		- Important Proposition. Local conformal generators can also be used as ladder operators, as
		  $$
		  \left[L_0, L_{-m}\right]=m L_{-m}
		  $$
	- #+BEGIN_TIP
	  The subspace generated by an asymptotic state and all its descendants **form a representation (module)** of the Virasoro algebra!
	  #+END_TIP
	- ## Verma modules and the operator algebra #card
	  collapsed:: true
		- Theorem. The correlator of descendants field are can be calculated from differentials of primary fields, i.e.
		  collapsed:: true
		  $$
		  \left\langle\phi^{(-n)}(w) X\right\rangle = \mathcal{L}_{-n}\langle\phi(w) X\rangle
		  $$
			- #+BEGIN_TIP
			  The technique is very general: (Conformal trans. ->) $L_n=\frac{1}{2 \pi i} \oint dz \  z^{n+1} T(z)$ -> OPE of primary fields -> Contour integration to extract the singularities.
			  #+END_TIP
				- The last step shows that only singularities are important in OPE.
			- Note the difference between $\mathcal L$ and $L$!
			- Notation
				- $$
				  X=\phi_1\left(w_1\right) \cdots \phi_N\left(w_N\right)
				  $$
				  is a product of primary fields.
				- $$
				  \mathcal{L}_{-n}=\sum_i\left\{\frac{(n-1) h_i}{\left(w_i-w\right)^n}-\frac{1}{\left(w_i-w\right)^{n-1}} \partial_{w_i}\right\}
				  $$
			- Proof
				- $$
				  \begin{aligned}
				  \left\langle\phi^{(-n)}(w) X\right\rangle= & \frac{1}{2 \pi i} \oint_w d z(z-w)^{1-n}\langle T(z) \phi(w) X\rangle \\
				  =- & \frac{1}{2 \pi i} \oint_{\left(w_i\right)} d z(z-w)^{1-n} \sum_i\left\{\frac{1}{z-w_i} \partial_{w_i}\langle\phi(w) X\rangle\right. \\
				  & \left.+\frac{h_i}{\left(z-w_i\right)^2}\langle\phi(w) X\rangle\right\}
				  \end{aligned}
				  $$
		- Corollary. The Verma modules are orthogonal, in the sense that
		  $$
		  \left \langle\phi_a^{(k_a, \bar{k_a})}(w, \bar w) \phi_b^{(k_b, \bar{k_b})}(0,0) \right \rangle = 0
		  $$
		- Theorem. The operator algebra is related to the coefficients of the three-point function by
		  $$
		  C_{ab}^{p(0,0)} \equiv C_{ab}^p=C_{p ab}
		  $$
			- Recall the notations
			  collapsed:: true
				- Three-point function
					- $$
					  \begin{aligned}
					  \left\langle\phi_r\left|\phi_a(z, \bar{z})\right| \phi_b\right\rangle & =\lim _{w, \bar{w} \rightarrow \infty} w^{2 h_r} w^{2 \bar{h}_r}\left\langle\phi_r(w, \bar{w}) \phi_a(z, \bar{z}) \phi_b(0,0)\right\rangle \\
					  & =\frac{C_{r ab}}{z^{h_1+h_2-h_r} \bar{z}^{\bar{h}_1+\bar{h}_2-\bar{h}_r}}
					  \end{aligned}
					  $$
				- Operator algebra
					- $$
					  \phi_a(z, \bar{z}) \phi_b(0,0)=\sum_p \sum_{\{k, \bar{k}\}} C_{ab}^{p\{k, \bar{k}\}} z^{h_p-h_a-h_b+K} \bar{z}^{\bar{h}_p-\bar{h}_a-\bar{h}_b+\bar{K}} \phi_p^{(k, \bar{k}\}}(0,0)
					  $$
			- Proposition. On the OPE side, the only contributing term is $p\{k, k\}=r\{0,0\}$.
				- First the orthogonality of Verma modules imply $p=r$.
		- Theorem. The coefficients $\beta_{i j}^{p(K)}$ are determined by the requirement that both sides of the OPE behave identically upon conformal transformations
			- See the [Yellow Book](((6604c8e6-e00d-41bd-bee5-95f38dcb49cd))) for a derivation.
			-
	- Conformal blocks
		- [mathematical physics - A pedestrian explanation of conformal blocks - Physics Stack Exchange](https://physics.stackexchange.com/questions/1799/a-pedestrian-explanation-of-conformal-blocks)
- # Central Extension and Virasoro Algebra
  collapsed:: true
	- A good source: [Why exactly do sometimes universal covers, and sometimes central extensions feature in the application of a symmetry group to quantum physics? - Physics Stack Exchange](https://physics.stackexchange.com/questions/203944/why-exactly-do-sometimes-universal-covers-and-sometimes-central-extensions-feat)
	-
	- Definition. Virasoro algebra
		- $$
		  \left[L_m, L_n\right]=(m-n) L_{m+n}+\frac{c}{12}\left(m^3-m\right) \delta_{m+n, 0}
		  $$
	- Why do we need the central extension?
	  background-color:: red
		- It has to do with anomaly when promoting the classical symmetry to a quantum symmetry.
	- See the Big Yellow Book for a physical viewpoint and the Mathematical Introduction for a mathematical viewpoint.
	-