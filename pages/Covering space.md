- Defs
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
		  collapsed:: true
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
	  collapsed:: true
		- The map $p: \mathbb{R} \rightarrow S^1$ given by the equation
		  $$
		  p(x)=(\cos 2 \pi x, \sin 2 \pi x)
		  $$
		  is a covering map. #card
			- A classical example, but extremely useful -- and with some deep thoughts behind.
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
-