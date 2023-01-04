- Model
	- Group G.
	- There is a degree of freedom on each edge labeled by a group element.
		- Note that we may **reverse the orientation** by **substituting $g$ by $g^{-1}$**
	- $A_v=\frac{1}{|G|} \sum_{g \in G} A_v^g$
		- ![image.png](../assets/image_1671109047284_0.png)
		  outgoing orientation.
		- Note that different edges may be **entangled**.
	- $B_p=\delta g_1 ... g_N, e$
		- ![image.png](../assets/image_1671108991839_0.png)
		  orientation in the most natural way.
		- 'Flux free' condition
	- $H=-\sum_{v } A_v-\sum_{p } B_p$
- Properties
	- $A_v^2=A_v, \quad B_p^2=B_p$
		- **Projectors**. The eigenvalues can only be 0 or 1.
	- $\left[A_v, A_v'\right]=\left[B_p, B_{p^{\prime}}\right]=\left[A_v, B_p\right]=0$
		- Simultaneously diagonalizable.
- Solution
	- Degeneracy #card #Learning-TODO
		- For $G$ abelian, $G S D_{\text {torus }}=|G|^2$
		- For $G$ nonabelian, $G S D_{\text {toms }}=\sum_A \# \operatorname{irrep}\left(Z^A\right)$
			- Number of irreps of centralizers of conjugacy classes
	- Anyon types #card #Learning-TODO
	  card-last-interval:: 16.67
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-01-01T21:52:33.349Z
	  card-last-reviewed:: 2022-12-16T05:52:33.350Z
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