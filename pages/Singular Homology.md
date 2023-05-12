- Idea #card
	- [[Green's Theorem]] tells us that we can determine the behavior of the bulk by its boundary.
	  We'd like to generalize this into topology.
	- Furthermore, a 'hole' in a space is implied by the existence of some **cycle** which is not a **boundary**.
		- The intuition comes from $S^1$ in $\mathbb R^2-0$.
		- However, note that a single point is a cycle but not a boundary.
- # Defs
  collapsed:: true
	- ## About Orientations
	  collapsed:: true
		- Def. Orientation #card
		  id:: 642578ff-9703-449c-b3df-41ffc344e641
		  collapsed:: true
			- An orientation of $\Delta^n=\left[e_0, e_1, \ldots, e_n\right]$ is a linear ordering of its **vertices**.
			  collapsed:: true
				- For a line segment, it is an ordering of the two endpoints.
			- Two orientations of $\Delta^n$ are the same if, as permutations of $\left\{e_0, e_1, \ldots, e_n\right\}$, they have the same **parity** (i.e., both are even or both are odd); otherwise the orientations are opposite.
			  collapsed:: true
				- Note that simplex can only have two different orientations.
			- It's amazing that such a simple definition grasps our intuition of orientation (or 'inside' and 'outside')!
			  collapsed:: true
				- Moreover, similar ideas appear in the definition of differential forms.
		- Induced orientation
		  id:: 6438bf08-5df7-4653-a22c-f97564f2812d
		  collapsed:: true
			- Given an orientation of $\Delta^n$, there is an induced orientation of its faces defined by orienting the $i$ th face in the sense $(-1)^i\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$
		- Example. Verify the induced orientation of $\Delta^2$, $[e_0,e_1,e_2]$, is compatible with the original one.
		  collapsed:: true
		  ![image.png](../assets/image_1681440654144_0.png){:height 336, :width 409}
			- The boundary of $\Delta^2$ is
			  $$
			  \left[e_1, e_2\right] \cup\left[e_0, e_2\right] \cup\left[e_0, e_1\right]=\left[\hat{e}_0, e_1, e_2\right] \cup\left[e_0, \hat{e}_1, e_2\right] \cup\left[e_0, e_1, \hat{e}_2\right] .
			  $$
			  The oriented boundary of $\Delta^2$ is
			  $$
			  \left[\hat{e}_0, e_1, e_2\right] \cup-\left[e_0, \hat{e}_1, e_2\right] \cup\left[e_0, e_1, \hat{e}_2\right]=\left[e_1, e_2\right] \cup\left[e_2, e_0\right] \cup\left[e_0, e_1\right] .
			  $$
			- More generally, the boundary of $\Delta^n=\left[e_0, \ldots, e_n\right]$ is $\bigcup_{i=0}^n\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$ and the oriented boundary of $\Delta^n$ is $\bigcup_{i=0}^n(-1)^i\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$.
			-
			-
	- (Singular) $n$-chain #card
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-09T00:22:44.916Z
	  card-last-reviewed:: 2023-05-10T00:22:44.916Z
	  card-last-score:: 5
		- Let $X$ be a topological space. For each $n \geq 0$, define $S_n(X)$ as the **free abelian group** with basis all ((64462ceb-3ede-4222-851b-57c2b29616b0)) in $X$; define $S_{-1}(X)=0$.
		  id:: 64462e13-2a8c-4f01-b999-632c7b8b0110
		  collapsed:: true
			- Often it seems that free (abelian) groups are structureless since they're free. How things are different here?
			  background-color:: pink
			- all singular $n$-simplexes in
		- The elements of $S_n(X)$ are called (singular) $n$-chains in $X$.
	- Boundary of a simplex #card
	  collapsed:: true
		- If $\sigma: \Delta^n \rightarrow X$ is continuous and $n>0$, then its boundary is
		  collapsed:: true
		  $$
		  \partial_n \sigma=\sum_{i=0}^n(-1)^i \sigma \varepsilon_i^n \in S_{n-1}(X)
		  $$
		  if $n=0$, define $\partial_0 \sigma=0$.
			- $\varepsilon_i^n$ is the $i$**th face map**.
			- $(-1)^i$ keeps the ((6438bf08-5df7-4653-a22c-f97564f2812d))
		- The intuition is that the oriented boundary of a singular $n$-simplex $\sigma: \Delta^n \rightarrow X$ ought to be $\sum_{i=0}^n(-1)^i\left(\sigma \mid\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]\right)$.
		  collapsed:: true
			- It's easy to verify the intuition for a triangle: The 'boundary' is the faces with one lower dimension, together with orientations (arrows for 1-simplexes).
			  ![Image(1).png](../assets/Image(1)_1682322105461_0.png){:height 204, :width 570}
		- Notes
		  collapsed:: true
			- $\partial_n \sigma$ is a **map** from $\Delta^{n-1}$ to $X$. Note that simplexes (as paths) are defined by maps.
			- A technical point arises: we prefer that this be a singular $(n-1)$-chain. However, the domain of $\sigma \mid\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$ is **not** the standard $(n-1)$-simplex $\Delta^{n-1}$.
			- The point is remedied by the $i$th face map $\varepsilon_i^n$ which takes the vertices $\left\{e_0, \ldots, e_{n-1}\right\}$ to the vertices $\left\{e_0, \ldots, \hat{e}_i, \ldots, e_n\right\}$, preserving the displayed orderings:
			  collapsed:: true
			  $$
			  \begin{aligned}
			  & \varepsilon_i^n:\left(t_0, \ldots, t_{n-1}\right) \mapsto\left(t_0, \ldots, t_{i-1}, 0, t_i, \ldots, t_{n-1}\right)
			  \end{aligned}
			  $$
				- Intuitively, embed the standard $n-1$ simplex into the $n$ simplex.
	- Boundary operator $\partial_n$ #card
	  collapsed:: true
		- The unique homomorphism $\partial_n: S_n(X) \rightarrow S_{n-1}(X)$ determined by
		  collapsed:: true
		  $$\partial_n \sigma=\sum_{i=0}^n(-1)^i \sigma \varepsilon_i$$
			- The behavior on a basis is enough to determine the hom.
			- 'Freedom is the left adjoint of forgetfulness'.
		- Example. $\partial_1: S_1(X) \to S_0(X)$
		  collapsed:: true
			- $S_1(X)$ is the free abelian group with basis all paths $\sigma: I \rightarrow X$
			- $S_0(X)$ is the free abelian group with basis $X$.
			- (i) $\partial_1: S_1(X) \rightarrow S_0(X)$ satisfies $\partial_1 \sigma=\sigma(1)-$ $\sigma(0)$ for every path $\sigma$ in $X$.
			- (ii) If $x_1, x_0 \in X$, show that $x_1-x_0 \in \operatorname{im} \partial_1$ if and only if $x_0, x_1$ lie in the same path component of $X$.
			  Fits our intuition of 'boundary'!
			- (iii) If $\sigma$ is a path in $X$, then $\sigma \in \operatorname{ker} \partial_1$ if and only if $\sigma$ is a closed path. Exhibit a nonzero element of $\operatorname{ker} \partial_1$ that is not a closed path.
			  Fits our intuition of 'closed' (boundaryless)!
	- Singular complex $S_*(X)$
	  collapsed:: true
		- A **sequence** of free abelian groups and homomorphisms
		  $$
		  \cdots \longrightarrow S_n(X) \stackrel{\partial_n}{\longrightarrow} S_{n-1}(X) \longrightarrow \cdots \longrightarrow S_1(X) \stackrel{\partial_1}{\longrightarrow} S_0(X) \stackrel{\partial_0}{\longrightarrow} 0
		  $$
	- (Singular) $n$-cycles and $n$-boundaries #card
	  collapsed:: true
		- The group of (singular) $n$-cycles in $X$, denoted by $Z_n(X)$, is $\text{Ker }\partial_n$.
		  collapsed:: true
			- 'Cycle' seems to mean 'boundaryless'.
			- '$Z$' is from the German **Zykel**.
		- The group of (singular) $n$-boundaries in $X$, denoted by $B_n(X)$, is $\text{Im }\partial_{n+1}$.
		  collapsed:: true
			- This is rather obvious: Boundary of something of higher dimension.
			- '$B$' is surely from **Boundary**.
	- Homology group #card
	  collapsed:: true
		- For each $n \geq 0$, the $n$th (singular) homology group of a space $X$ is
		  $$
		  H_n(X)={Z_n(X)}/{B_n(X)} \equiv {\operatorname{Ker} \partial_n}/{\operatorname{Im} \partial_{n+1}} .
		  $$
		  The coset $z_n+B_n(X)$, where $z_n$ is an $n$-cycle, is called the homology class of $z_n$, and it is denoted by cls $z_n$.
			- The spirit of Green's theorem: Holes <-> Cycles that are not boundaries.
			- Note that the group is **abelian** so everything is normal.
			- Proposition. $B_n(X) \in Z_n(X) \in S_n(X)$.
			  collapsed:: true
				- A simple exercise to recall the definitions and $\partial_n \partial_{n+1}=0$.
		- Strikingly simple in form, but daunting in its depth and implications!
		  background-color:: yellow
			- To study a space $X$, we invent strange things called 'simplexes' which is defined by a continuous map from $\Delta^n$ to $X$.
				- It's strange at first sight that we define structures by maps rather than 'things in $X$', but this somehow echoes the spirit of category theory.
			- Then we manage to shape our intuition into the boundary operator.
			- The most bizarre things is introducing a structure of free abelian groups generated by simplexes. With a group structure everything emerges, but at first sight freely generated groups seem 'structureless'.
	- Betti number #card
		- The $n$-th Betti number of $X$ is $\operatorname{rank}H_n(X)$.
	- Acyclic #card
		- A space $X$ is called acyclic if $H_n(X)=0$ for all $n \geq 1$.
		- The dimension axiom shows that every 1-point space is acyclic.
	- Support #card
		- If $\zeta=\sum m_i \sigma_i \in S_n(X)$, with all $m_i \neq 0$ and all $\sigma_i$ distinct, then the support of $\zeta$, denoted by $\mathrm{supp} \ \zeta$, is $\bigcup \sigma_i\left(\Delta^n\right)$.
		- Note that $\mathrm{supp} \ \zeta$ is compact since it is a finite union of compact subsets.
- # Basic Facts
  collapsed:: true
	- ((644638a3-9be7-46f8-8abb-f6c3ae2849af)) For all $n \geq 0$, we have $\partial_n \partial_{n+1}=0$. #card
	  collapsed:: true
		- First we explicitly write down 
		  $$\partial_n \partial_{n+1} \sigma=\sum_{j, k}(-1)^{j+k} \sigma \varepsilon_j^{n+1} \varepsilon_k^n$$
		- Lemma 4.5. If $k<j$, the face maps satisfy
		  collapsed:: true
		  $$
		  \varepsilon_j^{n+1} \varepsilon_k^n=\varepsilon_k^{n+1} \varepsilon_{j-1}^n: \Delta^{n-1} \rightarrow \Delta^{n+1} .
		  $$
			- Just write down the coordinates explicitly.
		- Therefore we can pair up the sums and cancel:
		  $$\begin{aligned}
		  \partial _{n} \partial _{n+1} \sigma  & =\sum _{j,k} (-1)^{j+k} \sigma \varepsilon _{j}^{n+1} \varepsilon _{k}^{n}\\
		   & =\sum _{k< j} \sigma \left[ (-1)^{j+k} \varepsilon _{j}^{n+1} \varepsilon _{k}^{n} +( -1)^{j+k-1} \varepsilon _{k}^{n+1} \varepsilon _{j-1}^{n}\right]\\
		  &= 0
		  \end{aligned}$$
		- How was this theorem first invented? It's simple to verify, but hard to observe...
		  background-color:: red
		  collapsed:: true
			- It reminds of the Poincare lemma.
			- Also similar to the geometrical intuition that 'a boundary is boundaryless'.
	- ((644a25af-79a6-4b3c-9ac7-e319e6a3b251)) For each $n \geq 0, H_n: \mathbf{Top}\rightarrow \mathbf{A b}$ is a functor. #card
		- '当你学了范畴后，看什么都是范畴'。
		- We should determine two things:
		  1. For $f \in \mathrm{Hom}_{\mathbf{Top}}(X,Y)$, how to define $H_n(f)$?
		  2. Does $H_n(f \circ g) = H_n(f) \circ H_n(g)$?
		- First question:
			- Obviously $f$ induces a homomorphism $f_\#: S_n(X) \to S_n(Y)$ by 
			  collapsed:: true
			  $$
			  f_{\#}\left(\sum m_\sigma \sigma\right)=\sum m_\sigma(f \circ \sigma)
			  $$
				- Note that $f \circ \sigma$ is also a simplex.
			- Key observation:
			  $$\partial_n f_{\#}=f_{\#} \partial_n$$
			  thus $f_{\#}$ both preserves cycles and chains.
			- The desired $H_n(f)$ is defined by $H_n(f): g+B_n(X) \mapsto f_{\#}(g)+B_n(Y)$.
			  Since $f_{\#}$ preserves cycles and chains, the codomain is correct and the map is independent of the representative.
		- Second question:
		  collapsed:: true
			- Equivalently, does $f_{\#} \circ g_{\#}=(f \circ g)_{\#}$?
			- Obviously, yes.
	- Corollary. If $X$ and $Y$ are homeomorphic, then $H_n(X) \cong H_n(Y)$ for all $n \geq 0$.
	  collapsed:: true
		- Since $f_{\#}$ can be inverted.
		- But to put it in another way -- the homology group is a topological invariant. We've found yet another one!
	- ((6451ce0c-d570-4606-b1f1-8982fc66eead)) (Dimension Axiom). If $X$ is a one-point space, then $H_n(X)=0$ for all $n>0$. #card
		- An easy exercise to recall the definitions.
		  Discuss $n$ even and odd separately.
	- Lemma 4.15. Let $A$ be a subspace of $X$ with inclusion $j: A \hookrightarrow X$. Then $j_{\#}: S_n(A) \rightarrow S_n(X)$ is an injection for every $n \geq 0$.
	- ((6455b888-36b0-487b-b550-448faf23952c)). Let $X=\bigcup _{p=1}^{\infty } X^{p}$ with $X^{p} \subset X^{p+1}$ for all $p$ (call the inclusion maps $\lambda ^{p} :X^{p} \hookrightarrow X$ and $\left. \varphi ^{p} :X^{p} \hookrightarrow X^{p+1}\right)$. If every compact subspace $A$ of $X$ is contained in some $X^{p}$, then cls $\zeta \in H_{n} (X)$ is zero if and only if there exist $p$ and $\operatorname{cls} \zeta ^{\prime } \in H_{n}\left( X^{p}\right)$ with
	  \begin{equation*}
	  \lambda _{*}^{p}\operatorname{cls} \zeta ^{\prime } =\operatorname{cls} \zeta \quad \text{ and } \quad \varphi _{*}^{p}\operatorname{cls} \zeta ^{\prime } =0\text{. }
	  \end{equation*}
		- Note that
		  ![image.png](../assets/image_1683339421269_0.png){:height 238, :width 327}
- # Trying to Calculate the Homology Groups
	- Theorem. If $\left\{X_\lambda: \lambda \in \Lambda\right\}$ is the set of path components of $X$, then, for every $n \geq 0$,
	  collapsed:: true
	  $$
	  H_n(X) \cong \sum_\lambda H_n\left(X_\lambda\right) .
	  $$
		- This also fits our intuition.
	- ((6451d268-21db-4ea0-979a-dc3a55766d0b))
	  collapsed:: true
	  (i) For any space $X$, the group $H_0(X)$ is free abelian of rank $=\operatorname{card} \Lambda$, where $\left\{X_\lambda: \lambda \in \Lambda\right\}$ is the family of path components.
	  (ii) If $X$ and $Y$ are path connected spaces and $f: X \rightarrow Y$ is continuous, then $f_*: H_0(X) \rightarrow H_0(Y)$ takes a generator of $H_0(X)$ to a generator of $H_0(Y)$. #card
		- Proof
			- (i) First consider a path-connected space. The general result follows.
				- $S_0(X) \cong \text{FreeAb}(X)$, since each point of $X$ can be the image of some map from $\{*\}$ to $X$.
				- $B_0(X)=\mathrm{Im} \ \partial_1= \langle \{x-y|x,y \text{ are in the same path component}\} \rangle$
					- Note that for a path $f$, $\partial_1(f)=f(1)-f(0)$.
					  But $S_1(X)$ is freely **generated** by the paths, thus $B_0(X)$ shall be freely **generated** by $\{x-y\}$.
					- Put in plain English, this is the subgroup that the coefficients of the generators **sum to zero**.
				- $Z_0(X)=\mathrm{Ker} \ \partial_0=S_0(X)$
				- Thus $Z_0(X)/B_0(X) \cong Z$, the group of 'sum of coefficients'.
			- (ii)
	- Theorem. If $X$ is a space with $H_n(A)=0$ for every compact subspace of $X$ and $n>0$, then $H_n(X)=0$. #card
	  collapsed:: true
		- *Note that this is a card combining two theorems, which has the advantage of illustrating the usage.*
		- ((645372b1-03c6-414f-a6d5-be8fcb51e8ac)) (Compact Supports). If cls $\zeta \in H_n(X)$, then there is a compact subspace $A$ of $X$ with $\operatorname{cls} \zeta \in \operatorname{Im} j_*$, where $j: A \hookrightarrow X$ is the inclusion.
			- This is equivalent to that the support space of $\zeta$ can be included in a compact subset $A$.
				- $j_*$ is the induced map of homology groups. Note that $j_*(B_n(A)) \sub B_n(X)$.
				- $\zeta$ is a finite formal sum of some simplexes.
			- However, $\operatorname{supp} \zeta$ itself is compact!
		- Therefore consider $x \in H_n(X)$. $x \in j_*(H_n(A))$, but $H_n(A)=0$, so $x=0$.
- # The Homotopy Axiom
	- ((6455bc34-9cfb-4aff-9eda-66b2797bb373)). If $X$ is a bounded convex subspace of euclidean space, then $H_n(X)=0$ for all $n \geq 1$. In particular, $H_n\left(D^k\right)=0$ for all $n>0$ and all $k$.
		- Remark
			- For $n=0$ and $X \neq \empty$, we know $H_0(X) \simeq \Z$ since convex implies path-connectedness.
		-