- [[Deformation Retraction]]
	- ((639541d5-9e08-4c84-97f1-a779990ec598)) Let $h, k : X \rightarrow Y$ be continuous maps, where $h(x_0)=k(x_0)=y_0$. If $h$ and $k$ are homotopic, and if the image of the base point $x_0$ of $X$ remains fixed at $y_0$ during the homotopy, then the homomorphisms $h_*$ and $k_*$ are equal. #card
	  card-last-interval:: 201.84
	  card-repeats:: 4
	  card-ease-factor:: 2.9
	  card-next-schedule:: 2023-10-09T23:19:07.921Z
	  card-last-reviewed:: 2023-03-22T03:19:07.922Z
	  card-last-score:: 5
	  id:: 63a507a1-db81-4fb5-99ad-f1c6af18e8fc
		- Intuitively, 
		  homotopic paths -> equivalent paths
		  homotopic maps -> equivalent homs of fundamental groups
		- $I \times I \stackrel{f \times i d}{\longrightarrow} X \times I \stackrel{H}{\longrightarrow} Y$
	- ((63954564-3e1d-4f74-81c3-bea192c5ffdd)) The inclusion map $j: S^n \rightarrow \mathbb{R}^{n+1}-0$ induces an isomorphism of fundamental groups. #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-05-08T16:52:51.960Z
	  card-last-reviewed:: 2023-03-02T12:52:51.960Z
	  card-last-score:: 5
		- Intuition
			- We have a natural way of deforming the identity map of $\mathbb{R}^{n+1}-\mathbf{0}$ to a map that collapsed all of $\mathbb{R}^{n+1}-0$ onto $S^n$.
		- First note that the retraction map $r$ is homotopic to the identity map $id_{\mathbb{R}^{n+1}-0}$.
		- Thus $r_*$ is an isomorphism of fundamental groups.
		- $$
		  \left\{\begin{array}{l}
		  (r \circ g)_*: \pi_1(S^{1}) \rightarrow \pi_1(S^{1}) \text { is an isomorphism } \\
		  r_* \text { is an isomorphism }
		  \end{array} \Rightarrow j_x \text { is an isomorphism }\right.$$
	- ((63a6624b-1643-4f31-9c6d-8f96e2245bda)) Let $A$ be a deformation retract of $X$; let $x_0 \in A$. Then the inclusion map
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-06-30T11:24:58.144Z
	  card-last-reviewed:: 2023-04-07T11:24:58.144Z
	  card-last-score:: 5
	  $$
	  j:\left(A, x_0\right) \rightarrow\left(X, x_0\right)
	  $$
	  induces an **isomorphism** of fundamental groups. #card
		- Intuition
			- Since deformation retracts preserve all information, they shall preserve fundamental groups.
		- Proof
			- Denote the retraction map as r. We may prove $r \circ j=id(\pi_1(A))$, $j \circ r =id(\pi_1(X))$.
			- The first is obvious, since retractions are identities on A.
			- The second: $j\circ r$ is 'retract onto X itself'.
			  Since r is homotopic to $id_X$ and A remains fixed during the homotopy, $r_*=(id_X)_*$. (See this [theorem](((63a507a1-db81-4fb5-99ad-f1c6af18e8fc))))
		- Example
			- Let $B$ denote the $z$-axis in $\mathbb{R}^3$ ;Consider the space $\mathbb{R}^3-B$.
				- It has the punctured $x y$-plane $\left(\mathbb{R}^2-\mathbf{0}\right) \times 0$ as a deformation retract.
				- The map $H$ defined by the equation
				  $$
				  H(x, y, z, t)=(x, y,(1-t) z)
				  $$
				  is a deformation retraction; it gradually collapses each line parallel to the $z$-axis into the point where the line intersects the $x y$-plane.
				- We conclude that the space $\mathbb{R}^3-B$ has an infinite cyclic fundamental group.