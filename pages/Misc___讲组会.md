# 怎么讲？
	- 讲述顺序
		- Overall comment
			- When we say a system exhibits topological orders, is it the ground state does or the Hamiltonian does?
				- Many hints suggest that the ground state does.
					- Wen defines TO from LU
					- TEE
					- Minimally entangled state: Extract ST matrices from the whole ground space
					-
				- Then a natural question arises: Given a ground state, how to define topological excitations (anyons)?
					- It turns out that the name 'excitation', related to the Hamiltonian, is misleading.
				- This paper tells us how to define anyons from a single ground state. Much information is contained in the ground state.
					- Related: Extract S-matrix and prove Verlinde formula, extract chiral central charge
				-
				- I would skip many technical details, since they are easily forgotten and would be greatly simplified in the future.
		- ((65e2857a-1ac5-43b7-af9c-7542aeefe4a0))
		- Collection of ((65e28899-6cc2-4ec1-81f7-8b25150c971f))
		- Setup
			- ((65a0b40e-d1f0-42b2-996f-937bc3da14c7))
			- ((65893f05-8c6b-4c41-9073-de9cec1e30b8)) and its relation to the area law
			- ((65e28724-1e52-44bd-965e-9fdc1011faf4))
		- ((65e285d9-886f-4cc0-ba5d-fd31a2035066))
		- Sketchy Proof of Key results
		- ((65e28726-3729-4342-a1e7-218512c56011))
	- 黑板安排
		- Table of content
		- Key ideas of the paper
		- Setup
		- Shorthands of main results
		- Short statements of key techniques (no proof)
	- Tips
		- 加点笑话
		- ((654072b4-05c7-4e28-bb1b-ce678486e593))
- # TODOs at second time
	- Re-arrange the blackboard as the first time
	- Area law implies A1 and A2
- # Key ideas of the paper
  id:: 65e2857a-1ac5-43b7-af9c-7542aeefe4a0
	- Locality
		- It is well-known that different ground states of topological orders are locally indistinguishable.
		- Formalization: Information convex set
		- Informally speaking, topological orders are the **global** DOFs left when we know all **local** information (reduced density matrices on finite disks).
	- Merging
		- How local reduced density matrices could merge to global states?
		- A bit similar to differential geometry: Locally everywhere is homeomorphic to $\mathbb R^n$, but globally things can be very interesting.
- # Main Results
  id:: 65e28899-6cc2-4ec1-81f7-8b25150c971f
	- Unique ground state on $S^2$
	  id:: 65fbe917-813e-493b-a8fc-72d766f86d72
		- Proof
			- Lemma. Unique element in ICS of contractible regions (disks)
				- This should be the correct starting point!
				- Proof
					- Reduced density matrices on disks are unique
					- Unique merging of Markov states
					- Merge disks repeatedly
			- Divide $S^2$ into the south disk and the north disk
			- Merge them to a sphere
	- Structure of the ICS (NOTE: We do not give full definition of ICS here. 简单来说，我们知道一个区域所有disk上的RDM，ICS是所有这些local RDM可能拼成的global RDM)
		- Definition of anyon as extreme points of ICS of an annulus (环状区域，戳了一个洞的圆)
		- Definition of fusion rules as ICS of an 2-holed disk
			-
		- ((65e2a27d-aa9f-46fe-bd6b-0a23ea888db9))
			- Orthogonality is proved by fidelity, a rather soft tool. Finiteness follows orthogonality.
			- The vacuum sector is obtained by tracing out the interior of a disk.
		- 2-hole disk
			- Significance: The ICS of an annulus is of **classical** structure, while states here can be **coherent**!
		-
		- ((65adc655-d62f-4fe7-aa2a-1c590241c0bb))
			- Proved by the isomorphism theorem
			- Proved by entropic relations
	-
	- Proof that TEE = ln D, without specific models or field theory
- # Key techniques used
  id:: 65e285d9-886f-4cc0-ba5d-fd31a2035066
	- Quantum Markov states
		- Special properties
			- Unique merging by ((659f5206-6b2d-4b8a-a381-8d16e20644f7))
	- ((65ab687d-244f-4792-8b78-fabf3a6937a4))
		- A nontrivial sufficient conditions for quantum states to be merged uniquely.
	- ((659f5e4e-c195-40cc-8996-3a018dbe3604))
		- In short, the Petz recovery map provides an inverse to the partial trace map.
	- Isomorphism theorem
		- Merging and removing a disk is a linear bijection, with special properties (preserve distance and entropy difference)
		- Essentially, the structure of info convex sets are invariant under continuous deformation.
	- Fidelity
	- Maximalization of entropy
		- This is used repeatedly, in proving TEE and axioms of fusion rules. I feel that it is necessary to dig into the technique.
	- Entropy difference
		- I think it is a characterization of the structure, like character in group reps and curvature in DG
		- Axioms of fusion are obtained by comparing entropic equations.
		- Prop. $f(a)$ is precisely the quantum dimension of $a$.
		  collapsed:: true
			- External. The merged state is the maximal-entropy element in $\Sigma^c_{ab}(Y)$, with entropy
			  $$
			  \begin{aligned}
			  & S\left(\sigma_Y^{a \times b}\right)-S\left(\sigma_Y^1\right) \\
			  & =f(a)+f(b)+\ln \left(\sum_c N_{a b}^c e^{f(c)}\right)
			  \end{aligned}
			  $$
			- From the merging perspective, we have
			  $$
			  S\left(\sigma_Y^{a \times b}\right)-S\left(\sigma_Y^1\right)=2 f(a)+2 f(b) .
			  $$
				- Note that merging preserves entropic difference.
			- Compare the above two expressions, we obtain
			  $$
			  e^{f(a)} e^{f(b)}=\sum_c N_{a b}^c e^{f(c)}
			  $$
			- Note that there is only one ring homomorphism $\mathrm{Gr}(\mathrm{C}) \rightarrow \mathbb{R}$ which takes positive values on simple objects, and the value is known to be their quantum dimensions.
- # Definition of anyons and fusion rules
  id:: 65e28724-1e52-44bd-965e-9fdc1011faf4
	- Def. Anyon types: Certain points on the info convex sets of a 1-hole disk (annulus).
		- What does it mean?
			- Example: Toric code (Ref. Simon's topobook)
			- Tube algebra
			- Localized, could be detected by a region around it (by flux and charge)
		- Def. Fusion spaces: Subspaces of ICS of an 2-hole disk, such that each annulus has the specified charge.
- # Technical results
	- ((65f24e29-f487-4714-ae77-b640eaa2f187))
	-
- # Open questions
  id:: 65e28726-3729-4342-a1e7-218512c56011
	- Easy part
		- Numerical calculation
			- Good news: We only need one ground state, which could be inexact.
		- Isomorphism theorem: What happens along domain walls?
			- The reason we can compare anyons in different regions is because we can move them.
			- Similar to differential geometry: To compare vectors on different points, we need the connection.
		- More data: F-symbol and R-symbol?
			- There has been work extracting CCC and S-matrices
		- Fermionic
	- Hard part
		- Get rid of scalars and better foundation
		- His axioms are not preserved under LU.
			- Counterexample: Cluster states.
		- Quantum merging problem
			- Sheaf theory?
			- Mittag-Leffler problem. Anyone familiar in complex variables?
		- Other aspects of TO
			- Symmetry and gauging
			- Anomaly and bulk-boundary correspondence
		- Derived gappedness from the state? Investigate gapless systems?
	-
- # Examples
  id:: 65e53b3f-f201-4432-8502-3831964f5f4f
	- *This section is not talked alone. I should use the examples all over the talk.
	-
	- Toric code
		- Note that the result of TC could be easily generalized to any quantum double.