- ![2020_Shi_Kato_Kim_Fusion rules from entanglement.pdf](file://zotero_link/Research/Entanglement/2020_Shi_Kato_Kim_Fusion rules from entanglement.pdf)
- # LooseEnds
  collapsed:: true
	- {{query (and [[LooseEnd]] (page [[2020_Shi_Kato_Kim_Fusion rules from entanglement]])) }}
- # BlackBoxes
	- ((6590d811-6f1c-4e0f-9c22-5c23ab2869f9))
	- ((65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2))
	- ((65a0b53f-9622-4b08-bf0f-f015a43f474b))
	- ((65ab6919-7791-414e-94b7-109b9b54b66e))
	- ((65ac7c26-e36e-4d29-b316-da693a10f142))
	- ((65addcba-e050-4ef6-86fe-754aaa68795d))
		- The maximization of the entropy is proved from SSA, while the maximal entropy is proved by another method in a different paper.
	- ((65b0739e-6fee-4c37-9b3a-176ef16f2e32))
- # Comments
	- #+BEGIN_CAUTION
	  We spend so much time juggling with entanglement entropy, which is only one scalar measure of entanglement.
	  #+END_CAUTION
		- It is indeed a valuable measure with several interesting properties, but it cannot lead us too far.
	- There are gapped systems with 'spurious EE contributions' where axiom A1 is violated, e.g. cluster states.
	  background-color:: red
	  id:: 65b0739e-6fee-4c37-9b3a-176ef16f2e32
		- First verify this! Isn't cluster states area-law entangled? Isn't it that area law implies the two axioms?
		- This is worrying yet interesting!
- # Setup
  collapsed:: true
	- First, we coarse-grain the system to group lots of microscopic DOF into 'supersites'.
	  collapsed:: true
		- ((6590d474-b56c-420d-8396-6cdc97795ee8))
		- We assume that the manifold can be partitioned into simply connected subsystems, associated with supersites.
		- Two subsystems are adjacent **iff** there is an edge between two vertices.
	- Summary
	  collapsed:: true
		- ((6590d6a5-2847-4f47-b138-37a8052ce485))
	- ## Notations
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
		- The set of all density matrices is $\mathcal{S}(\mathcal{H})$.
		- The global reference state $\sigma \in \mathcal{S}(\mathcal{H})$
		  collapsed:: true
			- ((6590d66a-c191-49b0-8c5f-043427ee829d))
			- Not pure in general!
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
	- ## Definitions #card
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
		- ((65a0b41b-9c69-4b4f-8a5a-30e888a0ab6e)) Information convex set
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
		- ((65ac937e-2687-49b9-bd28-1e5679bf927f)) 4.1. Superselection sectors
			- Let $X$ be a contractible annulus. The set of superselection sectors is a set of extreme points in $\Sigma(X)$.
		- ((65acb89b-6505-4a9b-8831-216efc878cac)) 4.2 Entropy contribution of superselection sector
		  id:: 65acb891-fe5d-439b-989a-deb677bd3678
			- For a contractible annulus $X$, we define the universal contribution to von Neumann entropy from superselection sector $a$ as
			  $$
			  f(a) \equiv \frac{S\left(\sigma_X^a\right)-S\left(\sigma_X^1\right)}{2}
			  $$
			- This definition makes sense since isomorphisms between subsystems preserves entropy difference.
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
- # Quantum information backgrounds
  collapsed:: true
	- ((65ab68d4-3dc8-4b75-b87e-8a9e00bce69c)) (Merging Lemma)
	  id:: 65ab687d-244f-4792-8b78-fabf3a6937a4
		- Given a set of density matrices $\mathcal{S} \equiv\left\{\rho^{(i)}_{A B C}\right\}$ and a density matrix $\sigma_{B C D}$ such that $\rho_{B C}=\sigma_{B C}$ and
		  collapsed:: true
		  $$
		  I(A: C \mid B)_\rho=I(B: D \mid C)_\sigma=0, \quad \forall \rho \in \mathcal{S},
		  $$
		  there exists a unique set of "merged" states $\left\{\tau_{A B C D}^\rho=\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho^{(i)}_{A B C}\right)\right\}$ which satisfy the following properties:
			- (1) $\tau^\rho$ is consistent with $\rho$ and $\sigma$, i.e.
			  $$
			  \tau_{A B C}^\rho=\rho_{A B C} \quad \text { and } \quad \tau_{B C D}^\rho=\sigma_{B C D}
			  $$
			- (2) Vanishing conditional mutual information,
			  $$
			  I(A: C D \mid B)_{\tau^\rho}=I(A B: D \mid C)_{\tau^\rho}=0, \quad \forall \rho
			  $$
			- (3) Conservation of von Neumann entropy difference, for arbitrary $\rho, \rho^{\prime} \in \mathcal{S}$,
			  $$
			  S\left(\tau_{A B C D}^\rho\right)-S\left(\tau_{A B C D}^{\rho^{\prime}}\right)=S\left(\rho_{A B C}\right)-S\left(\rho_{A B C}^{\prime}\right)
			  $$
		- Significance
		  collapsed:: true
			- We can restore the global state step-by-step from local information
			  logseq.order-list-type:: number
			- The conditions could be verified locally, i.e. the condition of $\rho$ could be verified only on $ABC$ and the condition of $\sigma$ could be verified only on $BCD$.
			  logseq.order-list-type:: number
			  collapsed:: true
				- Note that axioms A0 and A1 are local, but their corollaries (in their forms) are not.
		- logseq.order-list-type:: number
	-
- # Entropic Relations
  collapsed:: true
	- ((65ac7bbf-8fd8-49ef-85ef-112ae9a4b30f)) ... Path isomorphisms preserve entropy differences.
	- ((65adcbbb-f3d7-4134-803c-cd857f7d6f48)) 4.8. Let $\rho_Y$ be an extreme point of $\Sigma_{a b}^c(Y)$ and $\sigma_Y^1$ be the unique element of $\Sigma_{11}^1(Y)$, then
	  $$
	  S\left(\rho_Y\right)-S\left(\sigma_Y^1\right)=f(a)+f(b)+f(c)
	  $$
	  where $f(\cdot)$ is the function defined in ((65acb891-fe5d-439b-989a-deb677bd3678)).
		- See appendix E.
	-
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
  collapsed:: true
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
		  collapsed:: true
			- Physical fields and excitations are defined **locally**.
			- We need a **connection** to link different points!
			-
			- e.g. GR: Vectors at different points are comparable only due to a connection!
	- ## Extension of Axioms
	  id:: 659f5e4e-c195-40cc-8996-3a018dbe3604
		- ((659f5e74-1555-4968-b72e-66f4d159b87a)) If the axioms A0 and A1 are satisfied for r-disks, then they are satisfied for arbitrarily large disks.
		  collapsed:: true
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
			  collapsed:: true
				- Step 1. Enlarge B by B' while keeping C fixed.
				  collapsed:: true
					- By ((659f5ed9-dee2-44e1-b906-2049570fa33c)), we could add an arbitrary $B'$ to $B$ and preserve the axiom.
					- The condition seems very loose, no requirement on $B'$ at all. Could we find anything stronger?
					  background-color:: red
				- Step 2. Enlarge $C$ while keeping $BC$ fixed.
				  collapsed:: true
					- This step is necessary, since we need to show that $C$ could also exceed $r$.
					- ((659f5f2f-105f-4997-877d-c6b27fcd49c1))
	- ## Information convex set and uniqueness on disks
		- Proposition. ICS is convex and compact.
		  collapsed:: true
			- Partial trace is linear.
		- Uniqueness on disks and spheres #card
		  collapsed:: true
			- ((65a0b3a4-23cb-4731-8cfa-5efaea070cdb)) For any disk-like subsystem $\omega$, the information convex set has only one element
			  id:: 65a0b37c-57fa-4a1b-b2f2-75dc9da2cab4
			  collapsed:: true
			  $$
			  \Sigma(\omega)=\left\{\sigma_\omega\right\}
			  $$
			  where $\sigma_\omega \equiv \operatorname{Tr}_{\bar{\omega}}|\psi\rangle\langle\psi|$ and $\bar{\omega}$ is the complement of $\omega$.
				- The idea is to start from a $\mu$-disk and expand it by other disks step-by-step, so that it could become arbitrarily large.
				- Key techniques
				  collapsed:: true
					- ((659f5206-6b2d-4b8a-a381-8d16e20644f7))
					- ((65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2))
				- ((65a0b604-1416-4a9a-9f29-66310142243a))
				  collapsed:: true
					- Each step we add $C$ to the existing region $A$.
			- ((65a0b6c2-1aa7-4d83-8990-db951a9455f8)) The information convex contains only one state on the sphere, $\Sigma\left(S^2\right)=\{|\psi\rangle\langle\psi|\}$.
			  collapsed:: true
				- We divide the sphere into the upper 1/3 sphere $A$, the lower 1/3 sphere $C$, and the inner belt $B$.
				- By Prop 3.5, $\rho_{AC}$ and $\rho_{BC}$ are unique.
				- Proposition. 
				  collapsed:: true
				  $$
				  I(A: C \mid B) \leq S(B C)+S(C)-S(B)
				  $$
					- This can be proven by the triangle inequality.
				- But RHS is zero, so LHS is zero and we can perform Petz recovery.
	- ## Elementary steps and the isomorphism theorem
		- The idea is to use our axioms to upper bound some mutual information in the Merging Lemma, thus allowing merging local pieces in local information convex sets.
		- Comment
			- Intuitively, we could define smooth deformation of subsystems by adding or removing a small disk.
				- This process keeps the topology of the subsystem invariant, but not all topologically equivalent subsystems could be connected!
			- This is the strategy of ((63fa1061-a719-42a4-8b01-2bd603e394fc))
		-
		- ((65ab6bb9-b42b-486b-9123-d6eac2533def)) Consider the partition in the figure. Let the domain of $\operatorname{Tr}_D$ and $\mathcal{E}_{C \rightarrow C D}^\sigma$ to be $\Sigma\left(\Omega^{\prime}\right)$ and $\Sigma(\Omega)$ respectively. Then
		  id:: 65ab6919-7791-414e-94b7-109b9b54b66e
		  collapsed:: true
		  $$
		  \begin{aligned}
		  \operatorname{Tr}_D \circ \mathcal{E}_{C \rightarrow C D}^\sigma & =\operatorname{id}_{\Sigma(\Omega)} \\
		  \mathcal{E}_{C \rightarrow C D}^\sigma \circ \operatorname{Tr}_D & =\operatorname{id}_{\Sigma(\Omega')}
		  \end{aligned}
		  $$
			- ((65ab6c18-5f1a-499f-ac6a-ef341213c133))
			  collapsed:: true
				- $CD$ is contained in a $\mu$-disk.
				- $A$ and $D$ are assumed to be separated by at least $2 r+1$, where $r$ is the radius upper bound of $\mu$-disks.
				- $BCD$ has the topology of a disk, while the topology of $A$ is arbitrary.
				- $\Omega=A B C, \Omega^{\prime}=A B C D$
				-
			- In particular, $\Sigma\left(\Omega^{\prime}\right)$ and $\Sigma(\Omega)$ are isomorphic.
			- Moreover, $\mathcal{E}_{C \rightarrow C D}^\sigma$ only depends on $D$ and not the choice of $B$ or $C$.
			  collapsed:: true
				-
		- Corollaries
		  collapsed:: true
			- Corollary 3.9.1. (Distance preservation) Let $\rho_{\Omega}, \rho_{\Omega}^{\prime} \in \Sigma(\Omega)$ and $\rho_{\Omega^{\prime}}, \rho_{\Omega^{\prime}}^{\prime} \in \Sigma\left(\Omega^{\prime}\right)$. For any distance measure $D(\cdot, \cdot)$ between quantum states,
			  collapsed:: true
			  $$
			  D\left(\rho_{\Omega}, \rho_{\Omega}^{\prime}\right)=D\left(\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}\right), \mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}^{\prime}\right)\right) \\
			  
			  D\left(\rho_{\Omega^{\prime}}, \rho_{\Omega^{\prime}}^{\prime}\right)=D\left(\operatorname{Tr}_D\left(\rho_{\Omega^{\prime}}\right), \operatorname{Tr}_D\left(\rho_{\Omega^{\prime}}^{\prime}\right)\right)
			  $$
				- Proof
				  collapsed:: true
					- We only discuss the proof of the first identity.
					- Since both $\mathcal{E}_{C \rightarrow C D}^\sigma$ and $\operatorname{Tr}_D$ are CPTP maps, distance is nonincreasing under these maps. Therefore,
					  $$
					  \begin{aligned}
					  D\left(\rho_{\Omega}, \rho_{\Omega}^{\prime}\right) & \geq D\left(\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}\right), \mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}^{\prime}\right)\right) \\
					  & \geq D\left(\operatorname{Tr}_D \circ \mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}\right), \operatorname{Tr}_D \circ \mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}^{\prime}\right)\right) \\
					  & =D\left(\rho_{\Omega}, \rho_{\Omega}^{\prime}\right),
					  \end{aligned}
					  $$
					  where in the last line we used Proposition 3.9.
					- Therefore, $D\left(\rho_{\Omega}, \rho_{\Omega}^{\prime}\right)=D\left(\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}\right), \mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}^{\prime}\right)\right)$.
				- Note that although fidelity is not a distance measure, it is monotonic under CPTP maps, thus the proof still applies for fidelity.
			- Corollary 3.9.2. (Entropy difference preservation) Let $\rho_{\Omega}, \rho_{\Omega}^{\prime} \in \Sigma(\Omega)$ and $\rho_{\Omega^{\prime}}, \rho_{\Omega^{\prime}}^{\prime} \in \Sigma\left(\Omega^{\prime}\right)$. The von Neumann entropies satisfy
			  $$
			  S\left(\rho_{\Omega}\right)-S\left(\rho_{\Omega}^{\prime}\right)=S\left(\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}\right)\right)-S\left(\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}^{\prime}\right)\right) \\
			  
			  S\left(\rho_{\Omega^{\prime}}\right)-S\left(\rho_{\Omega^{\prime}}^{\prime}\right)=S\left(\operatorname{Tr}_D\left(\rho_{\Omega^{\prime}}\right)\right)-S\left(\operatorname{Tr}_D\left(\rho_{\Omega^{\prime}}^{\prime}\right)\right)
			  $$
			-
			-
		-
		- To summarize:
		- Definition 3.2. (Path) A finite sequence of subsystems $\left\{\Omega^t\right\}$ with $t=i / N$ and $i=0,1,2, \cdots, N$, is a path connecting $\Omega^0$ and $\Omega^1$ if each pair of nearby subsystems in the sequence are related by an elementary step of deformation.
		- ((65ac7bc9-f62b-4bf6-8777-059676b181c5)) 3.10. (Isomorphism Theorem) If $\Omega^0$ and $\Omega^1$ are connected by a path $\left\{\Omega^t\right\}$, then there is an isomorphism
		  id:: 65ac7bbf-8fd8-49ef-85ef-112ae9a4b30f
		  $$
		  \Phi_{\left\{\Omega^t\right\}}: \quad \Sigma\left(\Omega^0\right) \rightarrow \Sigma\left(\Omega^1\right)
		  $$
		  uniquely determined by the path $\left\{\Omega^t\right\}$. Moreover, it preserves the distance and the entropy difference between elements
		  $$
		  \begin{aligned}
		  D(\rho, \sigma) & =D\left(\Phi_{\left\{\Omega^t\right\}}(\rho), \Phi_{\left\{\Omega^t\right\}}(\sigma)\right) \\
		  S(\rho)-S(\sigma) & =S\left(\Phi_{\left\{\Omega^t\right\}}(\rho)\right)-S\left(\Phi_{\left\{\Omega^t\right\}}(\sigma)\right),
		  \end{aligned}
		  $$
		  where $D(\cdot, \cdot)$ is any distance measure which is non-increasing under CPTP-maps.
- # ((65ac7c23-279a-463e-90eb-73ce95a5e4bd))
  collapsed:: true
	- ((65ac902a-0946-4655-b9d6-76689f828a54)) 4.1. (Simplex Theorem) For an annulus $X$, the information convex set is the convex hull of a finite number of **orthogonal** extreme points, $\left\{\sigma_X^a\right\}$, i.e.
	  id:: 65ac7c26-e36e-4d29-b316-da693a10f142
	  $$
	  \Sigma(X)=\left\{\rho_X \mid \rho_X=\bigoplus_a p_a \sigma_X^a\right\},
	  $$
	  where $\{a\}$ is a finite set of labels and $\left\{p_a\right\}$ is a probability distribution.
		- Note that orthogonal means that for two extreme points $\rho_1, \rho_2$, we have $F(\rho_1, \rho_2)=0$ (zero fidelity).
	- Proposition 4.2 (Definition of vacuum). Let $\omega$ be a disk. For any annulus $X \subseteq \omega$
	  collapsed:: true
	  $$
	  \sigma_X^1 \equiv \operatorname{Tr}_{\omega \backslash X} \sigma_\omega,
	  $$
	  is an extreme point of $\Sigma(X)$, which could be identified as the vacuum sector.
		- $\sigma_\omega$ is the only element in $\Sigma(\omega)$.
	-
	- From the categorical viewpoint, we should next study the structure of morphisms.
	- ((65acb825-7117-4e5c-aa32-4d658d6ba89d)) 4.3. Let $X^0$ and $X^1$ be two annuli contained in a disk $C$. Let $\left\{X_{(1)}^t\right\}$ and $\left\{X_{(2)}^t\right\}$ be two paths connecting $X^0$ and $X^1$ such that $X_{(i)}^0=X^0, X_{(i)}^1=X^1$ for $i=1,2$. Moreover, assume that $\cup_t X_{(1)}^t \subseteq C, \cup_t X_{(2)}^t \subseteq C$. Then, the isomorphisms
	  id:: 65acb80a-219f-41c0-8de2-778437211ada
	  $$
	  \text { and } \quad \begin{aligned}
	  & \Phi_{\left\{X_{(1)}^t\right\}}: \Sigma\left(X^0\right) \rightarrow \Sigma\left(X^1\right) \\
	  & \Phi_{\left\{X_{(2)}^t\right\}}: \Sigma\left(X^0\right) \rightarrow \Sigma\left(X^1\right)
	  \end{aligned}
	  $$
	  are identical.
		- Essentially, homotopic paths induce identical isomorphisms.
		- This is also proved in appendix D.
	-
	- ## Fusion rules and fusion spaces
	  collapsed:: true
		- Definition. Fusion convex set
			- Y is a 2-hole disk.
				- ((65adc919-5b80-4467-ba7f-55707d40ecf8))
			- We define the extreme points of $\Sigma(Y)$ by
			  $$
			  \Sigma_{a b}^c(Y) \equiv\left\{\begin{array}{l|l}
			  \rho_Y \in \Sigma(Y) & \begin{array}{l}
			  \operatorname{Tr}_{Y \backslash B_1} \rho_Y=\sigma_{B_1}^a \\
			  \operatorname{Tr}_{Y \backslash B_2} \rho_Y=\sigma_{B_2}^b \\
			  \operatorname{Tr}_{Y \backslash B_3} \rho_Y=\sigma_{B_3}^c
			  \end{array}
			  \end{array}\right\}
			  $$
			- Note that [Lemma 4.3](((65acb80a-219f-41c0-8de2-778437211ada))) guarantees the **uniqueness** of isomorphism, thus we could unambiguously label extreme points of different annuli by the same labeling set.
		- ((65acbe7f-bed2-4357-b1bd-293d0b16f313)) 4.4. For a 2-hole disk $Y$, the information convex set $\Sigma(Y)$ is the following convex combination
		  $$
		  \Sigma(Y)=\left\{\rho_Y=\bigoplus_{a, b, c \in \mathcal{C}} p_{a b}^c \rho_Y^{a b c} \mid \rho_Y^{a b c} \in \Sigma_{a b}^c(Y)\right\},
		  $$
		  where $\left\{p_{a b}^c\right\}$ is a probability distribution.
			- Rephrased, $\Sigma(Y)$ equals the direct sum of fusion spaces.
			- Proof
		- #+BEGIN_CAUTION
		  $\Sigma^c_{ab}$ is coherent, while $\Sigma(Y)$ is not.
		  #+END_CAUTION
		- Theorem 4.5. Consider a 2-hole disk $Y . \forall a, b, c \in \mathcal{C}$,
		  $$
		  \Sigma_{a b}^c(Y) \cong \mathcal{S}\left(\mathbb{V}_{a b}^c\right)
		  $$
		  where $\mathbb{V}_{a b}^c$ is a finite-dimensional Hilbert space.
	- ## Axioms of fusion rules
	  collapsed:: true
		- Proposition 4.6.
		  collapsed:: true
		  $$
		  N_{a b}^c=N_{b a}^c 
		  $$
			- Pf. We can construct a path exchanging two holes, thus $\Sigma^c_{ab} \cong \Sigma^c_{ba}$.
		- Proposition 4.7.
		  collapsed:: true
		  $$
		  N_{1 a}^c=N_{a 1}^c=\delta_{a, c}
		  $$
			- The hole with vacuum charge could be extended to a disk.
			- Then the inner annulus and the outer annulus could be connected via a path.
		-
		- For the remaining rules, we need a different technique, i.e. compare entropic differences before and after merging.
		  collapsed:: true
			- Example. Merge 2 annuli
			  collapsed:: true
				- ((65addd17-dcc9-41d1-8db4-5529793d8345))
				- Proposition. Conditions in the [Merging Lemma](((65ab687d-244f-4792-8b78-fabf3a6937a4))) are satisfied, so we have a unique merged state on the 2-hole disk.
					- The upper annulus is $A$, the lower annulus is $D$, with 2 disk-like regions $B,C$ in the middle.
					- Proof
				- Proposition. From the merging lemma, we have
				  $$
				  S\left(\sigma_Y^{a \times b}\right)-S\left(\sigma_Y^1\right)=2 f(a)+2 f(b) .
				  $$
					- We need to use the merging lemma twice.
					- $$S(\sigma^{a \times 1})-S(\sigma^{1 \times 1})=2f(a) \\
					  S(\sigma^{a \times b})-S(\sigma^{a \times 1})=2f(b)
					  $$
					- Adding the two equations gives the result.
				- Proposition. The merged state is the maximal-entropy element in $\Sigma^c_{ab}(Y)$, with entropy
				  id:: 65addcba-e050-4ef6-86fe-754aaa68795d
				  $$
				  \begin{aligned}
				  & S\left(\sigma_Y^{a \times b}\right)-S\left(\sigma_Y^1\right) \\
				  & =f(a)+f(b)+\ln \left(\sum_c N_{a b}^c e^{f(c)}\right)
				  \end{aligned}
				  $$
					- Proof of maximal entropy
						-
					- The entropy difference is calculated in [another paper](((65addf0c-322e-44a5-b829-f59bfa7812e5))).
				-
				- Compare the above two expressions, we obtain
				  $$
				  e^{f(a)} e^{f(b)}=\sum_c N_{a b}^c e^{f(c)}
				  $$
		- ((65af8780-6980-4953-a18c-de93249a5257)) 4.9. For each charge sector $a \in \mathcal{C}$, there is a unique sector $\bar{a} \in \mathcal{C}$ such that
		  collapsed:: true
		  $$
		  N_{a b}^1=\delta_{b, \bar{a}} 
		  $$
			- Proof
				- The key is the following picture to merge an annulus into the hole of another:
				  ((65af88da-ce0f-4365-b63a-bbffdd407dbf))
				- Proposition. The global state exists and is unique.
					-
				- Proposition. 
				  $$
				  e^{f(a)}=\sum_b N_{a b}^1 e^{f(b)}
				  $$
					-
			- We can easily derive the following properties.
			  $$
			  \overline{1}=1, \quad \overline{\bar{a}}=a, \quad f(\bar{a})=f(a) .
			  $$
			-
		- Proposition 4.10.
		  collapsed:: true
		  $$
		  N_{a b}^c=N_{\bar{b} \bar{a}}^{\bar{c}}
		  $$
			- Proof
				- We need a different merging:
					- ((65af8b0f-a0d6-4b6a-957f-9a8d21dcecf7))
			- Then we can compare to the following diagram:
				- ((65af8b30-b5ad-48c7-9cc3-161494b47849))
			- Prop. Since the total charge is known to be 1, the left charge must be the anti-charge of the right.
			- Prop. 
			  $$
			  P_{(a \times b \rightarrow c)}=P_{(\bar{b} \times \bar{a} \rightarrow \bar{c})}
			  $$
				- This is still a blackbox for me. Let me crack it later.
				- This immediately implies
				  $$
				  N_{a b}^c=N_{\bar{b} \bar{a}}^{\bar{c}}
				  $$
		- Proposition 4.11. The fusion rules are associative, i.e.,
		  collapsed:: true
		  $$
		  N_{a b c}^d=\sum_i N_{a b}^i N_{i c}^d=\sum_j N_{a j}^d N_{b c}^j .
		  $$
			- We need two different ways of merging.
			- The first is apparent:
			  ((65b06d41-17c2-4211-8e5f-0de2f4e912ec))
				- This shows $N_{a b c}^d \geq \sum_i N_{a b}^i N_{i c}^d, N_{a b c}^d \geq \sum_j N_{a j}^d N_{b c}^j$
			- ((65b06d4b-bdbb-426a-817a-1bfeb3be5bde))
				- This shows
				  $$
				  e^{f(a)} e^{f(b)} e^{f(c)}=\sum_d N_{a b c}^d e^{f(d)}
				  $$
				  and proves the $\geq$ above must be replaced by $=$.
- # ((65b06f78-0eb4-454d-8efc-e5e2eeae8528))
	- This section is to be understood later.