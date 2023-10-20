- ![2020_Kong_Lan et al_Algebraic higher symmetry and categorical.pdf](file://zotero_link/Physics/Topological order/Higher Symmetry/2020_Kong_Lan et al_Algebraic higher symmetry and categorical.pdf)
- The key idea is that (conventional or higher) symmetries 1-1 corresponds to the bulk TO.
- # Setup
  collapsed:: true
	- The moduli space $\mathfrak{M}^{n+1}$
		- The space of Hamiltonians that support gapped liquid ground state.
		- An element in $\pi_0\left(\mathfrak{M}^{n+1}\right)$ is a gapped liquid phase, i.e. those could be connected by a smooth path are regarded as the same phase.
		- An element in $\pi_1\left(\mathfrak{M}^{n+1}\right)$ is a path connecting two Hamiltonians in the same phase.
		-
	- A topological order $\mathsf M ^{n+1}$
	- The category $\mathbb{T} \mathbb{O}^{n+1}$
		- The cat formed by $(n+1) \mathbf{D}$ topological orders
		- It consists of TOs, 1-codim domain walls, 2-codim domain walls, ...
	- The category $\mathbb{T} \mathbb{O}^{n+1}_{af}$
		- The cat formed by $(n+1) \mathbf{D}$ **anomaly-free** topological orders
	- Definition. Two anomaly-free topological orders $\mathrm{M}$ and $\mathrm{M}^{\prime}$ are called **equivalent** if they can be connected by an invertible domain wall $\hat{\gamma}$. We denote this isomorphism by $\mathrm{M} \stackrel{\hat{\sim}}{\simeq} \mathrm{M}^{\prime}$ or $\hat{\gamma}: \mathrm{M} \simeq \mathrm{M}^{\prime}$. The invertible domain walls are classified by $\pi_1\left(\mathfrak{M}^{n+1}\right)$.
	- The fusion n-cat formed by excitations of all codimensions, $\mathcal C^n$
		- Notation.
		  $$
		  \Omega \mathrm{C}^{n+1}:=\operatorname{Hom}\left(\mathrm{C}^{n+1}, \mathrm{C}^{n+1}\right)=\mathcal{C}^n
		  $$
	- The braided fusion (n-1)-cat formed by excitations of codimension larger than 1, $\Omega \mathcal C^n$
		- Or the 'looping'
	- Definition. A **symmetry** is simply a selection of a local operator algebra, called symmetric local operators.
	- Definition. Two symmetries are said to be **holographically equivalent** (holo-equivalent) if the linear algebras formed by $\{O\}$ and $\left\{O^{\prime}\right\}$ are isomorphic.
	- ((65309426-f07a-49a9-892b-a4c2ce7f111f)). An nd algebraic higher symmetry is **anomaly-free** if there exists a symmetric gapped Hamiltonian in the same dimension whose ground state is a non-degenerate product state.
		- In other words, the gapped ground state is non-degenerate for any closed space manifolds.
		- Such non-degenerate ground state is called trivial symmetric state.
		- The excitations on top of such a ground state are called charge objects, which carry "representations" of the algebraic higher symmetry.
	- ((65309cd5-1e26-4b78-a310-3bb67bfc27bc)). For an $(n+1) d$ anomaly-free topological order $\mathrm{M}$, the corresponding **categorical symmetry** is given by
		- A special boundary of $\mathrm{M}$ such that all the excitations in $\mathrm{M}$ are either condensed or have nearly zero energy gap. All the bulk excitations have an energy gap larger than a positive fixed value $\Delta_{\text {bulk }}$.
		- the symmetric local operators $\left\{O_{\mathrm{M}}\right\}$ are the local operators acting within the low energy boundary Hilbert space.
- # Main Results
	- $n$d potentially anomalous topological orders (without any symmetry) are classified, up to invertible topological orders, by fusion $n$-categories.
	  collapsed:: true
		- See [here](((65309257-62f9-488e-85fd-3cb7ef039005))).
	- The holographic principle. The excitations in the topological order $\mathrm{C}^{n+1}$, described by the fusion $n$-category $\Omega C^{n+1}$, can already uniquely determine the bulk anomaly-free topological order $\mathrm{M}^{n+2}$.
	  collapsed:: true
		- We denote the map from fusion higher categories $\Omega \mathrm{C}^{n+1}$ to topological orders $\mathrm{M}^{n+2}$ as
		  $$
		  \operatorname{bulk}\left(\Omega \mathrm{C}^{n+1}\right)=\mathrm{M}^{n+2}
		  $$
	- Proposition. Due to Tannaka duality, the fusion and braiding properties of G-excitations uniquely determine G.
	- ## Dual Symmetry
	  collapsed:: true
		- Better view a system with G-symmetry as the boundary of a bulk G-gauge theory.
		- Therefore there is a natural dual symmetry $\tilde G$ given by $(n-1)$-d gauge flux in the bulk.
		- If nothing is spontaneously broken, then the boundary must be gapless.
	- [Proposition](((65309eaf-96ed-43f1-b090-b0eb438bf10c))). Gapped liquid phases in $n$ d lattice systems with a fixed categorical symmetry $\mathrm{M}$ are classified by pairs $(\mathcal{C}, \hat{\gamma})$, where $\mathcal{C}$ is a fusion $n$-category that satisfies $\operatorname{bulk}(\mathcal{C})=\mathrm{M}$ and $\hat{\gamma}$ is an invertible domain wall in $\mathrm{M}$.
		- $\hat \gamma$ corresponds to the invertible part.
		- More specifically, we can use condensable algebras to perform the classification.