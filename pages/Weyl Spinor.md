- They are called chiral since in the massless case,
  $$
  \begin{aligned}
  \hat{h} \psi_L & =-\frac{1}{2} \psi_L \\
  \hat{h} \psi_R & =\frac{1}{2} \psi_R
  \end{aligned}
  $$
	- When they have mass we can always boost them to exchange their chirality.
- # Transformation rules
	- $$
	  \begin{array}{ll}
	  \left(\frac{1}{2}, 0\right): & J_i^{-}=\frac{1}{2} \sigma_i, \quad J_i^{+}=0 \quad \Rightarrow \quad J_i=\frac{1}{2} \sigma_i, \quad K_i=\frac{i}{2} \sigma_i \\
	  \left(0, \frac{1}{2}\right): & J_i^{-}=0, \quad J_i^{+}=\frac{1}{2} \sigma_i \quad \Rightarrow \quad J_i=\frac{1}{2} \sigma_i, \quad K_i=-\frac{i}{2} \sigma_i .
	  \end{array}
	  $$
	- Plug in
	  id:: 6539bd50-8c50-478d-bee2-6697fc249453
	  $$
	  \Lambda=e^{i\left(\theta_i J_i+\beta_i K_i\right)}
	  $$
	  we have
	  $$
	  \begin{aligned}
	  & \psi_L \rightarrow e^{\frac{1}{2}\left(i \theta_j-\beta_j\right) \sigma_j} \psi_L=\left[1+\frac{1}{2}\left(i \theta_j-\beta_j\right) \sigma_j+\cdots\right] \psi_L, \\
	  & \psi_R \rightarrow e^{\frac{1}{2}\left(i \theta_j+\beta_j\right) \sigma_j} \psi_R=\left[1+\frac{1}{2}\left(i \theta_j+\beta_j\right) \sigma_j+\cdots\right] \psi_R .
	  \end{aligned}
	  $$
	- Note that there is no $i$ before $\beta_j$ (due to the Wick rotation), thus the transformation isn't unitary.
- # Lorentz-covariant terms and Lagrangian
	- Notations
		- $$
		  \sigma^\mu=\left(\mathbb{1}, \sigma_1, \sigma_2, \sigma_3\right), \quad \bar{\sigma}^\mu=\left(\mathbb{1},-\sigma_1,-\sigma_2,-\sigma_3\right)
		  $$
		- $$
		  \sigma_L^{\mu \nu}=\frac{i}{4}\left(\sigma^\mu \bar{\sigma}^\nu-\sigma^\nu \bar{\sigma}^\mu\right), \quad \sigma_R^{\mu \nu}=\frac{i}{4}\left(\bar{\sigma}^\mu \sigma^\nu-\bar{\sigma}^\nu \sigma^\mu\right)
		  $$
	- Scalar terms
		- $$
		  \psi_R^{\dagger} \psi_L, \quad \psi_L^{\dagger} \psi_R
		  $$
		- Note that $\psi_L^{\dagger} \psi_L, \psi_R^{\dagger} \psi_R$ are **not** covariant since the [transformation](((6539bd50-8c50-478d-bee2-6697fc249453))) isn't unitary.
	- Vector terms
		- $$
		  \psi_L^{\dagger} \bar{\sigma}^\mu \psi_L, \quad \psi_R^{\dagger} \sigma^\mu \psi_R
		  $$
		- Proof of covariance
			- $$\begin{align*}
			  L^{\mu } :=\psi _{L}^{\dagger }\overline{\sigma }^{\mu } \psi _{L} & \rightarrow \psi _{L}^{\dagger } e^{\frac{1}{2}( -i\theta _{j} -\beta _{j}) \sigma _{j}}\overline{\sigma }^{\mu } e^{\frac{1}{2}( i\theta _{j} -\beta _{j}) \sigma _{j}} \psi _{L}\\
			  L^{0} & \rightarrow \psi _{L}^{\dagger } e^{\frac{1}{2}( -i\theta _{j} -\beta _{j}) \sigma _{j}} e^{\frac{1}{2}( i\theta _{j} -\beta _{j}) \sigma _{j}} \psi _{L}\\
			   & =\psi _{L}^{\dagger } e^{-\beta _{j} \sigma _{j}} \psi _{L}\\
			  L^{i} & \rightarrow \psi _{L}^{\dagger } e^{\frac{1}{2}( -i\theta _{j} -\beta _{j}) \sigma _{j}}( -\sigma _{i}) e^{\frac{1}{2}( i\theta _{j} -\beta _{j}) \sigma _{j}} \psi _{L}
			  \end{align*}$$
			- Consider an infinitesimal transformation:
			  \begin{align*}
			  L^{0} & \rightarrow \psi _{L}^{\dagger } e^{\frac{1}{2}( -i\theta _{j} -\beta _{j}) \sigma _{j}} e^{\frac{1}{2}( i\theta _{j} -\beta _{j}) \sigma _{j}} \psi _{L}\\
			   & =\psi _{L}^{\dagger }( 1-\beta _{j} \sigma _{j}) \psi _{L}\\
			   & =L^{0} -\psi _{L}^{\dagger } \beta _{j} \sigma _{j} \psi _{L}\\
			   & =L^{0} +\beta _{j} L^{j}\\
			  L^{i} & \rightarrow \psi _{L}^{\dagger }\left[ 1+\frac{1}{2}( -i\theta _{j} -\beta _{j}) \sigma _{j}\right]( -\sigma _{i})\left[ 1+\frac{1}{2}( i\theta _{k} -\beta _{k}) \sigma _{k}\right] \psi _{L}\\
			   & =L^{i} +\psi _{L}^{\dagger }\frac{1}{2}( i\theta _{j} +\beta _{j}) \sigma _{j} \sigma _{i} \psi _{L} +\psi _{L}^{\dagger }( \sigma _{i})\frac{1}{2}( -i\theta _{j} +\beta _{j}) \sigma _{j} \psi _{L}\\
			   & =L^{i} +( i\theta _{j} +\beta _{j}) \varepsilon ^{jik} L^{k} +\frac{1}{2}( i\theta _{i} +\beta _{i}) \psi _{L}^{\dagger } \psi _{L} +( -i\theta _{j} +\beta _{j}) \varepsilon ^{ijk} L^{k} +\frac{1}{2}( -i\theta _{i} +\beta _{i}) \psi _{L}^{\dagger } \psi _{L}\\
			   & =L^{i} -2i\theta _{j} \varepsilon ^{ijk} L^{k} +\beta _{i} L^{0}
			  \end{align*}
				- There may be some incorrect signs, but never mind...
			- Compare to an infinitesimal Lorentz transformation:
			  \begin{align*}
			  L^{\mu } & \rightarrow e^{i( \theta _{i} J_{i} +\beta _{i} K_{i})} L^{\mu }\\
			   & =L^{\mu } +i( \theta _{i} J_{i} +\beta _{i} K_{i})_{\ \nu }^{\mu } L^{\mu }
			  \end{align*}
			- Now we need the concrete form of the generators,
			  ((6539c22c-cdfa-4b6c-8507-83d03de42f4e))
			- We see they indeed match!
		- They may contract with other Lorentz-covariant terms to form invariant scalars, e.g.
		  $$
		  i \psi_L^{\dagger} \bar{\sigma}^\mu \partial_\mu \psi_L+i \psi_R^{\dagger} \sigma^\mu \partial_\mu \psi_R+\cdots
		  $$
	- Rank-2 terms
		- $$
		  \psi_R^{\dagger} \sigma_L^{\mu \nu} \psi_L, \quad \psi_L^{\dagger} \sigma_R^{\mu \nu} \psi_R
		  $$
	- ## The Lagrangian
		- Kinetic terms
			- 'Kinetic' means containing derivatives.
			- $$
			  i \lambda_1 \psi_L^{\dagger} \bar{\sigma}^\mu \partial_\mu \psi_L+i \lambda_2 \psi_R^{\dagger} \sigma^\mu \partial_\mu \psi_R
			  $$
			-
		- Dimension analysis
			- Since $[\mathcal L]=4$, we have 
			  $$
			  [\psi]=\frac{3}{2}
			  $$
		- Mass term
			- $$
			  -m\left(\psi_R^{\dagger} \psi_L+\psi_L^{\dagger} \psi_R\right)
			  $$
			- They must be paired up due to the requirement of Hermicity.
		- If we combine $\psi_L$ and $\psi_R$ to form a Dirac spinor
		  $$
		  \Psi \equiv\left(\begin{array}{l}
		  \psi_L \\
		  \psi_R
		  \end{array}\right)
		  $$
		  and further define
		  $$
		  \bar{\Psi} \equiv\left(\begin{array}{cc}
		  \psi_R^{\dagger} & \psi_L^{\dagger}
		  \end{array}\right)=\Psi^{\dagger} \gamma^0, \quad \gamma^\mu \equiv\left(\begin{array}{cc}
		  0 & \sigma^\mu \\
		  \bar{\sigma}^\mu & 0
		  \end{array}\right)
		  $$
		  then we obtain the familiar Dirac Lagrangian
		  $$
		  \mathcal{L}=i \bar{\Psi} \gamma^\mu \partial_\mu \Psi-m \bar{\Psi} \Psi
		  $$
		-