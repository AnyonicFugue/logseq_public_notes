- ((6370aa46-c9f9-4a49-8912-99dad0eb621c))
- ((6370a8fd-64aa-4453-9384-10636e61c42e))
	- Sometimes called first [[Homotopy group]]
- Hat-map
  collapsed:: true
	- ((6370a9b6-cfdd-49ed-a37e-e977b27e99ff))
	- ![图像.png](../assets/图像_1668328082216_0.png)
	- ((6370aafb-bdcd-4007-a202-73f669641f53)) #card
	  card-last-interval:: 10
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2022-12-10T07:01:41.412Z
	  card-last-reviewed:: 2022-11-30T07:01:41.414Z
	  card-last-score:: 3
		- This hints that the fundamental group doesn't depend on the points (on the same path component of X).
		  Moreover, $$\pi_1(C,x_0)=\pi_1(X,x_0)$$
		- Different path components are actually different 'objects'.
		- ((6370ad13-5e39-4c81-b39b-544b7be66b09))
	-
	-
-
- The fundamental group is a [[Topological invariant]] #card
  card-last-interval:: 10
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2022-12-25T05:20:03.507Z
  card-last-reviewed:: 2022-12-15T05:20:03.509Z
  card-last-score:: 5
	- Homomorphism induced by a continuous map
		- Definition. Let $h .\left(X, x_0\right) \rightarrow\left(Y, y_0\right)$ be a continuous map. Define
		  $$
		  h_* : \pi_1\left(X, x_0\right) \longrightarrow \pi_1\left(Y, y_0\right)
		  $$
		  by $h_*([f])=[h \circ f]$
		- Note that $$h_*$$ doesn't depend on the representation element. #Exercise
		- Moreover, $$h_*$$ is a group homomorphism. #Exercise
	- If h is a homeomorphism, then $$h_*$$ is a group isomorphism.
- $\pi_1\left(X \times Y, x_0 \times y_0\right)$ is isomorphic with $\pi_1\left(X, x_0\right) \times \pi_1\left(Y, y_0\right)$ #card
	- This is very intuitive.
	- Corollary. Since $T^2=S^1 \times S^1$, $\pi_1(T^2)=\mathbb Z \times \mathbb Z$
-
-
- Examples
	- The circle
		- $\pi_1(S^1)=\mathbb Z$ #card
		  card-last-interval:: 10.42
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-12-23T16:30:11.447Z
		  card-last-reviewed:: 2022-12-13T06:30:11.448Z
		  card-last-score:: 5
			- By the [Theorem](((638c0f2d-33eb-4634-9467-e083bf50506d))), we may select a simply connected covering space. Here we choose R and covers $S^1$ in the usual way.
			- Let $e_0=0$. Now it's easy to see that the lifting correspondence $\phi$ is a group homomorphism.
	- $S^n$
	  collapsed:: true
		- ((63a7ba49-e539-495b-a981-0f27d65e5201)) Suppose $X=U \cup V$, where $U$ and $V$ are open sets of $X$. Suppose that $U \cap V$ is path connected, and that $x_0 \in U \cap V$. Let $i$ and $j$ be the inclusion mappings of $U$ and $V$, respectively, into $X$. Then the images of the induced homomorphisms
		  $$
		  i_*: \pi_1\left(U, x_0\right) \rightarrow \pi_1\left(X, x_0\right) \quad \text { and } \quad j_*: \pi_1\left(V, x_0\right) \rightarrow \pi_1\left(X, x_0\right)
		  $$
		  **generate** $\pi_1\left(X, x_0\right)$. #card
			- **This would be used to prove that** ((63a7be70-1a63-4e7e-932f-66d5791e4a09)).
			- Intuition
				- ![Image.png](../assets/Image_1671936792013_0.png){:height 222, :width 426}
				- We may select a 'middle point' $p_0\in U \cap V$ and find a path connecting $x_0$ and $p_0$ (which must exist by assumption). Then the path is obtained by concatenating the U-part and the V-part.
				- For a loop going into U and V many times, we may cut it into many sections.
				- **It is correct! The official proof exactly expresses what I said!** Just more elegant and well-formulated.
			- Technical details
				- Step 1. We show there is a subdivision $a_0<a_1<\cdots<a_n$ of the unit interval such that $f\left(a_i\right) \in U \cap V$ and $f\left(\left[a_{i-1}, a_i\right]\right)$ is contained either in $U$ or in $V$, for each $i$.
					- To show the existence, use [[The Lebesgue number lemma]] to construct some closed intervals contained completely in U or V.
		- If $n \geq 2$, the $n$-sphere $S^n$ is simply connected.
		  id:: 63a7be70-1a63-4e7e-932f-66d5791e4a09
			- The punctured sphere is homeomorphic to $\mathbb R^n$.
			- A sphere is the union of the north punctured sphere and the south.
				- They're both open.
				- The intersection is path-connected.
		-
	- [[Surface]]
		- Def
			- A 2-dimensional [[Manifold]].
	- The [[Projective Space]]
		- Theorem 60.3. The projective plane $P^2$ is a compact surface, and the quotient map $p: S^2 \rightarrow P^2$ is a covering map.
			- Corollary. $\pi_1\left(P^2, y\right)$ is a group of order 2 #card
			  card-last-interval:: 25.01
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-01-21T06:18:48.949Z
			  card-last-reviewed:: 2022-12-27T06:18:48.949Z
			  card-last-score:: 5
				- ((638c0f2d-33eb-4634-9467-e083bf50506d))
				- $S^2$ is simply connected.
				-
				- This may be generalized to any $P^n$; the fundamental group is always $Z_2$.
	- The [[Double Torus]]
		- ((63a7c45c-fdbe-4da3-9b18-1ee279e2d9c4)) The fundamental group is nonabelian.
			- First note that it retracts to [[The Figure Eight]], which has a nonabelian fundamental group.