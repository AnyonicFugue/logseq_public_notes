- [[Jordan Separation Theorem]]
- ((63bbc09a-2a79-48b1-bb63-72957cc721cc)) (Invariance of domain)
  collapsed:: true
	- If $U$ is an open subset of $\mathbb{R}^2$ and $f: U \rightarrow$ $\mathbb{R}^2$ is continuous and injective, then $f(U)$ is open in $\mathbb{R}^2$ and the inverse function $f^{-1}: f(U) \rightarrow U$ is continuous.
- [[Jordan Curve Theorem]]
- Application on [[Graph]]
  collapsed:: true
	- ((63bd088d-0b32-447b-84ee-45bfc3959a98)) Let $X$ be a theta space that is a subspace of $S^2$; let $A, B$, and $C$ be the arcs whose union is $X$. Then $X$ separates $S^2$ into **three components**, whose boundaries are $A \cup B, B \cup C$, and $A \cup C$, respectively. #card
	  collapsed:: true
	  card-last-interval:: 117.6
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-11-27T03:08:14.649Z
	  card-last-reviewed:: 2023-08-01T13:08:14.649Z
	  card-last-score:: 5
		- Intuition is very clear. Now let's learn the construction.
		- Point: First separate $S^2$ into two parts, then add C to create the third part.
		- Step1. Consider $A\cup B$.
			- By the Jordan curve theorem, it separates $S^2$ into U and $U'$.
			- Take the endpoints of C to be a and b.
		- Step2.
			- $C-a-b$ connected -> in a single component, say $U'$.
			- Now let's consider two subspaces, $C$ and $U \cup A \cup B$.
				- Intersection is two points.
				- Closed connected.
				- Neither separates $S^2$.
			- The [theorem](((63bbddf3-847f-49e2-ac2a-90935bf64b53))) applies, that $U\cup A \cup B \cup C$ separates $S^2$ into two components!
			  id:: 63bd0bf2-1307-4b7d-846f-12c2d775d521
			- id:: 63bd0b55-7532-4b80-acb7-62765f843de2
	- ((63bd0c90-1981-4b7c-9b7f-ea9f9efc9eb0)) Let $X$ be the utilities graph. Then $X$ cannot be imbedded in the plane. #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-07-17T11:26:23.674Z
	  card-last-reviewed:: 2023-04-24T11:26:23.674Z
	  card-last-score:: 5
		- Idea: Reach a contradiction by showing the last point can be in no component.
		- First define three arcs: $A=g h_1 w$ $B=g h_2 w$ $C=g h_3 w$. Obviously they form a ((63bd0841-c1c2-4d33-8265-2d57561e49ac)).
			- They separate $S^2$ into three components $U,V,W$.
		- Now consider e.
			- $eh_1,eh_2,eh_3$ must be in the same component.
			- $h_1\notin U,h_2 \notin V, h_3\notin W$. Thus we arrive at a contradiction.
	- ((63bd1790-40f5-4e6f-a2f3-d021dd7c88dc)) $G_5$ cannot be imbedded in $S^2$. #card
	  collapsed:: true
	  card-last-interval:: 117.6
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-12-08T03:19:46.022Z
	  card-last-reviewed:: 2023-08-12T13:19:46.022Z
	  card-last-score:: 5
		- The strategy is similar: first show that $G_4$ divides $S^2$ into four parts and the boundaries, then show the fifth vertex can lie in none of the four.
		- Properties of $G_4$
			- $G_4$ minus an edge is a theta space, which separates $S^2$ into three parts.
				- Strategy of 'adding edges successively'.
			- By an similar operation of 'filling the previous shape' we show the last edge also separates $S^2$. Moreover, one of the components doesn't intersect $a_1$.
				- ((63bd18fc-f313-4f33-8d66-1244667d0d3b))
			- The following is completely analogous to that of the utility graph.
	- Theorem (Kuratowski's Theorem). A graph $G$ is planar if and only if it does not contain a subdivision of $K_5$ or $K_{3,3}$. #card
	  card-last-interval:: 117.6
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-11-07T03:41:51.067Z
	  card-last-reviewed:: 2023-07-12T13:41:51.067Z
	  card-last-score:: 5
		- This wasn't proven in Munkres, but quite interesting!
- Application on winding numbers
  collapsed:: true
	- We want to know the winding number of a simple curve, or equivalently, the winding number of injective $h: S^1\to R^2-0$
	- Thanks to Jordan, we know that $h(S^1)$ creates 2 component.
	- Lemma. If 0 is in the unbounded component, then $n=0$
		- This is equivalent to the [lemma](((63ba6c1e-488e-40e1-993b-729fc59ffccb))) on $S^2-p-q$
	- Theorem. If 0 is in the bounded component, then $n=\pm1$.
		- ((63be53bc-62bf-41bf-afc3-62805726de36)) Let $G$ be a subspace of $S^2$ that is a complete graph on four vertices $a_1, \ldots, a_4$. Let $C$ be the subgraph $a_1 a_2 a_3 a_4 a_1$, which is a simple closed curve. Let $p$ and $q$ be interior points of the edges $a_1 a_3$ and $a_2 a_4$, respectively. Then:
		  collapsed:: true
		  (a) The points $p$ and $q$ lie in different components of $S^2-C$.
		  (b) The inclusion $j: C \rightarrow S^2-p-q$ induces an **isomorphism** of fundamental groups.
			- ((63be53e5-0e1f-43be-8bb1-2bd7b88e5e16))
			- (a) is very simple. We may invoke the fact that the theta diagram divides into three components.
			- (b) might be proven by the [theorem](((63bbc3cd-2356-45f1-819c-e950c33d75aa)))
				- A quick review of the theorem: $X=U\cup V$, where $U \cap V =A \cup B$ disconnected. Then we may generate an inf cyc group by a certain loop; moreover, if $\pi_1(X)$ is inf cyc, then we generate it by the loop.
				- Here $X=S^2-p-q$, $U=S^2-D_1$ and $V=S^2-D_2$
					- $D_1=p a_3 a_2 q \quad$ and $\quad D_2=q a_4 a_1 p$, $D_2=q a_4 a_1 p$
				- (a) implies x and y lie in different components of $U \cap V$. Moreover, they can be connected since arcs don't separate the sphere.
			- Now we obtain a surjective homomorphism, which turns out to be an isomorphism.
		- The main theorem can be proven by constructing a $G_4$.
			- Statement
				- Let $C$ be a simple closed curve in $S^2$; let $p$ and $q$ lie in different components of $S^2-C$. Then the inclusion mapping $j: C \rightarrow S^2-p-q$ induces an isomorphism of fundamental groups.
			- There are some technical details to prove the existence of simple arcs (by joining to arcs), but the main line is clear:
				- Break the simple loop into two parts. Then we have two endpoints.
				- Select a point $m$ in the unbounded region. We may construct paths from $m$ to 0 in $X-C_1$ and $X-C_2$ respectively. We obtain another two endpoints (as the points of intersection)
				- We may connect the endpoints by using $m$ as an intermediary.
		-
	-