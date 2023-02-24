type:: paper_reading

- ![Simon_Topological Quantum.pdf](file://zotero_link/Physics/Topological order/Intros and Reviews/Simon_Topological Quantum.pdf)
-
-
- # ((63c2176e-689e-4871-9dcb-d820669e68ac))
  collapsed:: true
	- ### ((63c21788-4217-4cb3-8a20-099a3cfa23ba)) ; Diagrams and Physical Quantities #card
		- Define toric code by local dancing rules (similar to 2017_Wen)
			- Isotopy, adding/removing contractable loops, reconnection
		- Strange operation: Detect the total charge of a disk of [[Toric Code]] by an annulus surrounding it
			- #+BEGIN_NOTE
			  The name 'Tube' originated from its topology, which is the same as an annulus.
			  #+END_NOTE
			- **This is a bit mysterious... almost a bulk-boundary relation.**
			- Set the stage
				- We don't specify the details of the lattice.
				- We use the spin-up and spin-down basis and represent them by blue lines and nothing separately.
			- Idea
				- First, the presence of e charge can be detected by a nontrivial string
				- The presence of m charge can be detected by the phase difference between the trivial homotopy type on the annulus and the nontrivial loop
			- Details: Projectors
				- The subscripts denote the particle types.
				- ((63c24f08-74e0-47d7-8c28-bf0217916833))
				- ((63c24f10-c712-4262-860c-c34cdf9a69a1))
			- More properties
				- Annuli can be multiplied.
					- The annulus to be multiplied must both have or both not have strings connecting the boundaries.
					- The loops are multiplied mod 2.
				- We may define a [[Anyon Basis]] for the torus.
				  collapsed:: true
					- Two points of view
						- Obtain a certain element from the trivial element by running the anyon
						- Glue two boundaries of the annulus (and multiply the strings) to obtain a ground state.
							- The 'anyon' is the charge detected by the string configuration on the annulus.
				- Determine the [[Twist]] of the anyons
				  id:: 63c2532f-fd97-4a25-86ac-27fc600589ee
				  collapsed:: true
					- ((63c25463-4c00-47de-8b21-3c9b5f2740ef)) (Dehn twist)
					-
					- For I and e, a rotation for a whole round is certainly trivial.
					- For m and f, ((63c25382-8f46-4fd5-973a-ae5042a11520))
					- Thus $\theta_m=1, \theta_f=-1$
					- **There got to be something deeper inside.**
				- Determine the [[S-matrix]]
				  collapsed:: true
					- ((63c2552b-3d48-4a77-9891-ca7aca3817a7))
					- Making a basis transformation, we obtain our familiar S-matrix!
		- Generalization: Determine general braidings and fusions by a **double-punctured disk**
		  collapsed:: true
			- [[Braiding]]
				- ((63c25660-8f63-48ee-b221-4ecceea3314b))
					- $f \otimes f$
				- Then use the three moves to simplify the lower line
			- [[Fusion]]
				- Essentially merging the holes
				- ((63c25681-7b53-4c30-99c8-9af8bd2fda8a))
					- $e \otimes f$
		- **Also easily generalizable to other string-net models!**
			- There is an example of $Z_n$ on topobook
		- ((63c24f85-b229-4920-88cf-78b0207f7682))
			- There are two sets of solutions to the hexagons of the $Z_2$ planar algebra
- # ((63c356c2-2dfd-480e-a0a4-49e6db63d25f))
  collapsed:: true
	- Quantum Double
	- [[Double Semion Model]]
	- [[Levin-Wen Model]]
		- Seems to be directly motivated from planar algebras?
		- # Setup #card
		  collapsed:: true
			- ## Fat Lattice
				- Trivalent, with a direction on each edge
					- Why does the lattice need to be trivalent? #Learning-TODO
						- Fusion multiplicity is also defined for multiple particles fusion together
				- Each edge is labeled by a simple object of the input tensor category
					- Reversing the direction of an edge changes the particle to its dual
						- ((63e85270-994b-4bc9-b5b0-621fe43c45f2))
				- In the middle of each plaquette there is a $\times$, which indicates we cannot contract loops on the plaquettes.
			- ## Hamiltonian
			  collapsed:: true
				- $H=-\sum_v A_v-\sum_p B_p$
				- Vertex operators enforce the fusion rules, i.e. $A_v=1$ iff $\left(N_{a b c}=N_{a b}^{\bar{c}}>0\right)$
				- Plaquette operators add $\tilde \Omega$ loops on the plaquette
					- ((63e85457-40a3-4f6a-9c79-3cdee0efc747))
						- The precise definition is as follows:
							- ((63f1dc64-debc-421e-b334-2cfc0e75207c))
								- ((63f1ddd2-9f0d-4e7e-a23b-94ab139e161f)) #card
									- Note that ((63f1ddff-4d6d-4e9c-8703-eeac52e3bfb5)), incoming particle as positive
							- Sum over all possible fusion channels.
						- ((63e85493-7abb-4406-95d9-6059dbada06e))
				- Proposition. $A_v^2=A_v,B_p^2=B_p, [A_v,B_p]=0$ #card
					- (1) is obvious.
					- (2) Let's prove the handle-slide property by explicitly writing the loop and using F-move (on the vacuum): ((63f1dfaa-c3ef-4c6a-8cac-1c5a9aafbdc8))
					- (3): Note that adding a loop keeps the fusion rule.
		- # Solution
			- ## Ground states
			  collapsed:: true
				- Note that we may freely use diagrammatic rules and contract loops in ground states. #card
				  collapsed:: true
					- Ground states are eigen to $B_p$. So we can first add a $\tilde \Omega$ by $B_p$, use the handle-slide property to move across the puncture, then remove the $\tilde \Omega$.
				- Prop. The ground space is topological. #card
					- Use a set of elementary moves. Prove invariance under each element of the set. #Strategy
					- ((63f1e575-e066-4e22-9614-a8f2a6fd2ab6))
						- Note that not only the quantum numbers are changed, but also the underlying lattice structure.
					- ((63f1e581-4ebb-4a66-85a3-0af2aa11c759))
						- Solve this as an exercise!
					- Use the moves to transform a square to a triangle as an exercise!
						- Simple exercise: ![Image(1).png](../assets/Image(1)_1676798114616_0.png)
						- Hard exercise: Try to add more plaquettes to a torus.
							- But here comes a question: How to define the discrete version of torus? #Learning-TODO
								- It should actually be a [[Triangulation]], involving simplices
				- The ground space is nondegenerate on a sphere. #card
					- Prove this by investigating a minimal lattice!
			- ## Quasiparticles
				- General constructions of quasiparticles can be difficult, but easier for a braided input category.
			- String operators can be found in [topobook](((63f2ce3a-202d-4bb4-8c39-a923cda51c6e))).
		- # Examples
			- ## ((63f2cb2c-5abf-4881-bac9-403813ff05dd))
				- Diagrammatic rules
					- ((63f2cc10-b805-49a9-8d6d-370366dd60ad))
					- The first two are F-move.
					- The third is the quantum dimension. The last is the so called 'quantum dimension'.
				- The twists and braidings can be obtained by diagrammatic rules.
				- As an exercise, determine the GSD on a torus. #card
					- The answer is four. The theory is indeed doubled.
				- As another exercise, find out the S-matrix. #card
					- $$
					  S=\frac{1}{\mathcal{D}}\left(\begin{array}{ll}
					  1 & \phi \\
					  \phi & y
					  \end{array}\right)
					  $$
					- Solve by F-move and R-move. Not so hard.
					- Don't forget the prefactor for a unitary S-matrix!
		-
- # ((63f5d393-9003-4c31-b6de-5dc05564fdec))
- # ((63f5d3a0-24c4-49f6-bbd6-905c87ee21f8))
- # ((63f2cf5d-e5e1-423f-9ad7-90214e40392f))
  collapsed:: true
	- ((63f2d3e0-cdbb-4ba7-b167-e079ee114330))
	- Would splitting always lead to anyon permuting symmetry?
	- ## Simple case: Condensing an abelian anyon
	  collapsed:: true
		- That is, all fusion channels are simple, which is equivalent to $J \times \bar{J}=I$.
		- Condensable condition
			- $\theta_J=1$
		- ### Identification
		  collapsed:: true
			- The **orbit** of a particle type $a$ under the action of $J$ is the set of all particle types $b \in \mathcal{A}$ such that $b=J^p \times a$ for some integer $p$. We denote the orbit as $[a]^J$, or when it not ambiguous we just write $[a]$.
			- Obviously all particles in the same orbit are identified.
			- The orbits in the condensed theory will inherit fusion rules from the uncondensed theory.
			- #### Simpler case: All orbits are of maximal size, i.e. the order of $J$.
		- ### Confinement
			- Some anyons have nontrivial braidings with the condensed one, thus must be confined.
				- However they can survive on the edge theory, which has no braiding!
				- Physically, pulling the confined particles from the edge to the condensate costs an energy proportional to the distance. #Learning-TODO
			- Condition for allowed particles #card
				- $R_{J \times a}^{a, J} R_{J \times a}^{J, a}=\frac{\theta_{J \times a}}{\theta_a}=1$
				- The second line uses the fact that $R_c^{b a} R_c^{a b}=\frac{\theta_c}{\theta_a \theta_b}$.
			-
		- ### Splitting
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
			- Consequences
				- To have a consistent fusion rule with the original theory, $\left(\sum_{i=1}^{q_a} n_i^a[a]_i\right) \times\left(\sum_{i=1}^{q_b} n_i^b[b]_i\right)=\sum_c N_{a, b}^c\left(\sum_{i=1}^{q_c} n_i^c[c]_i\right)$
					- Prop. $\mathrm{d}_a=\sum_{i=1}^{q_a} n_i^a \mathrm{~d}_{[a]_i}$ #card #Learning-TODO
						- I can't prove it. Investigate it in a few examples?
	- ## [[Coset Theories]]
		- The idea originated from TQFTs.
		- Essentially, when we construct a coset theory $G_k/H_{k'}$, we gauge the d.o.f. of the subgroup $H$.
		-
		- However, $G_k / H_{k^{\prime}}$ can be easily comprehended by condensing all simple bosons in $G_k \times \bar H_{k'}$
		-
	- ## Examples
	  collapsed:: true
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
			- Setup
				- $SU(2)_2$ is [[Ising type]], with $\theta_{\sigma}=e^{2 \pi i 3 / 16}$
				- $\overline{U(1)_2}$
				  collapsed:: true
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
	- ## Relations between the theories #card
	  collapsed:: true
		- ((63f5d1a9-34d2-488d-b5d1-805be16af7a4))
		- The central charge (mod 8) isn't changed
		- The quantum dimensions are linked by 
		  $$
		  \frac{\mathcal{D}_{\mathcal{A}}}{\mathcal{D}_{\mathcal{T}}}=\frac{\mathcal{D}_{\mathcal{T}}}{\mathcal{D}_{\mathcal{U}}}
		  $$
		-
	- ## General Construction of Condensed Theories #card
	  collapsed:: true
		- [Boson Condensation in Topologically Ordered Quantum Liquids (arxiv.org)](https://arxiv.org/abs/1601.01320) #[[Research/To Be Investigated]]
		-
		- The central quantity is $M=n n^{T}$, where n is the rectangular matrix in splitting defined by $a \rightarrow \sum_{i=1}^{q_a} n_i^a[a]_i$, but only including the **deconfined** particles.
			- $n$ not necessarily a square matrix.
		- $[M, S]=[M, T]=0$
		- The condensed theory shall satisfy $S n=n S_{\text {condensed }} \quad T n=n T_{\text {condensed }}$
	- ## Boundaries and Gappability
	  collapsed:: true
		- If the central charge is nonzero, then the edge must carry heat and therefore gapless. But **not vice versa.**
		- ((63f5df0c-23b7-47b7-94d1-67355b1bd6f5))
			- ((63f5df67-c282-461b-bd71-fde7d5d37c40))
			- With lots of references!
		- However, the more general rule for gappability between two systems is different:
			- The boundary between two topologically ordered systems $\mathcal{C}$ and $\mathcal{D}$ can only be gapped if the system $\mathcal{C} \times \overline{\mathcal{D}}$ can have a gapped edge to the trivial theory, i.e., if a set of bosons from $\mathcal{C} \times \overline{\mathcal{D}}$ can be condensed to give a topologically trivially ordered system.
			- Actually they might **not** be linked by condensation. The difference is that particles can pair up then condense to vacuum, which is different from condensing $C$ to obtain $D$.
				- This is different from [[2018_Burnell_Anyon condensation and its applications]]
- # ((63f6d9c3-7d19-4d5c-9c5c-3ac52297b388))
	- ## Relation to [[Anyon Condensation]]
		- ((63f6db13-324a-405f-a76a-0110f0aacaa6)).
		- ((63f6db1b-ee95-4073-a8f5-374de40ae98b))
	- ## Examples
		- Toric code: Exchange $e$ and $m$
			- Could be obtained by condensing $\text{Ising} \times \overline{\text{Ising}}$
			- Duality mapping
				- Map to the dual lattice to exchange $e$ and $m$
			- Equalizing mapping
			  collapsed:: true
				- ((63f6dc5b-cb2c-4479-b282-9adf540020c9))
				- A further transformation is needed: apply $\sigma_y$ on the east and west corners of the green diamonds, 
				  $$
				  \begin{aligned}
				  \sigma_x & \rightarrow \sigma_z \\
				  \sigma_z & \rightarrow \sigma_x \\
				  \sigma_y & \rightarrow \sigma_y
				  \end{aligned}
				  $$
				- **Plaquette and vertex operators are identified in the new lattice!**
					- $$
					  H_{\text {toric code }}=-\frac{\Delta}{2} \sum_{\text {diamonds } q} \sigma_z^{q_N} \sigma_x^{q_E} \sigma_z^{q_S} \sigma_x^{q_W}
					  $$
					- N,E,S,W are the directions
				- However, one can only move on the pink plaquettes while the other can only move on the green plaquettes.
					- Like the chessboards.
			- Dislocation defect and the exchange domain wall
				-