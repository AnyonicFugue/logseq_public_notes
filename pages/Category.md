alias:: Category Theory

- Definitions
  collapsed:: true
	- Higher cats
	  collapsed:: true
		- [[Morita equivalence]]
			- ((636df950-4025-47cd-8d13-1862db33b9e2))
			- Equivalent representations?
		- [[Functor]]
			- Equivalent categories
				- ((636ca710-55ab-45a0-aa16-0274e4ed00e4))
				- Theorem 3.3.52. A functor $F: \mathcal{C} \rightarrow \mathcal{D}$ between two categories $\mathcal{C}, \mathcal{D}$ is an equivalence **if and only if** it satisfies the following conditions:
				  1. (fully faithful) For any $x, y \in \mathcal{C}$, the map $F_{x, y}: \operatorname{Hom}_{\mathcal{C}}(x, y) \rightarrow \operatorname{Hom}_{\mathcal{D}}(F(x), F(y))$ is a bijection
				  2. (essentially surjective) For any $z \in \mathcal{D}$, there exists an object $x \in \mathcal{C}$ such that $F(x) \simeq z$.
		- [[Natural transformation]] #card
			- A family $\{\alpha_x\}$ such that ((636ca3f1-0eb2-4ab9-b618-e430f99c3d90))
			- [[Natural isomorphism]]
				- Each $\alpha$ is an isomorphism
		- [[Monoidal functor]]
			- Physical intuitions
				- 'Map and fuse' shall be isomorphic to 'fuse and map'
					- ((6376e69f-4dbd-4465-b405-49950dce1124))
		- [[Monoidal natural transformation]]
		- [[Braided Monoidal functor]]
			- Def
				- A monoidal functor with ((6376e81c-2e47-48db-8cd0-86df3405e14e))
				-
	- Additional structures
		- [[C-linear category]]
		- [[Semisimplicity]]
		- [[Monoidal structure]]
		- [[Dagger structure]] and Unitarity
		- [[Rigidity]] and [[Pivotal structure]]
		- [[Quantum dimension]] and [[Trace]]
		- [[Braiding]]
		- [[Ribbon]]
		- [[Central functor]]
	- [[Muger center]]
		- [[Nondegenerate]]
	- Some terminologie
		- [[Fusion category]]
		- [[Unitary modular tensor category]]
	- Idempotent #card
	  collapsed:: true
	  card-last-interval:: 10
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-11-23T04:13:40.734Z
	  card-last-reviewed:: 2022-11-13T04:13:40.735Z
	  card-last-score:: 5
		- A morphism with $$e=e^2:=e \circ e$$
		-
		- Split #card
			- An idempotent $e: x \rightarrow x$ splits if there exists an object $y \in \mathcal{C}$ equipped with two morphisms $r: x \rightarrow y, s: y \rightarrow x$ such that $r \circ s=\mathrm{id}_y$ and $s \circ r=e$.
			- The triple $(y, r, s)$ (or simply the object $y)$ is called an image of the idempotent $e$.
		- Idempotent complete
		  id:: 636ca217-d22e-42b8-984f-f4f35d530948
			- A category $\mathcal{C}$ where every idempotent in $\mathcal{C}$ splits.
	- Constructions
		- [[Deligne tensor product]]
		- Reversing some spacetime direction of a [[Topological Order]]
		  collapsed:: true
			- [[Time-reversed category]], $$\bar{\mathcal C}$$
			  collapsed:: true
				- ((6374412e-afc1-4336-b9a7-512c8faf35f6))
				- ((63744224-6f7c-4ae0-9d8c-64f7d4af6968)), thus reversing the [[Braiding]].
				- ((63744151-8b20-457e-bad9-68a4b50f626a))
				- ((637441ed-94ab-42c2-b10d-2e7d41c4c047)) #TODO
			- [[Space-reversed category]]
			- ((63744374-4dd7-4462-add5-bf48376f25f7))
			  collapsed:: true
				- In other words, only flips in different directions.
		- Opposite category $C^{op}$
		  collapsed:: true
			- Essentially reversing all morphisms.
			- ((636ca0b0-663c-4a6d-a73d-132541c72d7d))
		- [[Cartesian product]] of categories
		  collapsed:: true
			- ((636ca0e8-2319-486b-99ab-44be23202cff))
		- Full subcategory
		  collapsed:: true
			- A subcategory D of C with $$\operatorname{Hom}_{\mathcal{D}}(x, y)=\operatorname{Hom}_{\mathcal{C}}(x, y) \text { for all } x, y \in \mathcal{D}$$
			-
		- [[Drinfeld center]]
	-
- Examples
  collapsed:: true
	- Representation category, $Rep(G)$
	  collapsed:: true
		- Definition
			- $ob(\operatorname{Rep}(G))=$ finite-dimensional $G$-representations (over $\mathbb{C}$ )
			- Homs: Given two finite-dimensional $G$-representations $(V, \rho)$ and $(W, \sigma)$, a morphism $f:(V, \rho) \rightarrow(W, \sigma)$ is a $\mathbb{C}$-linear map $f: V \rightarrow W$ satisfying $f \circ \rho(g)=\sigma(g) \circ f$ for all $g \in G$
				- Morphism of Reps
			- The composition of morphisms is the usual composition of maps.
			- The identity morphism: Trivial Rep.
		- Possible [[Braiding]]s
			- Trivial
				- ((6371a32a-c4f5-4a03-8818-fee1cc406e72))
			- Fermion-parity, $$Rep(G,z)$$
				- Select some idempotent $$z\in G$$ and divide the vector space into 2 sectors
					- ((6371a387-c94a-48d1-a914-27aaaac3765d))
				- Define the parity according to the eigenvalue of $$\rho(z)$$
					- ((6371a394-fa3e-40b8-a95d-ca3756fe209c))
					- Since multiplication is associative, the braiding satisfy the hexagon equations.
				-
				- Similarly we may define $$\theta_{(V,\rho)}=\rho(z)$$ as a ribbon structure.
				-
	- Group-graded vector category, $Vec(G)$
	  collapsed:: true
	  id:: 636df91a-04a7-4d74-ab05-5c5939616e84
		- Definition
		  collapsed:: true
			- $ob(\operatorname{Vec}_G)=$ locally finite-dimensional G-graded vector spaces (over $\mathbb{C}$ ), i.e., a collection of finite-dimensional vector spaces $\left\{V_g \in \operatorname{Vec}\right\}_{g \in G}$. The direct sum $V:=\bigoplus_{g \in G} V_g$ is called the total space. By abuse of notation, we also use $V$ to denote this $G$-graded vector space.
			- **Hom:** Given two locally finite-dimensional $G$-graded vector spaces $V=\bigoplus_{g \in G} V_g$ and $W=\bigoplus_{g \in G} W_g$, a morphism from $V$ to $W$ is a collection of $\mathbb{C}$-linear maps $\left\{f_g: V_g \rightarrow W_g\right\}_{g \in G}$.
				- A hom for each space separately.
			- The composition of morphisms is given by the usual composition of maps in each degree $g \in G$.
			- The identity morphism $id_V$ on $V=\bigoplus_{g \in G} V_g$ is given by the usual identity map id $V_g$ on each degree $g \in G$.
		-
		-
		- Simple objects of $Vec_{\mathbb Z_2}$ : $(0,\mathbb C)$ and $(\mathbb C,0)$
		-
	- Modules over an algebra, $$\operatorname{LMod}_A(\operatorname{Vec})$$
	- Category associated to $$\mathfrak{sl_2}$$
		- See ((63759405-cb93-4086-954b-a1c7cff6925e))
			- ((63759549-ad49-406f-abb6-f76fc612e52e))
			- Also links to the [[Vertex operator algebra]]. See the references in Kong.
		- This gives the $$SU(2)_k$$ [[Topological Order]] .
			- k=3: The familiar [[Fibonacci anyons]]!
		- Seems to be links with the [[Quantum Group]]
		- Complete the details here: Fusion rules, braiding structures, quantum dimension. #TODO
		-
- Thoughts
	- Precise equivalence is often too strict a requirement. {{cloze Being isomorphic}} is usually enough, though it leaves for different structures.
	  id:: 6376e69f-4dbd-4465-b405-49950dce1124