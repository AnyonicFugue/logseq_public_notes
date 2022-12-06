- [[Deformation Retraction]]
	- ((639541d5-9e08-4c84-97f1-a779990ec598)) Let $h, k : X \rightarrow Y$ be continuous maps, where $h(x_0)=k(x_0)=y_0$. If $h$ and $k$ are homotopic, and if the image of the base point $x_0$ of $X$ remains fixed at $y_0$ during the homotopy, then the homomorphisms $h_*$ and $k_*$ are equal. #card
	  card-last-interval:: 10
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2022-12-25T05:26:17.236Z
	  card-last-reviewed:: 2022-12-15T05:26:17.237Z
	  card-last-score:: 5
		- Intuitively, 
		  homotopical paths -> equivalent paths
		  homotopical maps -> equivalent homs of fundamental groups
		- $I \times I \stackrel{f \times i d}{\longrightarrow} X \times I \stackrel{H}{\longrightarrow} Y$
	- ((63954564-3e1d-4f74-81c3-bea192c5ffdd)) The inclusion map $j: S^n \rightarrow \mathbb{R}^{n+1}-0$ induces an isomorphism of fundamental groups. #card
		- Intuition
			- We have a natural way of deforming the identity map of $\mathbb{R}^{n+1}-\mathbf{0}$ to a map that collapsed all of $\mathbb{R}^{n+1}-0$ onto $S^n$.
		- First note that the retraction map $r$ is homotopic to the identity map $id_{\mathbb{R}^{n+1}-0}$.
		- Thus $r_*$ is an isomorphism of fundamental groups.
		- $$
		  \left\{\begin{array}{l}
		  (r \circ g)_*: \pi_1(S^{1}) \rightarrow \pi_1(S^{1}) \text { is an isomorphism } \\
		  r_* \text { is an isomorphism }
		  \end{array} \Rightarrow j_x \text { is an isomorphism }\right.$$