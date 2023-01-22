- This not only emerges in topological orders, but also in RCFTs.
	- If we view the same phenomena occur in different theories as a robust phenomena, it must have a simple reason. #Thoughts
	- ((63ba2d3f-81a8-4acb-b1c4-cc82f9d7ae2d))
		- ((63ba2d4c-0336-40d2-b096-5e9489404517)).
		- Interesting! Investigate it later! #[[ToRead]]
		- Mathematically: ((63ba2dc0-b1ee-48e6-8d59-201de7f43a7c)) #card
			- On the one hand, we may obtain the bulk from the boundary (if we know the correct definition of morphisms)
			- On the other hand, we may solve for the boundary by $\mathcal{C}=\mathfrak{Z}_1(?)$.
				- If there are no UMTC solutions, then the boundary must be gapless.
- Examples
  collapsed:: true
	- Counter example
		- Fuse 2 smooth boundaries of the toric code #card
		  card-last-interval:: 26.06
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-02-09T02:37:08.555Z
		  card-last-reviewed:: 2023-01-14T01:37:08.555Z
		  card-last-score:: 5
			- ((63a6b173-06e2-42e4-831d-f3e4d44d40ca))
			- The topological skeleton of the 1D order is $\operatorname{Rep}\left(\mathbb{Z}_2\right)$.
			- ((63a6b1a0-629d-4182-a4d1-1b0d6c6b75cf))
				- Why Vec? What's the bulk?
			- Answer: The topo order is **unstable**. With PBC, GSD=2.
				- The relation only holds for stable ones.
- Version of [[UMTC]] #card
  id:: 63a6b228-a5d2-400f-84c2-b7367f9cdef2
  card-last-interval:: 24
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-02-05T00:17:09.642Z
  card-last-reviewed:: 2023-01-12T00:17:09.642Z
  card-last-score:: 5
	- ((637ad40d-928c-428f-b8be-6efaaffb1156))
		- Which conditions are necessary?
	- (a) The bulk-to-boundary map $F: \mathcal{C} \rightarrow \mathcal{A}$ is a [[Central functor]].
	  (b) The central structure $F^{\prime}: \mathcal{C} \rightarrow \mathfrak{Z}_1(\mathcal{A})$ is a braided **equivalence**.
		- (b) gives an interesting restriction: An anomaly-free stable 2D topological order must be a [[Drinfeld center]] of something else.
		- Conversely, the theorem immediately implies that the [[Drinfeld center]] is **nondegenerate**. Mathematically, ((637ad683-2c60-43af-868c-f7eaacd40528))
	- ((637ad518-c09e-4960-9608-372911a8e757))
	-
- ((63aa639b-47e7-4f8f-b2d8-9f18c4231ac1)) Version of [[2-category]]
	- Setting
		- Topo skeleton of bulk is a 2-cat $\mathbf C$
		- Gapped boundaries of C and 0D domain walls form a finite semisimple 2-cat, $\mathbf M$
	- The [[bulk-to-boundary map]] induces an equivalence $\mathbf{C} \simeq \mathfrak{Z}_0(\mathbf{M})$ of multi-fusion 2-categories, where $\mathfrak{Z}_0(\mathbf{M}):=$ Fun $(\mathbf{M}, \mathbf{M})$ is the 2-category of $\mathbb{C}$-linear 2-functors from $\mathbf{M}$ to itself.
	-
	- ((63a6b228-a5d2-400f-84c2-b7367f9cdef2)) is a direct corollary when ((63aa6545-ebed-4d2f-962b-ebdb7b224be1)).
		- Just take $Hom(1_C,1_C)$, the cat of all topo excitations, in the equivalence.
-
- ((63aa65c7-5e7e-40f4-8216-535034102848)) 3D version #card
	- (a) The bulk topological defects of codimension 2 and higher form a braided fusion 2-category $\mathbf{B}$.
		- 'Codimemsion >=2' excludes point-like excitations??
	- (b) The topological skeleton of the boundary $\mathrm{C}$ is a multi-fusion 2-category $\mathrm{C}$.
	- (c) The bulk-to-boundary map induces an equivalence $\mathbf{B} \simeq \mathfrak{Z}_1(\mathbf{C})$ of braided fusion 2-categories.
-