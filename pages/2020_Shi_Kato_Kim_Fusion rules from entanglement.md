- ![2020_Shi_Kato_Kim_Fusion rules from entanglement.pdf](file://zotero_link/Research/Entanglement/From Local to global/2020_Shi_Kato_Kim_Fusion rules from entanglement.pdf)
- # LooseEnds
	- {{query (and [[LooseEnd]] (page [[2020_Shi_Kato_Kim_Fusion rules from entanglement]])) }}
	  query-table:: true
	  query-properties:: [:block]
- # BlackBoxes
  collapsed:: true
	- ((65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2))
	- ((65ab6919-7791-414e-94b7-109b9b54b66e))
	- ((65ac7c26-e36e-4d29-b316-da693a10f142))
	-
	-
- # Comments
  collapsed:: true
	- #+BEGIN_CAUTION
	  We spend so much time juggling with entanglement entropy, which is only one scalar measure of entanglement.
	  #+END_CAUTION
		- It is indeed a valuable measure with several interesting properties, but it cannot lead us too far.
	- There are gapped systems with 'spurious EE contributions' where axiom A1 is violated, e.g. cluster states.
	  background-color:: red
	  id:: 65b0739e-6fee-4c37-9b3a-176ef16f2e32
		- First verify this! Isn't cluster states area-law entangled? Isn't it that area law implies the two axioms?
		- This is worrying yet interesting!
	- Algebra is rigid, with lots of **equalities**; analysis is flexible, with lots of **inequalities**.
		- Entanglement entropy, fidelity, ..., can be viewed as tools from analysis when they present **inequalities**.
		-
	-
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
	  collapsed:: true
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
		- Distance between states
			- $$
			  \|\rho-\sigma\|_1 \equiv \operatorname{Tr} \sqrt{(\rho-\sigma)^2}
			  $$
		- If the boundary of $\Omega$ is expanded by a thickness of $\delta$, we shall refer to that subsystem as $\Omega_\delta$.
			- We use $\varepsilon$ as a very small length.
	- ## Starting axioms
	  id:: 65893f05-8c6b-4c41-9073-de9cec1e30b8
		- id:: 6590e1f0-5f63-4def-82e0-7d9a1aadc336
		  collapsed:: true
		  #+BEGIN_TIP
		  The axioms are expressed in terms of scalars, but there should be a better structure beyond scalars.
		  #+END_TIP
			- However, to understand their significance, it seems that knowledge about quantum information is necessary!
		- In most models and systems, they are expected to hold approximately, up to an error decaying with $r/\xi$.
		- ((65893cf9-7cea-42bf-a2e0-9fb81e10022e))
		  id:: 6590d78d-9c1a-4ba8-b099-a541a03cf94b
			- For any $\sigma_b \in \mu$, for any configuration of subsystems $B C \subseteq b$ topologically equivalent to the one described in ((6590d87f-e8b7-4d48-bfe8-13d0dc62aed8)),
			  $$
			  S\left(\sigma_{B C}\right)+S\left(\sigma_C\right)-S\left(\sigma_B\right)=0
			  $$
				- ((65ff64f0-cf02-40fa-ac98-45c41c781f80))
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
				- Ref. [Saturation of Araki-Lieb inequality](((65bf06ea-128e-4b76-8ea9-fc14687d28fa)))
		- ((65893d02-16ab-46c9-b8df-4a6ca6d79925))
		  id:: 6590d798-bb45-4057-a691-0b4afd736705
			- For any $\sigma_b \in \mu$, for any configuration of subsystems $B C D \subseteq b$ topologically equivalent to the one described in ((6590d875-50ab-4917-a693-f1dfa72d0fab)),
			  $$
			  S\left(\sigma_{B C}\right)+S\left(\sigma_{C D}\right)-S\left(\sigma_B\right)-S\left(\sigma_D\right)=0
			  $$
				- A disk is divided into three parts, i.e. a 'Poke Ball'.
				- ((65ff64e3-f0a4-4673-8c77-952c5fc8cb4c))
			- Intuition
				- We can decouple two subsystems (B,D) without affecting one too much.
				- This is motivated from the 'merging' operation.
					- i.e. We have a density matrix $\rho_{AB}$ and another $\rho_{BC}$, now we'd like to construct a density matrix $\rho_{ABC}$ with the previous ones.
					- ((6591147e-e39c-4000-af3a-f30c39cbba4a)) makes merging impossible in general situations.
					  id:: 659113e8-4138-4015-a578-7acdaa6f65b3
				- The condition makes merging always possible!
			- This axiom implies the vanishing of conditional mutual information,
			  id:: 65910b38-ed4c-4f7c-9c37-2cd9b8a8ddf2
			  $$
			  I(A: C \mid B)_\sigma \equiv\left(S_{A B}+S_{B C}-S_B-S_{A B C}\right)_\sigma=0
			  $$
				- Use the [lemma](((65cae198-2cb5-449f-8ef0-071f54190611))) together with the property that CMI is non-decreasing under inclusion of regions.
	- ## Definitions #card
	  collapsed:: true
		- $\mu$-disks and reduced density matrices
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
		  id:: 65a0b40e-d1f0-42b2-996f-937bc3da14c7
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
			- What's the point defining $\Sigma(\Omega)$ with thickening? Why isn't the unthickened version equivalent with $\hat\Sigma(\Omega)$?
			  collapsed:: true
				- The boundary have unneeded degrees of freedom for $\Sigma(\Omega)$, therefore we need to trace them out.
				- Take the example of the toric code. Tracing out the boundary takes account of $A_v$ and $B_p$ on the boundary.
				-
			-
		- ((65ac937e-2687-49b9-bd28-1e5679bf927f)) 4.1. Superselection sectors
			- Let $X$ be a contractible annulus. The set of superselection sectors is a set of extreme points in $\Sigma(X)$.
		- ((65acb89b-6505-4a9b-8831-216efc878cac)) 4.2 Entropy contribution of superselection sector
		  id:: 65acb891-fe5d-439b-989a-deb677bd3678
			- For a contractible annulus $X$, we define the universal contribution to von Neumann entropy from superselection sector $a$ as
			  $$
			  f(a) \equiv \frac{S\left(\sigma_X^a\right)-S\left(\sigma_X^1\right)}{2}
			  $$
			- This definition makes sense since isomorphisms between subsystems preserves entropy difference.
- # Quantum information backgrounds
  collapsed:: true
	- ((65ab68d4-3dc8-4b75-b87e-8a9e00bce69c)) (Merging Lemma)
	  id:: 65ab687d-244f-4792-8b78-fabf3a6937a4
		- Given a set of density matrices $\mathcal{S} \equiv\left\{\rho^{(i)}_{A B C}\right\}$ and a density matrix $\sigma_{B C D}$ such that $\rho_{B C}=\sigma_{B C}$ and
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
			- We can restore the global state step-by-step from local information
			  logseq.order-list-type:: number
			- The conditions could be verified locally, i.e. the condition of $\rho$ could be verified only on $ABC$ and the condition of $\sigma$ could be verified only on $BCD$.
			  logseq.order-list-type:: number
			  collapsed:: true
				- Note that axioms A0 and A1 are local, but their corollaries (in their forms) are not.
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
		- Why are they so many different approaches leading to similar results on the classification of gapped phases?
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
	- This motivates the third approach from entanglement.
- # ((6591193a-f4b5-4160-a1b4-4490dbab516b))
  collapsed:: true
	- How can we compare two excitations and decide whether they are the same anyon? #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2024-02-04T07:12:30.449Z
	  card-last-reviewed:: 2024-01-04T01:12:30.450Z
	  card-last-score:: 3
		- By adiabatically transporting anyons from different regions to the same location! Great thought! [Ref](((6591197b-142a-410e-899a-5af5fd7f0256)))
		-
		- Key idea: Locality and connection
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
			  $$
			  S_{B C}+S_C-S_B \geq S_{B B^{\prime} C}+S_C-S_{B B^{\prime}}
			  $$
				- It is just SSA.
			- Lemma 2.
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
			- Partial trace is linear and continuous.
		- Uniqueness on disks and spheres #card
			- ((65a0b3a4-23cb-4731-8cfa-5efaea070cdb)) For any disk-like subsystem $\omega$, the information convex set has only one element
			  id:: 65a0b37c-57fa-4a1b-b2f2-75dc9da2cab4
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
				- First, $\Sigma\left(S^2\right)$ obviously contains the global reference state.
				- By Prop 3.5, $\rho_{AC}$ and $\rho_{BC}$ are unique (the unique element of the ICS of disks).
				- Proposition. 
				  $$
				  I(A: C \mid B) \leq S(B C)+S(C)-S(B)
				  $$
					- This is the triangle inequality.
				- But RHS is zero, so LHS is zero and we can perform Petz recovery. Thus the global state is unique.
	- ## Elementary steps and the isomorphism theorem
		- The idea is to use our axioms to upper bound some mutual information in the Merging Lemma, thus allowing merging local pieces in local information convex sets.
		- Comment
			- Intuitively, we could define smooth deformation of subsystems by adding or removing a small disk.
				- This process keeps the topology of the subsystem invariant, but not all topologically equivalent subsystems could be connected!
			- This is the strategy of ((63fa1061-a719-42a4-8b01-2bd603e394fc))
		-
		- ((65ab6bb9-b42b-486b-9123-d6eac2533def)) Consider the partition in the figure. Let the domain of $\operatorname{Tr}_D$ and $\mathcal{E}_{C \rightarrow C D}^\sigma$ to be $\Sigma\left(\Omega^{\prime}\right)$ and $\Sigma(\Omega)$ respectively. Then
		  id:: 65ab6919-7791-414e-94b7-109b9b54b66e
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
			-
			- The [proof](((65bf86fe-054d-4214-ba38-e4a2f6c076ea))) is lengthy and highly technical. Let me omit it for now.
		- Corollaries
			- Corollary 3.9.1. (Distance preservation) Let $\rho_{\Omega}, \rho_{\Omega}^{\prime} \in \Sigma(\Omega)$ and $\rho_{\Omega^{\prime}}, \rho_{\Omega^{\prime}}^{\prime} \in \Sigma\left(\Omega^{\prime}\right)$. For any distance measure $D(\cdot, \cdot)$ between quantum states,
			  collapsed:: true
			  $$
			  D\left(\rho_{\Omega}, \rho_{\Omega}^{\prime}\right)=D\left(\mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}\right), \mathcal{E}_{C \rightarrow C D}^\sigma\left(\rho_{\Omega}^{\prime}\right)\right) \\
			  
			  D\left(\rho_{\Omega^{\prime}}, \rho_{\Omega^{\prime}}^{\prime}\right)=D\left(\operatorname{Tr}_D\left(\rho_{\Omega^{\prime}}\right), \operatorname{Tr}_D\left(\rho_{\Omega^{\prime}}^{\prime}\right)\right)
			  $$
				- Proof
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
		- Outline
			- First, note the factorization property of the fidelity $F(\rho, \tau)=(\operatorname{Tr} \sqrt{\sqrt{\rho} \tau \sqrt{\rho}})^2$.
			- Let $F_X$ be the fidelity of two extreme points in the information convex set of $X=L M R$ in Fig. 9(a). By using the fact that any extreme point has $I(L: R)=0$ ([Corollary D.5.1](((65e29dcb-82ba-4212-88f9-3bfa324fdcdd)))), we find
			  $$
			  F_{L R}=F_L F_R
			  $$
			- Somce the fidelity is non-decreasing under a partial trace, the isomorphism theorem implies $F=F_L=F_R=F_{L M R}$ and thus
			  $$
			  F \leq F^2 .
			  $$
			  $F \in[0,1]$.
			- Therefore, the two extreme points are **either the same** $(F=1)$ **or orthogonal** $(F=0)$.
	- Definition 4.2 (Vacuum). Let $\omega$ be a disk. For any annulus $X \subseteq \omega$
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
	  collapsed:: true
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
			- Note
				- The label is legitimate only if extreme points of $\Sigma(Y)$ are mapped to extreme points of $\Sigma(B_i)$ by partial trace.
					- $\operatorname{Tr}$ is a **surjective** linear map between ICSs doesn't suffice to show the fact.
					- This is proved in theorem 4.4
				- [Lemma 4.3](((65acb80a-219f-41c0-8de2-778437211ada))) guarantees the **uniqueness** of isomorphism, thus we could unambiguously label extreme points of different annuli by the same labeling set.
				-
		- ((6600f120-65f9-4c76-8ec8-1b96986038ec))
		  $$\Sigma(Y)=\bigoplus_{a, b, c \in \mathcal{C}} \rho_Y^{a b c}$$
			- Full statement
				- For a 2-hole disk $Y$, the information convex set $\Sigma(Y)$ is the following convex combination
				  $$
				  \Sigma(Y)=\left\{\rho_Y=\bigoplus_{a, b, c \in \mathcal{C}} p_{a b}^c \rho_Y^{a b c} \mid \rho_Y^{a b c} \in \Sigma_{a b}^c(Y)\right\},
				  $$
				  where $\left\{p_{a b}^c\right\}$ is a probability distribution.
			-
			- Proof
				- We only need to show that after the reduced density matrix of an extreme point of $\Sigma(Y)$ reduces to an extreme point of $\Sigma\left(B_1\right), \Sigma\left(B_2\right)$ and $\Sigma\left(B_3\right)$.
				- This fact follows from Lemma D.7 in the appendix, but is there a more general proof?
		- #+BEGIN_CAUTION
		  $\Sigma^c_{ab}$ is coherent, while $\Sigma(Y)$ is not.
		  #+END_CAUTION
		- Theorem 4.5. Consider a 2-hole disk $Y . \forall a, b, c \in \mathcal{C}$,
		  $$
		  \Sigma_{a b}^c(Y) \cong \mathcal{S}\left(\mathbb{V}_{a b}^c\right)
		  $$
		  where $\mathbb{V}_{a b}^c$ is a finite-dimensional Hilbert space.
	- ## Axioms of fusion rules
	  id:: 65adc655-d62f-4fe7-aa2a-1c590241c0bb
	  collapsed:: true
		- Proposition 4.6.
		  $$
		  N_{a b}^c=N_{b a}^c 
		  $$
			- Proof. We can construct a path exchanging two holes, thus $\Sigma^c_{ab} \cong \Sigma^c_{ba}$.
		- Proposition 4.7.
		  $$
		  N_{1 a}^c=N_{a 1}^c=\delta_{a, c}
		  $$
			- The hole with vacuum charge could be extended to a disk.
			- Then the inner annulus and the outer annulus could be connected via a path.
		-
		- For the remaining rules, we need a different technique, i.e. compare entropic differences before and after merging.
		- Merging of 2 annuli
			- ((65addd17-dcc9-41d1-8db4-5529793d8345))
			- Proposition. Conditions in the [Merging Lemma](((65ab687d-244f-4792-8b78-fabf3a6937a4))) are satisfied, so we have a unique merged state on the 2-hole disk.
				- The upper annulus is $A$, the lower annulus is $C$, with a disk-like regions $B$ in the middle.
				-
			- Proposition. From the merging lemma, we have
			  $$
			  S\left(\sigma_Y^{a \times b}\right)-S\left(\sigma_Y^1\right)=2 f(a)+2 f(b) .
			  $$
				- We need to use the merging lemma twice.
				- $$S(\sigma^{a \times 1})-S(\sigma^{1 \times 1})=2f(a) \\
				  S(\sigma^{a \times b})-S(\sigma^{a \times 1})=2f(b)
				  $$
				- Adding the two equations gives the result.
			- Proposition. The merged state is the maximal-entropy element in $\oplus_c \Sigma^c_{ab}(Y)$, with entropy
			  id:: 65addcba-e050-4ef6-86fe-754aaa68795d
			  $$
			  \begin{aligned}
			  & S\left(\sigma_Y^{a \times b}\right)-S\left(\sigma_Y^1\right) \\
			  & =f(a)+f(b)+\ln \left(\sum_c N_{a b}^c e^{f(c)}\right)
			  \end{aligned}
			  $$
				- Proof
					- The merged state has maximal entropy
						- First, note that we can rephrase SSA as $S_{ABC} \leq S_{AB}+S_{BC}-S_{B}$. The equality holds iff $I(A:C|B)$=0.
						- The axioms imply $I(A:C|B)$=0, thus the equality holds.
					- Calculation of the entropy
						- Lemma. $S\left(\sum_i p_i \rho^i\right)=$ $\sum_i p_i\left(S\left(\rho^i\right)-\ln p_i\right)$ if $\rho^i \cdot \rho^j=0, \forall i \neq j$
							- $\left\{p_i\right\}$ is a probability distribution ($p_i \in [0,1], \sum_i p_i=1$).
						- The full calculation is done in another paper 1810.01986, equation (14) to (15).
						-
			- Theorem. Compare the above two expressions, we obtain
			  $$
			  e^{f(a)} e^{f(b)}=\sum_c N_{a b}^c e^{f(c)}
			  $$
		- ((65af8780-6980-4953-a18c-de93249a5257)) 4.9. For each charge sector $a \in \mathcal{C}$, there is a unique sector $\bar{a} \in \mathcal{C}$ such that
		  $$
		  N_{a b}^1=\delta_{b, \bar{a}} 
		  $$
			- Proof
				- The key is the following picture to merge an annulus into the hole of another:
				  ((65af88da-ce0f-4365-b63a-bbffdd407dbf))
				- Why is the merging legitimate?
				  background-color:: red
				- Proposition. The global state exists and is unique.
					- Compatible on overlapping region:
					- Vanishing of CMI:
				- Proposition. 
				  $$
				  e^{f(a)}=\sum_b N_{a b}^1 e^{f(b)}
				  $$
				- Let us pick a sector $b$ such that $N_{a b}^1 \geq 1$. We can see that $e^{f(a)} \geq e^{f(b)}$. However, since $N_{a b}^1=N_{b a}^1$, by repeating the same logic we obtain $e^{f(b)} \geq e^{f(a)}$. For both of them to be true, we must have a unique sector $\bar{a}$ such that $N_{a b}^1=\delta_{b, \bar{a}}$ and $f(a)=f(\bar{a})$. Then it follows from $N_{11}^1=1$ that $\overline{1}=1$. Since $N_{\bar{a} a}^1=N_{a \bar{a}}^1=1$, we have $\overline{\bar{a}}=a$.
			- We can easily derive the following properties.
			  $$
			  \overline{1}=1, \quad \overline{\bar{a}}=a, \quad f(\bar{a})=f(a) .
			  $$
			-
		- Proposition 4.10.
		  $$
		  N_{a b}^c=N_{\bar{b} \bar{a}}^{\bar{c}}
		  $$
			- Proof
				- We need a different merging:
					- ((65af8b0f-a0d6-4b6a-957f-9a8d21dcecf7))
			- Then we can compare to the following diagram:
				- ((65af8b30-b5ad-48c7-9cc3-161494b47849))
			- Prop. Since the total charge is known to be 1, the left charge must be the anti-charge of the right.
			- Prop. If $a$ and $b$ are independently created (CMI vanishes),
			  $$
			  P_{(a \times b \rightarrow c)}=P_{(\bar{b} \times \bar{a} \rightarrow \bar{c})}
			  $$
				- This is still a blackbox for me.
			- The previous two propositions imply
			  $$
			  N_{a b}^c=N_{\bar{b} \bar{a}}^{\bar{c}}
			  $$
		- Proposition 4.11. The fusion rules are associative, i.e.,
		  $$
		  N_{a b c}^d=\sum_i N_{a b}^i N_{i c}^d=\sum_j N_{a j}^d N_{b c}^j .
		  $$
			- We need two different ways of merging.
			- The first is apparent:
			  ((65b06d41-17c2-4211-8e5f-0de2f4e912ec))
				- Key point
					- Merging of two extreme points is still an extreme point, from entropic relations
					- Merging of orthogonal extreme points are orthogonal, since fidelity is nondecreasing under partial trace.
				- This shows $N_{a b c}^d \geq \sum_i N_{a b}^i N_{i c}^d, N_{a b c}^d \geq \sum_j N_{a j}^d N_{b c}^j$
			- ((65b06d4b-bdbb-426a-817a-1bfeb3be5bde))
				- Input: Element of maximal entropy of 3 annuli,
				  $$
				  e^{f(a)} e^{f(b)} e^{f(c)}=\sum_d N_{a b c}^d e^{f(d)}
				  $$
				- Compare the element of maximal entropy of merging 2 annuli,
				  $$
				  e^{f(a)} e^{f(b)} e^{f(c)}=\sum_d\left(\sum_i N_{a b}^i N_{i c}^d\right) e^{f(d)}
				  $$
				- This proves the $\geq$ above must be replaced by $=$.
- # ((65b06f78-0eb4-454d-8efc-e5e2eeae8528))
  collapsed:: true
	- ((65ffd14b-9ae5-4444-b72a-0a9f08981e10)) For the Levin-Wen partition (Fig. 20(b)), it holds that
	  $$
	  I(A: C \mid B)_{\sigma^1}=2 \ln \mathcal{D} .
	  $$
		- ((65ffd160-2fba-46fd-ae5d-9d4d90a30676))
		- Proof
			- Consider the merging process from two (topologically) disks to an annulus
			  ((65ffd177-496f-43b9-9343-9192c16c1cc3))
			- Proposition. It is the maximal-entropy element of $\Sigma(X)$.
				- First, note that we can rephrase SSA as $S_{ABC} \leq S_{AB}+S_{BC}-S_{B}$. The equality holds iff $I(A:C|B)$=0.
				- The axioms imply $I(A:C|B)$=0, thus the equality holds.
			- Lemma. $S\left(\sum_i p_i \rho^i\right)=\sum_i p_i\left(S\left(\rho^i\right)-\ln p_i\right)$ if $\rho^i \cdot \rho^j=0, \forall i \neq j$
				- $\left\{p_i\right\}$ is a probability distribution ($p_i \in [0,1], \sum_i p_i=1$).
			- Note that the [Simplex Theorem](((65ac7c26-e36e-4d29-b316-da693a10f142))) tells us that different extreme points are orthogonal ($\sigma^a \cdot \sigma^b=0, \forall a \neq b$), so we can use the above Lemma.
			- Therefore, the entropy can be calculated by maximizing $\sum_i p_i\left(S\left(\rho^i\right)-\ln p_i\right)$ with the parameters $p_i$, with the constraint $p_i \in [0,1], \sum_i p_i=1$.
			- The maximization by Lagrangian multipliers is straightforward, with the result
			  $$
			  \tilde{\sigma}_X=\sum_a \frac{d_a^2}{\mathcal{D}^2} \sigma_X^a
			  $$
			- Plug in the probabilities $p_a=\frac {d_a^2}{D^2}$, we arrive at
			  $$
			  S\left(\tilde{\sigma}_X\right)-S\left(\sigma_X^1\right)=2 \ln \mathcal{D}
			  $$
- # ((65bf36a6-acad-4b0a-a4f6-54da71de3f20))
	- Theorem B.1. Let $M$ be a closed 2D manifold. Let $\sigma$ be a reference state on this manifold satisfying axiom $\mathbf{A 0}$ and $\mathbf{A 1}$. With respect to this reference state,
	  $$
	  \Sigma(M)=\mathcal{S}(\mathbb{V})
	  $$
	  for some finite dimensional Hilbert space $\mathbb{V} \subseteq \mathcal{H}$. Moreover, $\mathbb{V}$ is nonempty. #card
		- Why doesn't the same argument apply to arbitrary regions?
		  background-color:: red
		- Takeaway message
			- The main technique would be [Lemma A.1.(3)](((65bf06ea-128e-4b76-8ea9-fc14687d28fa))): For any expression of the form $\rho_{B C}=\sum_i q_i \rho_{B C}^i$, where $\left\{q_i\right\}$ is a probability distribution with $q_i>0, \forall i$ and $\left\{\rho_{B C}^i\right\}$ is a set of density matrices, we have
			  $$
			  \forall i, \quad \rho_C=\operatorname{Tr}_B \rho_{B C}^i
			  $$
				- Basically, it means that for a classical mix, any pure-state component would be consistent on $C$.
		-
		- Non-empty
			- Note that we started from a given reference state $\sigma$, which is surely in $\Sigma$.
		- Structure of $\Sigma$
			- Consider any state $\rho \in \Sigma(M)$ as
			  $$
			  \rho=\sum_i p_i|i\rangle\langle i|
			  $$
				- From ((659f5e4e-c195-40cc-8996-3a018dbe3604)), it is consistent with $\sigma$ on any disk of arbitrary size.
			- Consider the following region: a $\mu$-disk denoted as $c$ and an annulus that surrounds $c$, which we denote as $b$.
				- This annulus is chosen so that $b c$ is again a disk.
				- From ((659f5e4e-c195-40cc-8996-3a018dbe3604)), $\left(S_{b c}+S_c-S_b\right)_\rho=0$, which allows us to use Lemma A.1
				- By the lemma, for any $i$ we have
				  $$
				  \operatorname{Tr}_{M - c}(|i\rangle\langle j|)=\delta_{ij} \sigma_c
				  $$
				  which implies that any $\sum_i a_i |i\rangle$ is consistent with $\sigma$ on $c$.
				- This means that any $\sum_i a_i |i\rangle$ is in $\Sigma(M)$.
				-
- # ((65bf8707-fcea-4b97-9b4f-ab7db620f5d6))
  id:: 65bf86fe-054d-4214-ba38-e4a2f6c076ea
  collapsed:: true
	- Alternative definition of the information convex and equivalence #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2024-04-12T06:53:31.720Z
	  card-last-reviewed:: 2024-03-12T00:53:31.720Z
	  card-last-score:: 3
		- Takeaway message
			- We still require 'compatible with the reference state locally', but now we impose extra conditions on the **convex set** rather than the **reference state**.
			- The operation to enlarge a region by small disks is very important.
		- Definition C.1. Alternative definition $\hat{\Sigma}(\Omega)$ A set such that $\forall \rho \in \hat{\Sigma}(\Omega)$
		  collapsed:: true
		  (1) $\rho \stackrel{c}{=} \sigma_b \quad \forall \sigma_b \in \mu$.
		  (2) $I(A: C)_\rho=0$ for the partition in Fig. 1
		  (3) $I(A: C \mid B)_\rho=0$ for the partitions in Fig. 2
			- ((65c03c51-e00d-40b7-b1be-f3c5c78d217b))
			- ((65c03c5d-63d3-449e-8e62-1f84ed8dfff5))
		- Proposition C.1. $\hat{\Sigma}(\Omega)$ is convex.
		  collapsed:: true
			- Let $\rho_{\Omega}, \lambda_{\Omega} \in \hat{\Sigma}(\Omega)$. Consider the convex combination $p \rho_{\Omega}+(1-p) \lambda_{\Omega}$ where $p \in[0,1]$.
			- #+BEGIN_WARNING
			  Which properties are used and which properties are unused?
			  #+END_WARNING
				- Used
					- Inclusion and concavity of conditional mutual information
					- All states are consistent on $BC$
				- Unused
					- Topology of the configuration
			- (1) is obviously true.
			- (2)
				- Note that $\rho _{AC} =\rho _{A} \otimes \rho _{C}$ and $\lambda _{AC} =\lambda _{A} \otimes \lambda _{C}$ . Moreover, because $C$ is in a $\mu$-disk, $\rho _{C} =\lambda _{C} =\sigma _{C}$.
				- Therefore,
				  \begin{equation*}
				  c_{1} \rho _{AC} +c_{2} \lambda _{AC} =( c_{1} \rho _{A} +c_{2} \lambda _{A}) \otimes \sigma _{C}
				  \end{equation*}
				- #+BEGIN_TIP
				  Consistency provides factorization.
				  #+END_TIP
			- (3)
				- Consider the conditional mutual information of the convex combination.
				  $$I(A:C\mid B)_{p\rho +(1-p)\lambda } = ( S_{BC} -S_{B})_{p\rho +(1-p)\lambda } +( S_{AB} -S_{ABC})_{p\rho +(1-p)\lambda }$$
				- First, $BC$ is in a $\mu$-disk. Therefore, $S_{BC} -S_{B}$ is the same for $\rho ,\lambda$ and $c_{1} \rho +c_{2} \lambda$.
				- Second, conditional entropy is concave,
				  $$
				  \sum _{i} p_{i}( S_{AB} -S_{B})_{\rho ^{i}} \leq ( S_{AB} -S_{B})_{\sum _{i} p_{i} \rho ^{i}}
				  $$
				- Therefore,
				  $$
				  \begin{aligned}
				  I(A:C\mid B)_{p\rho +(1-p)\lambda } = & ( S_{BC} -S_{B})_{p\rho +(1-p)\lambda } +( S_{AB} -S_{ABC})_{p\rho +(1-p)\lambda }\\
				  = & p( S_{BC} -S_{B})_{\rho } +(1-p)( S_{BC} -S_{B})_{\lambda } +\\
				  & ( S_{AB} -S_{ABC})_{p\rho +(1-p)\lambda }\\
				  \leq  & p( S_{BC} -S_{B})_{\rho } +(1-p)( S_{BC} -S_{B})_{\lambda } +\\
				  & p( S_{AB} -S_{ABC})_{\rho } +(1-p)( S_{AB} -S_{ABC})_{\lambda } +\\
				  = & pI(A:C\mid B)_{\rho } +(1-p)I(A:C\mid B)_{\lambda }\\
				  = & 0
				  \end{aligned}
				  $$
		- ((65c0454e-d99f-4f62-9eb9-a0e803f7a810)) Consider two density matrices $\rho_{A B C} \in \Sigma(A B C)$ and $\lambda_{B C D} \in \bar{\Sigma}(B C D)$. If the following conditions hold, $\rho_{A B C}$ and $\lambda_{B C D}$ can be merged.
		  id:: 65c04522-0377-4566-8af4-71c167b534e3
		  collapsed:: true
		  (1) There exists a partition $B^{\prime} C^{\prime}=B C$, such that no $\mu$-disk overlaps with both $A B^{\prime}$ and $C D$; see Fig. 23.
		  (2) $\rho \stackrel{c}{=} \lambda$.
		  (3) $I(A: C \mid B)_\rho=I(B: D \mid C)_\lambda=0$.
		  (4) $I\left(A: C^{\prime} \mid B^{\prime}\right)_\rho=I\left(B^{\prime}: D \mid C^{\prime}\right)_\lambda=0$.
		  Moreover, the resulting density matrix is an element of $\hat{\Sigma}(A B C D)$.
			- Takeaway message
				- The proof is largely technical. No need to memorize the details.
				- The point is that we should always allow some sort of merging to **build global states from local states**.
			-
			- From the [merging lemma](((65ab687d-244f-4792-8b78-fabf3a6937a4))), we see that the state can be merged.
				- Note that the two different mergings corresponding to two different partitions give the same result.
				- This is because both of them satisfy $I(A: D \mid B C)$ and they have the same marginal on $A B C$ and $B C D$. Therefore, the merging lemma implies that $\tau_{A B C D}=\tau_{A B C D}^{\prime}$.
			- Below, we show that $\tau_{A B C D}$ is an element of $\hat{\Sigma}(A B C D)$ by checking the three conditions.
				- (1) is easy to check.
					- Because no $\mu$-disk overlaps with both $A B^{\prime}$ and $C D$, the overlap between a $\mu$-disk and $A B C D$ is either contained in $A B C$ or $B C D$.
				- (2)
					- ((65c0467f-673e-4b62-a58e-f040c2ff59b7))
					- Indeed, the merging maps we described above are instances of quantum channels. Therefore, the mutual information in the second condition is upper bounded by 0.
				- (3)
					- ((65c0467f-b2c0-48a6-93a6-a1e7f69b5e4a))
					- Similarly, the CMI is upper bounded by 0.
		- ((65c09487-a8fb-446f-943b-362b7066af60)) $\Sigma(\Omega)=\hat{\Sigma}(\Omega), \forall \Omega$.
			- Note that A0 and A1 are imposed on the global reference states, which is used in the proof.
			- If $\Omega$ is a closed manifold:
				- $\Sigma(\Omega) \supseteq \hat{\Sigma}(\Omega)$
					- Since there is no way of thickening at all.
				- $\Sigma(\Omega) \subseteq \hat{\Sigma}(\Omega)$
					- This is a direct corollary of the axioms.
			- If $\Omega$ has boundaries:
				- $\Sigma(\Omega) \subseteq \hat{\Sigma}(\Omega)$
					- (1) is trivially satisfied.
					- (2)(3) are implied by A0 and A1.
				- $\Sigma(\Omega) \supseteq \hat{\Sigma}(\Omega)$
					- Prop. Any $\rho_{\Omega} \in \hat{\Sigma}(\Omega)$ can be written as $\rho_{\Omega}=\operatorname{Tr}_{\Omega_\epsilon \backslash \Omega} \rho_{\Omega_\epsilon}$ for some element $\rho_{\Omega_\epsilon} \in \hat{\Sigma}\left(\Omega_\epsilon\right)$.
						- From [Prop C.2](((65c04522-0377-4566-8af4-71c167b534e3))), we can enlarge $\Omega$ repeatedly by small disks and merge the states.
						- It follows that $\rho_{\Omega} \in \Sigma(\Omega)$
	- Then we may transplant the merging theorem to the original definition of information convex.
- # ((65cac7b0-8727-41da-9429-4b67c92b7c59))
	- #+BEGIN_WARNING
	  All $\Omega$ in this section could have arbitrary topology, so A0 and A1 do not hold on $\Omega$ in general!
	  #+END_WARNING
	- Outline of the proof
		- Key properties
			- The Markov chain property allows factorization.
			- The isomorphism theorem provides a linear bijection, which puts very strong conditions on extreme points.
			- Finally, use fidelity.
		- ((6600ec74-ca4a-4549-b6c8-743cbca70fc6)) is a detour. It isn't used in the proof of the simplex theorem, but highly useful elsewhere.
	- Lemma D.1. Suppose $\rho_{\Omega_{2 \epsilon}} \in \Sigma\left(\Omega_{2 \epsilon}\right)$ can be written as
	  collapsed:: true
	  $$
	  \rho_{\Omega_{2 \epsilon}}=\sum_i q_i \rho_{\Omega_{2 \epsilon}}^i,
	  $$
	  where $\left\{q_i\right\}$ is a probability distribution with $q_i>0, \forall i$ and $\left\{\rho_{\Omega_{2 \epsilon}}^i\right\}$ is a set of density matrices. Then,
	  $$
	  \operatorname{Tr}_{\Omega_{2 \epsilon} \backslash \Omega} \rho_{\Omega_{2 \epsilon}}^i \in \Sigma(\Omega)
	  $$
		- Takeaway message
		  collapsed:: true
			- The lemma is similar to A.1, but with some differences:
			  collapsed:: true
				- The region might not be a disk, so A0 and A1 are not available.
				- The reduced density matrices might not be identical, only within $\Sigma(\Omega)$.
			- Though A0 and A1 do not hold on $\Omega$, they still hold on $\mu$-disks. Note that we only need to check $\mu$-disks to ensure that $\operatorname{Tr}_{\Omega_{2 \epsilon} \backslash \Omega} \rho_{\Omega_{2 \epsilon}}^i \in \Sigma(\Omega)$.
			  collapsed:: true
				- Again, local properties can be very different from global ones!
			- #+BEGIN_TIP
			  One good thing about quantum states: Though the whole state might not behave well due to nontrivial topology, we could always select a region with good topology and trace out all other parts!
			  #+END_TIP
	- Lemma D.2. (Markov-chain condition) Let $\Omega=A B C$. Suppose $B$ and $C$ are concentric annuli described in the figure. Then
	  id:: 65cae198-2cb5-449f-8ef0-071f54190611
	  collapsed:: true
	  $$
	  I(A: C \mid B)_\rho=0, \quad \forall \rho_{A B C} \in \Sigma(A B C) .
	  $$
		- ((65cae25f-faeb-48f4-b0ee-90da0e553699))
		- My own proof
			- Start from ((6590d78d-9c1a-4ba8-b099-a541a03cf94b)) and note that
			  $$S_{B C}+S_C-S_B \geq I(A: C \mid B)$$
				- Note $C$ here is the whole inner disk containing the hole.
			- Therefore RHS is 0.
			-
			- Since CMI is non-decreasing under inclusion of regions (non-increasing under deletion of regions), we see that 'removing the hole' doesn't increase CMI.
			-
		- The official proof is lengthy. Essentially it says that enlarging by $\mu$-disks preserves CMI.
			- What if $C$ is an arbitrary region? Could we use the same method to prove CMI=0?
	- ((65cae686-cb53-4873-9b60-e2ae9dd439f0)) All summands of an extreme points are mapped to the same extreme point, after tracing out the periphery.
	  collapsed:: true
		- Full statement
			- Consider an extreme point $\sigma_{\Omega_{2 \epsilon}}^{\langle e\rangle} \in \operatorname{Ext}(\Sigma\left(\Omega_{2 \epsilon}\right))$ written as
			  $$
			  \sigma_{\Omega_{2 \epsilon}}^{\langle e\rangle}=\sum_i q_i \rho_{\Omega_{2 \epsilon}}^i
			  $$
			  where $\left\{q_i\right\}$ is a probability distribution with $q_i>0, \forall i$ and $\left\{\rho_{\Omega_2 \epsilon}^i\right\}$ is a set of density matrices. Then,
			  $$
			  \operatorname{Tr}_{\Omega_{2 \epsilon} \backslash \Omega} \rho_{\Omega_{2 \epsilon}}^i=\operatorname{Tr}_{\Omega_{2 \epsilon} \backslash \Omega} \sigma_{\Omega_{2 \epsilon}}^{\langle e\rangle}, \quad \forall i
			  $$
			  doesn't depend on $i$ and is an extreme point of $\Sigma(\Omega)$.
		- Takeaway message
			- Proof
				- The [isomorphism theorem](((65ab6919-7791-414e-94b7-109b9b54b66e))) provides a linear isomorphisms between topologically equivalent subsystems. Note that linear isomorphisms preserve extreme points.
			- Rephrase
			  collapsed:: true
				- Systems of nontrivial topology may not behave so well, but the extreme points are special (restoring Araki-Lieb).
			-
	- ((6600ec74-ca4a-4549-b6c8-743cbca70fc6)) Saturation of Araki-Lieb for extreme points
	  collapsed:: true
		- Full statement
			- Consider an extreme point $\sigma_{\Omega_{2 \epsilon}}^{\langle e\rangle} \in \Sigma\left(\Omega_{2 \epsilon}\right)$ and let $B=\Omega_{2 \epsilon} \backslash \Omega$, then
			  $$
			  \left(S_{B \Omega}+S_{\Omega}-S_B\right)_{\sigma\langle e\rangle}=0 .
			  $$
		- Note that this holds for **arbitrary** regions, including n-hole disks.
		- Proof
			- Just combining Lemma D.3 and (3) -> (1) of Araki-Lieb saturation.
	- Lemma D.5. Extreme points of annulus has zero MI.
		- Full statement
		  collapsed:: true
			- Let $\Omega=A B C$ with a choice of subsystems described in the figure. If $\sigma_{\Omega}^{\langle e\rangle}$ is an extreme point of $\Sigma(\Omega)$ :
			  $$
			  I(A: C)_{\sigma\langle e\rangle}=0 .
			  $$
				- ((65cae25f-faeb-48f4-b0ee-90da0e553699))
		- Key points
			- Factorization of Markov state
	- Corollary D.5.1 and D.5.2. Full-factorization properties of extreme points
		- D.5.1. For the annulus $X=L M R$ in Fig. 9(a), for any extreme point $\sigma_X^a \in \Sigma(X)$
		  id:: 65e29dcb-82ba-4212-88f9-3bfa324fdcdd
		  $$
		  \operatorname{Tr}_M \sigma_X^a=\sigma_L^a \otimes \sigma_R^a,
		  $$
		  where $\sigma_L^a$ and $\sigma_R^a$ are the reduced density matrices of $\sigma_X^a$ on $L$ and $R$ respectively.
		- Corollary D.5.2. Consider the partition of a 2-hole disk $Y$ in the figure, i.e. $Y=Y^{\prime} B$ an $B=B_1 B_2 B_3$. Let $\sigma_Y^{\langle e\rangle}$ be an extreme point of $\Sigma(Y)$, then
		  collapsed:: true
		  $$
		  \left(S_{B_1}+S_{B_2}+S_{B_3}-S_B\right)_{\sigma\langle e\rangle}=0
		  $$
		  Equivalently, $\sigma_{B_1 B_2 B_3}^{\langle e\rangle}$ is a **tripartite product state**.
			- ((65adc919-5b80-4467-ba7f-55707d40ecf8))
	-
	- ## The Simplex Theorem
	  id:: 65e2a27d-aa9f-46fe-bd6b-0a23ea888db9
		- ((65e2a276-aefb-4d96-a726-9dffc714b2e9)) The info convex set of an annulus is the convex hull of **finitely** many **orthogonal** extreme points.
		  collapsed:: true
			- Comments
			  collapsed:: true
				- The finiteness condition is nontrivial. For example, $S^n$ doesn't satisfy it.
			- Takeaway message
				- Fidelity could be a useful quantification!
				- Key points in proof
					- We just need to prove orthogonality. Orthogonality implies finiteness.
					- Key properties
						- (1) The isomorphism preserves fidelity.
						- (2) Fidelity is non-decreasing under partial trace.
						- (3) Factorization property of extreme points and Fidelity.
					- Consider an extreme point $\sigma^a_X \in \Sigma(X)$ and corresponding extreme points $\sigma^a_L \in \Sigma(L)$, $\sigma^a_R \in \Sigma(R)$.
					- (1) -> $F\left(\sigma_X^a, \sigma_X^b\right)=F\left(\sigma_L^a, \sigma_L^b\right)=F\left(\sigma_R^a, \sigma_R^b\right)$
					- (2) -> $F\left( \sigma _{X}^{a} ,\sigma _{X}^{b}\right) \leq F\left(\operatorname{Tr}_{M} \sigma _{X}^{a} ,\operatorname{Tr}_{M} \sigma _{X}^{b}\right)$
					- (3) -> 
					  $$\begin{aligned}
					  F\left(\operatorname{Tr}_{M} \sigma _{X}^{a} ,\operatorname{Tr}_{M} \sigma _{X}^{b}\right) & =F\left( \sigma _{L}^{a} \otimes \sigma _{R}^{a} ,\sigma _{L}^{b} \otimes \sigma _{R}^{b}\right)\\
					   & =F\left( \sigma _{L}^{a} ,\sigma _{L}^{b}\right) \cdot F\left( \sigma _{R}^{a} ,\sigma _{R}^{b}\right)
					  \end{aligned}$$
					- Therefore, $F\left(\sigma_X^a, \sigma_X^b\right) \leq F^2\left(\sigma_X^a, \sigma_X^b\right)$, which means that $F \in \{0,1\}$.
					-
					-
				-
			- ((65e2a2df-2082-4cc1-ba09-feec370dda42))
- # ((65f3b8a1-abb4-4356-9f26-dd4f3fe1d04b))
	-