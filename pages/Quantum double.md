- # Model
	- Group G.
	- There is a degree of freedom on each edge labeled by a group element.
	  collapsed:: true
		- Note that we may **reverse the orientation** by substituting $g$ by $g^{-1}$
	- ## Lattice
		- $A_v=\frac{1}{|G|} \sum_{g \in G} A_v^g$
		  collapsed:: true
			- ![image.png](../assets/image_1671109047284_0.png)
			  outgoing orientation.
			- Note that different edges may be **entangled**.
		- $B_p=\delta g_1 ... g_N, e$
		  collapsed:: true
			- ![image.png](../assets/image_1671108991839_0.png)
			  orientation in the most natural way.
			- **The order of the multiplication is important. Group elements of adjacent edges must be adjacent in the expression.**
			  collapsed:: true
				- Generally the group is nonabelian.
			- 'Flux free' condition
		- $H=-\sum_{v } A_v-\sum_{p } B_p$
	- ## Continuum
	  collapsed:: true
		- The edges are dual to themselves, so no need to worry.
		- Dancing rules
			- Isotopy
			- Adding or removing contractible loops
				- ((63c35e83-e9eb-4022-8ba1-d78433fb3a41))
			- F-move
				- ((63c35db9-7581-4bb9-b557-8a4f428fb71e))
					- The move can be better memorized on the dual lattice, where the total charge of a vertex is zero.
				- Note that it is the trivial one. Other nontrivial ones are also possible; they're called [[Twisted Quantum Double]].
				- It's the third move in toric code, with $ab=ca=e$. So the inner vertex is vacuum.
		- Corollary
		  collapsed:: true
			- ((63c36205-6142-426d-b135-78ed41fc12f2))
				- Note that ![image.png](../assets/image_1673750138277_0.png)
					- Cut some threads open to invoke the moves! #Strategy
				- i.e. An internal loop is also contractible.
			- ((63c35e34-0bb7-4b7e-80ff-9801ce4c1143)) #Learning-TODO
				- The first step uses F-move.
				- The second step invokes the above corollary.
				- $\times$ in the middle means that we **cannot** remove the loop by rule 2, but should merge it with the edges.
				- Therefore, ((63c366db-187f-4c87-b7ff-e47dc4bde837))
					- ((63c366e4-dfa4-4466-a587-8b6f8d1e7512))
- # Properties
	- $A_v^2=A_v, \quad B_p^2=B_p$
		- **Projectors**. The eigenvalues can only be 0 or 1.
	- $\left[A_v, A_v'\right]=\left[B_p, B_{p^{\prime}}\right]=\left[A_v, B_p\right]=0$
		- Simultaneously diagonalizable.
	- The ground state is topological, i.e. independent of the details of the lattice.
		- Proof strategy: Find a set of **generating moves** and prove the model is invariant under them.
		- ((63c35d0a-d99c-40d3-9a33-0e1ab6b67f35))
			- The internal vertex is fixed. No extra d.o.f.
		- ((63c35d32-495b-46d6-b8a8-ca80a077ee6b))
		-
- # Solution
	- GSD on a torus #card
		- Idea: Since it is topological (independent of the details), we may examine a minimal lattice.
			- Note that the analysis is given on the dual lattice.
			- **It seems more complicated on the original lattice. Or did I make mistakes?**
		- ((63c3b5c4-31cd-4d46-ac19-ea191ea27c71))
			- One plaquette, two edges.
		- Vertex condition -> $ab=ba$
		- Plaquette condition -> $\left|\Psi_{b, a}\right\rangle \propto \hat{P}_\beta|b, a\rangle \propto \sum_{h \in G}\left|h b h^{-1}, h a h^{-1}\right\rangle$
		-
		- Prop. $G S D_{\text {torus }}=\sum_A \# \operatorname{irrep}\left(Z^A\right)$.
			- Corollary. For $G$ abelian, $G S D_{\text {torus }}=|G|^2$
	- Anyon types #card #Learning-TODO
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-02-03T01:15:20.610Z
	  card-last-reviewed:: 2023-01-10T01:15:20.611Z
	  card-last-score:: 5
		- Abelian
			- $|G|$ G-charges, $|G|$-fluxes.
			- $|G|^2$ anyon types $=G S D_{\text {torus }}$
		- Non-abelian
			- Fluxes labeled by **conjugacy classes** $A$
				- Action of $A^v_h$ takes $g_1...g_n$ to $hg_1...g_nh^{-1}$
				- $A^v$ is the equal sum of all 'inner automorphisms'
			- Charges labeled by **irreps** of $Z^A$
			- Thus each anyon labeled by a **pair** $(A, \mu)$.
			- Wan argued from a gauge theory perspective.
				- Flux <-> [[Holonomy]]. **Invariant** under gauge transformations where $h \rightarrow g h g^{-1}$, thus the notion of conjugacy classes.
				- Charges shall be invariant under the actions of fluxes. 'Invariant' is expressed by centralizers.
			- ### Still $\text{\# anyon types}=GSD_{torus}$
			  heading:: 3
- Quantum double [[Category]]
	- See ((63744ba1-f824-4527-870b-0bd482b3bacc))
- Explore the example of $Z_n$ quantum double. #Learning-TODO [#A]
	- Ground states, excitations, fusion rules, braidings, S and T matrices.
	- Is the presentation on Topobook (Z_n toric code) equivalent to Z_n quantum double?