- Idea #card
  card-last-interval:: 42
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2023-09-11T12:32:16.599Z
  card-last-reviewed:: 2023-07-31T12:32:16.600Z
  card-last-score:: 5
  collapsed:: true
	- [[Green's Theorem]] tells us that we can determine the behavior of the bulk by its boundary.
	  We'd like to generalize this into topology.
	- Furthermore, a 'hole' in a space is implied by the existence of some **cycle** which is not a **boundary**.
		- The intuition comes from $S^1$ in $\mathbb R^2-0$.
		- However, note that a single point is a cycle but not a boundary.
- # Defs
  collapsed:: true
	- ## About Orientations #card
	  card-last-interval:: 28.47
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2024-02-01T12:10:16.953Z
	  card-last-reviewed:: 2024-01-04T01:10:16.953Z
	  card-last-score:: 5
	  collapsed:: true
		- Def. Orientation
		  id:: 642578ff-9703-449c-b3df-41ffc344e641
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-10T18:58:16.463Z
		  card-last-reviewed:: 2023-07-10T12:58:16.463Z
		  card-last-score:: 5
		  collapsed:: true
			- An orientation of $\Delta^n=\left[e_0, e_1, \ldots, e_n\right]$ is a **linear ordering of its vertices**.
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
	- (Singular) $n$-chain
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
	- Boundary of a simplex
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-05T19:07:36.003Z
	  card-last-reviewed:: 2023-08-05T13:07:36.003Z
	  card-last-score:: 5
		- If $\sigma: \Delta^n \rightarrow X$ is continuous and $n>0$, then its boundary is
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
	- Boundary operator $\partial_n$
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-07-18T07:23:13.154Z
	  card-last-reviewed:: 2023-06-17T01:23:13.154Z
	  card-last-score:: 5
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
	  id:: 6454f1b7-f979-485a-aafb-fa39fd34e0af
	  collapsed:: true
		- A **sequence** of free abelian groups and homomorphisms
		  $$
		  \cdots \longrightarrow S_n(X) \stackrel{\partial_n}{\longrightarrow} S_{n-1}(X) \longrightarrow \cdots \longrightarrow S_1(X) \stackrel{\partial_1}{\longrightarrow} S_0(X) \stackrel{\partial_0}{\longrightarrow} 0
		  $$
	- (Singular) $n$-cycles and $n$-boundaries
	  collapsed:: true
		- The group of (singular) $n$-cycles in $X$, denoted by $Z_n(X)$, is $\text{Ker }\partial_n$.
		  collapsed:: true
			- 'Cycle' seems to mean 'boundaryless'.
			- '$Z$' is from the German **Zykel**.
		- The group of (singular) $n$-boundaries in $X$, denoted by $B_n(X)$, is $\text{Im }\partial_{n+1}$.
		  collapsed:: true
			- This is rather obvious: Boundary of something of higher dimension.
			- '$B$' is surely from **Boundary**.
	- Homology group
	  card-last-interval:: 31.21
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-07-20T06:07:37.780Z
	  card-last-reviewed:: 2023-06-19T01:07:37.781Z
	  card-last-score:: 5
	  collapsed:: true
		- For each $n \geq 0$, the $n$th (singular) homology group of a space $X$ is
		  $$
		  H_n(X)={Z_n(X)}/{B_n(X)} \equiv {\operatorname{Ker} \partial_n}/{\operatorname{Im} \partial_{n+1}} .
		  $$
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
			- The most bizarre things is introducing a structure of **free** abelian groups generated by simplexes.
			  At first sight freely generated groups seem structureless, but the kernels and images of $\partial$ is not.
				- Actually it is the complex which is rich in structure!
	- Betti number
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-11-09T00:50:52.282Z
	  card-last-reviewed:: 2023-09-28T00:50:52.283Z
	  card-last-score:: 5
		- The $n$-th Betti number of $X$ is $\operatorname{rank}H_n(X)$.
			- Note that here the rank is the *rank of abelian groups*, i.e. rank of the **torsion-free** part.
			- There's another rank:
			  $$
			  \operatorname{rank}(G)=\min \{|X|: X \subseteq G,\langle X\rangle=G\}
			  $$
	- Acyclic
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-11-09T00:45:28.152Z
	  card-last-reviewed:: 2023-09-28T00:45:28.153Z
	  card-last-score:: 5
	  collapsed:: true
		- A space $X$ is called acyclic if $H_n(X)=0$ for all $n \geq 1$.
		- The dimension axiom shows that every 1-point space is acyclic.
	- Support
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-12-06T00:32:13.109Z
	  card-last-reviewed:: 2023-10-25T00:32:13.110Z
	  card-last-score:: 5
	  collapsed:: true
		- If $\zeta=\sum m_i \sigma_i \in S_n(X)$, with all $m_i \neq 0$ and all $\sigma_i$ distinct, then the support of $\zeta$, denoted by $\mathrm{supp} \ \zeta$, is $\bigcup \sigma_i\left(\Delta^n\right)$.
		- Note that $\mathrm{supp} \ \zeta$ is compact since it is a finite union of compact subsets.
	- The cone construction #card
	  id:: 6461ca0c-d0bf-40d1-bc3f-5ce24fd244b9
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-12-30T01:03:02.579Z
	  card-last-reviewed:: 2023-11-18T01:03:02.580Z
	  card-last-score:: 5
	  collapsed:: true
		- The 'cone map' $c_n:S_n (X) \to S_{n+1} (X)$ for a convex subset of $\mathbb R^n$ by its action on the generators:
		  $$
		  (c_n( \sigma))\left(t_0, t_1, \ldots, t_{n+1}\right)= \begin{cases}b & \text { if } t_0=1 \\ t_0 b+\left(1-t_0\right) \sigma\left(\frac{t_1}{1-t_0}, \ldots, \frac{t_{n+1}}{1-t_0}\right) & \text { if } t_0 \neq 1\end{cases}
		  $$
			- Intuitively, construct a cone using $b$ as the 'top' and $\sigma$ as the 'bottom'.
			- Note that the 'scaling construction' requires a structure of $\mathbb R$ ... or something similar?
		- Proposition. $\partial_{n+1} c_n(\sigma)=\sigma-c_{n-1} \partial_n(\sigma)$
			- Verify by the definition of the boundary operator. A small exercise!
			- Geometric intuition:
			  ((6461a7c8-3e70-4218-8989-a2b1fa67accf))
			  the 'side faces' of the cone is produced by cones over the boundary.
- # Basic Facts
  collapsed:: true
	- ((644638a3-9be7-46f8-8abb-f6c3ae2849af)) For all $n \geq 0$, we have $\partial_n \partial_{n+1}=0$. #card
	  collapsed:: true
	  card-last-interval:: 117.6
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2024-02-16T14:31:57.267Z
	  card-last-reviewed:: 2023-10-22T00:31:57.268Z
	  card-last-score:: 5
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
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-07-31T01:03:36.447Z
	  card-last-reviewed:: 2023-06-19T01:03:36.447Z
	  card-last-score:: 5
	  id:: 64b48496-7607-4075-8451-d120e228dafc
	  collapsed:: true
		- '当你学了范畴后，看什么都是范畴'。
		- We should determine two things:
		  1. For $f \in \mathrm{Hom}_{\mathbf{Top}}(X,Y)$, how to define $H_n(f)$?
		  2. Does $H_n(f \circ g) = H_n(f) \circ H_n(g)$?
		- First question:
		  collapsed:: true
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
	  id:: 6454f1b7-5d36-4a76-b56c-aa3dc7b2515d
	  card-last-interval:: 32.57
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-25T01:37:33.014Z
	  card-last-reviewed:: 2023-08-23T12:37:33.015Z
	  card-last-score:: 5
	  collapsed:: true
		- An easy exercise to recall the definitions.
		  Discuss $n$ even and odd separately.
	- Lemma 4.15. Let $A$ be a subspace of $X$ with inclusion $j: A \hookrightarrow X$. Then $j_{\#}: S_n(A) \rightarrow S_n(X)$ is an injection for every $n \geq 0$.
	- ((6455b888-36b0-487b-b550-448faf23952c)). Let $X=\bigcup _{p=1}^{\infty } X^{p}$ with $X^{p} \subset X^{p+1}$ for all $p$ (call the inclusion maps $\lambda ^{p} :X^{p} \hookrightarrow X$ and $\left. \varphi ^{p} :X^{p} \hookrightarrow X^{p+1}\right)$. If every compact subspace $A$ of $X$ is contained in some $X^{p}$, then cls $\zeta \in H_{n} (X)$ is zero if and only if there exist $p$ and $\operatorname{cls} \zeta ^{\prime } \in H_{n}\left( X^{p}\right)$ with
	  collapsed:: true
	  \begin{equation*}
	  \lambda _{*}^{p}\operatorname{cls} \zeta ^{\prime } =\operatorname{cls} \zeta \quad \text{ and } \quad \varphi _{*}^{p}\operatorname{cls} \zeta ^{\prime } =0\text{. }
	  \end{equation*}
		- Note that
		  ![image.png](../assets/image_1683339421269_0.png){:height 238, :width 327}
	- ((6471627c-36a0-4abb-ad61-cda6a9bb6eb1)). A **polygon** in a space $X$ is a 1-chain $\pi=\sum_{i=0}^k \sigma_i$, where $\sigma_i\left(e_1\right)=$ $\sigma_{i+1}\left(e_0\right)$ for all $i$. 
	  Then a 1-chain $\gamma=\sum m_i \sigma_i \in S_1(X)$ is a cycle if and only if $\gamma$ is homologous to a linear combination of polygons.
		- q -> p is obvious, since each polygon is a cycle.
		- p -> q: By direct construction. We can start from a point and find out the next 'edge' successively.
	- Theorem. If $\left\{X_\lambda: \lambda \in \Lambda\right\}$ is the set of path components of $X$, then, for every $n \geq 0$,
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-08-14T19:04:11.616Z
	  card-last-reviewed:: 2023-07-14T13:04:11.616Z
	  card-last-score:: 5
	  collapsed:: true
	  $$
	  H_n(X) \cong \sum_\lambda H_n\left(X_\lambda\right) .
	  $$ #card
		- This fits our intuition.
		- The key is that $\Delta^n$ is path-connected, thus a simplex is also path-connected, i.e. within a single path component.
	- ((6451d268-21db-4ea0-979a-dc3a55766d0b))
	  collapsed:: true
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-08-06T01:01:48.009Z
	  card-last-reviewed:: 2023-06-25T01:01:48.009Z
	  card-last-score:: 5
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
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-07-28T06:58:53.436Z
	  card-last-reviewed:: 2023-06-27T00:58:53.437Z
	  card-last-score:: 5
		- *Note that this is a card combining two theorems, which has the advantage of illustrating the usage.*
		- ((645372b1-03c6-414f-a6d5-be8fcb51e8ac)) (Compact Supports). If cls $\zeta \in H_n(X)$, then there is a compact subspace $A$ of $X$ with $\operatorname{cls} \zeta \in \operatorname{Im} j_*$, where $j: A \hookrightarrow X$ is the inclusion.
			- The idea is to use the topological properties of $\Delta^n$. Here we use compactness.
			- This is equivalent to that the support space of $\zeta$ can be included in a compact subset $A$.
				- $j_*$ is the induced map of homology groups. Note that $j_*(B_n(A)) \sub B_n(X)$.
				- $\zeta$ is a finite formal sum of some simplexes.
			- However, $\operatorname{supp} \zeta$ itself is compact since *a finite union of compact subsets is compact*.
		- Therefore consider $x \in H_n(X)$. $x \in j_*(H_n(A))$, but $H_n(A)=0$, so $x=0$.
- # Excision
	- ## Notations
		- If $A$ is a subspace of $X$, then $\bar{A}$ denotes its closure and $A^{\circ}$ denotes its interior.
	-
	- ## Excision and Barycentric Division #card
	  card-last-score:: 5
	  card-repeats:: 1
	  card-next-schedule:: 2023-07-28T06:43:35.570Z
	  card-last-interval:: 31.26
	  card-ease-factor:: 2.6
	  card-last-reviewed:: 2023-06-27T00:43:35.570Z
		- Geometric intuition
		  collapsed:: true
			- ((6498e0fe-d925-45b8-8532-f90ed5c95f32)) means 'identifying a subspace as a single point'.
			- Therefore we expect that we could **remove some part of the subspace** without affecting the space after identification!
		- Version I
		  collapsed:: true
			- Assume that $U \subset A \subset X$ are subspaces with $\bar{U} \subset A^{\circ}$.
			- The inclusion $i:(X-U, A-U) \hookrightarrow(X, A)$ induces **isomorphisms**
			  $$
			  i_*: H_n(X-U, A-U) \stackrel{\sim}{\rightarrow} H_n(X, A)
			  $$
			  for all $n$.
		- Version II
		  collapsed:: true
			- Let $X_1$ and $X_2$ be subspaces of $X$ with $X=X_1^{\circ} \cup X_2^{\circ}$.
			- The inclusion $j:\left(X_1, X_1 \cap X_2\right) \hookrightarrow\left(X_1 \cup X_2, X_2\right)=\left(X, X_2\right)$ induces isomorphisms
			  $$
			  j_*: H_n\left(X_1, X_1 \cap X_2\right) \stackrel{\sim}{\rightarrow} {H_n}\left(X, X_2\right)
			  $$
			  for all $n$.
			- ((649940c8-ab08-4e88-ba1d-4dd7ac323e7f)) Version I of excision is equivalent to version II.
			  collapsed:: true
				- I -> II
				  collapsed:: true
					- Obviously we should take $U=X_2-X_1$, which is the part to be removed.
					  We should prove $\overline{(X_2 - X_1)} \sub X_2 ^ \circ$.
					- Proposition. $X-X_1^\circ$ contains $\overline{(X_2 - X_1)}$.
						- $\overline{(X_2 - X_1)}$ is the intersection of all closed sets containing $X_2-X_1$.
						- $X-X_1^\circ$ is a closed set containing $X_2-X_1$.
						- *When feeling stuck at simple topology, convert everything to basic set theory, e.g. 'intersection' ->* $x \in A, x \in B$
					- Proposition. $X-X_1^\circ \sub X_2^\circ$.
						- Directly follows $X=X_1^\circ \cup X_2^\circ$.
				- II -> I
					- Take $X_2=A,X_1=X-U$.
					  We should prove $X=X_1^{\circ} \cup X_2^{\circ}$.
					- Note that $(X-U)^\circ = X-\bar U$.
				-
		- Barycentric division
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-27T19:25:43.034Z
		  card-last-reviewed:: 2023-07-27T13:25:43.034Z
		  card-last-score:: 5
			- Idea
			  collapsed:: true
				- We wish to divide a simplex repeatedly to 'arbitrarily small'.
				- Then we could apply [[The Lebesgue number lemma]].
				- Note that it is not the only way, but the **inductive construction** is always the simplest! #Strategy
			- ((64ab1a09-5b3b-4278-9f5e-6b364634c78c)) The barycentric subdivision of an affine $n$-simplex $\Sigma^n$, denoted by $\operatorname{Sd} \Sigma^n$, is a family of affine $n$-simplexes defined inductively for $n \geq 0$ :
			  (i) $\operatorname{Sd} \Sigma^0=\Sigma^0$;
			  (ii) if $\varphi_0, \varphi_1, \ldots, \varphi_{n+1}$ are the $n$-faces of $\Sigma^{n+1}$ and if $b$ is the barycenter of $\Sigma^{n+1}$, then Sd $\Sigma^{n+1}$ consists of all the $(n+1)$-simplexes spanned by $b$ and $n$-simplexes in $\operatorname{Sd} \varphi_i, i=0, \ldots, n+1$.
			- ((64ab1a5b-d15c-449d-89ff-ae0c8100a239))
			- Key property. $\operatorname{Sd} \sigma -\sigma \in B_n(X)$.
			-
		- ## Proof
		  collapsed:: true
			- Lemma 6.11. Let $X_1$ and $X_2$ be subspaces of $X$. If the inclusion $S_*\left(X_1\right)+$ $S_*\left(X_2\right) \hookrightarrow S_*(X)$ induces isomorphisms in homology, then excision holds for the subspaces $X_1$ and $X_2$ of $X$.
			  card-last-interval:: 31.21
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-08-13T18:38:22.677Z
			  card-last-reviewed:: 2023-07-13T13:38:22.678Z
			  card-last-score:: 5
				- How was the proof motivated?
				  background-color:: red
				  collapsed:: true
					- Seems the proof is directly motivated by the ((649e4af5-3e8a-4202-831b-2ad858b4b337)) and manipulating compositions of isomorphisms...
						- To be more specific, we notice we could invoke the second isomorphism theorem to deal with the quotient.
					- In other words, is the observation very important?
					  We couldn't proceed without the observation?
						- Indeed observations, especially very stupid ones, are very important. #[[System/Math and Physics]]
						  background-color:: yellow
						- In this case the observation is ((649e49f0-6cef-4631-bb01-027b94b5422c)), which is quite stupid.
				- *Remark: When dealing with groups, isomorphism theorems could be extremely useful.*
				- First construct an exact sequence:
				  collapsed:: true
				  $$
				  0 \rightarrow S_*\left(X_1\right)+S_*\left(X_2\right) \stackrel{i}{\rightarrow} S_*(X) \rightarrow S_*(X) /\left(S_*\left(X_1\right)+S_*\left(X_2\right)\right) \rightarrow 0
				  $$
					- Since $i$ is an isomorphism, the corresponding long exact sequence has every third term zero, i.e.
					  $$
					  H_n\left(S_*(X) /\left(S_*\left(X_1\right)+S_*\left(X_2\right)\right)\right)=0
					  $$
				- Then construct the second exact sequence, motivated by the third isomorphism theorem:
				  collapsed:: true
				  $$
				  0 \rightarrow \frac{S_*\left(X_1\right)+S_*\left(X_2\right)}{S_*\left(X_2\right)} \stackrel{j}{\rightarrow} \frac{S_*(X)}{S_*\left(X_2\right)} \rightarrow \frac{S_*(X)}{S_*\left(X_1\right)+S_*\left(X_2\right)} \rightarrow 0
				  $$
					- Consider the corresponding long exact sequence.
					- We know every third term is zero, thus $j$ induces isomorphisms.
				- Finally we make a beautiful construction:
				  ((649e4a3e-67e0-4327-9819-262437a3b1c8))
					- It's easy to verify $\mathcal l$ is an isomorphism since ((649e49f0-6cef-4631-bb01-027b94b5422c))
					- Since both $l$ is itself an isomorphism and $j$ induces isomorphisms between homology groups, it follows that $k$ induces isomorphisms between homology groups.
					  The proof finishes.
				-
			- The whole proof is quite lengthy, but the key ideas are quite simple (I could even come up with them myself!).
				- First, $\Delta^n$ is compact, therefore [[The Lebesgue number lemma]] says the 'minimum containing property' of the inverse images of $X_1^\circ \cap \sigma(\Delta^n)$ and $X_2^\circ \cap \sigma(\Delta^n)$.
				- Next we could use Barycentric division to divide the simplexes repeatedly, until each is smaller than the Lebesgue number and could be contained in a single piece.
				- Since the Barycentric division doesn't change the properties of boundaries (as the extra faces cancel each other), we're done.
	- ## Mayer-Vietoris Theorem #card
		- Lemma (Barratt-Whitehead). Consider the commutative diagram
		  id:: 649955ae-5920-4aa5-8d1d-f5a3171d430c
		  card-last-interval:: 31.21
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-13T18:42:15.696Z
		  card-last-reviewed:: 2023-07-13T13:42:15.697Z
		  card-last-score:: 5
		  collapsed:: true
		  ((649955c6-e5a3-4cad-9648-224497609a54))
		  in which every third vertical map $h_n$ is an **isomorphism**. Then there is an exact sequence
		  $$
		  \cdots \longrightarrow A_n \stackrel{\left(i_n, f_n\right)}{\longrightarrow} B_n \oplus A_n^{\prime} \stackrel{g_n-j_n}{\longrightarrow} B_n^{\prime} \stackrel{d_n h_n^{-1} q_n}{\longrightarrow} A_{n-1} \longrightarrow \cdots
		  $$
			- The proof is a regular diagram chasing,
			  but I still don't understand how could they spot such theorems...
			- $\operatorname{Im}(i_n,f_n)$ and $\operatorname{Ker}(g_n-j_n)$
				- $\operatorname{Im}(i_n,f_n) \sub \operatorname{Ker}(g_n-j_n)$ is manifest from commutativity.
				- The reverse inclusion needs more manipulation.
				- To prove for $i_n$:
					- $\operatorname{Im}i_n=\operatorname{Ker}p_n$, thus we should prove $p_n(x)=0$
					- $$h_n p_n(x)=q_n g_n(x)=q_n j_n(y)=0$$
					  which finishes the proof.
				- To prove for $f_n$:
					- First note $j_n f_n(a)=g_n i_n(a)$, therefore
					  $$z \equiv f_n(a)-y \in \operatorname{Ker}j_n$$
					- We can further use commutativity on the left square to show that $z \in \operatorname{Im} f_n d_{n+1}$.
					- Therefore we can add $d_{n+1}(c)$ to compensate for $z$ without affecting $x$.
			- $\operatorname{Im}(g_n-j_n)$ and $\operatorname{Ker}(d_n h_n^{-1}q_n)$
				- $\operatorname{Im}(g_n-j_n) \sub \operatorname{Ker}(d_n h_n^{-1}q_n)$
					- First note that $\operatorname{Im}(g_n-j_n)=\operatorname{Im}g_n \oplus \operatorname{Im}j_n$ due to the structure of abelian groups, therefore we should actually prove $\operatorname{Im}g_n \sub \operatorname{Ker}(d_n h_n^{-1}q_n)$ and $\operatorname{Im}j_n \sub \operatorname{Ker}(d_n h_n^{-1}q_n)$.
					- This is manifest due to the complexness (not using exactness) of top and lower rows.
				- Reverse inclusion
					- $d_n h_n^{-1} q_n(x)=0$ <-> $q_n h_n^{-1}(x) \in \operatorname{Im}p_n$ <-> $q_n(x) \in  \operatorname{Im}(h_n p_n)$
					- For $q_n(x)=h_np_n(a)$:
					  $$x \in g_n(a)+ \operatorname{Ker}q_n=g_n(a)+ \operatorname{Im}j_n$$
					  which finishes the proof.
			- $\operatorname{Im}(d_n h_n^{-1}q_n)$ and $\operatorname{Ker}(i_{n-1},f_{n-1})$
				- $\operatorname{Im}(d_n h_n^{-1}q_n) \sub \operatorname{Ker}(i_{n-1},f_{n-1})$ is manifest.
				- The reverse inclusion:
					- First note that $\operatorname{Ker}i_{n-1}=\operatorname{Im}d_n$.
					- Now consider $\operatorname{Ker}f_{n-1}$.
					  $f_{n-1}d_n(x)=0$ <-> $\Delta_n h_n(x)=0$ <-> $h_n(x) \in \operatorname{Im}q_n$.
		- ((649b9b72-174d-40b4-bcff-9f48f3b1e56b)) (Mayer-Vietoris). If $X_1, X_2$ are subspaces of $X$ with $X=$ $X_1^{\circ} \cup X_2^{\circ}$, then there is an exact sequence
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-14T19:15:29.781Z
		  card-last-reviewed:: 2023-07-14T13:15:29.782Z
		  card-last-score:: 5
		  $$
		  \cdots \longrightarrow H_n\left(X_1 \cap X_2\right) \stackrel{\left(i_{1 *}, i_{2 *}\right)}{\longrightarrow} H_n\left(X_1\right) \oplus H_n\left(X_2\right) \stackrel{g_*-j_*}{\longrightarrow} H_n(X) \stackrel{D}{\longrightarrow} H_{n-1}\left(X_1 \cap X_2\right) \longrightarrow \cdots,
		  $$
		  with $i_1, i_2, g, j$ inclusions and $D=d h_*^{-1} q_*$, where $h, q$ are inclusions and $d$ is the connecting homomorphism of the pair $\left(X_1, X_1 \cap X_2\right)$.
			- The proof is not hard, just using excision, the above [lemma](((649955ae-5920-4aa5-8d1d-f5a3171d430c))) and [naturality of the connecting homomorphism](((647e8f80-4fe7-4abf-9afb-b68d9132f3db))) together.
			- However it's obvious the theorem is powerful.
			  It's the analog of the [[Seifert-van Kampen Theorem]], which allows to construct the group of the whole space from its 'parts'.
				- Seifert-van Kampen Theorem can be rephrased by the short exact sequence:
				  $$0 \rightarrow \pi_1(X_1 \cap X_2)  \stackrel{i}{\rightarrow} \pi_1(X_1) * \pi_1(X_2) \stackrel{p}{\rightarrow}  \pi_1(X) \stackrel{}{\rightarrow} 0$$
				- Strategy: ((649b9c9e-6796-4991-9241-b012ae76ccee))
			- Example. Homology groups of $S^1$
			  id:: 649b9cbd-4a34-42d6-bcc4-97f1a0f91445
				-
				- Divide $S^1$ into two subspaces:
				  ![Image.png](../assets/Image_1687921021121_0.png){:height 232, :width 211}
					- Note that both are contractible, so
					  $H_n(X_1)=0$ for $n \geq 1$, $H_n(X_1)=\mathbb Z$ for $n = 0$
				- For $n>1$, we have the sequence
				  $$0 \rightarrow H_n(S^1) \rightarrow 0$$,
				  thus $H_n(S^1)=0$.
				- For $n=1$:
					- $$
					  0 \rightarrow H_1(S^1) \stackrel{D}{\longrightarrow} H_0\left(X_1 \cap X_2\right) \stackrel{\left(i_{1 *}, i_{2 *}\right)}{\longrightarrow} H_0\left(X_1\right) \oplus H_0\left(X_2\right) \stackrel{g_*-j_*}{\longrightarrow} H_0(X) \stackrel{D}{\longrightarrow} 0
					  $$
					- The sequence can be rewritten:
					  $$
					  0 \rightarrow H_1(S^1) \stackrel{D}{\longrightarrow} Z \oplus Z \stackrel{\left(i_{1 *}, i_{2 *}\right)}{\longrightarrow} Z \oplus Z \stackrel{g_*-j_*}{\longrightarrow} Z\stackrel{D}{\longrightarrow} 0
					  $$
					- $$
					  0 \rightarrow H_1(S^1) \stackrel{D}{\longrightarrow} Z \oplus Z \stackrel{\begin{array}{l}Im=Z\\Ker=Z\end{array}}{\longrightarrow} Z \oplus Z \stackrel{ \begin{array}{l}Im=Z\\Ker=Z\end{array}}{\longrightarrow }Z\stackrel{\begin{array}{l}Im=0\\Ker=Z\end{array}}{\longrightarrow} 0
					  $$
						- Note that we must examine the details of maps like $(i_{1*},i_{2*})$, since we cannot obtain $\operatorname{Ker}$ from $\operatorname{Im}$.
						  background-color:: red
						  For example, $Z / Z_n \simeq Z$ for arbitrary $n$.
					- Obviously $H_1(S^1)=\operatorname{Im}D=Z$.
				-
		- ((649cef7f-3587-45f0-af4b-ec8471ef0d5d)) (Mayer-Vietoris Theorem for Reduced Homology). If $X_1, X_2$ are subspaces of $X$ with $X=X_1^{\circ} \cup X_2^{\circ}$ and $X_1 \cap X_2 \neq \varnothing$, then there is an exact sequence
		  card-last-interval:: 29.95
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-11T11:51:17.923Z
		  card-last-reviewed:: 2023-07-12T13:51:17.923Z
		  card-last-score:: 5
		  $$
		  \cdots \rightarrow \widetilde{H}_n\left(X_1 \cap X_2\right) \rightarrow \widetilde{H}_n\left(X_1\right) \oplus \widetilde{H}_n\left(X_2\right) \rightarrow \widetilde{H}_n(X) \rightarrow \widetilde{H}_{n-1}\left(X_1 \cap X_2\right) \rightarrow \cdots
		  $$
		  with induced maps as in Theorem 6.3. This sequence ends
		  $$
		  \cdots \rightarrow \widetilde{H}_0\left(X_1\right) \oplus \widetilde{H}_0\left(X_2\right) \rightarrow \widetilde{H}_0(X) \rightarrow 0
		  $$
			- The key ideas are all the same: Use excision to obtain the isomorphisms, naturality of connecting homomorphisms, Barrett-Whitehead.
			- The only additional subtlety is at $n=0$, where we should verify the embedding map is indeed an isomorphism.
				- Note that $\tilde S_{-1}(X,A)=0$, thus $\tilde H_0(X,A)=H_0(X,A)$.
				-
			- i.e. **Reduced homology doesn't affect relative homology.**
	- ## Applications
	  collapsed:: true
		- ((649cf085-8b8d-44f2-b4ef-e754b39ba39e)). (Homology of [[Sphere]]) Let $S^n$ be the $n$-sphere, where $n \geq 0$. Then
		  card-last-score:: 5
		  card-repeats:: 1
		  card-next-schedule:: 2023-08-28T18:48:31.221Z
		  card-last-interval:: 31.26
		  card-ease-factor:: 2.6
		  card-last-reviewed:: 2023-07-28T12:48:31.222Z
		  $$
		  \widetilde{H}_p\left(S^n\right)= \begin{cases}\mathbf{Z} & \text { if } p=n \\ 0 & \text { if } p \neq n\end{cases}
		  $$ #card
			- Intuition
				- On $S^n$ there is only one 'whole', i.e. the interior of the sphere.
			- $n=0$ is trivial.
			- $n \geq 1$:
			  collapsed:: true
				- Separate $S^n$ into two charts (as if giving it the simplest smooth structure).
				- $X_1$, $X_2$ are both contractible, while $X_1 \cap X_2 \simeq S^{n-1}$.
				  collapsed:: true
					- Note that for contractible spaces, $\tilde H_n(X)=0$.
				- Therefore we can rewrite the exact sequence
				  $$
				  \cdots \rightarrow \widetilde{H}_n\left(X_1 \cap X_2\right) \rightarrow \widetilde{H}_n\left(X_1\right) \oplus \widetilde{H}_n\left(X_2\right) \rightarrow \widetilde{H}_n(X) \rightarrow \widetilde{H}_{n-1}\left(X_1 \cap X_2\right) \rightarrow \cdots
				  $$into
				  $$
				  \cdots \rightarrow \widetilde{H}_p (S^{n-1}) \rightarrow 0 \rightarrow \widetilde{H}_p(S^n) \rightarrow \widetilde{H}_{p-1}(S^{n-1}) \rightarrow 0 \rightarrow \cdots
				  $$
				  which finishes the proof by induction.
			- #+BEGIN_NOTE
			  Again the value of the reduced homology is illustrated.
			  Without it we have to treat $n=0$ and $n \geq 1$ separately!
			  #+END_NOTE
			- Corollary. $S^n$ isn't contractible.
			- Corollary. $\mathbb R^m$ isn't homeomorphic to $\mathbb R^n$ when $m \neq n$.
			-
		- Lemma 6.21. Let $f, g: S^n \rightarrow S^n$ be continuous maps.
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-26T18:39:57.936Z
		  card-last-reviewed:: 2023-07-26T12:39:57.936Z
		  card-last-score:: 5
		  (i) $d(g \circ f)=d(g) d(f)$.
		  (ii) $d\left(1_{S^n}\right)=1$.
		  (iii) If $f$ is constant, then $d(f)=0$.
		  (iv) If $f \simeq g$, then $d(f)=d(g)$.
		  (v) If $f$ is a homotopy equivalence, then $d(f)= \pm 1$.
			- (i) and (ii) roughly states that 'd is a homomorphism'.
		- ((64aebc8f-0c64-4254-8e23-9ab108975547)). If $n \geq 1$, then the antipodal map $a^n: S^n \rightarrow S^n$ has degree $(-1)^{n+1}$. #card
		  id:: 64aebc70-fcef-45e1-b9d1-2f81749bb8c4
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.36
		  card-next-schedule:: 2023-09-16T18:28:23.887Z
		  card-last-reviewed:: 2023-08-16T12:28:23.887Z
		  card-last-score:: 3
			- *To be completed.*
				- The exercise doesn't concern 'intrinsic properties', but it is a great test of the technique.
			- Degree of a continuous map $f$ : $S^n \rightarrow S^n$
			  card-last-interval:: 32.57
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-09-12T01:25:10.313Z
			  card-last-reviewed:: 2023-08-10T12:25:10.313Z
			  card-last-score:: 5
				- Definition. A continuous map $f$ : $S^n \rightarrow S^n$ (where $n>0$ ) has degree $m$, denoted by $d(f)=m$, if $f_*: H_n\left(S^n\right) \rightarrow H_n\left(S^n\right)$ is multiplication by $m$.
			- Definition. If $x=\left(x_1, \ldots, x_{n+1}\right) \in S^n$, its antipode is $-x=\left(-x_1, \ldots,-x_{n+1}\right)$. The antipodal map $a=a^n: S^n \rightarrow S^n$ is defined by $x \mapsto-x$.
			-
			- Proof
				- First, the antipodal map is the composition of $n+1$ maps to invert one coordinate. So we only need find the degree of one such map.
				-
				-
- # The Homotopy Axiom
  collapsed:: true
	- We are concerned with the problem:
	  When does $H_n(f)=H_n(g)$
	  Does it hold when $f$ and $g$ are homotopic?
	- ((6455bc34-9cfb-4aff-9eda-66b2797bb373)). If $X$ is a bounded convex subspace of euclidean space, then $H_n(X)=0$ for all $n \geq 1$.
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-08-29T18:30:54.440Z
	  card-last-reviewed:: 2023-07-29T12:30:54.441Z
	  card-last-score:: 5
	  collapsed:: true
		- Remark
			- Actually $X$ is contractible. But the method of cone construction is also worth learning.
		- Geometric intuition
			- Consider an 1-cycle in $D^2$. 
			  We want to 'fill the interior' of the cycle to obtain its bulk. But how to define the 'filling'?
		- Proof
			- Key idea: ((6461ca0c-d0bf-40d1-bc3f-5ce24fd244b9))
				- It is an elegant solution for 'filling the interior'!
				- The unwanted faces of the cones would cancel if $\sigma$ is a cycle.
				- The insight is that dealing with each simplex **separately** would be much easier than dealing with the chain as a whole.
			- Use the proposition $\partial_{n+1} c_n(\sigma)=\sigma-c_{n-1} \partial_n(\sigma)$, we easily see that $c_n(\sigma)$ is precisely the desired bulk!
	- ((64677c74-e1cc-4cb6-8792-ba9c791213f7)) (Homotopy Axiom). If $f, g: X \rightarrow Y$ are homotopic, then $H_n(f)=H_n(g)$ for all $n \geq 0$. #card
	  id:: 6498e102-758e-44db-bbcb-a7c679b43a90
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.46
	  card-next-schedule:: 2023-12-08T00:34:02.978Z
	  card-last-reviewed:: 2023-10-27T00:34:02.978Z
	  card-last-score:: 5
		- Intuition
			- Obviously we need to start from the homotopy map $F$.
			- In short, if we view $F_\#(\sigma \times I)$ as a map from $\Delta^n \times I$ to $X \times I$, then $\partial F_\#(\sigma \times I)$ consists of the 'top' $f_\# (\sigma)$, the 'bottom' $-g_\# (\sigma$) and 'sides' $F_\# (\partial \sigma)$.
		-
		- This is a standard construction called *the method of acyclic models*!
			- The problem is, why does the author proves a simple intuition in such a cumbersome way? Is there any deeper reason?
			-
		- Lemma 1. Assume that $f, g: X \rightarrow Y$ are continuous maps and that there are homomorphisms $P_n: S_n(X) \rightarrow S_{n+1}(Y)$ with
		  id:: 64645091-3e12-430a-aeb4-5ec910663e10
		  $$
		  f_{\#}-g_{\#}=\partial_{n+1}^{\prime} P_n+P_{n-1} \partial_n .
		  $$
		  then $H_n(f)=H_n(g)$ for all $n \geq 0$.
			- The lemma formalizes the intuition of 'find a bulk for any $f_\#(\sigma)-g_\#(\sigma)$'
			- The second term is zero for cycles, i.e. a 'freedom of choice'.
		- Lemma 2. Let $X$ be a space and, for $i=0,1$, let $\lambda_i^X: X \rightarrow X \times \mathbf{I}$ be defined by $x \mapsto(x, i)$. If $H_n\left(\lambda_0^X\right)=H_n\left(\lambda_1^X\right): H_n(X) \rightarrow H_n(X \times \mathbf{I})$, then $H_n(f)=H_n(g)$ whenever $f$ and $g: X \rightarrow Y$ are homotopic. #card
		  card-last-interval:: 32.57
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-06-22T14:04:06.283Z
		  card-last-reviewed:: 2023-05-21T01:04:06.284Z
		  card-last-score:: 5
			- An interesting exercise -- mainly a conceptual challenge rather than a technical one!
				- This is the merit of formality: We can view path and homotopy as maps and operate on them formally!
		- By lemma 1, we need to show $H_n\left(\lambda_0^X\right)=H_n\left(\lambda_1^X\right): H_n(X) \rightarrow H_n(X \times \mathbf{I})$.
			- Intuitively this is obvious:
			  ![Image(1).png](../assets/Image(1)_1684503924712_0.png){:height 232, :width 159}
			  we just need to fill the 'body' of the upper and lower face.
			- However, the precise filling map is hard to construct.
			- Actually we can't directly construct one for $X \times I$, but we should construct
			  $$\beta_{n+1}=\sum_{i=0}^n(-1)^i\left[a_0, \ldots, a_i, b_i, b_{i+1}, \ldots, b_n\right]$$
			  as a simplex in $\Delta^n \times I$.
			- Exercise. Compare to 
			  $$
			  P_n^X(\sigma)=(\sigma \times 1)_{\#}\left(\beta_{n+1}\right)
			  $$
			  and discuss: how is the problem 'can't directly construct' resolved?
		- By lemma 2, we need to find a map $P_n: S_n(X) \rightarrow S_{n+1}(X \times I)$ with
		  $$
		  (\lambda_0^X)_{\#}-(\lambda_1^X)_{\#}=\partial_{n+1}^{\prime} P_n+P_{n-1} \partial_n .
		  $$
		- Our strategy would be induction.
			- The inductive hypothesis should be strengthened by a **naturality condition**:
			  ((64677ebd-5c56-4ade-a1bc-cea658778ec7))
		- $n=0$:
			- Necessarily $P_{n-1}=0$.
			- We need to find $P_0$ such that $(\lambda_0^X)_{\#}-(\lambda_1^X)_{\#}=\partial_{n+1}^{\prime} P_0$.
				- Note that $\Delta_0$ is a single point.
			- Directly plug in a simplex $\sigma$, we find that $P_0(\sigma): t \mapsto (\sigma(e),t)$ serves.
		- Now lets use induction for some $n$:
			- We'd like to find some $P_n$ s.t.
			  $$
			  (\lambda_0^X)_{\#}-(\lambda_1^X)_{\#}=\partial_{n+1}^{\prime} P_n+P_{n-1} \partial_n .
			  $$
			- First, note that
			  $$
			  \begin{aligned}
			  \partial_n\left(\lambda_{1 \#}^{X}-\lambda_{0 \#}^{X}-P_{n-1}^{X} \partial_n\right) & =\lambda_{1 \#}^{X} \partial_n-\lambda_{0 \#}^{X} \partial_n-\partial_n P_{n-1}^{X} \partial_n  \\
			  & =\lambda_{1 \#}^{X} \partial_n-\lambda_{0 \#}^{X} \partial_n-\left(\lambda_{1 \#}^{X}-\lambda_{0 \#}^{X}-P_{n-2}^{X} \partial_{n-1}\right) \partial_n \quad \text{(by induction)}
			  \\
			  & =0 \quad(\text { since } \partial \partial=0)
			  \end{aligned}
			  $$
			  which means it is a boundary.
			- Here is the stroke of genius:
			  We take the simplex to be the identity map $\delta: \Delta^n \rightarrow \Delta^n$ and the space to be $\Delta^n$.
			- Now since $H_n(\Delta^n \times I)=0$, a cycle must also be a boundary.
			  Thus we can find $\beta_{n+1} \in S_{n+1}\left(\Delta^n \times \mathrm{I}\right)$ with 
			  $$
			  \partial_{n+1} \beta_{n+1}=\left(\lambda_{1 \#}^{\Delta}-\lambda_{0 \#}^{\Delta}-P_{n-1}^{\Delta} \partial_n\right)(\delta) .
			  $$
			- Define $P_n^X: S_n(X) \rightarrow S_{n+1}(X \times \mathrm{I})$ by
			  $$
			  P_n^X(\sigma)=(\sigma \times 1)_{\#}\left(\beta_{n+1}\right)
			  $$
			  and we're done.
				- Just check the two conditions to be satisfied!
	- Corollary. If $X$ is contractible, then $H_n(X)=0$ for all $n>0$. #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-07-07T07:41:36.766Z
	  card-last-reviewed:: 2023-06-06T01:41:36.766Z
	  card-last-score:: 5
- # The Hurewicz Theorem #card
  id:: 654072b9-eb4d-452a-bd41-aff0c934d68c
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-12-30T07:19:59.296Z
  card-last-reviewed:: 2023-11-29T01:19:59.297Z
  card-last-score:: 3
  collapsed:: true
	- Definition. Hurewicz map
		- For any path-connected space $X$ and positive integer $n$ there exists a group homomorphism
		  $$
		  h_*: \pi_n(X) \rightarrow H_n(X),
		  $$
		  called the Hurewicz homomorphism, defined in the following way: choose a canonical generator $u_n \in H_n\left(S^n\right)$, then a homotopy class of maps $f \in \pi_n(X)$ is taken to $f_*\left(u_n\right) \in H_n(X)$.
		- For $n=1$, it is just 'taking the homology class of the path'.
	- Theorem. The Hurewicz map is a homomorphism.
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-22T19:16:39.273Z
	  card-last-reviewed:: 2023-08-22T13:16:39.273Z
	  card-last-score:: 5
	  collapsed:: true
		- The goal is to prove that $\varphi([f * g])=\varphi([f])+\varphi([g])$, i.e.
		  collapsed:: true
		  $$\operatorname{cls} (f*g)\eta=\operatorname{cls} f\eta+\operatorname{cls} g\eta$$
			- $\eta$ is the homeomorphism identifying $\Delta^1$ and $I$
		- Which means I shall prove
		  $$(f*g)\eta-f\eta-g\eta$$
		  is a boundary.
		- The geometric construction is follows:
		  ![Image(1).png](../assets/Image(1)_1684844301594_0.png){:height 379, :width 433}
			- Key idea: $f_\# \partial=\partial f_\#$, thus we can use the space $I \times I$, which has better properties.
				- To be more specific, we want to show the boundary of a certain simplex is $f+g-f*g$.
				- Therefore we could view it as being pushed forward from a simplex in another space ($X \times I$) and consider the boundary operator in that space.
				- Moreover, $I \times I$ could be easily mapped into $X \times I$.
					- Direct product with $I$ is the simplest way to 'add a dimension'.
					- Finding an interior is hard (only easy for convex sets). $X \times I$ is a childish way to find an interior, i.e. collapse a dimension.
					-
				-
			- First we construct a chain $\sigma \in S_2(I \times I)$ illustrated as in the figure.
			- Consider $\pi:(x,t) \mapsto x$.
			  collapsed:: true
			  Easy to see $\pi_\# \partial_2 \sigma = (f*g)\eta-f\eta-g\eta$.
				- The left and right sides cancel.
				- Two blue arrows on the upper sides are just $f\eta$ and $g\eta$.
			- Then by the key idea, RHS is a boundary!
			-
	- ((646cb116-3fcc-4afe-9117-7e4157dc1689))  (Hurewicz Theorem). If $X$ is path connected, then the Hurewicz map $\varphi: \pi_1\left(X, x_0\right) \rightarrow H_1(X)$ is a surjection with kernel $\pi_1\left(X, x_0\right)^{\prime}$, the commutator subgroup of $\pi_1\left(X, x_0\right)$. Hence
	  card-last-interval:: 27.32
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-07-12T08:15:12.784Z
	  card-last-reviewed:: 2023-06-15T01:15:12.784Z
	  card-last-score:: 5
	  $$
	  \pi_1\left(X\right) / \pi_1\left(X\right)^{\prime} \cong H_1(X)
	  $$
		- *Could be generalized to higher homotopy and homology groups, which would lead to new insights!
		- Surjectivity
			- Could be explicitly constructed by 'joining' the simplexes like line segments to form a closed path.
		- Kernel
			- Step 1. $\pi_1' \sub \operatorname{ker}\varphi$
				- It's rather simple, since $H_1(X)$ is abelian and every $H=G'$ is the smallest subgroup s.t. $G/H$ is abelian.
			- Step 2. $\operatorname{ker}\varphi \sub \pi_1'$
				- #+BEGIN_NOTE
				  It is necessary to look into the boundary map and construct paths.
				  #+END_NOTE
				- First, we consider some $f \in \operatorname{ker} \varphi$, i.e. $f \eta = \partial_2 \sigma$.
				- Expand into basis elements (2-simplexes),
				  $$\gamma\eta=\sum n_{i}(\tau_{i0}-\tau_{i1}+\tau_{i2})$$
				- Then it is necessary to construct a path. However, it is easier to work in the abelian group $\pi / \pi'$ where all elements commute.
				- The rest of the work is to construct a path and show that it indeed belongs to $\pi'$, which requires some simple algebra.