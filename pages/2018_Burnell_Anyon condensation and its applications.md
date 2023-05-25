type:: paper_reading

- [[To be recorded]]
  SCHEDULED: <2023-02-16 Thu>
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
	  card-last-interval:: 27.15
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-09T15:16:48.833Z
	  card-last-reviewed:: 2023-03-13T12:16:48.833Z
	  card-last-score:: 5
		- ((63d87ab7-cf2e-4c76-833e-f02c8a92d40c))
		- ((63d87b0d-33e4-4add-beb8-a78299edffb4))
	- ((63d87b66-fa46-4c0e-ae19-2faf248fdbd1))
- # ((63d873f3-58cd-4d48-b066-1db9cacae89c))
	- ## Similarities to boson condensation #card
	  id:: 63d87e90-19ca-426a-93d5-77c0b39eac21
	  collapsed:: true
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-08-14T00:56:57.830Z
	  card-last-reviewed:: 2023-05-22T00:56:57.831Z
	  card-last-score:: 5
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
	- ## ((63db1d78-28d6-469b-bc93-808cf8bce702))
		- Main complications
			- ((63db1d9e-5704-402f-88e6-3cca500d3951))
			- ((63db1db1-b3fc-45e6-9ba1-6e2181840a9f))
	- ## Relation to Field Theory and [[Higgs Mechanism]]
	  collapsed:: true
		- There do exist a partial relation
			- ((63db2299-1c12-4e12-b2d5-2aba292d26f6))
		- Counterexample
			- ((63db22af-446a-415a-a70b-d3947dfbda7b))
- # ((63db239a-76d1-41f8-9736-8b52f1cd4f65))
  collapsed:: true
	- ((63db2510-dd12-4a31-8a40-c7b129c44f3b))
		- For example, an ordinary band insulator admits a gapped boundary with a Mott insulating state, but a quantum Hall insulator, whose band structure is topologically nontrivial, does not.
	- ((63db2560-1f72-426d-86b0-bc4ecbfda560))
	  id:: 63db2524-002c-41f4-84d1-4a6c2cb6882a
		- #+BEGIN_NOTE
		  These are only **arguments** from theory of CFT, not **proofs**
		  #+END_NOTE
		- Simplification: [[Folding trick]]
		  collapsed:: true
			- ((63dc6419-e606-46ea-bd64-6a576a6acfb6))
			- Thus we only need to consider the boundary to vacuum
		- Idea
		  collapsed:: true
			- Assume a trip of $\mathcal T$ has the upper boundary gapless and the lower boundary gapped. 
			  Examine whether the effective theory, a CFT, is well-defined.
				- ((63dc6512-b706-412f-b5a6-e267ae68e4f8))
					- Very interesting. Individually gappable?
				- It is believed that 'legitimate CFT' -> partition functions invariant under modular transformations
		- Conclusion #card
		  card-last-interval:: 30
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-05-04T11:36:20.027Z
		  card-last-reviewed:: 2023-04-04T11:36:20.027Z
		  card-last-score:: 5
			- ((63dc62f4-12d5-4fcf-8046-9e5aed8894fa)), then the Hamiltonian models with gapped boundaries can be explicitly constructed. Thus gappable.
			  id:: 63dc6611-b249-4a6b-9d84-61424d5eb2b0
			- Conversely, ((63dc6627-451d-4910-8dec-df9069fd9d1f))
	- ## ((63dc6779-5db0-4282-9299-3d2c00e971f1))
		- Generally there may be different boundaries between two phases.
			- eg. Toric code: e-condensed and m-condensed
		- The presence of different types of boundaries adds to GSD!
		  background-color:: yellow
			- Argument: Homotopy inequivalent tracks of anyons are distinct basis vectors.
				- ((63dc67f4-2540-44eb-b7bc-64cf53790405))
			- See the example of [[Surface Code]].
- # ((63e596ca-3a36-45c5-a5e4-e9b010914654))
	- [[Anyon Permuting Symmetry]]
		- Definition. Permuting some anyons preserve the braiding and fusion rules.
		- Thoughts
			- ((63e598a3-08bc-463d-a0d5-1811d2b4b644))
				- Thus it is also [[Emergent]] in some sense.
		- Examples
			- [[Toric Code]]: Exchange e and m.
	- One way to understand [[Anyon Permuting Symmetry]] is through TSB!
		- Examples
			- [[Toric Code]]: It could be obtained by condensing $\psi_1\psi_2$ in the double Ising.
				- After condensation, the non-abelian anyon $\sigma_1 \sigma_2$ splits into two abelian anyons $\tilde{\sigma}_e$ and $\tilde{\sigma}_m$, which we identify with the $e$ and $m$ anyons.
				- Therefore, arbitrary permutations of the results of splitting must be a symmetry!
				- Can we have some symmetry which is not $S_n$? #[[Open problem]]
		- The exchange domain wall could also be understood ((63e59a16-79ea-47db-9108-9f7b02aa7952))!
			- Intuitively, the domain wall corresponds to confined anyons in the condensed phase. Therefore crossing the walls corresponds to braiding with the confined anyons in the parent phase.
		- ((63e59ac6-63fe-4fa3-ace7-bef1e93f239c)).
			- General picture
				- Anyons that can be permuted are the results of splitting.
				- The endpoints of the domain walls can be viewed as confined non-abelian anyons.
				- ((63e59bb0-c3f6-4994-bc2b-ef7f79320965))
			- Two papers of Wan #[[Research/To Be Investigated]]
				- [[1308.4673] Symmetry Enriched Phases via Pseudo Anyon Condensation (arxiv.org)](https://arxiv.org/abs/1308.4673)
				- [[1402.3356] A Unified Framework of Topological Phases with Symmetry (arxiv.org)](https://arxiv.org/abs/1402.3356)
			-
	-
- # ((63e59e44-b68a-4bcd-945c-82c3a8b541dd))
	- Duality mapping
	  collapsed:: true
		- Ideas
		  collapsed:: true
			- Reduce TSB to more familiar quantum phase transitions
			- Somewhat suspicious. Could the property of being topological eliminated by duality mapping?
			  background-color:: red
		- Examples
		  collapsed:: true
			- Map toric code condensation to a 3D Ising critical point
			- Map a general abelian boson to a p-state Potts spin
			- ((63e59fd0-742b-427d-b513-0457af410432))
			  collapsed:: true
				- Then the critical point could be mapped to the [[Higgs Transition]].
				  id:: 63e59fd5-dcb4-4008-8b78-6ef5a6f38331
	- On the other hand, when the anyon to be condensed is nonabelian, it **cannot** be mapped to a dual spin description.
		- This is more interesting -- and perhaps reveals something more fundamental!
		- ((63e5a0b6-8650-4b2d-adc4-b7c1bc764786))
	- ((63e59eb0-8b95-4032-8bbf-ccd1935320d1)) #[[Research/To Be Investigated]]
	-
-