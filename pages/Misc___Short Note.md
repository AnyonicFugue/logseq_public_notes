# Key ideas of the paper
	- Locality
		- It is well-known that different ground states of topological orders are locally indistinguishable.
		- Formalization: Information convex set
		- Informally speaking, topological orders are the **global** DOFs left when we know all **local** information (reduced density matrices on finite disks).
	- Merging
		- How local reduced density matrices could merge to global states?
		- A bit similar to differential geometry: Locally everywhere is homeomorphic to $\mathbb R^n$, but globally things can be very interesting.
- # Main Results
	- Unique ground state on $S^2$
		- Proof
			- Lemma. Unique element in ICS of contractible regions (disks)
				- This should be the correct starting point!
				- Proof
					- Reduced density matrices on disks are unique
					- Unique merging of Markov states
					- Merge disks repeatedly
			- Divide $S^2$ into the south disk and the north disk
			- Merge them to a sphere
	- Structure of the information convex set
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
	- Toric code
		- Note that the result of TC could be easily generalized to any quantum double.