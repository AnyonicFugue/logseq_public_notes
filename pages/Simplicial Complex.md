- In contrast to the singular theory, a $q$-simplex will once again be an honest space (and not a continuous map with domain $\Delta^q$ ).
	- A map contains much more information than a simple domain, e.g. orientation, boundary, etc.
-
- Why simplicial complexes?
	- Essentially, we convert a topological problem to a combinatorial problem, then it is easy to argue injectivity, surjectivity, etc.
	- On the other hand, due to the simplicial approximation theorem, we always have a simplicial map homotopic to the original one.
	  **Homotopy preserves all information we want.**
-
- # Definitions
  collapsed:: true
	- ((64b4848d-32de-4083-a028-c5424818237d))
	- Simplicial complex #card
	  card-last-interval:: 27.27
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-11-24T06:59:20.418Z
	  card-last-reviewed:: 2023-10-28T00:59:20.419Z
	  card-last-score:: 5
	  collapsed:: true
		- A finite collection of simplexes in some **Euclidean space** such that:
		- (i) if $s \in K$, then every face of $s$ also belongs to $K$;
			- We can always talk about boundaries and faces of any simplex.
		- (ii) if $s, t \in K$, then $s \cap t$ is either empty or a common face of $s$ and of $t$.
			- The sub-simplexes are always properly glued together, no 'mismatchings'.
		-
		- #+BEGIN_WARNING
		  Note this definition has an intrinsic weakness of viewing spaces as embedded in $\mathbb R^n$.
		  #+END_WARNING
		-
	- Underlying space $|K|$ of a simplicial complex $K$
	  collapsed:: true
		- If $K$ is a simplicial complex, its underlying space $|K|$ is the subspace (of the ambient euclidean space)
		  $$
		  |K|=\bigcup_{s \in K} s,
		  $$
		  the union of all the simplexes in $K$.
		- Proposition. $|K|$ is compact.
	- ((653a1102-9da2-4249-b0f3-31d698402124)) Polyhedron and Triangulation #card
	  collapsed:: true
		- A topological space $X$ is a **polyhedron** if there exists a simplicial complex $K$ and a homemorphism $h:|K| \rightarrow X$.
		- The ordered pair $(K, h)$ is called a **triangulation** of $X$.
		-
		- In plane English, $X$ is (homeomorphic to) some simplexes glued together.
		-
		- Examples
			- If $K$ is the family of all proper faces of an $n$-simplex $s$, then there is a triangulation $(K, h)$ of $S^{n-1}$. Denote this simplicial complex $K$ by $\dot{s}$. (Note that $|K|$ is the boundary $\dot{s} \approx S^{n-1}$, so that our two dot notations are compatible.)
			- A polyhedron that is not conventionally called so:
			  ![Image.png](../assets/Image_1698304601069_0.png)
				- Obviously it would not be called a manifold.
			- [[Torus]]
				- ((653a12a9-ada3-4cc1-9347-5dd5c2566ac2))
				- Inserting the diagonal $bd$ isn't a valid triangulation since the two triangles share the same vertices.
				  Recall that a simplicial complex is a collection of simplexes, which are solely determined by the vertices, in an Euclidean space.
	- ((653a14d2-9671-4f8f-a5aa-900e9a0b06ac)) The star of a vertex #card
	  collapsed:: true
		- Let $K$ be a simplicial complex and let $p \in \operatorname{Vert}(K)$. The star of $p$, denoted by $\operatorname{st}(p)$, is defined by
		  $$
		  \operatorname{st}(p)=\bigcup_{\substack{s \in K \\ p \in \operatorname{Vert}(s)}} s^{\circ} \subset|K|
		  $$
		- ((653a152e-159e-4b81-bf91-17675bf94100))
		- In plain English, the region spanned by the collection of all points with distance $1$.
	- Dimension of a simplicial complex
		- $$
		  \operatorname{dim} K=\sup _{s \in K}\{\operatorname{dim} s\}
		  $$
	- Subcomplex of a simplicial complex
	  collapsed:: true
		- A subcomplex $L$ of a simplicial complex $K$ is a simplicial complex contained in $K$ (i.e., $s \in L$ implies that $s \in K$ ) with $\operatorname{Vert}(L) \subset \operatorname{Vert}(K)$.
		- Note that $\mathrm{Sd} K$ is not a subcomplex of $K$ (nor is $K$ a subcomplex of $\mathrm{Sd} K$) since simplexes of neither is contained in the other.
	- $q$-skeleton
		- For any $q \geq-1$, the $q$-skeleton of $K$, denoted by $K^{(q)}$, is the subcomplex of $K$ consisting of all simplexes $s \in K$ with $\operatorname{dim}(s) \leq q$.
		-
- Theorem (Invariance of Dimension). If $K$ and $L$ are simplicial complexes and if there exists a homeomorphism $f:|K| \rightarrow|L|$, then $\operatorname{dim} K=\operatorname{dim} L$. #card
  collapsed:: true
	- A technical exercise. The proof doesn't contain much general insight, but mostly playing with some specific properties.
	-
	- Remark. It follows that one can define the dimension of a polyhedron $X$ as the common dimension of the simplicial complexes involved in triangulations of $X$.
	-
	- Proof. Assume, on the contrary, that $m=\operatorname{dim} K>\operatorname{dim} L=n$ (replacing $f$ by $f^{-1}$ handles the reverse inequality).
	- Take an $m$-simplex $\sigma$ in $K$, and let $\sigma^{\circ}=\sigma-\dot{\sigma}$ be its interior. Now $\sigma^{\circ}$ is an open set in $|K|$, by Exercise 7.4(ii).
	- Since $f$ is a homeomorphism, $f\left(\sigma^{\circ}\right)$ is open in $|L|$. There thus exists some $p$ simplex $\tau$ in $L$ (of course, $p \leq n<m$ ) with $f\left(\sigma^{\circ}\right) \cap \tau^{\circ}=W$, a nonempty open set in $|L|$.
	- Choose a homeomorphism $\varphi: \Delta^m \rightarrow \sigma$ with $\varphi\left(\dot{\Delta}^m\right)=\dot{\sigma}$; then $U$, defined by $U=\varphi^{-1} f^{-1}(W)$, is an open subset of $\left(\Delta^m\right)^{\circ}$.
	- Since $p<m$, there exists an imbedding $g: \Delta^p \rightarrow\left(\Delta^m\right)^{\circ}$ such that im $g$ contains no nonempty open subsets of $\left(\Delta^m\right)^{\circ}$.
	- Both $U$ and $g(W)$ are homeomorphic subsets of $\left(\Delta^m\right)^{\circ}$; as $U$ is open and $g(W)$ is not, which is a contradiction.
- # Simplicial Approximation
  collapsed:: true
	- #+BEGIN_NOTE
	  If we want a category whose objects are simplicial complexes, what are the morphisms?
	  #+END_NOTE
		- Obviously, the morphisms should preserve the simplicial properties.
	- ((653a1b1d-23b1-4b10-b964-05804ab0b2cc)) Simplicial map #card
	  card-last-interval:: 32.57
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-11-29T13:49:02.117Z
	  card-last-reviewed:: 2023-10-28T00:49:02.118Z
	  card-last-score:: 5
	  collapsed:: true
		- Let $K$ and $L$ be simplicial complexes.
		- A simplicial map $\varphi: K \rightarrow L$ is a function $\varphi: \operatorname{Vert}(K) \rightarrow \operatorname{Vert}(L)$ such that whenever $\left\{p_0, p_1, \ldots, p_q\right\}$ spans a simplex of $K$, then $\left\{\varphi\left(p_0\right), \varphi\left(p_1\right), \ldots, \varphi\left(p_q\right)\right\}$ spans a simplex of $L$.
		- The map do not need to be injective.
	- Theorem. If $\mathscr{K}$ consists of all simplicial complexes and all simplicial maps (with usual composition), then $\mathscr{K}$ is a category, and underlying defines a functor | $\mid: \mathscr{K} \rightarrow$ Top.
	- Definition. Piecewise linear #card
	  collapsed:: true
		- A map of the form $|\varphi|:|K| \rightarrow|L|$, where $\varphi: K \rightarrow L$ is a simplicial map, is called piecewise linear.
		- i.e. With a proper triangulation, $\varphi$ is linear in each simplex.
	- ((653a1b1d-23b1-4b10-b964-05804ab0b2cc)) Simplicial approximation #card
	  collapsed:: true
		- Motivation 1: Is there an obvious functor $\mathbf{Top} \to \mathbb{\mathscr{K}}$?
			- It further illustrates how category theory helps to **raise the correct question**!
			- However, naive attempts would fail: there are only finite simplicial maps, while there could be infinitely many non-homotopic maps, even between polyhedra.
			- For example,  if $K=L=\left\{\right.$ all proper faces of $\left.\left[p_0, p_1, p_2\right]\right\}$, then $|K| \approx S^1 \approx|L|$. Since $\pi_1\left(S^1\right) \cong \mathbf{Z}$, there are **infinitely** many nonhomotopic maps $f: S^1 \rightarrow S^1$, while there are still only **finitely** many simplicial maps $\varphi: K \rightarrow L$.
			  id:: 653cafe3-1003-41d0-b4fb-9d68194f91a9
		- Motivation 2.
		-
		- Let $K$ and $L$ be simplicial complexes, let $\varphi: K \rightarrow L$ be a simplicial map, and let $f:|K| \rightarrow|L|$ be continuous.
		- Then $\varphi$ is a **simplicial approximation** to $f$ if, for every vertex $p$ of $K$,
		  $$
		  f(\operatorname{st}(p)) \subset \operatorname{st}(\varphi(p))
		  $$
		-
		- A very strange condition... why's that?
			- Intuitively, a star doesn't include the boundaries. Since the image of different stars must be contained in corresponding stars, this means that the boundaries of the stars must be exactly in the boundaries of the corresponding stars.
			- i.e. the images are properly glued together.
				- Within the faces things are not so rigidly constrained.
		-
		- Proposition. If $\varphi$ is a simplicial approximation to $f$, then $\varphi \simeq f$.
			- Use the scaling trick.
	- Definition. Barycentric subdivision #card
	  collapsed:: true
		- Motivation
			- As shown in excision, we need to sometimes divide simplexes to obtain certain properties.
		- If $s$ is a simplex, let $b^s$ denote its barycenter. If $K$ is a simplicial complex, define $\operatorname{Sd} K$, the barycentric subdivision of $K$, to be the simplicial complex with
		  $$
		  \operatorname{Vert}(\operatorname{Sd} K)=\left\{b^s: s \in K\right\}
		  $$
		  and with simplexes $\left[b^{s_0}, b^{s_1}, \ldots, b^{s_q}\right]$, where the $s_i$ are simplexes in $K$ with $s_0<s_1<\cdots<s_q$.
			- Note that if $s$ is a vertex, then $b^s=s$, thus $\operatorname{Vert}(K) \subset \operatorname{Vert}(\operatorname{Sd} K)$.
			- $s_0<s_1<\cdots<s_q$ means that we should always divide a simplex **within itself**.
		- Example
			- If $\sigma=\left[p_0, p_1, p_2\right]$, then $\operatorname{Vert}(\operatorname{Sd} \sigma)=\left\{p_0, p_1, p_2, b_0, b_1, b_2, b^\sigma\right\}$
				- ((653cb1b6-f6b1-4685-94c6-6a0ab06be9bd))
			- Tetrahedron
				- ![Image.png](../assets/Image_1698476625600_0.png){:height 327, :width 239}
	- Definition. Mesh of a simplicial complex: If $K$ is a simplicial complex, then
	  $$
	  \operatorname{ mesh } K=\sup _{s \in K}\{\operatorname{diam}(s)\}
	  $$
	- ((654079ce-813e-4604-88ba-24ce10b5de48)) (Simplicial Approximation Theorem). If $K$ and $L$ are simplicial complexes and if $f:|K| \rightarrow|L|$ is continuous, then there is an integer $q \geq 1$ and a simplicial approximation $\varphi: \mathrm{Sd}^q K \rightarrow L$ to $f$. #card
	  collapsed:: true
		- Example. $|K|=|L|=S^1$
		  collapsed:: true
			- Consider the original triangulation into three segments.
				- ![Image.png](../assets/Image_1698478457504_0.png){:height 174, :width 398}
			- When the map is linear and the winding number $n=2$, we cannot find a simplicial approximation in the original triangulation.
			- However, we can further divide each original simplex into two:
				- ![Image.png](../assets/Image_1698478419953_0.png){:height 177, :width 416}
			-
			- The point is that after the division, the image of each open $q$-simplex would be inside another open $q$-simplex.
			- The next question is that whether they can be properly glued together. Here they are already so, but what about the general case?
		- Why is star needed?
		  collapsed:: true
			- Still consider $S^1 \to S^1$, but now the mapping ratio is irrational in some section, thus no matter how many times we perform subdivision, the barycenters would not be mapped to vertices in the target simplicial complex.
				- ![Image.png](../assets/Image_1698481697955_0.png){:height 320, :width 417}
			- If we require the image simplex is contained in a target simplex then it would fail, since no simplex could contain the 'crossing line section'.
			-
			- However, if we relax the condition to a star, it would become possible:
			  ![Image.png](../assets/Image_1698482103905_0.png){:height 338, :width 417}
			- $a_2$, $a_3$ could both be mapped to the blue point, then the two stars are both contained in the target star.
		- Step 1. Show that we can always perform subdivision to map stars into stars.
			- In short, the inverse images of stars in $L$ are open, thus they form a finite open cover of $|K|$.
			- Therefore there is a [[Lebesgue Number]]. Note also that a subdivision always reduces the diameter by half.
		- Step 2. Show that simplexes in $\varphi: \mathrm{Sd}^q K$ would be mapped into simplexes in $L$.
			- Observation. Let $q_0, q_1, \ldots, q_n \in \operatorname{Vert}(K)$. $\left\{q_0, \ldots,q_n\right\}$ spans a simplex of $L$ if and only if $\bigcap_{i=0}^n \operatorname{st}\left(q_i\right) \neq \varnothing$.
			-
			- Proposition. $\bigcap_{i=0}^m \operatorname{st}\left(p_i\right) \neq \varnothing$.
				- $$
				  \varnothing \neq f\left(\bigcap \operatorname{st}\left(p_i\right)\right) \subset \bigcap f\left(\operatorname{st}\left(p_i\right)\right) \subset \bigcap \operatorname{st}\left(\varphi\left(p_i\right)\right) .
				  $$
	- ((654245d1-f19a-4b5d-9b77-4a8f93adb8f0)) If $m<n$, then every continuous map $f: S^m \rightarrow S^n$ is nullhomotopic.
	  collapsed:: true
		- Intuitively, there are always enough dimensions in $S^n$ to collapse $f(S^m)$ to a single point.
		- Observations
			- Only dimensional arguments don't hold, since we have nontrivial loops $f: S^1 \to T^n$, which are both triangulable.
			- Therefore we must use some special properties of $S^n$.
			- ((65425a62-2e8d-4e18-916f-712a4b35c506))
			-
		- The proof is largely technical.
		- The key property used is that $S^n-\{x\}$ is contractible, which not quite a simplicial property. Thus the proof isn't quite 'fundamental'.
- # Abstract Simplicial Complex
  collapsed:: true
	- Why care about them?
		- Why simplicial complex?
			- A simplicial complex tells us how to 'glue simple things to obtain a space'. After that the problem becomes combinatorial.
		- Therefore, ASC should tell us how to 'glue simple objects for a set with a certain structure' and make the study easier.
		- Important objects and facts
			- Barycentric division
			- Approximation theorem
				- This should hint at 'weak equivalences' between sets with certain structures.
	- Definition. Abstract simplicial complex
	  collapsed:: true
		- Let $V$ be a (possibly infinite) set. An abstract simplicial complex $K$ is a set of finite nonempty subsets of $V$ (simplexes) such that:
			- (i) If $v \in V$, then the single-point set $\{v\}$ is a simplex, i.e. $\{v\} \in K$.
				- They might not be any subset of other simplexes, but they should be simplexes themselves!
			- (ii) If $s \in K, s' \sub S$, then $s' \in K$.
				- Sub-simplexes are also simplexes.
		- We denote $V=\operatorname{Vert}(K)$ (i.e. the vertex set).
		- A simplex having $q+1$ distinct vertices is called a $q$-simplex.
		-
		- Examples
			- Let $X$ be a topological space, and let $\mathscr{U}$ be a finite open cover of $X$. Define an abstract simplicial complex
				- Vertices are open sets in $\mathscr{U}$
				- Open sets $U_0, U_1, \ldots, U_q$ in $\mathscr{U}$ form a simplex if $\bigcap_{i=0}^q U_i \neq \varnothing$.
				- This simplicial complex is called the **nerve** of the open cover $\mathscr{U}$ and is denoted by $N(\mathscr{U})$.
			- Let $G$ be a finite group. Define an abstract simplicial complex $Q_p(G)$
				- The vertex set consists of all nontrivial $p$-subgroups (for some fixed prime divisor $p$ of $|G|)$
				- Some subgroups $P_0, P_1, \ldots, P_q$ forming a simplex if $\bigcap_{i=0}^q P_i \neq\{1\}$.
		- Comment
			- Essentially, we have a set of objects (points, open sets, subgroups, etc.) and 'form a simplex' roughly says 'the finite subsets of objects are compatible'.
			- Whenever a finite set of objects is compatible, its subsets should also be compatible.
	- Definition. Simplicial map
	  collapsed:: true
		- A map $\operatorname{Vert}(K) \to \operatorname{Vert}(L)$ such that whenever $\left\{v_0, \ldots, v_q\right\}$ is a simplex in $K$, then $\left\{\varphi v_0, \ldots, \varphi v_q\right\}$ is a simplex in $L$
		- Of course, it is possible that the latter list of vertices has repetitions, i.e. the image becomes degenerate.
	-
	-
- # Simplicial Homology
	- ## Definitions #card
		- ((654492a5-485c-46cd-ba7e-744404547c08)) Oriented Simplicial Complex
		  collapsed:: true
			- A simplicial complex $K$ with a partial order, such that the restriction to vertices of any simplex is a linear order.
			- Why not a full order on the whole complex?
			  background-color:: red
				- For simplexes with common faces, their ordering must be compatible, but the orders may not naturally merge.
				- In short, 'partial order' means $a<b>c$ or $a>b<c$.
				- For example,
				  ![Image.png](../assets/Image_1698993333587_0.png){:height 261, :width 455}
					- The two orderings are compatible, but they do not merge.
		- $C_q(K)$
		  collapsed:: true
			- An abelian group with the following presentation:
				- Generators
					- All $(q+1)$-tuples $\left(p_0, \ldots, p_q\right)$ with $p_i \in \operatorname{Vert}(K)$ such that $\left\{p_0, \ldots, p_q\right\}$ spans a simplex in $K$.
				- Relations
					- (i) $\left(p_0, \ldots, p_q\right)=0$ if some vertex is repeated;
					- (ii) $\left(p_0, \ldots, p_q\right)=(\operatorname{sgn} \pi)\left(p_{\pi 0}, p_{\pi 1}, \ldots, p_{\pi q}\right)$, where $\pi$ is a permutation of $\{0,1, \ldots, q\}$.
			- Intuitively, it is the 'free group generated by oriented simplexes'. The second relation is essentially defining equivalence of orientations.
		- Boundary map
		  collapsed:: true
			- $$
			  \partial_q: C_q(K) \rightarrow C_{q-1}(K), \\
			  \partial_q\left(\left\langle p_0, \ldots, p_q\right\rangle\right)=\sum_{i=0}^q(-1)^i\left\langle p_0, \ldots, \hat{p}_i, \ldots, p_q\right\rangle
			  $$
			  (where $\hat{p}_i$ means delete the vertex $p_i$ ) and extending by linearity.
		- Cycle, boundary and homology groups
		  collapsed:: true
			- $Z_q(K)=\operatorname{ker} \partial_q$, $B_q(K)=\operatorname{im} \partial_{q+1}$, $H_q(K)=Z_q(K) / B_q(K)$.
			-
		- Associated map of simplicial map
		  collapsed:: true
			- Let $K$ and $L$ be oriented simplicial complexes. If $\varphi: K \rightarrow L$ is a simplicial map, define $\varphi_{\#}: C_q(K) \rightarrow C_q(L)$, for each $q \geq 0$, by
			  $$
			  \varphi_{\#}\left(\left\langle p_0, \ldots, p_a\right\rangle\right)=\left\langle\varphi\left(p_0\right), \ldots, \varphi\left(p_a\right)\right\rangle .
			  $$
		- Relative homology group
		  collapsed:: true
			- If $L$ is a subcomplex of an oriented simplicial complex $K$ (with the inherited ordering), then the $q$ th relative simplicial homology group is
			  $$
			  H_q(K, L)=H_q\left(C_*(K) / C_*(L)\right) .
			  $$
		- [Euler-Poincare Characteristic](((65449fbd-691c-4c46-b321-9ac7fd2bd3c6)))
	- ## Setting up the Homology
		- Don't forget to check the functoriality!
		-
		- ### Basic Facts
			- Lemma. Let $K$ be an oriented simplicial complex of dimension $m$.
			  (i) $C_q(K)$ is a free abelian group with basis all symbols $\left\langle p_0, \ldots, p_q\right\rangle$, where $\left\{p_0, \ldots, p_q\right\}$ spans a q-simplex in $K$ and $p_0<p_1<\cdots<p_q$. Moreover, $\left\langle p_{\pi 0}, \ldots, p_{\pi q}\right\rangle=(\operatorname{sgn} \pi)\left\langle p_0, \ldots, p_q\right\rangle$.
			  (ii) $C_q(K)=0$ for all $q>m$.
			- Theorem. $C_*(K) := \{C_q(K),\partial_q\}$ is a chain complex.
				- Same argument as before.
			- Lemma. If $\varphi: K \rightarrow L$ is a simplicial map, then $\varphi_{\#}: C_*(K) \rightarrow C_*(L)$ is a chain map; that is, $\varphi_{\#} \partial=\partial \varphi_{\#}$.
		- Theorem. For each $q \geq 0, H_q: \mathscr{K} \rightarrow \mathbf{A b}$ is a functor.
		- The dimensional axiom holds trivially.
		- Theorem (Excision). If $K_1$ and $K_2$ are subcomplexes of a simplicial complex $K$ with $K_1 \cup K_2=K$, then the inclusion $\left(K_1, K_1 \cap K_2\right) \hookrightarrow\left(K, K_2\right)$ induces isomorphisms, for all $q \geq 0$,
		  $$
		  H_q\left(K_1, K_1 \cap K_2\right) \stackrel{\sim}{\rightarrow} H_q\left(K, K_2\right) .
		  $$
			-
	- ## Euler-Poincare Characteristic #card
	  id:: 65449fbc-6522-4b43-bfcc-1527128a2908
	  collapsed:: true
		- Definition
		  id:: 65449fbd-691c-4c46-b321-9ac7fd2bd3c6
			- Let $K$ be a simplicial complex of dimension $m$.
			- For each $q \geq 0$, let $\alpha_q$ be the number of $q$-simplexes in $K$.
			- The Euler-Poincaré characteristic of $K$, denoted by $\chi(K)$, is defined by
			  $$
			  \chi(K)=\sum_{q=0}^m(-1)^q \alpha_q .
			  $$
		- Theorem. If $K$ is an oriented simplicial complex of dimension $m$, then
		  $$
		  \chi(K)=\sum_{q=0}^m(-1)^q \operatorname{rank} H_q(K)
		  $$
			- We immediately see it is a very weak invariant, but nonetheless useful since it can be directly read off from the triangulation without any further calculation.
			- Observations
				- About rank
					- Rank has two distinct meanings. The first is the min. number of generators, while the second is the number of generators of the free-abelian part.
					- Let me take the second, since it satisfies $\operatorname{rank}(G/H)=\operatorname{rank}G-\operatorname{rank}H$.
					-
			- Key points
				- $$
				  \operatorname{rank} H_q(K)=\operatorname{rank} Z_q(K)-\operatorname{rank} B_q(K)
				  $$
				- $$
				  \alpha_q=\operatorname{rank} C_q(K)=\operatorname{rank} Z_q(K)+\operatorname{rank} B_{q-1}(K)
				  $$
			- Actually this result holds for **any** chain complex with each term free abelian.
	- ## Promote the functor to Polyhedra
	  collapsed:: true
		- Possible problems
			- Prove the invariance under equivalent triangulations.
			- We only have simplicial maps in the category of simplicial complexes, $\mathscr{K}$, while we have continuous maps between polyhedra.
				- Obviously we need simplicial approximations.
			- Then we need to prove the invariance under equivalent simplicial approximations.
		- ### Compare $H_q(K)$ and $H_q(\operatorname{Sd} K)$
			- Proposition. Let $K$ be a (finite) oriented simplicial complex of dimension $m$.
			  (i) $H_q(K)$ is f.g. (finitely generated) for every $q \geq 0$.
			  (ii) $H_q(K)=0$ for all $q>m$.
			  (iii) $H_m(K)$ is free abelian, possibly zero.
				- (i) is trivial.
				- (ii) Since $C_q(K)$=0.
				- (iii) The boundary is zero and the cycle part is necessarily free abelian.
					- More generally, ((65449dd9-071b-49c1-ac36-ba6a250956cc))
	-