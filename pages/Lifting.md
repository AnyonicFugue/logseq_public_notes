- # Defs
	- Lifting #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-08-15T00:39:31.969Z
	  card-last-reviewed:: 2023-05-23T00:39:31.969Z
	  card-last-score:: 5
		- ((63784f8e-385d-4529-9c3b-3af9cb1b9d82))
		  $\bar f$ is a lifting of f.
			- *Not restricted to paths.*
			- p is a [[Covering map]]
		- Idea: Embed into something better.
	- Lifting correspondence #card
		- ((638c0dc2-8ba5-49b1-a443-6a4c808f0acf)) Let $p: E \rightarrow B$ be a covering map; let $b_0 \in B$ Choose $e_0$ so that $p\left(e_0\right)=b_0$. Given an element $[f]$ of $\pi_1\left(B, b_0\right)$, let $\bar{f}$ be the lifting of $f$ to a path in $E$ that begins at $e_0$. Let $\phi([f])$ denote the end point $\tilde{f}(1)$ of $\tilde{f}$.
			- Note that lifting preserves path homotopy, so the map is independent of the representative.
		- Then the **lifting correspondence** $\phi$ is a well-defined set map
		  $$
		  \phi: \pi_1\left(B, b_0\right) \rightarrow p^{-1}\left(b_0\right) .
		  $$
			- Interestingly, a loop may not be mapped to a loop. eg $\ln z$
			- Something similar to [[Berry Phase]]?
- # Facts
	- Paths and path homotopies can be uniquely lifted.
	  collapsed:: true
		- ((63830159-da94-4cac-9da6-bf8c5a61256e)) Let $p: E \rightarrow B$ be a covering map, let $p\left(e_0\right)=b_0$. Any path $f: [0,1] \rightarrow B$ beginning at $b_0$ has a unique lifting to a path $\bar{f}$ in $E$ beginning at $e_0$. #card
		  card-last-interval:: 67.2
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-05-14T07:57:03.342Z
		  card-last-reviewed:: 2023-03-08T03:57:03.342Z
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
		  card-last-interval:: 67.2
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-05-20T05:00:55.053Z
		  card-last-reviewed:: 2023-03-14T01:00:55.053Z
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
		- Theorem 54.3. Let $p : E \rightarrow B$ be a covering map; let $p\left(e_0\right)=b_0$. Let $f$ and $g$ be two paths in $B$ from $b_0$ to $b_1$, let $\tilde{f}$ and $\tilde{g}$ be their respective liftings to paths in $E$ beginning at $e_0$. If $f$ and $g$ are path homotopic, then $\tilde{f}$ and $\tilde{g}$ end at the same point of $E$ and are path homotopic.
		-
	-