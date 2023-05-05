- Actually $Z_2$ [[Quantum Double]]
- # Solution
	- 4 ground states <-> 4 homotopy classes.
		- ((6368789c-5189-4377-a4a7-55516a81ee18))
		- ((636878d9-84fc-418a-a61c-90845774d77f))
	- Counting the ground state degeneracy
		- Total d.o.f: $F=2n^2$
		- Constraints: $E+V-2$
		- Free d.o.f. : $N=F-E-V+2=2g$
- # [[Topological skeleton]] of toric code #card
  collapsed:: true
  card-last-interval:: 30
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2023-05-13T11:42:34.937Z
  card-last-reviewed:: 2023-04-13T11:42:34.937Z
  card-last-score:: 5
	- ((63aa5b5b-1bd1-47bd-941c-a5c86a2fd734)) Invitation
	- A monoidal [[2-category]], denoted by $\mathbf{TC}$
		- Monoidal means the objects (1D domain walls) can be fused.
		- However, some objects aren't invertible? #Inbox/Problem
	- ((63aa5b9e-3d1c-450a-9877-4bc7b61b2766))
		- Objects -> Six simple domain walls
		- Black arrow -> Topo skeleton of the 1D domain walls
		- Red and bluelines -> Hom categories
	- [[Fusion rules]] of the domain walls #Learning-TODO
	  id:: 63b186e5-7748-4701-8357-c2cb83a51fcc
		- ((63aa5c67-13b4-49cf-aeac-39e5670b1b42))
- # Different viewpoints
	- ((63842469-5dc0-4676-9daa-b5ee2000e5a4)) is a toric code on a strange lattice!
		- The lattice is obtained by connecting 3 spheres in a triangular manner.
		- See ((63b28e8f-3c98-420e-ba5f-95f95f20202c)).
	- ((6368782c-d09f-467b-a891-689e3f35f66a)) Invitation
	- ## Quantum memory
		- Stabilizers and logical states #card
		  card-last-interval:: 30
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-06-03T00:43:34.539Z
		  card-last-reviewed:: 2023-05-04T00:43:34.540Z
		  card-last-score:: 5
			- $A_v$, $B_p$ as the stabilizers of the code. Flips are regarded as errors.
			- Ground space (different homotopy types) as the logical space.
		- Logical operators #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-04-26T01:08:51.606Z
		  card-last-reviewed:: 2023-04-02T01:08:51.606Z
		  card-last-score:: 5
			- There are 4 string operators: $X_1,X_2,Z_1,Z_2$.
			- $X_1$ commutes with $X_2$ and $Z_2$. Similar for others.
			- We may select any 2 commuting operators as logical X. Those anti-commuting would be logical Z.
				- Note those operators aren't universal.
			- We obtain two qubits, but only **single-qubit** gates. No entanglement.
- # Misc
	- Theorem. Toric code is robust against local perturbations. #card
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-02-03T01:10:01.330Z
	  card-last-reviewed:: 2023-01-10T01:10:01.331Z
	  card-last-score:: 5
		- Rough argument
			- Treat $\delta H$ in perturbation theory order by order.
			- Change topo quantities <-> Form a nontrivial loop.
			- At the thermodynamic limit, the lattice is very large. So nontrivial loops are only formed at very high orders of the perturbation theory.
		- Setting
			- $\delta H$ is an **arbitrary sum** of local perturbations.
				- ((63b29124-d69c-46e4-9973-32fc95c2ecad))
				- Denote the range by $t$.
		- First, invoke [[Brillouin-Wigner Perturbation Expansion]]
			- $\begin{aligned} H_{p n}^{\mathrm{eff}} & =E_0+\left\langle p\left|\delta H \frac{1}{1-G \delta H}\right| n\right\rangle \\ & =E_0+\langle p|\delta H| n\rangle+\langle p|\delta H G \delta H| n\rangle+\langle p|\delta H G \delta H G \delta H| n\rangle+\ldots\end{aligned}$
				- $G(E)=\sum_{n \in \text { excited }} \frac{|n\rangle\langle n|}{E-E_n^0}$
				- Here are actually some implications, eg $G$ depends on the perturbed spectrum; some extra normalization is required.
					- But the picture is clear: The perturbation must come to high orders to have a nonzero effect.
		- Effect on ground states
			- Each application of $\delta H$ moves a quasiparticle for t steps.
			- To obtain a nonzero correction term, we must move a quasiparticle along the whole torus.
			  id:: 63b29c20-9dce-4db3-b7c0-7e81dff5cd27
			- When $L \to \infty$, this requires extremely high orders of the perturbation terms.
		- Effect on excitations  #[[Research/To Be Investigated]]
			- Simon claims that the positions of the excitations would fluctuate due to the perturbation, i.e. a finite-size cloud.
			- However, if we do the braidings far enough, then the size of the cloud is negligible.
			- He doesn't mention the extra pairs (strings) of excitations incurred by the perturbation term, which may cause extra minuses?
			  background-color:: red
				- Tentative arguments: Only extra pairs excitations near the boundary of the braiding, with one inside and one outside, matters.
				- However, the probability of even and odd numbers shall be roughly equal?
		- See [[Simon's Topobook]], section 27
		- Do we have a more elegant argument without the need for various perturbation techniques? #[[Open problem]]
		  id:: 63c14170-78b2-4e51-91d3-c07fed031c50
			- Rigidity of [[TQFT]], i.e. No deformations? This seem to motivate the definition of topological orders by deformations.
- # Problems
	- How to prove there are only 4 simple topo ((636879d9-dfe3-4bdd-a078-587cc9c25350)) and thus labelled? They can't be connected by local operators?
	   #Inbox/Problem
		- The excitations can only be $A_v=-1$ or $B_p=-1$. But is this sufficient?
	- [[Ribbon]] structure
	  collapsed:: true
		- ((6371a8f3-e2d5-4eb9-91e3-e0342be2efcc))
		- He doesn't write the [[Dual structure]]. Instead, he just moved the particle along a circle.
		  Is this equivalent to Double [[Braiding]] with vacuum? If not, why? How to explicitly write out the creators and annihilators? #Learning-TODO
- Explicitly calculate all relevent structures and write them in the familiar operator form: Dual, Ribbon, Braiding, Drinfeld center of the boundary, etc. #Learning-TODO
	- [[Fusion]]
		- Note that I may need to select a homotopy class. There is a convenient choice: those not crossing the left and right 'borders'.
		- Also I shall fix how e and m fuse.
	- Given n pairs of excitations (at different locations), the pairs can always be connected with nonintersecting paths. Because a path doesn't change the [[Path Connectedness]] of the [[Torus]].
-