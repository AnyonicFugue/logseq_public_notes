- ![2020_Shi_Kato_Kim_Fusion rules from entanglement.pdf](file://zotero_link/Research/Entanglement/2020_Shi_Kato_Kim_Fusion rules from entanglement.pdf)
- # LooseEnds
  collapsed:: true
	- {{query (and [[LooseEnd]] (page [[2020_Shi_Kato_Kim_Fusion rules from entanglement]])) }}
- # BlackBoxes
	- ((6590d811-6f1c-4e0f-9c22-5c23ab2869f9))
	- ((65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2))
	- ((65a0b53f-9622-4b08-bf0f-f015a43f474b))
- # Comments
	- #+BEGIN_CAUTION
	  We spend so much time juggling with entanglement entropy, which is only one scalar measure of entanglement.
	  #+END_CAUTION
		- It is indeed a valuable measure with several interesting properties, but it cannot lead us too far.
- # Setup
	- First, we coarse-grain the system to group lots of microscopic DOF into 'supersites'.
	  collapsed:: true
		- ((6590d474-b56c-420d-8396-6cdc97795ee8))
		- We assume that the manifold can be partitioned into simply connected subsystems, associated with supersites.
		- Two subsystems are adjacent **iff** there is an edge between two vertices.
	- Summary
	  collapsed:: true
		- ((6590d6a5-2847-4f47-b138-37a8052ce485))
	- The Hilbert space
	  collapsed:: true
	  $$
	  \mathcal{H}=\otimes_{v \in V} \mathcal{H}_v
	  $$
		- $\mathcal H_v$ is a finite-dimensional Hilbert space.
		- $V$ is the set of vertices of a finite graph $G=(V,E)$, defined on a manifold.
			- Could this be further viewed as a triangulation of the manifold? In this way we have the further information of faces, rather than only a graph. #LooseEnd
			  id:: 6590d4e0-ba3b-4b6c-b607-05ca847afd0b
		- Note that each vertex is a **supersite**.
	- ## Starting axioms
	  collapsed:: true
		- id:: 6590e1f0-5f63-4def-82e0-7d9a1aadc336
		  collapsed:: true
		  #+BEGIN_TIP
		  The axioms are expressed in terms of scalars, but there should be a deeper structure behind the simple scalars. #LooseEnd
		  #+END_TIP
			- However, to understand their significance, it seems that knowledge about quantum information is necessary!
		- They are expected to hold approximately, up to an error decaying with $r/\xi$.
		- ((65893cf9-7cea-42bf-a2e0-9fb81e10022e))
		  id:: 6590d78d-9c1a-4ba8-b099-a541a03cf94b
			- For any $\sigma_b \in \mu$, for any configuration of subsystems $B C \subseteq b$ topologically equivalent to the one described in ((6590d87f-e8b7-4d48-bfe8-13d0dc62aed8)),
			  $$
			  S\left(\sigma_{B C}\right)+S\left(\sigma_C\right)-S\left(\sigma_B\right)=0
			  $$
				- A disk is divided into a core and a boundary.
			- Intuition
				- The correlation between sufficiently separated (by B) subsystems (A and C) is negligible.
			- This implies the vanishing of mutual information,
			  id:: 6590d811-6f1c-4e0f-9c22-5c23ab2869f9
			  $$
			  I(A: C)_\sigma \equiv\left(S_A+S_C-S_{A C}\right)_\sigma=0
			  $$
			  from ((6590e387-581c-499d-8987-207a3fd0042d)).
				- $A$ is contained in the complement of $B C$ and $I(A: C)$ is the mutual information
				- It seems that we should assume that $A$ is the complement of $BC$ and the system is in a pure state!
				  background-color:: red
		- ((65893d02-16ab-46c9-b8df-4a6ca6d79925))
		  id:: 6590d798-bb45-4057-a691-0b4afd736705
		  collapsed:: true
			- For any $\sigma_b \in \mu$, for any configuration of subsystems $B C D \subseteq b$ topologically equivalent to the one described in ((6590d875-50ab-4917-a693-f1dfa72d0fab)),
			  $$
			  S\left(\sigma_{B C}\right)+S\left(\sigma_{C D}\right)-S\left(\sigma_B\right)-S\left(\sigma_D\right)=0
			  $$
				- A disk is divided into three parts, i.e. a 'Poke Ball'.
			- Intuition
				- We can decouple two subsystems (B,D) without affecting one too much.
				- This is motivated from the 'merging' operation.
					- i.e. We have a density matrix $\rho_{AB}$ and another $\rho_{BC}$, now we'd like to construct a density matrix $\rho_{ABC}$ with the previous ones.
					- ((6591147e-e39c-4000-af3a-f30c39cbba4a)) makes merging impossible in general situations.
					  id:: 659113e8-4138-4015-a578-7acdaa6f65b3
				- The condition makes merging always possible!
			- This implies the vanishing of conditional mutual information,
			  id:: 65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2
			  $$
			  I(A: C \mid B)_\sigma \equiv\left(S_{A B}+S_{B C}-S_B-S_{A B C}\right)_\sigma=0
			  $$
				-
		- What do they mean?
		-
	- The set of all density matrices is $\mathcal{S}(\mathcal{H})$.
	- The global reference state $\sigma \in \mathcal{S}(\mathcal{H})$
	  collapsed:: true
		- ((6590d66a-c191-49b0-8c5f-043427ee829d))
		- Not pure in general!
	- $\mu$-disks and reduced density matrices
	  collapsed:: true
		- $$
		  \mu(r)=\left\{\sigma_b \mid b \in \mathcal{B}(r)\right\}
		  $$
		- $\mathcal{B}(r)$ is a set of balls of radius less or equal to $r$.
			- Note that the distance is the graph distance (of supersites),
		- $\sigma_b$ is the reduced density matrix of the reference state $(\sigma)$ on $b$.
		-
		- Because $r$ will be chosen to be a constant independent of the system size, we will simply denote $\mu(r)$ by $\mu$.
		- We will refer to the set of $b \in \mathcal{B}(r)$ as the set of $\mu$-disks.
	- ((65a0b41b-9c69-4b4f-8a5a-30e888a0ab6e)) Information convex set #card
	  collapsed:: true
		- Preparations
			- Thickening
				- Let $\partial \Omega \subseteq V$ be a set of vertices that are (graph) distance 1 away from $\Omega$.
				- If the subsystem $\Omega \sqcup \partial \Omega$ is topologically equivalent to $\Omega$, we refer to that subsystem as a **thickening** of $\Omega$.
					- We denote the thickening as $\Omega^{\prime}$.
				- Intuitively, $\Omega^{\prime}$ is a subsystem that can be smoothly deformed into $\Omega$ such that $\Omega^{\prime} \backslash \Omega$ is a boundary of $\Omega$ with a non-vanishing thickness.
				-
				- This thickness must be chosen to be sufficiently large compared to the correlation length of the underlying state.
			- Consistency of density matrices
				- Two reduced density matrices (with different supports) are consistent if they have identical reduced density matrices on the overlap of their supports, denoted
				  $$\rho \overset{c}{=} \rho'$$
		- The information convex set of $\Omega$ is defined as
		  $$
		  \Sigma(\Omega) \equiv\left\{\rho_{\Omega} \mid \rho_{\Omega}=\operatorname{Tr}_{\Omega^{\prime} \backslash \Omega} \rho_{\Omega^{\prime}}, \rho_{\Omega^{\prime}} \in \tilde{\Sigma}\left(\Omega^{\prime}\right)\right\}
		  $$
			- Let $\Omega \subseteq V$ be a subsystem and let $\Omega^{\prime}$ be the thickening of $\Omega$.
			- $\tilde{\Sigma}\left(\Omega^{\prime}\right)$ is defined as
			  $$
			  \tilde{\Sigma}\left(\Omega^{\prime}\right)=\left\{\rho_{\Omega^{\prime}} \mid \rho_{\Omega^{\prime}} \stackrel{c}{=} \sigma_b, \quad \forall \sigma_b \in \mu\right\}
			  $$
			- A thickening is necessary to eliminate correlations on the boundaries.
			  id:: 65a0b53f-9622-4b08-bf0f-f015a43f474b
- # Summary of the Approach
  collapsed:: true
	- ## Starting Axioms
		- They are assumed rather than proved, though they seem well reasonable.
		- Approach 1
			- The entanglement area law
			  $$
			  S(A)=\alpha \ell-\gamma
			  $$
		- Approach 2
			- ((6590d78d-9c1a-4ba8-b099-a541a03cf94b)) and ((6590d798-bb45-4057-a691-0b4afd736705))
			- Note that these axioms follow from approach 1, however they are easier for computation.
	- No Hamiltonian is needed. Only a global states satisfying entropic constraints is necessary.
	- The notion of an 'information convex set' is central.
- # ((658936ae-1e93-4aee-9ecd-6bad09320e41))
  collapsed:: true
	- Questions
		- Why are they so many different approaches leading to similar results?
		- Are the results complete?
	- MPS approach and difficulty for higher-dimensional systems #card
		- In 1D...
			- ((658936e0-d90a-4803-968a-b22fac61436a)) implies that gapped states obey area-law entanglement. See ((654078ce-2ffb-4f24-be56-31c8887e8cb9)).
			- Another theorem then implies we can approximate the ground state by [[MPS]] efficiently.
		- In 2D and higher...
			- No guarantee for area-law.
			- Even for area-law states, MPS might not be efficient!
	- Conclusion: Approaches other than MPS is needed!
	  background-color:: yellow
	- TQFT approach?
		- It is generally believed that TQFT is complete in 2D, but [[Fracton]] (in 3D) is outside TQFT.
		- Moreover, how to prove it from first principles?
		-
	- This motivates the third approach in the paper, i.e. from entanglement.
- # ((6591193a-f4b5-4160-a1b4-4490dbab516b))
	- How can we compare two excitations and decide whether they are the same anyon? #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2024-02-04T07:12:30.449Z
	  card-last-reviewed:: 2024-01-04T01:12:30.450Z
	  card-last-score:: 3
	  collapsed:: true
		- By adiabatically transporting anyons from different regions to the same location! Great thought! [Ref](((6591197b-142a-410e-899a-5af5fd7f0256)))
		-
		- Key idea: {{cloze Locality and Connection}}
			- Physical fields and excitations are defined **locally**.
			- We need a **connection** to link different points!
			-
			- e.g. GR: Vectors at different points are comparable only due to a connection!
	- ## Extension of Axioms
	  id:: 659f5e4e-c195-40cc-8996-3a018dbe3604
	  collapsed:: true
		- ((659f5e74-1555-4968-b72e-66f4d159b87a)) If the axioms A0 and A1 are satisfied for r-disks, then they are satisfied for arbitrarily large disks.
			- The strategy is to enlarge each region by r-disks and show that the axioms are preserved in each step.
			-
			- Lemma 1. 
			  id:: 659f5ed9-dee2-44e1-b906-2049570fa33c
			  collapsed:: true
			  $$
			  S_{B C}+S_C-S_B \geq S_{B B^{\prime} C}+S_C-S_{B B^{\prime}}
			  $$
				- It is just SSA.
			- Lemma 2.
			  collapsed:: true
			  $$
			  S_{B C}+S_{C D}-S_B-S_D \geq S_{B B^{\prime} C}+S_{C D D^{\prime}}-S_{B B^{\prime}}-S_{D D^{\prime}}
			  $$
				- Add two SSA together.
			-
			- Axiom A0
				- Step 1. Enlarge B by B' while keeping C fixed.
					- By ((659f5ed9-dee2-44e1-b906-2049570fa33c)), we could add an arbitrary $B'$ to $B$ and preserve the axiom.
					- The condition seems very loose, no requirement on $B'$ at all. Could we find anything stronger?
					  background-color:: red
				- Step 2. Enlarge $C$ while keeping $BC$ fixed.
					- This step is necessary, since we need to show that $C$ could also exceed $r$.
					- ((659f5f2f-105f-4997-877d-c6b27fcd49c1))
	- ## Information convex set and uniqueness on disks
		- Proposition. ICS is convex and compact.
			- Partial trace is linear.
		- Uniqueness on disks and spheres #card
			- ((65a0b3a4-23cb-4731-8cfa-5efaea070cdb)) For any disk-like subsystem $\omega$, the information convex set has only one element
			  id:: 65a0b37c-57fa-4a1b-b2f2-75dc9da2cab4
			  collapsed:: true
			  $$
			  \Sigma(\omega)=\left\{\sigma_\omega\right\}
			  $$
			  where $\sigma_\omega \equiv \operatorname{Tr}_{\bar{\omega}}|\psi\rangle\langle\psi|$ and $\bar{\omega}$ is the complement of $\omega$.
				- The idea is to start from a $\mu$-disk and expand it by other disks step-by-step, so that it could become arbitrarily large.
				- Key techniques
					- ((659f5206-6b2d-4b8a-a381-8d16e20644f7))
					- ((65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2))
				- ((65a0b604-1416-4a9a-9f29-66310142243a))
					- Each step we add $C$ to the existing region $A$.
			- ((65a0b6c2-1aa7-4d83-8990-db951a9455f8)) The information convex contains only one state on the sphere, $\Sigma\left(S^2\right)=\{|\psi\rangle\langle\psi|\}$.
				- We divide the sphere into the upper 1/3 sphere $A$, the lower 1/3 sphere $C$, and the inner belt $B$.
				- By Prop 3.5, $\rho_{AC}$ and $\rho_{BC}$ are unique.
				- Proposition. 
				  $$
				  I(A: C \mid B) \leq S(B C)+S(C)-S(B)
				  $$
					- This can be proven by the triangle inequality.
				- But RHS is zero, so LHS is zero and we can perform Petz recovery.