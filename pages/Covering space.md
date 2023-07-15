- # Defs
	- Evenly covered #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-04-16T15:19:05.456Z
	  card-last-reviewed:: 2023-02-08T11:19:05.456Z
	  card-last-score:: 5
		- Definition. Let $p : E \rightarrow B$ be a continuous surjective map. The open set $U$ of $B$ is said to be **evenly covered** by $p$ if the inverse image $p^{-1}(U)$ can be written as the union of **disjoint** open sets $V_\alpha$ in $E$ such that for each $\alpha$, the restriction of $p$ to $V_\alpha$ is a **homeomorphism** of $V_\alpha$ onto $U$ The collection $\left\{V_\alpha\right\}$ will be called a partition of $p^{-1}(U)$ into slices
			- In other words, E contains several disjoint copies of U, which are 'squashed into one' by p.
	- [[Covering map]]
		- Def #card
		  card-last-interval:: 67.2
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-04-10T16:12:10.508Z
		  card-last-reviewed:: 2023-02-02T12:12:10.510Z
		  card-last-score:: 5
			- Let $p: E \rightarrow B$ be continuous and surjective. If every point $b$ of $B$ **has a neighborhood** $U$ that is evenly covered by $p$, then $p$ is called a covering map, and $E$ is said to be a covering space of $B$
				- This is not a very [[Global]] property. Each point can only be sliced [[Locally]]
			- ((637847e2-9127-482b-b496-95136f6e6f95))
			- ((6378484a-4de6-4e9c-9ea8-8b3c8572e378))
			- A [[Covering map]] is a [[Local Homeomorphism]], but not vice versa. For example, the map $p: \mathbb{R}_{+} \rightarrow S^i$ given by the equation
			  collapsed:: true
			  $$
			  p(x)=(\cos 2 \pi x, \sin 2 \pi x)
			  $$
				- The map is 'broken' near the origin.
	- Examples
		- The map $p: \mathbb{R} \rightarrow S^1$ given by the equation
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-14T19:11:23.223Z
		  card-last-reviewed:: 2023-07-14T13:11:23.223Z
		  card-last-score:: 5
		  $$
		  p(x)=(\cos 2 \pi x, \sin 2 \pi x)
		  $$
		  is a covering map. #card
			- A classical example, but extremely useful -- and with some deep thoughts behind.
				- Intuitively, 'expand the space globally while retaining the local structure'.
			- We can construct a covering of $$T^2=S^1\times S^1$$ by $$R\times R$$ in this way.
		- $p:S^1\to S^1$ by $$p(\theta)=2\theta$$
		- Figure-eight space
			- ((63784d71-542c-40ba-be3d-f1946bca1676))
			- ((63784d7a-336b-4b06-8ca7-2641dce6a7de))
		- [[Riemann surface]]
			- Composite $p \times i: \mathbb{R} \times \mathbb{R}_{+} \longrightarrow S^1 \times \mathbb{R}_{+}$ with the standard isomorphism of $S^1\times R_+$ with $R^2-0$
			- ((63784f05-388d-4aee-a1a4-91261088de4c))
			-
		-
- [[Lifting]]
- # Calculate the [[Fundamental Group]]
	- ((638c3f1f-7609-4ec8-880f-7b851dea0f63)) Let $p: E \rightarrow B$ be a covering map; let $p\left(e_0\right)=b_0$. If $E$ is **path connected**, then the lifting correspondence $\phi: \pi_1\left(B, b_0\right) \rightarrow p^{-1}\left(b_0\right)$ is **surjective**. If $E$ is **simply connected**, it is **bijective**. #card
	  card-last-score:: 5
	  card-repeats:: 3
	  card-next-schedule:: 2023-07-07T00:31:01.610Z
	  card-last-interval:: 84
	  id:: 638c0f2d-33eb-4634-9467-e083bf50506d
	  card-ease-factor:: 2.8
	  card-last-reviewed:: 2023-04-14T00:31:01.611Z
		- Intuition
			- (1) A path from $e_0$ to $e_1$ is compressed into a loop by the covering map. It is decompressed by the lifting correspondence.
			- (2) We just need to prove it is injective.
				- Simply connected -> All paths with same endpoints are homotopic -> Still homotopic after kicked down by the covering map
		- What about the inverse?
		  collapsed:: true
			- Surjective -> All 'copies' can be connected by paths. Anything stronger?
			- Injective -> Different loops get mapped to different endpoints.
		- Examples in complex analysis
		  collapsed:: true
			- $\ln z$
				- The [[Riemann surface]] is path connected. Indeed the lifting is surjective; each round adds $2\pi$.
				- Is the [[Riemann surface]] simply connected? But it seems indeed bijective, because the fundamental group of $\mathbb C -0$ is $\mathbb Z$.
			- $\sqrt x$
				- Surjective but not bijective.
			-
		- Applications
			- Construct a simply connected covering space to obtain the fundamental group?
	- ((638c406f-36aa-4e14-916a-5bfa265284e8)) Let $p: E \rightarrow B$ be a covering map; let $p\left(e_0\right)=b_0$.
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-03-24T00:40:44.713Z
	  card-last-reviewed:: 2023-02-28T00:40:44.714Z
	  card-last-score:: 5
	  (a) The homomorphism $p_*: \pi_1\left(E, e_0\right) \rightarrow \pi_1\left(B, b_0\right)$ is a **monomorphism**.
	  (b) Let $H=p_*\left(\pi_1\left(E, e_0\right)\right)$. The lifting correspondence $\phi$ induces an **injective** map
	  $$
	  \Phi: \pi_1\left(B, b_0\right) / H \rightarrow p^{-1}\left(b_0\right)
	  $$
	  of the collection of right cosets of $H$ into $p^{-1}\left(b_0\right)$, which is **bijective** if $E$ is path connected.
	  (c) If $f$ is a loop in $B$ based at $b_0$, then $[f] \in H$ **if and only if** $f$ lifts to a loop in $E$ based at $e_0$. #card
		- (a) Lifting preserves path homotopy.
		- (b)(c) Intuitively, H is the 'trivial part after lifting'.
		- (b)
			- Independent of the representative element: If $f_2=f_1 * h$ and $\tilde h$ is a loop, then obviously $\phi(f_2)=\phi(f_1)$
			- Injective: If $\phi(f_2)=\phi(f_1)$, then $\phi(f_2 * f_1^{-1})=e$ (go backwards)
			- Bijective(Surjective): If E is path connected, we can always find a path from $b_1$ to $b_2$. Thus $\phi$ is surjective.
		- (c)
			- Directly follows from the definition of lifting. Or from (b).
	-