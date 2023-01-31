- Defs
	- Lifting #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-02-23T03:25:30.230Z
	  card-last-reviewed:: 2023-01-30T03:25:30.231Z
	  card-last-score:: 5
		- ((63784f8e-385d-4529-9c3b-3af9cb1b9d82))
		  $\bar f$ is a lifting of f.
			- *Not restricted to paths.*
			- p is a [[Covering map]]
	- Lifting correspondence
	  collapsed:: true
		- ((638c0dc2-8ba5-49b1-a443-6a4c808f0acf)) Let $p: E \rightarrow B$ be a covering map; let $b_0 \in B$ Choose $e_0$ so that $p\left(e_0\right)=b_0$. Given an element $[f]$ of $\pi_1\left(B, b_0\right)$, let $\bar{f}$ be the lifting of $f$ to a path in $E$ that begins at $e_0$. Let $\phi([f])$ denote the end point $\tilde{f}(1)$ of $\tilde{f}$.
			- Note that lifting preserves path homotopy, so the map is independent of the representative.
		- Then the **lifting correspondence** $\phi$ is a well-defined set map
		  $$
		  \phi: \pi_1\left(B, b_0\right) \rightarrow p^{-1}\left(b_0\right) .
		  $$
			- Interestingly, a loop may not be mapped to a loop. eg $\ln z$
			- Something similar to [[Berry Phase]]?
- Paths and path homotopies can be uniquely lifted.
  collapsed:: true
	- ((63830159-da94-4cac-9da6-bf8c5a61256e)) Let $p: E \rightarrow B$ be a covering map, let $p\left(e_0\right)=b_0$. Any path $f: [0,1] \rightarrow B$ beginning at $b_0$ has a unique lifting to a path $\bar{f}$ in $E$ beginning at $e_0$. #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-01-20T06:15:19.538Z
	  card-last-reviewed:: 2022-12-27T06:15:19.539Z
	  card-last-score:: 5
		- Intuition
			- The path f have several 'copies' in the covering space, with different starting points.
		- Proof
			- Idea
				- Each segment (small enough to be contained in some $U_i$) has several disjoint copies in E.
				- Construct closed sets, so the $j^{th}$ segment can grant the unique choice of $(j+1)^{th}$.
				- Put the segments together, we obtain a path in E.
			- 1. Take the open sets $\{U_j\}$, which are evenly covered by p.
			- 2. Divide $[0,1]$ into several closed intervals $\{[s_i,s_{i+1}]\}$ such that $f([s_i,s_{i+1}])$ is entirely contained in some $U_{j_i}$
				- The existence of the division is guaranteed by [[The Lebesgue number lemma]]. **[0,1] is a compact metric space!**
				- The construction has several merits: Each set is closed, whose endpoints can be used; the collection is finite (Let alone [[Countable]] ), which allows induction.
			- 3. Proceed inductively to define $\bar f$.
				- The intervals are mapped back by $p^{-1}$ into disjoint slices.
				- The endpoints grant a unique choice.
	- ((639146c8-4398-49fe-b838-f118e24d243b)) Let $p: E \rightarrow B$ be a covering map; let $p\left(e_0\right)=b_0$. Let the map $F: I \times I \rightarrow B$ be continuous, with $F(0,0)=b_0$. There is a **unique lifting** of $F$ to a continuous map
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-01-17T12:55:43.810Z
	  card-last-reviewed:: 2022-12-24T12:55:43.810Z
	  card-last-score:: 5
	  $$
	  \tilde{F}: I \times I \rightarrow E
	  $$
	  such that $\bar{F}(0,0)=e_0$. If $F$ is a path homotopy, then $\tilde{F}$ is a **path homotopy**. #card
		- The strategy is similar to Lemma 54.1 : Construct a finite collection of closed sets (For example, rectangles), then define $\bar F$ on them one by one.
		- It's also easy to verify that $\bar F$ is a path homotopy. We only need to verify the extra condition that the endpoints are fixed.
		-
	-
- Therefore, 'being homotopic' can also be lifted.
  collapsed:: true
	- Theorem 54.3. Let $p . E \rightarrow B$ be a covering map; let $p\left(e_0\right)=b_0$. Let $f$ and $g$ be two paths in $B$ from $b_0$ to $b_1$, let $\tilde{f}$ and $\tilde{g}$ be their respective liftings to paths in $E$ beginning at $e_0$. If $f$ and $g$ are path homotopic, then $\tilde{f}$ and $\tilde{g}$ end at the same point of $E$ and are path homotopic.
	-
-
- Lifting the fundamental group
	- ((638c3f1f-7609-4ec8-880f-7b851dea0f63)) Let $p: E \rightarrow B$ be a covering map; let $p\left(e_0\right)=b_0$. If $E$ is **path connected**, then the lifting correspondence $\phi: \pi_1\left(B, b_0\right) \rightarrow p^{-1}\left(b_0\right)$ is **surjective**. If $E$ is **simply connected**, it is **bijective**. #card
	  card-last-score:: 5
	  card-repeats:: 2
	  card-next-schedule:: 2023-01-19T04:18:07.464Z
	  card-last-interval:: 24
	  id:: 638c0f2d-33eb-4634-9467-e083bf50506d
	  card-ease-factor:: 2.7
	  card-last-reviewed:: 2022-12-26T04:18:07.464Z
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
			- Bijective(Surjective): If E is path connected, $\phi$ is surjective.
		- (c)
			- Directly follows from the definition of lifting. Or from (b).