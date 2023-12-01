# Idea
	- Simplexes as building blocks is too good to abandon altogether.
	  However, they are indeed too restrictive.
	- Therefore we seek slightly weaker conditions, i.e. allow the boundaries of simplexes to be identified a bit.
- # Basic Definitions
	- Definition. Diagonal of a space X
		- $$D=\{ {x,x} \in X \times X \}$$
	- Definition. Graph related to a binary relation
		- If $\sim$ is a binary relation on a space $X$, then its graph $G$ is the subset of $X \times X$ defined by
		  $$
		  G=\left\{\left(x_1, x_2\right) \in X \times X: x_1 \sim x_2\right\} ;
		  $$
		- We say that $\sim$ is **closed** if its graph $G$ is a closed subset of $X \times X$.
	- Proposition. The identity relation on $X$ is closed iff $X$ is Hausdorff.
		- q -> p
			- Rephrased, we need to prove $X \times X - D$ is open.
			- A basis of $X \times X$ is $\{O_i \times O_j \}$. We need to write $X \times X - D$ as a union of basis elements.
			-
			- $$\bigcup_{(x_1,x_2) \in X \times X} O(x_1, x_2) \times O(x_2, x_1)$$ is the desired union.
		- p -> q
			- Suppose $X$ isn't Hausdorff, i.e. there is a pair $(x_1, x_2)$ which cannot be separated.
			- Therefore, any union of basis elements of $X \times X$ cannot contain $(x_1, x_2)$ without intersecting $G$.
	- Corollary. When $X / \sim$ is Hausdorff, $\sim$ is closed.
		- When $X / \sim$ is Hausdorff, the diagonal $D \subset(X / \sim) \times(X / \sim)$ is closed.
		- Hence $G$ is closed in $X \times X$ because $v$ and hence $v \times v$ are continuous.
	- Lemma. Let $v: W \rightarrow Z$ be a closed map, let $S$ be a subset of $Z$, and let $U$ be an open subset of $W$ containing $v^{-1}(S)$. Then there exists an open set $V$ in $Z$ with
	  $$
	  S \subset V \quad \text { and } \quad v^{-1}(V) \subset U
	  $$
	-