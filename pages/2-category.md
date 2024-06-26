- Def #card
  card-last-interval:: 76.8
  card-repeats:: 3
  card-ease-factor:: 2.56
  card-next-schedule:: 2023-08-08T19:01:15.370Z
  card-last-reviewed:: 2023-05-24T00:01:15.371Z
  card-last-score:: 3
	- ((63aa5759-9d8e-48cd-acee-b1d4c54fee31))
	- a collection ob$(\mathbf{C})$, whose elements are called objects of $\mathbf{C}$;
	- a category $\operatorname{Hom}_\mathrm{C}(x, y)$ for each $x, y \in \mathrm{ob}(\mathcal{C})$, called the **hom category** from $x$ to $y$;
	- a functor $\circ: \operatorname{Hom}_{\mathrm{C}}(y, z) \times \operatorname{Hom} \mathrm{C}(x, y) \rightarrow \operatorname{Hom}_\mathrm{C}(x, z)$ for every $x, y, z \in \mathrm{ob}_(\mathbf{C})$, called the **composition functor**;
	- an object $1_x \in \operatorname{Hom}_C(x, x)$ for every $x \in \mathrm{ob}(\mathbf{C})$, called the **identity**
	-
	- In short, the collection of Homs in 1-cats are 0-cats (Sets), while in 2-cats they're 1-cats
- Examples
  collapsed:: true
	- Cats (Ob), functors (Homs) and natural transformations (Composition functor) form a 2-cat.
	- 2Vec
		- Finite semisimple categories, $\mathbb{C}$-linear functors and natural transformations
	- ((63aa59fc-0206-4dd0-ade2-930331519524)) #card
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.46
	  card-next-schedule:: 2023-05-04T11:24:42.900Z
	  card-last-reviewed:: 2023-04-04T11:24:42.902Z
	  card-last-score:: 3
		- Objects are gapped 1D domain walls
		- 1-morphisms are 0D domain walls
			- In particular, the hom category $\operatorname{Hom}{ }_{\mathrm{C}}\left(\mathbb{1}_{\mathrm{C}}, \mathbb{1}_{\mathrm{C}}\right)$ from the trivial 1d domain wall to itself is the category $\mathcal{C}$ of particle-like topological defects of C.
		- 2-morphisms are instantons between 0D domain walls
		- Composition functors are fusions of 0D domain walls. **Not fusion of 1D walls!**
			- Consistency
				- We can fuse instantons of the same domain wall first, or fuse different domain walls first. These shall be equal.
				- ((63aa5ab1-c88c-4224-8399-a1292f9983d6))
-