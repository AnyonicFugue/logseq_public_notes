- Description of the [[Boundary]]
  collapsed:: true
	- Boundaries of the [[Toric code]] #card
	  card-last-interval:: 10
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-12-24T05:57:49.474Z
	  card-last-reviewed:: 2022-12-14T05:57:49.475Z
	  card-last-score:: 5
		- ((6376e089-fce4-4848-81c9-ba80dc22e8ff))
			- ((6376e0a2-267d-44b2-b4ce-07caab40cd56))
		- [[Smooth boundary]]
		  collapsed:: true
			- ((6376e003-91e9-4f72-b8b3-c3f649b36388))
			- ((6376e048-b064-4620-9051-da7a913415c6)) m can be annihilated by $$\sigma_x$$ on the boundary.
			-
			-
		- [[Rough boundary]]
		  collapsed:: true
			- ((6376e016-4480-4dcb-898f-460d62d7f0fb))
			- Similarly, simple excitations are 1 and M.
		- Do we lose information on the boundary, since e and 1 seems indistinguishable on the rough boundary? #card
		  collapsed:: true
		  card-last-interval:: 10
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2022-12-18T02:06:43.018Z
		  card-last-reviewed:: 2022-12-08T02:06:43.019Z
		  card-last-score:: 5
			- NO.
			- We can use [[Braiding]] to reveal that the type of excitation exists in the bulk.
				- ((6376e2ef-953a-42f0-9245-45df8de79bf6))
				- ((6376e31a-a14e-46b3-b327-677c2cdfa16d))
			- Note that **there are no e present on the boundary**. We just used a string operator associated with e.
			  In other word, the existence of such nontrivial string operator reveals the type in the [[Bulk]].
		- ((637ad557-7f50-4769-bbd9-12670b94f740))
			- Somewhat analogous to 'inequivalent homotopies between two paths'.
- Structures and properties
  collapsed:: true
	- ((6376e3e8-d3ef-44b3-9d52-30e6d6c3f9eb))
	- [[Bulk-boundary relation]]
		- Theorem about the [[bulk-to-boundary map]] #card
		  card-last-score:: 5
		  card-repeats:: 2
		  card-next-schedule:: 2022-12-20T11:43:59.656Z
		  card-last-interval:: 10
		  card-ease-factor:: 2.46
		  card-last-reviewed:: 2022-12-10T11:43:59.658Z
			- ((637ad40d-928c-428f-b8be-6efaaffb1156))
			  id:: 637ad30c-703e-4c78-b175-4d60505f6af0
				- Which conditions are necessary?
			- (a) The bulk-to-boundary map $F: \mathcal{C} \rightarrow \mathcal{A}$ is a [[Central functor]].
			  (b) The central structure $F^{\prime}: \mathcal{C} \rightarrow \mathfrak{Z}_1(\mathcal{A})$ is a braided equivalence.
				- (b) gives an interesting restriction: An anomaly-free stable 2D topological order must be a [[Drinfeld center]] of something else.
				- Conversely, the theorem immediately implies that the [[Drinfeld center]] is nondegenerate. Mathematically, ((637ad683-2c60-43af-868c-f7eaacd40528))
			- ((637ad518-c09e-4960-9608-372911a8e757))
		- ((637ad78a-4267-428e-84b3-f93291247476))
-
- 1D [[Domain walls]]
	- Defs
	  collapsed:: true
		- [[Invertible]] domain walls
		  collapsed:: true
			- ((6396c8ae-1392-44c2-9548-289c962b426b))
			- $M \otimes_{\mathrm{D}} \mathrm{N}=\mathrm{C}_1, \quad \mathrm{~N} \boldsymbol{\otimes}_{\mathrm{C}} \mathrm{M}=\mathrm{D}_1$
			  collapsed:: true
				- Indeed, the inverse $\mathrm{N}$, if exists, must be the time-reversal $\overline{\mathrm{M}}$ by a general argument.
				- Quite strange. Another domain wall fuses D into C?
				  background-color:: red
	- [[Fusion]] of domain walls
	  collapsed:: true
		- ((6396c7da-7ad3-4b94-bec5-0391f39cd6ab))
		  collapsed:: true
			- If D is trivial this is just stacking. Otherwise, interesting things might happen.
			- ((6396c828-35e5-4c50-ac66-97596bf4c794)) $\mathcal{M} \otimes_{\mathcal{D}} \mathcal{N}$ only depends on the multi-fusion categories $\mathcal{M}, \mathcal{N}$, the braided fusion category $\mathcal{D}$ and the multi-fusion module structures of $\mathcal{M}, \mathcal{N}$ over $\mathcal{D}$.
			  collapsed:: true
				- In other words, it smooths out all details!
	- Move particle-like [[Topological excitation]] across the invertible domain wall #card
	  collapsed:: true
		- ((6396c9bd-f680-4a7d-b1e5-d9f8de7ae7ff))
		  collapsed:: true
			- The second step holds only when M is invertible.
		- Since we can also move anyons from C to D, $x \mapsto \phi(x)$ defines a **braided equivalence** $\phi: \mathcal{D} \rightarrow \mathcal{C}$.
		- Thus we have a **group homomorphism** from the group of braided autoequivalences of $\mathcal{C}$ (with composition) to the group of equivalence classes of invertible fusion $(\mathcal{C}, \mathcal{C})$-bimodules (domain walls) (with fusion).
		- ((6396cb2f-4bd5-4007-8a41-368b75419231))
		-
	- Folding trick #card
	  card-last-interval:: 10
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2022-12-22T05:52:53.596Z
	  card-last-reviewed:: 2022-12-12T05:52:53.596Z
	  card-last-score:: 5
	  collapsed:: true
		- ((637ad93c-b21f-446d-9d6c-54b25d5ddff7))
		- Seems quite strange but interesting.
		- How can you fold a torus? Or just fold locally, not globally?
		- Intuitively, we have the following structures
		  collapsed:: true
			- Left [[bulk-to-boundary map]] $F: \mathcal{C} \rightarrow \mathcal{M}$ and the right one $G: \overline{\mathcal{D}} \rightarrow \mathcal{M}$. Note that D is a [[Time-reversed category]]
			- The total [[bulk-to-boundary map]] $F \times G: \mathcal{C} \times \overline{\mathcal{D}} \rightarrow \mathcal{M}$
			  collapsed:: true
				- Actually the [[Deligne tensor product]], but I don't know how to type it in LaTex.
			-
	- [[Multi-fusion modules]]
	  collapsed:: true
		- Def #card
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.36
		  card-next-schedule:: 2022-12-06T06:34:55.132Z
		  card-last-reviewed:: 2022-11-26T06:34:55.132Z
		  card-last-score:: 3
		  collapsed:: true
			- ((6396c42e-78cc-49aa-9862-fb85bef0c8d0)) Let $\mathcal{C}, \mathcal{D}$ be braided fusion categories.
			- (1) A (multi-)fusion left $\mathcal{C}$-module is a (multi-)fusion category $\mathcal{M}$ equipped with a braided functor $F: \mathcal{C} \rightarrow \mathfrak{Z}_1(\mathcal{M})$. It is called closed if $F$ is an equivalence.
			- (2) A (multi-)fusion right $\mathcal{D}$-module is a (multi-)fusion category $\mathcal{M}$ equipped with a braided functor $G: \overline{\mathcal{D}} \rightarrow \mathfrak{Z}_1(\mathcal{M})$. It is called closed if $G$ is an equivalence.
			- (3) A (multi-)fusion ( $(\mathcal{C}, \mathcal{D})$-bimodule is a (multi-)fusion category $\mathcal{M}$ equipped with braided functors $F: \mathcal{C} \rightarrow \mathfrak{Z}_1(\mathcal{M})$ and $G: \overline{\mathcal{D}} \rightarrow \mathfrak{Z}_1(\mathcal{M})$. It is called **closed** if $F \otimes G: \mathcal{C} \otimes \overline{\mathcal{D}} \rightarrow \mathfrak{Z}_1(\mathcal{M})$ is an **equivalence**.
			- A boundary with a bulk-to-boundary map as an action
	- Examples
		- The trivial domain wall
		  collapsed:: true
			- Obtained by restricting a topological order to a line
			- Topological skeleton: Same as $\mathcal C$
			- Fusion module: braided functor $\mathcal{C} \otimes \bar{C} \rightarrow \mathfrak Z_1(\mathcal{C})$,
			  collapsed:: true
				- This is quite interesting.
		- Anyon-permuting domain wall
		  collapsed:: true
			- For a braided autoequivalence $\phi: \mathcal{C} \rightarrow \mathcal{C}$, construct
			  collapsed:: true
			  $$
			  \mathcal{C} \otimes \overline{\mathcal{C}} \stackrel{\operatorname{id_{\mathcal C}} \otimes \phi}{\longrightarrow} \mathcal{C} \otimes \overline{\mathcal{C}} \rightarrow \mathfrak{Z}_1(\mathcal{C})
			  $$
				- Actually Deligne tensor products.
			- Intuitively, the anyons on the right side are permuted by $\phi$.
		- Gapped 1D domain walls in [[Toric code]]
			- ((6396cfd2-fc56-46df-9ec7-b97a3ddf7bd5))
			  collapsed:: true
				- A natural problem: How are we sure that they are the only examples? #Learning-TODO
			- Non-invertible ones
				- ((6396cfdd-67ea-4977-a4ab-4f34abe42fb9))
					- This notation suggests that the walls are viewed as fusions of the boundaries
					- Why noninvertible?
					  collapsed:: true
						- Intuitively, some bulk excitations can't be recovered if they come into the wall.
					-
				- We examine the first as an example.
				  collapsed:: true
					- Bulk-to-boundary map
					  collapsed:: true
						- The right one is $\mathbb{1}, m \mapsto \mathbb{1} \otimes \mathbb{1}, \quad e, f \mapsto \mathbb{1} \otimes E$.
						- Similar for the left one.
					- 4 excitations
					  collapsed:: true
						- $1\otimes 1, 1\otimes 1, E\otimes 1, E\otimes E$
				- Prop. The domain walls are indeed different. #card
				  collapsed:: true
					- First, what is 'different'?
					  collapsed:: true
						- There are no braided equivalences between them which preserves the bulk-to-boundary map.
					- In this case it is obvious; just examine the kernel of the bulk-to-boundary map.
			- Invertible ones #card
				- Trivial wall
				- Dislocation
				  collapsed:: true
					- ((6396d07b-023c-4673-b778-cc1e03d629db))
						- $B_p=\sigma_z^1 \sigma_z^2 \sigma_z^3 \sigma_x^4$ and $B_q=\sigma_z^5 \sigma_z^6 \sigma_z^7 \sigma_x^8$
						  collapsed:: true
							- Be careful that the last operator is $\sigma_x$.
							- This is reasonable to preserve commutativeness of operators.
						- Very interesting. But how do they come up with such construction?
					- 4 excitations
						- $\mathbb 1$, $X$ for $B_p=-1$, $Y$ for $B_q=-1$, $Z=X\otimes Y$
					- Fusion rules
						- $X \otimes X=Y \otimes Y=Z \otimes Z=\mathbb{1}, X \otimes Y=Y \otimes X=Z$
					- Bulk-to-wall map #card
						- Move m to the wall as usual. Become X on the same side.
						- Move e to the wall by $\sigma_z$. Become X **on the opposite side**.
					- Move particles across the domain wall #card
					  card-last-interval:: 12.82
					  card-repeats:: 1
					  card-ease-factor:: 2.6
					  card-next-schedule:: 2022-12-28T00:26:14.258Z
					  card-last-reviewed:: 2022-12-15T05:26:14.259Z
					  card-last-score:: 5
						- m is easily recovered by moving back to the same side.
						- We notice that $X$ becomes $e$ on the other side with an action of $\sigma_z^4$.
							- The interesting thing happens: **The anyon type flips when crossing the wall**!
							- ((6397d5cf-973b-4b7d-9ffd-56379c4d8b84))
				- Let's now stand a bit higher to look at the things.
				  collapsed:: true
					- These are the only two automorphisms of TC.
						- Somewhat analogous to [[Galois Theory]]? #Possibility
							- Can we define a fusion of the roots of a polynomial?
							- Seems that the fusion channels must be simple, since we don't have a natural definition of direct sums of numbers (except addition)
							- What if we view the extension as a linear  space spanned by the Irrs?
					- Non-invertible ones are the (noninvertible) endomorphisms.
			- [[Fusion rules]] of the domain walls #card
				- ((6397d84a-bb0f-4e71-93b8-5077ea559ddb))
					- I would have written $$SWAP \otimes SWAP = \mathcal{TC}_1$$.
					- What does this notation mean? #Learning-TODO
						- Maybe the folding trick. Fuse domain walls <-> stack 2 'half-plane' topo orders
				- ((6397d8c8-261e-4b5e-8bb6-0dff22e5daec))
				- ((6397d8cf-5735-4cb5-a000-e3edcf67c3a6))
-
-