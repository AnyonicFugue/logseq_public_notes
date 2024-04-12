alias:: OPE

- # Primary Field
	- Statement
		- For a primary field $\phi(z, \bar{z})$ with conformal dimensions $(h, \bar{h})$,
		  collapsed:: true
		  $$
		  \begin{aligned}
		  & T(z) \phi(w, \bar{w})=\frac{h}{(z-w)^2} \phi(w, \bar{w})+\frac{1}{z-w} \partial_w \phi(w, \bar{w})+\ldots \\
		  & \bar{T}(\bar{z}) \phi(w, \bar{w})=\frac{\bar{h}}{(\bar{z}-\bar{w})^2} \phi(w, \bar{w})+\frac{1}{\bar{z}-\bar{w}} \partial_{\bar{w}} \phi(w, \bar{w})+\ldots
		  \end{aligned}
		  $$
			- Note that OPE is only meaningful within correlation functions. See Yellowbook and stackexchange.
	- Proof
	  collapsed:: true
		- Key idea
			- We can compare two ways to compute the change of primary fields under infinitesimal conformal transformations.
			- The first way is to start from the definition, while the second way is to use the symmetry charge as a generator.
		- Definition. Radial ordering
		  collapsed:: true
			- $$
			  R(A(z) B(w)):=\left\{\begin{array}{l}
			  A(z) B(w) \text { for }|z|>|w| \\
			  B(w) A(z) \text { for }|w|>|z|
			  \end{array}\right.
			  $$
			- Actually time ordering on the cylinder.
		- The first way gives
		  collapsed:: true
		  $$
		  \delta_{\epsilon, \bar{\epsilon}} \phi(z, \bar{z})=\left(h \partial_z \epsilon+\epsilon \partial_z+\bar{h} \partial_{\bar{z}} \bar{\epsilon}+\bar{\epsilon} \partial_{\bar{z}}\right) \phi(z, \bar{z}) .
		  $$
			- Refer to ((65ee7bec-5960-462a-b50c-ec8de7eb7908)).
		- The second way gives 
		  $$
		  \delta_{\epsilon, \bar{\epsilon}} \phi(w, \bar{w})=\frac{1}{2 \pi i} \oint_{\mathcal{C}(w)} d z \ \epsilon(z) R(T(z) \phi(w, \bar{w}))+\text { anti-chiral }
		  $$
			- Recall that since the current $j_\mu=T_{\mu \nu} \epsilon^\nu$ associated to the conformal symmetry is preserved, there exists a conserved charge which is expressed in the following way:
			  $$
			  Q=\int d x^1 j_0 \quad \text { at } \quad x^0=\text { const }
			  $$
			- This conserved charge is the **generator** of symmetry transformations for an operator $A$, which can be written in the Heisenberg picture as
			  collapsed:: true
			  $$
			  \delta A=[Q, A]
			  $$
				- This is a highly nontrivial claim. I don't know how to prove it for even translation and rotation (maybe it's wrong altogether), but it points the way to OPE.
			- $x^0=$ const corresponds to $|z|=$ const, so the integral over space $\int d x^1$ becomes a **contour integral**. Therefore, the conserved charge in complex coordinates reads
			  $$
			  Q=\frac{1}{2 \pi i} \oint_{\mathcal{C}}(d z T(z) \epsilon(z)+d \bar{z} \bar{T}(\bar{z}) \bar{\epsilon}(\bar{z}))
			  $$
			- Therefore, under an infinitesimal conformal transformation,
			  $$
			  \delta \phi(w, \bar{w})=\frac{1}{2 \pi i} \oint_{\mathcal{C}} d z[T(z) \epsilon(z), \phi(w, \bar{w})]+\frac{1}{2 \pi i} \oint_{\mathcal{C}} d \bar{z}[\bar{T}(\bar{z}) \bar{\epsilon}(\bar{z}), \phi(w, \bar{w})]
			  $$
			- Use the radial ordering, it becomes
			  $$
			  \begin{aligned}
			  \oint d z[A(z), B(w)] & =\oint_{|z|>|w|} d z A(z) B(w)-\oint_{|z|<|w|} d z B(w) A(z) \\
			  & =\oint_{\mathcal{C}(w)} d z R(A(z) B(w)),
			  \end{aligned}
			  $$
			- Then we arrive at the result
		- Rephrase the first way as contour integrals,
		  $$
		  \begin{aligned}
		  h\left(\partial_w \epsilon(w)\right) \phi(w, \bar{w}) & =\frac{h}{2 \pi i} \oint_{\mathcal{C}(w)} d z  \frac{\epsilon(z)}{(z-w)^2} \phi(w, \bar{w}) \\
		  \epsilon(w)\left(\partial_w \phi(w, \bar{w})\right) & =\frac{1}{2 \pi i} \oint_{\mathcal{C}(w)} d z \frac{\epsilon(z)}{z-w} \partial_w \phi(w, \bar{w})
		  \end{aligned}
		  $$
		- Comparing the two ways gives the OPE.
	- The ellipses denotes **non-singular terms**. Only the singular terms carry essential information.
- # Energy-Momentum Tensor
  collapsed:: true
	- Statement
		- When $|z|>|w|$, the OPE of the energy-momentum tensor is
		  collapsed:: true
		  $$
		  T(z) T(w)=\frac{c / 2}{(z-w)^4}+\frac{2 T(w)}{(z-w)^2}+\frac{\partial_w T(w)}{z-w}+\ldots
		  $$
		  with a same expression for $\bar T(z) \bar T(w)$. The OPE for $T(z) \bar T(w)$ contains only non-singular terms.
			- $c$ denotes the central charge.
	- Verification
		- Key idea
			- Identify Laurent modes of EM tensor with generators of conformal generators.
				- The Laurent modes can be seen as generators acting on the **spacetime**, while $l_n$ acts on the **function space** (space of fields).
		- Expand
		  $$
		  T(z)=\sum_{n \in \mathbb{Z}} z^{-n-2} L_n \quad \text { where } \quad L_n=\frac{1}{2 \pi i} \oint d z z^{n+1} T(z) .
		  $$
		- Use the expansion and choose the transformations to be generators $\epsilon(z)=-\epsilon_n z^{n+1}$, we find that
		  $$
		  Q_n=\oint \frac{d z}{2 \pi i} T(z)\left(-\epsilon_n z^{n+1}\right)=-\epsilon_n \sum_{m \in \mathbb{Z}} \oint \frac{d z}{2 \pi i} L_m z^{n-m-1}=-\epsilon_n L_n .
		  $$
		-
		- The lengthy [calculation](((65fd30d3-bf8e-414d-a2b0-dbf130f0bd46))) then shows the result
		  $$
		  (m-n) L_{m+n}+\frac{c}{12}\left(m^3-m\right) \delta_{m,-n}
		  $$
- # General Quasi-Primary Fields
	- Note that the EM tensor is a quasi-primary field with $h=2$. Ref. ((65fd3214-419c-40b0-bb24-e8c523d1a1f7))
	- Statement
		- $$
		  \phi_a(z, \bar{z}) \phi_b(0,0)=\sum_p \sum_{\{k, \bar{k}\}} C_{ab}^{p\{k, \bar{k}\}} z^{h_p-h_a-h_b+K} \bar{z}^{\bar{h}_p-\bar{h}_a-\bar{h}_b+\bar{K}} \phi_p^{(k, \bar{k}\}}(0,0)
		  $$
- For a rigorous proof, we need the VOA.