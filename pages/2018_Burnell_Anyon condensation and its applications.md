type:: paper_reading

- [[To be recorded]]
  SCHEDULED: <2023-02-08 Wed>
- ![2018_Burnell_Anyon condensation and its applications.pdf](file://zotero_link/Physics/Topological order/Anyon Condensation/2018_Burnell_Anyon condensation and its applications.pdf)
- # Intro
  collapsed:: true
	- Different from vortex proliferation in 2D [[Superfluid]]
		- Energy cost diverges >= logarithmically
	- Similar to 2D superconductors
		- Vortices are point defects, with long-range statitics
		- ((63d873c2-b58b-4e3b-8469-3fe30da04a61))
		- However, vortices in superconductors are created by external fields, whereas anyons are excited states of the Hamiltonian.
	- Terminology: topological symmetry breaking (TSB) := condense self-bosons #card
		- ((63d87ab7-cf2e-4c76-833e-f02c8a92d40c))
		- ((63d87b0d-33e4-4add-beb8-a78299edffb4))
	- ((63d87b66-fa46-4c0e-ae19-2faf248fdbd1))
- # ((63d873f3-58cd-4d48-b066-1db9cacae89c))
  collapsed:: true
	- ## Condensable bosons
	  id:: 63d873f9-1041-49a2-8b5a-1908f8fa53a8
		- Requirement #card
			- $R_{a\bar a}^cR_{\bar a a}^c=1$ for **at least one** of the fusion channels of $a \otimes \bar a$
				- Note that it is the **double braiding**.
				- Why? #Learning-TODO
					- Maybe start from Wan's construction and derive a contradiction?
			-
	- ## Similarities to boson condensation #card
		- Identification of different particles
			- eg. Superconductor: Cooper pairs, which have charge $2e$, are condensed. Thus quasiparticles are labeled by charge **modulo 2e**
			- This seems hard to explain just by representations
		- Splitting of irreps
			- Since the group is smaller
		- Confinement of some quasiparticles
			- Principle
				- [The](((63da0538-be4c-44ca-a996-c6db61e99a11))) bosons we condense have non-trivial braiding with some of the other anyons. These anyons will therefore cause destructive interference between different configuration histories of the condensate, and become **confined** in the condensed phase.
			- eg. Flux in superconductors
				- ((63da0573-e5f4-4625-aad1-c37cc553363f))
	- ## ((63da0e16-0074-496a-952b-bd3534890de6)): Double Ising to [[Toric Code]] condensation
	  collapsed:: true
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
	- ## ((63db1d78-28d6-469b-bc93-808cf8bce702))
	  collapsed:: true
		- Main complications
			- ((63db1d9e-5704-402f-88e6-3cca500d3951))
			- ((63db1db1-b3fc-45e6-9ba1-6e2181840a9f))
		- ((63db223b-823d-4c25-8301-f669a6ff09cd))
		- ### Three steps
			- Identification
				- Identify the condensed anyon(s) $\{\gamma_i\}$ to the vacuum
				- Identify several anyons linked by the condensate as well
			- Splitting
				- If $a \times \bar{a}=1+\gamma_i+\ldots$, then $a\times \bar a$ contains orthogonal copies of the condensate vacuum.
				- This means $a$ must split in the condensed phase.
			- Confinement
				- Only $a$ with **at least one channel** in $a \otimes \gamma_i$ having trivial double braiding can survive.
					- ((63db212c-55c2-4693-a5c8-bb5713898e44))
				- Also, if $N_{\gamma_i, \gamma_i}^c>0$ and $c$ is not a boson, then $c$ is confined in the condensed phase.
					- Note that it is related to the condition of ((63d873f9-1041-49a2-8b5a-1908f8fa53a8))
			-
	- ## Relation to Field Theory and [[Higgs Mechanism]]
	  collapsed:: true
		- There do exist a partial relation
			- ((63db2299-1c12-4e12-b2d5-2aba292d26f6))
		- Counterexample
			- ((63db22af-446a-415a-a70b-d3947dfbda7b))
- # ((63db239a-76d1-41f8-9736-8b52f1cd4f65))
	- An interesting question: Could the boundary (to vacuum or to other phases) be gapped?
		- This turned out to be related to anyon condensation??
	- ((63db2510-dd12-4a31-8a40-c7b129c44f3b))
		- For example, an ordinary band insulator admits a gapped boundary with a Mott insulating state, but a quantum Hall insulator, whose band structure is topologically nontrivial, does not.
	- ((63db2560-1f72-426d-86b0-bc4ecbfda560))
	  collapsed:: true
		- #+BEGIN_NOTE
		  These are only **arguments** from theory of CFT, not **proofs**
		  #+END_NOTE
		- Simplification: [[Folding trick]]
			- ((63dc6419-e606-46ea-bd64-6a576a6acfb6))
			- Thus we only need to consider the boundary to vacuum
		- Idea
			- Assume a trip of $\mathcal T$ has the upper boundary gapless and the lower boundary gapped. 
			  Examine whether the effective theory, a CFT, is well-defined.
				- ((63dc6512-b706-412f-b5a6-e267ae68e4f8))
					- Very interesting. Individually gappable?
				- It is believed that 'legitimate CFT' -> partition functions invariant under modular transformations
		- Conclusion #card
			- ((63dc62f4-12d5-4fcf-8046-9e5aed8894fa)), then the Hamiltonian models with gapped boundaries can be explicitly constructed. Thus gappable.
			- Conversely, ((63dc6627-451d-4910-8dec-df9069fd9d1f))
	- ## ((63dc6779-5db0-4282-9299-3d2c00e971f1))
		- Generally there may be different boundaries between two phases.
			- eg. Toric code: e-condensed and m-condensed
		- The presence of different types of boundaries add to GSD!
		  background-color:: yellow
			- Argument: Homotopy inequivalent tracks of anyons are distinct basis vectors.
				- ((63dc67f4-2540-44eb-b7bc-64cf53790405))
			- See the example of [[Surface Code]].
-