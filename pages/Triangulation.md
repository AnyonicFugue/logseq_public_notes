- Definition
	- Let $X$ be a compact Hausdorff space.
	- **Curved triangle**
		- A subspace $A$ of $X$ and a homeomorphism $h: T \rightarrow A$, where $T$ is a closed triangular region in the plane.
		- If $e$ is an edge of $T$, then $h(e)$ is is said to be an edge of $A$; if $v$ is a vertex of $T$, then $h(v)$ is said to be a vertex of $A$.
	- **Triangulation** #card
		- A collection of curved triangles $A_1, \ldots, A_n$ in $X$ whose union is $X$,
		   such that for $i \neq j$, the intersection $A_i \cap A_j$ is either empty, or a vertex of both $A_i$ and $A_j$, or an edge of both.
		- Furthermore, if $h_i: T_i \rightarrow A_i$ is the homeomorphism associated with $A_i$, we require that when $A_i \cap A_j$ is an edge $e$ of both, then the map $h_j^{-1} h_i$ defines a **linear homeomorphism** of the edge $h_i^{-1}(e)$ of $T_i$ with the edge $h_j^{-1}(e)$ of $T_j$.
			- What does this mean?
				- Intuitively, this means that the edges must be pasted in a consistent manner.
			- Any counterexamples?
- # Basic Facts
	- Theorem. Every compact surface is triangulable. #card
	  id:: 6407fc4c-c8f0-405e-9919-d73a637dbe87
		- Munkres gave this without proof.
	-
-