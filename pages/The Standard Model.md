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
			- In SM there are only gauge vector fields. No additional ones.
	- ## Write down allowed terms
	  collapsed:: true
		- Notation
			- $$\tilde{H}\equiv\epsilon H^*\sim(1\mathrm{~,~}2)_{-\frac12}$$
		- The terms need to be Lorentz-invariant, satisfy the the symmetries, and be renormalizable.
		- It turned out that allowed terms in SM are
		  ((65475c6a-e2eb-4bb8-9932-3a87bdc6986e))
	- ## Determine SSB
	-
- # Electroweak Symmetry Breaking
	- Definitions
	  collapsed:: true
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
			  id:: 65489294-0fbf-4ce2-b91c-98e3bb8575b5
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
	  collapsed:: true
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
	- The Higgs particle
	  collapsed:: true
		- It is a single scalar field in
		  $$
		  H=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
		  0 \\
		  v+h
		  \end{array}\right)
		  $$
		- Mass of the Higgs particle
		  collapsed:: true
			- Plug in
			  $$\mathcal{L}=(D_\mu H)^\dagger\left(D^\mu H\right)-V(H)$$
			- $$\begin{aligned}
			  V(H)& \begin{aligned}=m^2H^\dagger H+\lambda\left(H^\dagger H\right)^2\end{aligned}  \\
			  &=\lambda v^2h^2+\lambda vh^3+\frac\lambda4h^4+\text{ constant}
			  \end{aligned}$$
			- Therefore we can read off the mass
			  $$m_h =\sqrt{2\lambda}v$$
		- Interaction with gauge bosons
			- Trick: Refer the the [mass terms](((65489294-0fbf-4ce2-b91c-98e3bb8575b5))) of gauge bosons and substitute $v$ by $v+h$.
			-
		-
	- Custodial symmetry
	  collapsed:: true
		- Start from the tree-level relation
		  $$\frac{m_W}{m_Z}=\cos\theta_W=\frac g{\sqrt{g^2+g^{\prime2}}}$$
		- Note that when $g' \to 0$, we have $m_W=m_Z$. This is **not a coincidence**.
		-
		- The $O(4)$ global symmetry
		  collapsed:: true
			- Rewrite the fields as real fields, 
			  $$H=\dfrac{1}{\sqrt{2}}\begin{pmatrix}\phi_3+i\phi_4\\\\\phi_1+i\phi_2\end{pmatrix}$$
			- Then
			  $$\begin{aligned}
			  V(H)& \begin{aligned}=m^2H^+H+\lambda\left(H^+H\right)^2\end{aligned}  \\
			  &=\frac{m^2}2\left(\phi_1^2+\phi_2^2+\phi_3^2+\phi_4^2\right)+\frac\lambda4\left(\phi_1^2+\phi_2^2+\phi_3^2+\phi_4^2\right)^2
			  \end{aligned}$$
			  which obviously have a $O(4)$ symmetry.
		- The $O(3)$ symmetry and the custodial symmetry
		  collapsed:: true
			- $$\begin{aligned}&1\\\\&\langle\Phi\rangle=\begin{pmatrix}v\\0\\0\\0\end{pmatrix}\end{aligned}$$
			- Apparently there is still a remaining $O(3)$ symmetry.
		- This explains why $W_{1,2,3}^{\mu}$ have the same mass when $g' \to 0$. However, the symmetry is broken by the Yukawa interactions.
	- Neutral and charged currents
	  collapsed:: true
		- Interaction between fermions and gauge bosons
			- Start from the kinetic terms
			  $$i\bar{L}_{L}\not D L_{L}+i\bar{e}_{R} \not De_{R}$$
			- Expand the covariant derivatives and redefine some terms, we find
			  $$\mathcal{L}_{\mathrm{int}}\equiv-\frac{g}{\sqrt{2}}\left(W_{\mu}^{+}J_{+}^{\mu}+W_{\mu}^{-}J_{-}^{\mu}\right)-\frac{g}{c_{w}}Z_{\mu}J_{Z}^{\mu}-eA_{\mu}J_{EM}^{\mu}$$
				- $$D^{\mu}=\partial^{\mu}+igT_{a}W_{a}^{\mu}+ig'YB^{\mu}$$
				- Here we only consider the $SU(2)_W$ and $U(1)_Y$. Each gauge group would correspond to a gauge field in the covariant derivative.
			- After including all quarks, the complete form is
			  $$\begin{aligned}
			  J_{+}^{\mu}& \begin{aligned}=\bar{\nu}_{L}^{i}\gamma^{\mu}e_{L}^{i}+\bar{u}_{L}^{\color{red}{i}}\gamma^{\mu}d_{L}^{\color{red}{i}},\end{aligned}  \\
			  J\underline{\mu}& =\left.\bar{e}_{L}^{\color{red}{i}}\gamma^{\mu}\nu_{L}^{\color{red}{i}}+\bar{d}_{L}^{\color{red}{i}}\gamma^{\mu}u_{L}^{\color{red}{i}}\right.,  \\
			  J_{Z}^{\mu}& =\left.\bar{\nu}_L^i\gamma^\mu\frac12\nu_L^i+\bar{e}_L^i\gamma^\mu\left(-\frac12+s_w^2\right)e_L^i+\bar{e}_R^i\gamma^\mu s_w^2e_R^i\right.  \\
			  &+\bar{u}_{L}^{\color{red}{i}}\gamma^{\mu}\left(\frac12-\frac23s_{w}^{2}\right)u_{L}^{\color{red}{i}}+\bar{u}_{R}^{\color{red}{i}}\gamma^{\mu}\left(-\frac23s_{w}^{2}\right)u_{R}^{\color{red}{i}} \\
			  &+\bar{d}_{L}^{i}\gamma^{\mu}\left(-\frac12+\frac13s_{w}^{2}\right)d_{L}^{i}+\bar{d}_{R}^{i}\gamma^{\mu}\left(\frac13s_{w}^{2}\right)d_{R}^{i}, \\
			  J_{EM}^{\mu}& =-\bar{e}^i\gamma^\mu e^i+\frac23\bar{u}^i\gamma^\mu u^i-\frac13\bar{d}^i\gamma^\mu d^i, 
			  \end{aligned}$$
		- Since the term must be invariant under $U(1)_{EM}$, we can deduce the charges of multiple currents: $J_+$ must have charge $-1$, $J_-$ must have charge $+1$, and the remaining two are neutral.
		-
		-
	- ## Fermion Masses
		- The masses come from the Yukawa interaction after EWSB.
		- Derivation of masses
		  collapsed:: true
			- Treat two components of the $SU(2)$ doublets as different fields,
			  collapsed:: true
			  $$Q_L=\begin{pmatrix}u_L\\\\d_L\end{pmatrix},\quad L_L=\begin{pmatrix}\nu_L\\\\e_L\end{pmatrix},\quad H=\frac1{\sqrt2}\begin{pmatrix}0\\v+h\end{pmatrix}$$
				- This is necessary since EWSB breaks $SU(2)$ symmetry and requires treating different components separately.
			- Then we have
			  collapsed:: true
			  $$\begin{aligned}
			  -\mathcal{L}_{\mathrm{Yukawa}}=& m_{u}^{\color{red}{ij}}\bar{u}_{L}^{\color{red}{i}}u_{R}^{\color{red}{j}}+m_{d}^{\color{red}{ij}}\bar{d}_{L}^{\color{red}{i}}d_{R}^{\color{red}{j}}+m_{e}^{\color{red}{ij}}\bar{e}_{L}^{\color{red}{i}}e_{R}^{\color{red}{j}}  \\
			  &+\frac{\color{red}{y_u^{ij}}}{\sqrt{2}}h\bar{u}_L^iu_R^j+\frac{\color{red}{y_d^{ij}}}{\sqrt{2}}h\bar{d}_L^id_R^j+\frac{\color{red}{y_e^{ij}}}{\sqrt{2}}h\bar{e}_L^ie_R^j+\mathrm{h.c.}
			  \end{aligned}$$
				- Note that the generation indices are still present, which are to be diagonalized.
				- $$m_u^{\color{red}{ij}}=\frac{y_u^{\color{red}{ij}}v}{\sqrt{2}},\quad m_d^{\color{red}{ij}}=\frac{y_d^{\color{red}{ij}}v}{\sqrt{2}},\quad m_e^{\color{red}{ij}}=\frac{y_e^{\color{red}{ij}}v}{\sqrt{2}}$$
			- The matrices could be diagonalized by SVD:
			- After some algebra and redefinitions, we arrive at
			  collapsed:: true
			  $$\begin{aligned}
			  -L_{\text{fermion mass}}= m_u\bar{u}_Lu_R+m_c\bar{c}_Lc_R+m_t\bar{t}_Lt_R  \\
			  +m_d\bar{d}_Ld_R+m_s\bar{s}_Ls_R+m_b\bar{b}_Lb_R \\
			  +m_e\bar{e}_Le_R+m_\mu\bar{\mu}_L\mu_R+m_\tau\bar{\tau}_L\tau_R+\mathrm{h.c.}
			  \end{aligned}$$
				- Notes
					- This is **not** diagonalization (though we can do this in principle). The point is to find a suitable paring of LH fermions with RH ones, thus the fermions would obtain **Dirac mass**.
					- $u,c,t$ are just names for redefined fields (mix of different generations),
					  $$\begin{pmatrix}u_L^1\\\\u_L^2\\\\u_L^3\\\end{pmatrix}=L_u\begin{pmatrix}u_L\\c_L\\t_L\end{pmatrix},\quad\begin{pmatrix}u_R^1\\\\u_R^2\\\\u_R^3\end{pmatrix}=R_u\begin{pmatrix}u_R\\\\c_R\\\\t_R\end{pmatrix}$$
				- Similarly,
				  $$\begin{pmatrix}d_L^1\\\\d_L^2\\\\d_L^3\end{pmatrix}=L_d\begin{pmatrix}d_L\\\\s_L\\\\b_L\end{pmatrix},\quad\begin{pmatrix}d_R^1\\\\d_R^2\\\\d_R^3\end{pmatrix}=R_d\begin{pmatrix}d_R\\\\s_R\\\\b_R\end{pmatrix}$$
			- #+BEGIN_NOTE
			  Most of our masses (those of protons and neutrons) come from QCD effects instead of EWSB.
			  #+END_NOTE
		- CKM matrix
		  collapsed:: true
			- Note that the forms of interactions (currents) would be changed by the field redefinitions.
			- Charged current
				- $$
				  \mathcal{L}_{W \text {-quarks }}=-\frac{g}{\sqrt{2}} W_\mu^{+} \bar{u}_L^i \gamma^\mu d_L^i+\text { h.c. }
				  $$
				- $$
				  \begin{aligned}
				  \mathcal{L}_{W \text {-quarks }} & =-\frac{g}{\sqrt{2}} W_\mu^{+}\left(\begin{array}{lll}
				  \bar{u}_L & \bar{c}_L & \bar{t}_L
				  \end{array}\right) L_u^{\dagger} \gamma^\mu L_d\left(\begin{array}{c}
				  d_L \\
				  s_L \\
				  b_L
				  \end{array}\right)+\text { h.c. } \\
				  & \equiv-\frac{g}{\sqrt{2}} W_\mu^{+}\left(\begin{array}{lll}
				  \bar{u}_L & \bar{c}_L & \bar{t}_L
				  \end{array}\right) \gamma^\mu V_{C K M}\left(\begin{array}{l}
				  d_L \\
				  s_L \\
				  b_L
				  \end{array}\right)+\text { h.c. }
				  \end{aligned}
				  $$
				- $$V_{CKM}:=L_u^\dag L_d$$
			- Leptons
				- Note that if neutrinos have zero masses, the mass eigenstates could be arbitrarily selected and the CKM matrix could always be chosen to be diagonal.
				- The basis where the lepton CKM matrix is diagonal is called the **flavor basis**.
					- Even if they have masses.
					  In that case the flavor basis states would not be mass eigenstates.
			- Neutral current
				- They are of the form
				  $$
				  J_Z^\mu=\bar{\psi}_i \gamma^\mu\left(T_3-Q s_w^2\right) \psi_i, \quad J_{E M}^\mu=Q \bar{\psi}_i \gamma^\mu \psi_i
				  $$
				  i.e. left-side and right-side fermions are the same.
				- Therefore any rotations would cancel.
	- Neutrino mass
		- We have different ways to have nonzero neutrino masses.
		- The simplest way is to introduce an extra particle.
			- Yukawa interaction and EWSB gives the Dirac mass.
			- We could also have majorana mass, since neutrinos are neutral!