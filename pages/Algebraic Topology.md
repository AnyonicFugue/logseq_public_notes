- [[References]]
  id:: 63c14161-aa39-45f2-9e56-717fda4804b2
	- ![2000_Munkres_Topology](file://zotero_link/Mathematics/Topology/2000_Munkres_Topology.pdf) Topology, Munkres
-
- Study obscure topological properties in an algebraic manner! #Thoughts
  id:: 638d57a7-30e1-4243-8ec8-babe77af9cf8
	- There seems to be something deeper inside. Galois theory -> Study field extensions by means of automorphism groups.
-
- Homotopy
	- Defs
	  collapsed:: true
		- Homotopy of maps
		  collapsed:: true
			- If $f$ and $f^{\prime}$ are continuous maps of the space $X$ into the space $Y$, we say that $f$ is homotopic to $f^{\prime}$ if there is a continuous map $F : X \times I \rightarrow Y$ such that
			  $$F(x, 0)=f(x) \quad \text { and } \quad F(x, 1)=f^{\prime}(x)$$
			  for each $x$. (Here $I=[0,1]$.) The map $F$ is called a homotopy between $f$ and $f^{\prime}$. If $f$ is homotopic to $f^{\prime}$, we write $f \simeq f^{\prime}$. If $f \simeq f^{\prime}$ and $f^{\prime}$ is a constant map, we say that $f$ is **nulhomotopic**.
			-
			- The maps don't have 'endpoints' as paths, so there's no extra condition of 'fixed endpoints'.
		- Homotopy of paths
		  collapsed:: true
			- With the extra requirement that the **endpoints are fixed.**
			- Two paths $f$ and $f^{\prime}$, mapping the interval $I=[0,1]$ into $X$, are said to be path homotopic if they have the same initial point $x_0$ and the same final point $x_1$, and if there is a continuous map $F: I \times I \rightarrow X$ such that
			- $$\begin{array}{lll}
			  F(s, 0)=f(s) & \text { and } & F(s, 1)=f^{\prime}(s), \\
			  F(0, t)=x_0 & \text { and } & F(1, t)=x_1,
			  \end{array}$$
			-
			- for each $s \in I$ and each $t \in I$. We call $F$ a path homotopy between $f$ and $f^{\prime}$ See Figure 51.1. If $f$ is path homotopic to $f^{\prime}$, we write $f \simeq_p f^{\prime}$.
			  id:: 63c14161-a2e6-4179-a53c-7bc62b6233d5
	- Lemma. The relations $\simeq$ and $\simeq p$ are equivalence relations.
	  collapsed:: true
		- Easy to verify identity, reflexivity and transitivity.
	- Homotopy class
- [[Fundamental group]]
  collapsed:: true
	- [[Simply connected]]
	- [[Covering space]]
	- [[Retraction]]
	  collapsed:: true
		- Def
		  collapsed:: true
			- $A \subset X$, a **retraction** of $X$ onto $A$ is a continuous map $r: X \rightarrow A$ such that $r | _ A$ is the **identity** map of $A$. $A$ is a retract of $X$.
		- Examples
		  collapsed:: true
			- $r(x)=x /\|x\|$ retracts $\mathbb{R}^2-0$ onto $S^1$
		- ((638d5522-85b2-4c12-bca3-62846d934042)) If $A$ is a retract of $X$, then the homomorphism of fundamental groups induced by inclusion $j: A \rightarrow X$ is injective.
		  collapsed:: true
			- Intuition #card
			  card-last-interval:: 24
			  card-repeats:: 2
			  card-ease-factor:: 2.7
			  card-next-schedule:: 2023-01-30T06:04:06.831Z
			  card-last-reviewed:: 2023-01-06T06:04:06.832Z
			  card-last-score:: 5
			  collapsed:: true
				- X and A are 'homeomorphic in A'. Thus, homotopic in X <-> homotopic in A.
			-
			- If $r: X \rightarrow A$ is a retraction, then the composite map $r \circ j$ equals the identity map of $A$. It follows that $r_* \circ j_*$ is the identity map of $\pi_1(A, a)$, so that $j_*$ must be injective.
			  collapsed:: true
				- This is a general property of inclusions: {{cloze One-side invertible}}
		- Corollary. No retraction of $B^2$ into $S^1$. #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-01-17T12:58:44.355Z
		  card-last-reviewed:: 2022-12-24T12:58:44.356Z
		  card-last-score:: 5
		  collapsed:: true
			- $\pi_1(S^1)=\mathbb Z, \pi_1(B^2)=e$. No injection.
			- Another application of ((638d57a7-30e1-4243-8ec8-babe77af9cf8)).
			  id:: 63c14161-2eea-4c90-94d9-cb032f916f40
		- Lemma 55.3. Let $h: S^1 \rightarrow X$ be a continuous map. Then the following conditions are **equivalent**: $h$ is nulhomotopic; $h$ extends to a continuous map $k: B^2 \rightarrow X$; $h_*$ is the trivial homomorphism of fundamental groups.
		  collapsed:: true
			- Intuitions #card
			  card-last-interval:: 67.2
			  card-repeats:: 3
			  card-ease-factor:: 2.8
			  card-next-schedule:: 2023-04-24T15:39:27.657Z
			  card-last-reviewed:: 2023-02-16T11:39:27.657Z
			  card-last-score:: 5
			  collapsed:: true
				- (1) and (3) are directly seen to be equivalent, since nulhomotopic means that the image can be contracted to be a point. Thus the generator of $\pi_1(S^1)$ is mapped to the trivial element.
				- (2) to (1): In $B^2$, $S^1$ can be contracted to a point. Since [[Continuous]] maps preserve path homotopies, the image can also be contracted.
				- (1) to (2) is the most interesting part. We may construct maps which shrink $S^1$ and $h(S^1)$ to a point respectively, then establish a correspondence between them.
				  collapsed:: true
					- ![image.png](../assets/image_1670210360212_0.png){:height 169, :width 372}
					- Or ((638d639f-33d9-4a25-b658-4f63d2ddb144))
					  id:: 63c14161-6c0b-4e20-8aed-7b1ef3003b03
				-
		- ((6393ecbc-590b-426b-8528-d730e640b237)) The inclusion map $j : S^1 \rightarrow \mathbb{R}^2-\mathbf{0}$ is not nulhomotopic. #card
		  card-last-score:: 5
		  card-repeats:: 2
		  card-next-schedule:: 2023-02-24T13:13:04.854Z
		  card-last-interval:: 24
		  card-ease-factor:: 2.7
		  card-last-reviewed:: 2023-01-31T13:13:04.854Z
		  collapsed:: true
			- An exercise to express the intuition via the language of retractions.
			- Hint: Nul -> Trivial hom of $\pi_1$; Retraction -> Injective
	- [[Deformation Retraction]] and [[Homotopy Equivalence]]
	- ((6393f3d8-803c-4134-af68-b91b9739c5e7)) Given a **nonvanishing** vector field on $B^2$, there exists a point of $S^1$ where the vector field points directly inward and a point of $S^1$ where it points directly outward.
	  collapsed:: true
		- Intuition #card
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-02-18T01:13:24.361Z
		  card-last-reviewed:: 2023-01-25T01:13:24.362Z
		  card-last-score:: 5
		  collapsed:: true
			- A vector field on $B^2$ is a continuous map of $B^2$ into $\mathbb{R}^2$. Nonvanishing -> $v$ actually maps $B^2$ into $\mathbb{R}^2-0$.
			  collapsed:: true
				- ((63860946-8380-45c7-b564-1c08f9e7cc70))
				- ((6393f445-3a3c-4366-a1d1-bbc1587873a0))
			- $\mathbb{R}^2-0$ retracts into $S^1$ (which preserves the directions). Now we have a (nulhomotopic) map $B^2\to S^1$.
			- Restrict to $S^1$, we obtain another nul map.
			- The existence of the fixed point (which means the vector field points outward!) can be proven by the intermediate value theorem.
			  collapsed:: true
				- Inward is $f(\phi)=\phi+\pi$. We may construct $h=f-\pi$ and find the fixed point of $h$.
				- Actually we should prove it by constructing a path homotopy in the context of algebraic topology.
		- Official
		  collapsed:: true
			- Prove by contradiction.
			- $w=v|_{S^1}$ is nulhomotopic.
			- We try to define a homotopy between w and the inclusion map $j: S^1 \rightarrow \mathbb{R}^2-\mathbf{0}$. Since the latter isn't null, a contradiction arises.
			- The homotopy $F(x, t)=t x+(1-t) w(x)$. Obviously it's continuous.
			- It is illegitimate only if $F(x,t) = 0$, i.e. $t x+(1-t) w(x)=0$ <-> the vector points directly outwards at x!
			  id:: 63c14161-a01a-4b97-876f-c426df2df736
	- ((6393f81a-de32-4d11-b971-629c48983742)) (Brouwer fixed-point theorem for the disc). If $f: B^2 \rightarrow B^2$ is continuous, then there exists a **fixed point** $x \in B^2$ such that $f(x)=x$. #card
	  collapsed:: true
		- A very interesting trick: Construct a vector field $v(x)=f(x)-x$ by embedding $B^2$ into $R^2$.
		- There should be something deeper inside this trick.
		- Embed the object (A topological object in this case) into something with better structures. #[[Thoughts/Math and Physics]]
		  id:: 63c14161-9b19-4985-b2d6-1b13391e194a
		- Extra structures may provide extra insights. The  properties of the object itself restricts the possible structures. #[[Thoughts/Math and Physics]]
		  collapsed:: true
			- Recall inner product in linear algebra.
		-
	- ((63953b25-8709-4182-9cb5-87d46acf1a4f))
	- ((63953d32-29d5-4ffe-aec8-c9a40be4e936)) Let $A$ be a 3 by 3 matrix of positive real numbers. Then $A$ has a positive real eigenvalue. #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-01-25T07:08:06.285Z
	  card-last-reviewed:: 2022-12-31T07:08:06.286Z
	  card-last-score:: 5
	  collapsed:: true
		- Let B be the intersection of $S^2$ with the first octant $$\left\{\left(x_1, x_2, x_3\right) \mid x_1 \geq 0 \text { and } x_2 \geq 0 \text { and } x_3 \geq 0\right\}$$.
		- Obviously $B \cong B^2$.
		- Moreover, $f:x \mapsto T(x) /\|T(x)\|$ is a continuous map, so the fixed-point theorem applies.
		-
		- If the fixed-point theorem holds, we can easily generalize it to arbitrary dimensions. But the fixed-point theorem seems to need some modification.
	- We can even prove [[The Fundamental Theorem of Algebra]]! #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-02-26T12:19:40.674Z
	  card-last-reviewed:: 2023-02-02T12:19:40.674Z
	  card-last-score:: 5
	  collapsed:: true
		- *Review the thought in this card. No need to memorize all details.
		  collapsed:: true
			- Deformation provides much information. #[[Thoughts/Math and Physics]]
			  id:: 63c14161-1549-4b29-b6b3-84321340d574
		- We first deal with the special case that $x^n+a_{n-1} x^{n-1}+\cdots+a_1 x+a_0=0$ where $\left|a_{n-1}\right|+\cdots+\left|a_1\right|+\left|a_0\right|<1$. The general case can be obtained by 'rescaling' the variable.
		  collapsed:: true
			- Assume no root exists for the equation.
			- Then we may define a map $k: B^2 \rightarrow \mathbb{R}^2-0$ by $k(z)=z^n+a_{n-1} z^{n-1}+\cdots+a_1 z+a_0$.
			  collapsed:: true
				- The polynomial must be nonzero on all of $B^2$.
			- Let $h=k|_{S^1}$. h is null since it extends to k.
			- On the other hand, we may define a homotopy $F(z, t)=z^n+t\left(a_{n-1} z^{n-1}+\cdots+a_0\right)$, then h isn't null.
			  collapsed:: true
				- The condition $\left|a_{n-1}\right|+\cdots+\left|a_1\right|+\left|a_0\right|<1$ grants that the homotopy can be defined on $S^1$
			- **We obtain a contradiction.**
	- [[Lifting]]
	-
- [[The Separation Theorems]]
- [[Seifert-van Kampen Theorem]]
- Classification of Surfaces
	- Defs
	  collapsed:: true
		- Polygonal region
			- Roughly speaking, we have a set of points $\{a_n\}$equaldistant to the center $c$. $P$ is the intersection of the closed half-planes created by the lines $a_{i-1}a_i$
		- Orientation
			- An ordering of the two end points of a line segment
		- Positive linear map between line segments
			- Preserving the orientations, i.e. is the homeomorphism $h$ that carries the point $x=(1-s) a+s b$ of $L$ to the point $h(x)=(1-s) c+s d$
		- Pasting the edges
			- ((63eed74a-00c4-4be3-9add-e89064a97dca)) Let $P$ be a polygonal region in the plane. A **labelling** of the edges of $P$ is a map from the set of edges of $P$ to a set $S$ called the set of labels.
			- Given an orientation of each edge of $P$, and given a labelling of the edges of $P$, we define an *equivalence relation* on the points of $P$:
				- Each point of Int $P$ is equivalent only to itself.
				- Given any two edges of $P$ that have the same label, let $h$ be the *positive linear map* of one onto the other, and define each point $x$ to be equivalent to the point $h(x)$.
			- The quotient space $X$ obtained from this equivalence relation is said to have been obtained by **pasting the edges** of $P$ together according to the given *orientations* and labelling.
				- Orientations matter!
			- Examples (to gain intuitions) #card
				- ((63eed83b-fcf4-4bd5-88f5-ef10ccafa501))
					- The unit ball
					- Note that $a$ is nothing special in the space $B^2$, not any kind of boundary. Only an ancillary device to visualize the generation of $B^2$ from polygons.
				- ((63eed843-b814-406c-901b-e7ebbaeda54d))
					- $S^2$
					- Note that $a$ and $b$ are nothing special in the space $S^2$, not any kind of boundaries. They're only ancillary devices to visualize the generation of $S^2$ from polygons.
			- Convenient notation: Labelling scheme
				- ((63eed911-bc13-4c34-8089-b7a5a155a035)) Let $P$ be a polygonal region with successive vertices $p_0, \ldots, p_n$, where $p_0=p_n$.
				- For each $k$, let $a_{i_k}$ be the label assigned to the edge $p_{k-1} p_k$, and let $\epsilon_k=+1$ or $-1$ according as the orientation assigned to this edge goes from $p_{k-1}$ to $p_k$ or the reverse. Then the number of edges of $P$, the orientations of the edges, and the labelling are completely specified by the symbol
				  $$
				  w=\left(a_{i_1}\right)^{\epsilon_1}\left(a_{i_2}\right)^{\epsilon_2} \cdots\left(a_{i_n}\right)^{\epsilon_n} .
				  $$
				- Examples
					- ((63eed843-b814-406c-901b-e7ebbaeda54d)) is $bb^{-1}aa^{-1}$
					- $RP^2$
						- First thought: Identifying $x$ and $-x$ on $S^1$
						- Expressed by polynomials and labelling schemes is $abab$
					- The [[Mobius Band]]
						- $abac$
					- Vaguely reminiscent to a freely generated group?
				-
	- Basic facts
		- ((63eedadc-dcd0-43a1-8515-5bb384b50e50)) Let $X$ be the space obtained from a finite collection of polygonal regions by pasting edges together according to some labelling scheme. Then $X$ is a compact Hausdorff space. #card
			- Compact is immediate, since $\pi$ is continuous.
			- Hausdorff can be shown using the metric and finiteness, but another more elegant way.
				- Exercise. A closed quotient map preserves normality.
		- ((63eee202-1568-4bf6-8431-b49a1be4497b)) Let $P$ be a polygonal region; let
		  $$
		  w=\left(a_{i_1}\right)^{\epsilon_1} \cdots\left(a_{i_n}\right)^{\epsilon_n}
		  $$
		  be a labelling scheme for the edges of $P$. Let $X$ be the resulting quotient space. 
		  If all the vertices of $P$ are pasted to a single point $x_0$, then $\pi_1\left(X, x_0\right)$ is isomorphic to the quotient of the free group on $k$ generators $\alpha_1, \ldots, \alpha_k$ by the least normal subgroup containing the element
		  $$
		  \left(\alpha_{i_1}\right)^{\epsilon 1} \cdots\left(\alpha_{i_n}\right)^{\epsilon_n} .
		  $$ #card
			- This is the case for the [[Torus]] and ((63e86249-c48a-4740-a36d-100aeb1da16c)) . Thus the striking resemblance.
			- The proof directly follows ((63db6326-2852-429b-acc7-21e25d249828)).