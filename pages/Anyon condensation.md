# Mathematical Description
	- ## Condensable bosons
	  id:: 63d873f9-1041-49a2-8b5a-1908f8fa53a8
	  collapsed:: true
		- Requirement #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-04-06T01:21:34.482Z
		  card-last-reviewed:: 2023-03-13T01:21:34.482Z
		  card-last-score:: 5
			- $R_{a\bar a}^cR_{\bar a a}^c=1$ (bosonic) for **at least one** of the fusion channels of $a \otimes \bar a$
				- Note that it is the **double braiding**.
				- Why? #Learning-TODO
					- Maybe start from Wan's construction and derive a contradiction?
			-
	- ((63f2d3e0-cdbb-4ba7-b167-e079ee114330))
	- ### Three steps
	  collapsed:: true
		- **Identification**
		  id:: 63e86242-6b88-4bab-b3f1-36df62e80c0a
			- Identify the condensed anyon(s) $\{\gamma_i\}$ to the vacuum
			- Identify several anyons linked by the condensate (i.e. orbits) as well
				- How do we identify anyons in case of nonabelian condensates, which means 'orbits' are not simple? #Learning-TODO
		- **Splitting**
		  id:: 63e86242-da92-4498-9f19-ba410ca929fa
			- If $a \times \bar{a}=1+\gamma_i+\ldots$, then $a\times \bar a$ contains orthogonal copies of the condensate vacuum.
			- This means $a$ must split in the condensed phase.
		- **Confinement**
			- Only $a$ with **at least one channel** in $a \otimes \gamma_i$ having trivial double braiding can survive.
				- ((63db212c-55c2-4693-a5c8-bb5713898e44))
			- Also, if $N_{\gamma_i, \gamma_i}^c>0$ and $c$ is not a boson, then $c$ is confined in the condensed phase.
				- Note that it is related to the condition of ((63d873f9-1041-49a2-8b5a-1908f8fa53a8))
	- ((63db223b-823d-4c25-8301-f669a6ff09cd))
	- ## Simple case: Condensing an abelian anyon
		- That is, all fusion channels are simple, which is equivalent to $J \times \bar{J}=I$.
		- Condensable condition
			- $\theta_J=1$
		- ((63e86242-6b88-4bab-b3f1-36df62e80c0a))
			- The **orbit** of a particle type $a$ under the action of $J$ is the set of all particle types $b \in \mathcal{A}$ such that $b=J^p \times a$ for some integer $p$. We denote the orbit as $[a]^J$, or when it not ambiguous we just write $[a]$.
			- Obviously all particles in the same orbit are identified.
			- The orbits in the condensed theory will inherit fusion rules from the uncondensed theory.
		- ((63e86242-da92-4498-9f19-ba410ca929fa))
		  collapsed:: true
			- Orbits are not of maximum size implies splitting. #card
			  card-last-interval:: 24
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-03-20T01:41:24.658Z
			  card-last-reviewed:: 2023-02-24T01:41:24.660Z
			  card-last-score:: 5
				- Suppose $J^m \otimes a = a$, where $m<n$.
				- Then $J^m\otimes a \otimes \bar a=J^m \otimes (I+c_2+...+c_k)=I+c_2+...+c_k$
					- We have $k \geq 2$, otherwise we would have $J^m=I$.
				- That means $I,c_2,...,c_k$ are all in the same orbit.
				- Is the converse true?
				  background-color:: red
					- Equivalently, could maximal orbits split?
			- Therefore the orbit must split on the edge theory!
				- $a \rightarrow \sum_{i=1}^{q_a} n_i^a[a]_i$
				- The twist factors are $\theta_{[a]_i}=\theta_a$.
			- ((63f46e64-addc-45fb-899a-b713b1398657))
			- Note that we have not had confinement, i.e. we only have an edge theory without braiding here.
			- To have a consistent fusion rule with the original theory, $\left(\sum_{i=1}^{q_a} n_i^a[a]_i\right) \times\left(\sum_{i=1}^{q_b} n_i^b[b]_i\right)=\sum_c N_{a, b}^c\left(\sum_{i=1}^{q_c} n_i^c[c]_i\right)$
				- Prop. $\mathrm{d}_a=\sum_{i=1}^{q_a} n_i^a \mathrm{~d}_{[a]_i}$ #card #Learning-TODO
				  card-last-interval:: -1
				  card-repeats:: 1
				  card-ease-factor:: 2.5
				  card-next-schedule:: 2023-02-28T16:00:00.000Z
				  card-last-reviewed:: 2023-02-28T00:44:57.150Z
				  card-last-score:: 1
					- I can't prove it. Investigate it in a few examples?
			-
		- ### Confinement
		  collapsed:: true
			- Some anyons have nontrivial braidings with the condensed one, thus must be confined.
				- However they can survive on the edge theory, which has no braiding!
				- Physically, pulling the confined particles from the edge to the condensate costs an energy proportional to the distance. #Learning-TODO
			- Condition for allowed particles #card
			  card-last-interval:: 117.6
			  card-repeats:: 3
			  card-ease-factor:: 2.8
			  card-next-schedule:: 2024-04-08T14:52:05.604Z
			  card-last-reviewed:: 2023-12-13T00:52:05.604Z
			  card-last-score:: 5
				- $$R_{J \times a}^{a, J} R_{J \times a}^{J, a}=\frac{\theta_{J \times a}}{\theta_a}=1$$
					- Note that the condition concerns **double** braiding, which is physically observable.
				- The second line uses the fact that $R_c^{b a} R_c^{a b}=\frac{\theta_c}{\theta_a \theta_b}$.
			-
	- ## General Construction of Condensed Theories #card
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-08-14T19:09:53.583Z
	  card-last-reviewed:: 2023-07-14T13:09:53.583Z
	  card-last-score:: 3
		- [Boson Condensation in Topologically Ordered Quantum Liquids (arxiv.org)](https://arxiv.org/abs/1601.01320) #[[Research/To Be Investigated]]
		-
		- The central quantity is $M=n n^{T}$, where n is the rectangular matrix in splitting defined by $a \rightarrow \sum_{i=1}^{q_a} n_i^a[a]_i$, but only including the **deconfined** particles.
			- $n$ not necessarily a square matrix.
		- $[M, S]=[M, T]=0$
		- The condensed theory shall satisfy $S n=n S_{\text {condensed }} \quad T n=n T_{\text {condensed }}$
- # Topics
	- ## Boundaries and Gappability
	  collapsed:: true
		- If the central charge is nonzero, then the edge must carry heat and therefore gapless. But **not vice versa.**
		- ((63f5df0c-23b7-47b7-94d1-67355b1bd6f5))
			- ((63f5df67-c282-461b-bd71-fde7d5d37c40))
			- With lots of references!
		- However, the more general rule for gappability between two systems is **different**: #card
		  card-last-interval:: 25.01
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-04-09T00:39:23.934Z
		  card-last-reviewed:: 2023-03-15T00:39:23.935Z
		  card-last-score:: 5
			- The boundary between two topologically ordered systems $\mathcal{C}$ and $\mathcal{D}$ can only be gapped if the system $\mathcal{C} \times \overline{\mathcal{D}}$ can have a gapped edge to the trivial theory, i.e. if a set of bosons from $\mathcal{C} \times \overline{\mathcal{D}}$ can be condensed to give a topologically trivially ordered system.
			- Actually they might **not** be linked by condensation. The difference is that particles can pair up then condense to vacuum, which is different from condensing $C$ to obtain $D$.
				- This is different from [Burnell2018]([[2018_Burnell_Anyon condensation and its applications]]). But also some useful references and arguments there.
		- ((63dc6611-b249-4a6b-9d84-61424d5eb2b0))
	- ## Relations between the theories before and after #card
	  card-last-interval:: 107.52
	  card-repeats:: 3
	  card-ease-factor:: 2.56
	  card-next-schedule:: 2023-12-10T01:06:52.962Z
	  card-last-reviewed:: 2023-08-24T13:06:52.962Z
	  card-last-score:: 3
		- ((63f5d1a9-34d2-488d-b5d1-805be16af7a4))
		- The central charge (mod 8) isn't changed
		- The quantum dimensions are linked by 
		  $$
		  \frac{\mathcal{D}_{\mathcal{A}}}{\mathcal{D}_{\mathcal{T}}}=\frac{\mathcal{D}_{\mathcal{T}}}{\mathcal{D}_{\mathcal{U}}}
		  $$
		-
	- ## [[Coset Theories]]
		- The idea originated from TQFTs.
		- Essentially, when we construct a coset theory $G_k/H_{k'}$, we gauge the d.o.f. of the subgroup $H$.
		-
		- However, $G_k / H_{k^{\prime}}$ can be easily comprehended by condensing all simple bosons in $G_k \times \bar H_{k'}$
		-
	- ## Relation to Domain walls
		-
- # Examples
	- ## ((63da0e16-0074-496a-952b-bd3534890de6)): Double Ising to [[Toric Code]] condensation #card
	  collapsed:: true
	  card-last-interval:: 107.52
	  card-repeats:: 3
	  card-ease-factor:: 2.56
	  card-next-schedule:: 2023-11-15T00:31:30.005Z
	  card-last-reviewed:: 2023-07-30T12:31:30.005Z
	  card-last-score:: 3
		- Note: We choose double Ising rather than Ising because $s_\psi=-1$. Pair two $\psi$ cancels the sign.
		- Choose $\psi_1\psi_2$ as the anyon to be condensed.
			- Confined anyons
				- Note 'confined' = Nontrivial double braiding
				- $\sigma_1,\sigma_2,\psi\sigma,\sigma\psi$
			- Deconfined ones
				- $\psi_1,\psi_2,\sigma_1\sigma_2$
			- Determine the new phase
				- [Wan]([[2021_Hu_Huang_Wan_Anyon Condensation]])'s approach
					- Find out the $+1$ eigenvectors for all $W_n(\psi_1\psi_2)$
					- But splitting cannot be obtained?
				- $\sigma_1\sigma_2$ **splits** into two flavors to resolve $\tilde{\sigma} \times \tilde{\sigma}=\tilde{1}+\tilde{1}+\tilde{\psi}+\tilde{\psi}$.
		- Result
			- $\begin{aligned} \tilde{\psi} \times \tilde{\psi}=1, \quad \tilde{\psi} \times \tilde{\sigma}_e=\tilde{\sigma}_m, & \tilde{\psi} \times \tilde{\sigma}_m=\tilde{\sigma}_e \\ \tilde{\sigma}_e \times \tilde{\sigma}_e=\tilde{\sigma}_m \times \tilde{\sigma}_m=1, & \tilde{\sigma}_e \times \tilde{\sigma}_m=\tilde{\psi}\end{aligned}$
			- Just toric code!
		- Splitting is determined by 'violation of fusion rule', which is problematic. #Learning-TODO
		  background-color:: red
	- ### Condensing $\mathbb{Z}_8^{(3+1 / 2)}= SU(8)_1$
	  collapsed:: true
		- Setup
			- $p \times p^{\prime}=\left(p+p^{\prime}\right) \bmod 8$, $\theta_p=\exp \left[\frac{2 \pi i 7}{16} p^2\right]$
		- $\theta_4=0$, so $4$ is a boson with order 2.
		- Identification
			- Obviously all orbits are of maximal size. The intermediate theory is $Z_4$.
		- Confinement
			- Invoke $R_c^{b a} R_c^{a b}=\frac{\theta_c}{\theta_a \theta_b}$, we see {{cloze [1] and [3]}} are confined.
			- The remaining fusion rule is $[2] \times[2]=[0]$, which turn out to be {{cloze the semion}}!
		- Splitting
			- No need to split here.
	- ### Condensing $SU(2)_4$ #card
	  collapsed:: true
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-09-22T12:57:18.386Z
	  card-last-reviewed:: 2023-08-11T12:57:18.386Z
	  card-last-score:: 5
		- Setup
			- $$
			  \begin{array}{|c|cccc|}
			  \hline \times & 1 & 2 & 3 & 4 \\
			  \hline 1 & 0+2 & 1+3 & 2+4 & 3 \\
			  2 & 1+3 & 0+2+4 & 1+3 & 2 \\
			  3 & 2+4 & 1+3 & 0+2 & 1 \\
			  4 & 3 & 2 & 1 & 0 \\
			  \hline
			  \end{array}
			  $$
			- $$
			  \begin{array}{||c|l|l||}
			  \hline \text { particle } & \text { d } & \theta \\
			  \hline 0 & 1 & 1 \\
			  1 & \sqrt{3} & e^{2 \pi i / 8} \\
			  2 & 2 & e^{2 \pi i / 3} \\
			  3 & \sqrt{3} & e^{2 \pi i 5 / 8} \\
			  4 & 1 & 1 \\
			  \hline
			  \end{array}
			  $$
		- We condense the particle 4.
		- Identification
			- Identify 1 and 3.
		- Splitting
			- $2 \times 2=0+2+4$, thus $[2] \times [2]=[0]+[0]+[2]$. Splitting needed.
			- It is obvious that $[2]$ should split into two particle. The consistency relations (mainly associativity) of fusion rules gives the unique solution 
			  $$
			  \begin{array}{|c|ccc|}
			  \hline \times & {[1]} & {[2]_1} & {[2]_2} \\
			  \hline[1] & {[0]+[2]_1+[2]_2} & {[1]} & {[1]} \\
			  {[2]_1} & {[1]} & {[2]_2} & {[0]} \\
			  {[2]_2} & {[1]} & {[0]} & {[2]_1} \\
			  \hline
			  \end{array}
			  $$
		- Confinement
			- $1$ must be confined by calculating its double braiding.
		- Final result
			- ((63f4c021-3966-42c9-9ad3-50a2dc95fe3d))
	- ### Constructing $S U(2)_2 / U(1)_2$ #card
	  collapsed:: true
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-05-11T01:33:24.740Z
	  card-last-reviewed:: 2023-04-11T01:33:24.740Z
	  card-last-score:: 5
		- Setup
			- $SU(2)_2$ is [[Ising type]], with $\theta_{\sigma}=e^{2 \pi i 3 / 16}$
			- $\overline{U(1)_2}$
				- $$
				  \begin{aligned}
				  &\begin{array}{||c|c|l||}
				  \hline \text { particle } & \mathrm{d} & \theta \\
				  \hline 0 & 1 & 1 \\
				  1 & 1 & e^{2 \pi i 7 / 8} \\
				  2 & 1 & -1 \\
				  3 & 1 & e^{2 \pi i 7 / 8} \\
				  \hline
				  \end{array}\\
				  &i \times j=(i+j) \bmod 4
				  \end{aligned}
				  $$
		- Condensing $SU(2)_2 \times \overline{U(1)_2}$
			- The only nontrivial boson is $\psi \times 2$
			- All of the orbits are of maximal size.
			- The deconfined particles are $[I],[\psi\times 0],[\sigma\times 1]$
		- The final theory is equivalent to Ising, with $\theta_\sigma=e^{2\pi i \frac 1 {16}}$
		-
- # Comments
  collapsed:: true
	- ((63d87e90-19ca-426a-93d5-77c0b39eac21))
	- Why does the mathematical structure (not being first principles) fit so well with physics? #[[System/Math and Physics]]
		- Deeper structures behind?
	- ((63d8728e-64bc-4c90-aaf2-63efb1e11fac))
	- ((63d872bb-9d03-495a-8030-e76fb77eb849))
- # Misc
	- A critical point of the condensation
		- ((63aa5ee4-d8ac-4c34-aa3c-fe3a1d5c8ac9)) #Inbox/Problem
			- Can we obtain the exchange domain wall from the trivial one?
		- ((63a95e51-a8e4-4bd3-bc50-77ce4d2dd60f))
- [[Condensation Completeness]]