-
- # Questions and Ideas
  collapsed:: true
	- We have a natural product operation (tensor product). But does addition (direct sum) make sense?
		- For example, what is the direct sum of two toric codes?
			- TODO Calculate its info convex set.
	- A natural framework to incorporate LU?
		- The problem is, for regions like the annulus and 2-hole disk, we can't naturally define an asymptotic info convex set, since there is not an embedding from the latter term to the former.
		- Define something like 'stable ICS' (which does not require an embedding)?
		- Yuan's suggestion: We do not try to make the set of good states closed under general LU, only define two good states to be equivalent if they can be connected by LU.
	- Formalize [Kitaev's algebraic treatment](((661f4196-2c7e-4ba0-a76f-2cb9b81e3562))) of his quantum double?
		- The first step should be considering a single hole.
	- Locality is natural, but why do we only allow unitaries?
		- Here only one state is present, does the notion of unitarity make sense?
		- Should we only talk about preserving the norm of the state? Or the full operator contains necessary information beyond the state in question?
	- ## Possible Generalizations
		- Deal with asymptotic states like Kitaev's honeycomb?
			- This may be done later; to classify states that satisfy A0 and A1 is already good enough.
		- Asymptotically good states
			- Radius: The minimum radius of $\mu$-disks are $a \sqrt {R_n}$
				- This ensures both that the lower bound tends to infinity and the number of balls in a disk tends to infinity.
				- Note that it is inequivalent to merging several sites into one, since this form still allows balls to cross the 'merged' sites.
					- As a result, LU could still break A0 and A1 under this formalism.
			- Error: Good up to an error $e^{-k R_n}$
		- Obtain a nontrivial compact manifold by gluing disks
			- Similar to gluing schemes of surfaces in Munkres.
			- Obviously, we require (1) each gluing component tends to infinity (2) compatible on gluing boundaries (3) good everywhere
- # TODOs
	- References
		- Those referred by Kitaev's quantum double paper
		- Otaga
		- Kapustin
		-
- # Problems
  background-color:: red
	- The sequence of disk states doesn't have a sensible limit. It is only a formal sequence.
		- To have a limit or a colimit, we have 2 approaches:
		  (1) Define a sequence of states on a pre-defined infinite lattice (region)
		  (2) Define a suitable category with morphisms
	- ((6619e3ab-398b-40b6-adb0-fc1fb17d58f9))
	- ((661b4736-e217-467a-b06b-0bd403103871))
- # Setup
	- Known facts
		- Each site should have a vector space $V_i \cong \mathbb C^\infty$.
		- The notion of partial trace and entanglement (perhaps also entropy) are important. We cannot afford to lose them.
		- Locality could only be defined in the thermodynamic limit, so infinity must somehow come in.
	- Formulation 1: Sequence of disks
	  collapsed:: true
		- Consider a sequence of disks $\{D_n\}$.
			- Each disk $D_n$ consists of $N_n$ sites $1,...,N_n$, with a vector space $V_i \cong \mathbb C^\infty$ on each site. The Hilbert space of $D_n$ is 
			  $$\mathcal H_n=\otimes_{i=1}^{N_n} V_i$$
				-
			- Each disk $D_n$ is assigned with a density matrix $\rho_n \in Hom(\mathcal H_n)$.
				- We call $\rho_n$ **good** if it satisfies Bowen's A0 and A1 in the bulk.
				- The key is to derive the isomorphism theorem, which roughly says that (1) the state is the same everywhere (2) the state allows continuous deformation.
					- There should be some better definition than A0 and A1. Perhaps local isomorphisms between different points?
			-
			- There is a natural embedding of sites $i_n$ from $D_n$ to $D_{n+1}$ preserving the topology.
				- $D_{n+1}$ can be viewed as the result of adding more sites to $D_n$ on the boundary.
				- However, for closed (more generally, non-sectorizable) manifolds there are not such good embeddings.
				  background-color:: red
					- Disks are worthy of studying, but closed manifolds should also be included.
			- Moreover, since $i_n$ is an embedding of sites, it induces an embedding of the Hom space $i_n: Hom(\mathcal H_n) \hookrightarrow Hom(\mathcal H_{n+1})$. (The notation $i$ has two meanings, which should be clear from the context.)
				-
			- Obviously we require $\rho_n$ to be consistent with $\rho_{n+1}$, which means that
			  $$\operatorname{Tr}_{D_{n+1} - D_n} (\rho_{n+1})  = \rho_n$$
				-
			- Definition. Direct limit of good disk states
				- The state $\rho^\infty = \lim_{n \to \infty} \rho_n$ defined on $\lim_{n \to \infty} Hom (\mathcal H_n)$, with each $\rho_n$ being good.
				-
			- Definition. Equivalence of direct limit of disk states
				- $\rho_1^\infty$ amd $\rho_2^\infty$ are called equivalent if they can be transformed to each other by LU and identifying/splitting sites.
	- Formulation 2: Infinite region with RDMs (Which is obviously more elegant!)
		- Notes
			- Density matrix and operator algebra are equivalent. We could choose any.
		- Consider an infinite lattice, with an RDM (mixed state) $\rho_X$ defined on each finite region $X$, such that the inclusion of regions induce the partial trace of RDMs.
		-
- # Possible Definitions of LU (LCPTP?)
	- To understand the correct definition, I need to first understand why toric code cannot be made trivial by LU.
	  background-color:: yellow
		- Think by examples.
		-
	- Finite product of single-layer operators, or exponential of local Hamiltonians?
	  background-color:: pink
		- The latter seems more natural and elegant, since (1) we have a structure of a Lie algebra (2) we have a manifold rather than discrete steps.
		- Also mentioned in [[2024_Kapustin_Sopenko_Anomalous symmetries and LSM]]. See references therein.
	- ## LU
		- To define LU on the sequence is problematic, since a LU on $D_{n+1}$ may not be restricted to $D_n$.
		  id:: 6619e3ab-398b-40b6-adb0-fc1fb17d58f9
		  background-color:: red
			- Maybe CPTP map together with some sense of locality is better.
		- Finitely generated many single-layer local unitaries
			- Definition. Single-layer local unitary
				- An unitary transformation $U\in\lim_{n\to\infty}Hom(\mathcal{H}_{n})$, such that there exists a maximal radius $r_0$, that $U$ is a tensor product of disjoint unitary operators with support within a disk of radius $r_0$.
				- ![image.png](../assets/image_1712731091929_0.png){:height 153, :width 419}
	- ## LCPTP
		- ### Locality
			- How to define locality for CPTP?
			  background-color:: red
			  id:: 661b4736-e217-467a-b06b-0bd403103871
				- Locality of the unitary on a larger system, either by purification or by embedding
				  logseq.order-list-type:: number
				- Locality-preserving automorphism of operator algebras
				  logseq.order-list-type:: number
					- Idea: A locality-preserving morphism maps local operators to local ones.
					- Would this be equivalent to our embedding-LU-partial trace formalism?
			- Purification way
				- The purifying sys is rather arbitrary. We could even purify the (finite) system with a single site!
				- Would the arbitrariness break locality?
				  background-color:: red
			- Embedding way
				-
			- Example: Toric code
				-
		- Motivation
			- A general LU could cross the whole region, so we may not restrict it to finite regions. On the other hand, we do not have the proper notion of partial trace an infinite unitary.
			- However, CPTP maps can be naturally defined for finite regions, and the restriction is done by partial trace.
		- Definition. LCPTP
			- A local CPTP $U$ is a CPTP $U_X$ on each finite region $X$, with some upper bound $k$ and $r_0$, such that for any finite region $X$, we can find a finite region $Y$ containing $X$, that $U$ on $X$ can be realized as a local unitary (bounded by $k$ and $r_0$) acting on $Y$ (followed a partial trace $Tr_{Y \backslash X}$)
		- Alternative: Purification
			-
	- ## Alternative: Generated by exponentiating local Hamiltonian
		- Ref. [[2024_Kapustin_Sopenko_Anomalous symmetries and LSM]]
			- Tian yuan: 他把事情弄得更复杂了 (?)
			  background-color:: red
		- Prop. The set of local Hamiltonians is a Lie algebra, i.e. a vector space closed under commutators.
- # Manifold and field theory
	- Replace density matrices by vn algebras is straightforward.
	- Pproblem
		- The notion of locality
			- Could we learn from the definition and classification of TQFT?
		- Definition of the Hilbert space
			- It must work for the toric code, which is naively an infinite formal sum of closed-loop configurations.
			  background-color:: yellow
			- It seems hopeless to consider the tensor product of a Hilbert space associated with each point.
			- Continuous functions?