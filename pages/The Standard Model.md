id:: 65475c6a-e2eb-4bb8-9932-3a87bdc6986e
$$
\begin{aligned}
\mathcal{L}_{\mathrm{SM}} = & -\frac{1}{4} G_{A,\mu \nu } G_{A}^{\mu \nu } -\frac{1}{4} W_{a,\mu \nu } W_{a}^{\mu v} -\frac{1}{4} B_{\mu \nu } B^{\mu \nu }\\
 & +( D_{\mu } H)^{\dagger }\left( D^{\mu } H\right) -m^{2} H^{\dagger } H-\lambda \left( H^{\dagger } H\right)^{2}\\
 & +iQ_{L}^{\dagger }\overline{\sigma }^{\mu } D_{\mu } Q_{L} +iu_{R}^{\dagger } \sigma ^{\mu } D_{\mu } u_{R} +id_{R}^{\dagger } \sigma ^{\mu } D_{\mu } d_{R} +iL_{L}^{\dagger }\overline{\sigma }^{\mu } D_{\mu } L_{L} +ie_{R}^{\dagger } \sigma ^{\mu } D_{\mu } e_{R}\\
 & -\left( Y_{u}^{ij} Q_{L}^{m\alpha i} u_{R}^{( c) mj} \epsilon _{\alpha \beta } H^{\beta } +Y_{d}^{ij} Q_{L}^{m\alpha i} d_{R}^{( c) mj} H_{\alpha }^{*} +Y_{e}^{ij} L_{L}^{m\alpha i} e_{R}^{( c) mj} H_{\alpha }^{*} +\text{ h.c. }\right)
\end{aligned}
$$

	- Notations for different parts of the symmetry
	  collapsed:: true
		- Write the indices as $Q_L^{m a i}$, where
		  $$
		  \begin{array}{lll}
		  m, n, \cdots=1,2,3 & \text { are } & S U(3)_c \text { indices } \\
		  \alpha, \beta, \cdots=1,2 & \text { are } & S U(2)_W \text { indices } \\
		  i, j, \cdots=1,2,3 & \text { are } & \text { generation indices } .
		  \end{array}
		  $$
		- $$
		  Q_L^{m \alpha i} \rightarrow U^m{ }_n S^\alpha{ }_\beta e^{-i Y \theta} Q_L^{n \beta i}
		  $$
	- The first line contains kinetic terms of gauge bosons.
	- The second line is the Higgs boson.
	- The third line contains kinetic terms of fermions.
		- All three indices $m,\alpha,i$ should be summed in the line.
		- Note that they are all massless since chirality only allows them have majorana mass, but they have nonzero hypercharge, so majorana mass terms are forbidden.
	- The last line contains Yukawa couplings.
		- Notation
			- The $Y$s are the matrices of coupling constants.
			- $(c)$ means that the fields are conjugated, which flips the charges.
			- $\chi \psi \equiv \chi^T \epsilon \psi$ is Lorentz invariant for two left-handed Weyl spinors. Here we just replace $\chi, \psi \rightarrow Q_L, u_R^c$.
		-
		- Note that we either needs $\epsilon_{\alpha \beta}$ or complex conjugation to obtain $SU(2)$ and $SU(3)$ invariant terms.
			- The former is invariant itself.
			- The latter provides the complex conjugation needed in the $\dagger$.
- # General procedure to write down a model
	- ## Specify symmetries
	  collapsed:: true
		- Spacetime
			- It must be Poincare symmetry.
		- Gauge
			- The gauge symmetry turns out to be
			  $$
			  S U(3)_c \times S U(2)_W \times U(1)_Y
			  $$
				- $c,W,Y$ stands for color, weak and hypercharge respectively.
		- Global
			- No global symmetry is imposed in SM.
	- ## Specify fields and corresponding reps
	  collapsed:: true
		- Spinor
			- In SM the fields are
			  collapsed:: true
			  $$
			  \begin{aligned}
			  Q_L^i & \sim(3,2)_{+\frac{1}{6}} \\
			  u_R^i & \sim(3,1)_{+\frac{2}{3}}, \\
			  d_R^i & \sim(3,1)_{-\frac{1}{3}}, \\
			  L_L^i & \sim(1,2)_{-\frac{1}{2}}, \\
			  e_R^i & \sim(1,1)_{-1},
			  \end{aligned}
			  $$
				- $L,R$ denotes the helicity.
				- $i \in \{1,2,3\}$ labels the **generation** of the fermions.
					- Different generations have different masses. They **do not** mix under actions of gauge groups.
				- The first number labels the representation of $SU(3)_c$.
					- 3 means the fundamental rep and 1 means the trivial rep.
					- The trivial rep means that it doesn't participate in the strong interaction.
				- The first number labels the representation of $SU(2)_W$.
					- 2 means the fundamental rep and 1 means the trivial rep.
				- The last number labels $U(1)_Y$, which is not $U(1)_EM$. The number is the charge.
		- Scalar
			- Only one complex scalar $H$ (Higgs boson) in SM.
			- The rep is
			  $$
			  H \sim(1,2)_{+\frac{1}{2}}
			  $$
		- Vector
		  collapsed:: true
			- In SM there are only gauge vector fields. No additional ones.
	- ## Write down allowed terms
		- The terms need to be Lorentz-invariant, satisfy the the symmetries, and be renormalizable.
		- It turned out that allowed terms in SM are
		  ((65475c6a-e2eb-4bb8-9932-3a87bdc6986e))
	- ## Determine SSB
	-
- # Electroweak Symmetry Breaking
	- Definitions
		- $$
		  \tan \theta_W \equiv \frac{g^{\prime}}{g}
		  $$
		- ((654892d0-cad6-49fc-ae81-48a6e4d143d4))
		- $$
		  T_a=\frac{\sigma_a}{2}, Y=\frac{1}{2}
		  $$
		- $$
		  U(\alpha_a,\theta)=e^{-i\left(\alpha_a T_a+\theta Y \mathbb{1}_2\right)}
		  $$
	- Summary
	  collapsed:: true
		- The Higgs boson breaks the $SU(2)_W$ symmetry spontaneously.
			- Note that it doesn't participate in the strong interaction.
		- Then the three $SU(2)_W$ gauge fields plus the $U(1)$ gauge field would become three massive vector fields, plus one massless vector field -- the photon!
		- The remaining $U(1)_{EM}$ is a **mix** of $SU(2)_W$ and $U(1)_Y$.
			- ((65489450-a294-432c-9173-1b756dbaede5))
			- We can obtain electric charges of different fields from their transformations rules under $U(1)_{EM}$.
		- The fermions would obtain masses after EWSB through Yukawa interactions in SM (the last line in the Lagrangian).
	- Step 1. Determine the actual vacuum.
	  collapsed:: true
		- Consider the Higgs part in the SM Lagrangian,
		  $$
		  \left(D_\mu H\right)^{\dagger}\left(D^\mu H\right)-m^2 H^{\dagger} H-\lambda\left(H^{\dagger} H\right)^2
		  $$
		- As usual, denote $v=\sqrt{\frac{-m^2}{\lambda}}$, then
		  $$
		  \langle H\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{l}
		  0 \\
		  v
		  \end{array}\right)
		  $$
		- Choose the unitary gauge and remove the $\pi$ fields, we obtain
		  $$
		  H=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
		  0 \\
		  v+h
		  \end{array}\right)
		  $$
		- Note that the symmetry breaking pattern is $SU(N) \to SU(N-1)$, thus here the whole $SU(2)$ is completely broken.
	- Step 2. Find out masses of gauge bosons.
	  collapsed:: true
		- Now we should consider a bit more terms,
		  $$
		  \mathcal{L}=-\frac{1}{4} W_{a, \mu \nu} W_a^{\mu v}-\frac{1}{4} B_{\mu \nu} B^{\mu \nu}+\left(D_\mu H\right)^{\dagger}\left(D^\mu H\right)-m^2 H^{\dagger} H-\lambda\left(H^{\dagger} H\right)^2
		  $$
		- Find the mass terms
		  collapsed:: true
			- The mass terms originate from the covariant derivatives $\left(D_\mu H\right)^{\dagger}\left(D^\mu H\right)$,
			  $$
			  \frac{1}{\sqrt{2}}\left(\begin{array}{ll}
			  0 & v
			  \end{array}\right)\left[-i g \frac{\sigma_a}{2} W_{a, \mu}-i g^{\prime} \frac{1}{2} B_\mu \mathbb{1}_2\right]\left[i g \frac{\sigma_a}{2} W_a^\mu+i g^{\prime} \frac{1}{2} B^\mu \mathbb{1}_2\right] \frac{1}{\sqrt{2}}\left(\begin{array}{l}
			  0 \\
			  v
			  \end{array}\right)
			  $$
				- $W$ denotes the $SU(2)_Y$ gauge fields and $B$ denotes the $U(1)_Y$ gauge field.
			- Expand the previous expression into indices, we get
			  $$
			  \left(D_\mu H\right)^{\dagger}\left(D^\mu H\right) \supset \frac{v^2}{8} g^2\left(W_{1, \mu}+i W_{2, \mu}\right)\left(W_1^\mu-i W_2^\mu\right)+\frac{v^2}{8}\left(g W_3^\mu-g^{\prime} B^\mu\right)^2
			  $$
				- Specifically, we expand
				  $$
				  g \frac{\sigma_a}{2} W_a^\mu+g^{\prime} \frac{1}{2} B^\mu=\frac{1}{2}\left(\begin{array}{cc}
				  g W_3^\mu+g^{\prime} B^\mu & g\left(W_1^\mu-i W_2^\mu\right) \\
				  g\left(W_1^\mu+i W_2^\mu\right) & -g W_3^\mu+g^{\prime} B^\mu
				  \end{array}\right)
				  $$
		- #+BEGIN_NOTE
		  We have three mass terms: $W_1$ and $W_2$ get the same mass respectively, while $W_3$ needs to combine with $B$ to obtain mass.
		  #+END_NOTE
		- Redefine the fields
			- id:: 654892d0-cad6-49fc-ae81-48a6e4d143d4
			  $$
			  \begin{aligned}
			  W^{ \pm \mu} & =\frac{1}{\sqrt{2}}\left(W_1^\mu \mp i W_2^\mu\right) \\
			  Z^\mu & =\frac{g W_3^\mu-g^{\prime} B^\mu}{\sqrt{g^2+g^{\prime 2}}}
			  \end{aligned}
			  $$
				- $W^\pm$ is defined in a manner such that they are charge eigenstates.
				- $Z$ is rescaled to be canonically normalized.
			- The mass terms then become
			  $$
			  \frac{g^2 v^2}{4} W_\mu^{-} W^{+\mu}+\frac{1}{2}\left(g^2+g^{\prime 2}\right) \frac{v^2}{4} Z_\mu Z^\mu \equiv m_W^2 W_\mu^{-} W^{+\mu}+\frac{1}{2} m_Z^2 Z_\mu Z^\mu
			  $$
		- Find out the massless vector field
			- Note that there are 4 gauge fields, while we only have 3 massive ones above.
			- Redefine
			  $$
			  \left(\begin{array}{c}
			  Z^\mu \\
			  A^\mu
			  \end{array}\right)=\left(\begin{array}{cc}
			  c_w & -s_w \\
			  s_w & c_w
			  \end{array}\right)\left(\begin{array}{c}
			  W_3^\mu \\
			  B^\mu
			  \end{array}\right)
			  $$
			- Then apparently $A^\mu$ is massless. As implied by the name, it would be the EM field.
			- Note that
			  $$
			  \frac{m_W}{m_Z}=\cos \theta_W
			  $$
	- Summary of DOFs:
	  $$
	  \begin{array}{cc|ccc}
	  \text { before SSB } & \text { d.o.f. } & \text { after SSB } & \text { d.o.f. } \\
	  \hline H & 4 & h & 1 & \\
	  \text { massless } W_a^\mu, a=1,2,3 & 2 \times 3 & \text { massive (complex) } W^{ \pm \mu} & 3 \times 2 & m_W=\frac{1}{2} g v \\
	  \text { massless } B^\mu & 2 & \text { massive } Z^\mu & 3 & m_Z=\frac{1}{2 c_w} g v \\
	  & & \text { massless } A^\mu & 2 &
	  \end{array}
	  $$
	- Step 3. Find out $U(1)_{EM}$
		- Write down the unbroken $U(1)_{EM}$ symmetry
			- Under a general $S U(2)_W \times U(1)_Y$ transformation, we have
			  $$
			  \langle H\rangle=\left(\begin{array}{c}
			  0 \\
			  \frac{v}{\sqrt{2}}
			  \end{array}\right) \rightarrow e^{-i\left(\alpha_a T_a+\theta Y \mathbb{1}_2\right)}\left(\begin{array}{c}
			  0 \\
			  \frac{v}{\sqrt{2}}
			  \end{array}\right)=e^{-\frac{i}{2}\left(\alpha_a \sigma_a+\theta \mathbb{1}_2\right)}\left(\begin{array}{c}
			  0 \\
			  \frac{v}{\sqrt{2}}
			  \end{array}\right),
			  $$
			- Thus only when
			  $$
			  \alpha_1=\alpha_2=0, \quad \alpha_3=\theta
			  $$
			  would we have $\langle H \rangle$ invariant under the transformation.
				- The corresponding generator is
				  $$
				  \frac{1}{2}\left(\sigma_3+\mathbb{1}_2\right)=\left(\begin{array}{ll}
				  1 & 0 \\
				  0 & 0
				  \end{array}\right)
				  $$
			- Therefore, the unbroken gauge transformation is
			  id:: 65489450-a294-432c-9173-1b756dbaede5
			  $$
			  Q=T_3+Y \mathbb{1}_2
			  $$
			  which is the generator of $U(1)_{EM}$!
		- We can check the electric charges of different fermions (quarks and leptons) by investigating their transformations under $Q$:
			- Note that quarks and leptons are both in the fundamental representation of $SU(2)$. They differ by the rep of $SU(3)$.
			- $$
			  \begin{aligned}
			  & Q Q_L=\left(\begin{array}{cc}
			  \frac{1}{2}+\frac{1}{6} & \\
			  & -\frac{1}{2}+\frac{1}{6}
			  \end{array}\right)\left(\begin{array}{l}
			  u_L \\
			  d_L
			  \end{array}\right)=\left(\begin{array}{ll}
			  \frac{2}{3} & \\
			  & -\frac{1}{3}
			  \end{array}\right)\left(\begin{array}{l}
			  u_L \\
			  d_L
			  \end{array}\right) \\
			  & Q L_L=\left(\begin{array}{ll}
			  \frac{1}{2}-\frac{1}{2} & \\
			  & -\frac{1}{2}-\frac{1}{2}
			  \end{array}\right)\left(\begin{array}{l}
			  \nu_L \\
			  e_L
			  \end{array}\right)=\left(\begin{array}{ll}
			  0 & \\
			  & -1
			  \end{array}\right)\left(\begin{array}{l}
			  \nu_L \\
			  e_L
			  \end{array}\right)
			  \end{aligned}
			  $$
			- This reproduces the familiar result that quarks have electric charges $2/3$ and $1/3$, the neutrino is neutral, and the electron has electric charge $-1$.
		- Find out the covariant derivative
		  collapsed:: true
			- Expand
			  $$
			  D^\mu=\partial^\mu+i g T_a W_a^\mu+i g^{\prime} Y B^\mu
			  $$
				- $$
				  \begin{aligned}
				  D^\mu & =\partial^\mu+i g\left(T_{+} W^{+\mu}+T_{-} W^{-\mu}\right)+i \frac{1}{\sqrt{g^2+g^{\prime 2}}} Z^\mu\left(g^2 T_3-g^{\prime 2} Y\right)+i \frac{g g^{\prime}}{\sqrt{g^2+g^{\prime 2}}} Q A^\mu \\
				  & =\partial^\mu+i g\left(T_{+} W^{+\mu}+T_{-} W^{-\mu}\right)+i \frac{g}{c_w} Z^\mu\left(T_3-s_w^2 Q\right)+i e Q A^\mu
				  \end{aligned}
				  $$
					- Note that $c_w \equiv \cos \theta_W, s_w \equiv \sin \theta_W$, $T_{ \pm}=\frac{1}{\sqrt{2}}\left(T_1 \pm i T_2\right)$, $e \equiv \frac{g g^{\prime}}{\sqrt{g^2+g^{\prime 2}}}$.
			-
			- Since $W^\pm$ and $Z$ are massive ($m_Z \approx 91.2 \mathrm{GeV}$ and $m_W=80.4 \mathrm{GeV}$), they **can be ignored** at low energy.
			- Thus we obtain our familiar covariant derivative in QED,
			  $$
			  D^\mu=\partial^\mu+i e Q A^\mu
			  $$
			-
-