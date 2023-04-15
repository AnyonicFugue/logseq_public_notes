- ((63e44b9a-8e76-4cce-9663-a87a332bad1b)) 
  card-last-interval:: 84
  card-repeats:: 3
  card-ease-factor:: 2.8
  card-next-schedule:: 2023-07-06T11:31:53.796Z
  card-last-reviewed:: 2023-04-13T11:31:53.798Z
  card-last-score:: 5
  1. Let $V$ and $W$ be irreducible **real or complex** representations of a **group** or **Lie algebra** and let $\phi: V \rightarrow W$ be an intertwining map. Then either $\phi=0$ or $\phi$ is an isomorphism.
  2. Let $V$ be an irreducible **complex** representation of a group or Lie algebra and let $\phi: V \rightarrow V$ be an intertwining map of $V$ with itself. Then $\phi=\lambda I$, for some $\lambda \in \mathbb{C}$.
  3. Let $V$ and $W$ be irreducible **complex** representations of a group or Lie algebra and let $\phi_1, \phi_2: V \rightarrow W$ be nonzero intertwining maps. Then $\phi_1=\lambda \phi_2$, for some $\lambda \in \mathbb{C}$. #card
	- Obviously the lemma isn't restricted to groups or algebras, but more general representations of algebraic structures.
	- Proof
		- 1 is proved by considering $\operatorname {Ker} \phi$
			- $T_1(x) \phi=\phi T_2(x)$
			- Thus the kernel is preserved.
			- Exercise: $\phi$ is a surjective map since $W$ is irreducible.
		- 2 is proved by considering the eigenspace of $\phi$.
			- Thus complex is necessary.
		- Obviously 3 is a corollary of 2.