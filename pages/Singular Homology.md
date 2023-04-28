- Idea #card
	- [[Green's Theorem]] tells us that we can determine the behavior of the bulk by its boundary.
	  We'd like to generalize this into topology.
	- Furthermore, a 'hole' in a space is implied by the existence of some **cycle** which is not a **boundary**.
		- The intuition comes from $S^1$ in $\mathbb R^2-0$.
		- However, note that a single point is a cycle but not a boundary.
- # Defs
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
	  collapsed:: true
		- Let $X$ be a topological space. For each $n \geq 0$, define $S_n(X)$ as the **free abelian group** with basis all singular $n$-simplexes in $X$; define $S_{-1}(X)=0$.
		  id:: 64462e13-2a8c-4f01-b999-632c7b8b0110
		  collapsed:: true
			- Often it seems that free (abelian) groups are structureless since they're free. How things are different here?
			  background-color:: pink
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
		- For each $n \geq 0$, the $n$th (singular) homology group of a space $X$ is
		  $$
		  H_n(X)={Z_n(X)}/{B_n(X)} \equiv {\operatorname{Ker} \partial_n}/{\operatorname{Im} \partial_{n+1}} .
		  $$
		  The coset $z_n+B_n(X)$, where $z_n$ is an $n$-cycle, is called the homology class of $z_n$, and it is denoted by cls $z_n$.
			- Note that the group is **abelian** so everything is normal.
		- Strikingly simple in form, but daunting in its depth and implications!
		  background-color:: yellow
			- To study a space $X$, we invent strange things called 'simplexes' which is defined by a continuous map from $\Delta^n$ to $X$.
				- It's strange at first sight that we define structures by maps rather than 'things in $X$', but this somehow echoes the spirit of category theory.
			- Then we manage to shape our intuition into the boundary operator.
			- The most bizarre things is introducing a structure of free abelian groups generated by simplexes. With a group structure everything emerges, but at first sight freely generated groups seem 'structureless'.
	- Betti number #card
		- The $n$-th Betti number of $X$ is $\operatorname{rank}H_n(X)$.
- # Basic Facts
	- ((644638a3-9be7-46f8-8abb-f6c3ae2849af)) For all $n \geq 0$, we have $\partial_n \partial_{n+1}=0$. #card
		- First we explicitly write down 
		  $$\partial_n \partial_{n+1} \sigma=\sum_{j, k}(-1)^{j+k} \sigma \varepsilon_j^{n+1} \varepsilon_k^n$$
		- Lemma 4.5. If $k<j$, the face maps satisfy
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
			- It reminds of the Poincare lemma.
			- Also similar to the geometrical intuition that 'a boundary is boundaryless'.
	- Proposition. $B_n(X) \in Z_n(X) \in S_n(X)$ #card
		- A simple exercise to recall the definitions and $\partial_n \partial_{n+1}=0$.
	- ((644a25af-79a6-4b3c-9ac7-e319e6a3b251)) For each $n \geq 0, H_n: \mathbf{Top}\rightarrow \mathbf{A b}$ is a functor. #card
		- '当你学了范畴后，看什么都是范畴'。
		- We should determine two things:
		  1. For $f \in \mathrm{Hom}_{\mathbf{Top}}(X,Y)$, how to define $H_n(f)$?
		  2. Does $H_n(f \circ g) = H_n(f) \circ H_n(g)$?
		- First question:
			- Obviously $f$ induces a homomorphism $f_\#: S_n(X) \to S_n(Y)$ by 
			  $$
			  f_{\#}\left(\sum m_\sigma \sigma\right)=\sum m_\sigma(f \circ \sigma)
			  $$
				- Note that $f \circ \sigma$ is also a simplex.
			- The key observation is
			  $$\partial_n f_{\#}=f_{\#} \partial_n$$
			  thus $f_{\#}$ both preserves cycles and chains.
			- The desired $H_n(f)$ is defined by $H_n(f): g+B_n(X) \mapsto f_{\#}(g)+B_n(Y)$.
			  Since $f_{\#}$ preserves cycles and chains, the codomain is correct and the map is independent of the representative.
		- Second question:
			- Equivalently, does $f_{\#} \circ g_{\#}=(f \circ g)_{\#}$?
			- Obviously, yes.
	- Corollary. If $X$ and $Y$ are homeomorphic, then $H_n(X) \cong H_n(Y)$ for all $n \geq 0$.
		- Since $f_{\#}$ can be inverted.
		- But to put it in another way -- the homology group is a topological invariant. We've found yet another one!