# Defs
	- ((642578ff-9703-449c-b3df-41ffc344e641))
	- Polygonal region
	  collapsed:: true
		- Roughly speaking, we have a set of points $\{a_n\}$equaldistant to the center $c$. $P$ is the intersection of the closed half-planes created by the lines $a_{i-1}a_i$
	- Positive linear map between line segments
	  collapsed:: true
		- Preserving the orientations, i.e. is the homeomorphism $h$ that carries the point $x=(1-s) a+s b$ of $L$ to the point $h(x)=(1-s) c+s d$
	- Pasting the edges
	  collapsed:: true
		- ((63eed74a-00c4-4be3-9add-e89064a97dca)) Let $P$ be a polygonal region in the plane. A **labelling** of the edges of $P$ is a map from the set of edges of $P$ to a set $S$ called the set of labels.
		- Given an orientation of each edge of $P$, and given a labelling of the edges of $P$, we define an *equivalence relation* on the points of $P$:
		  collapsed:: true
			- Each point of Int $P$ is equivalent only to itself.
			- Given any two edges of $P$ that have the same label, let $h$ be the *positive linear map* of one onto the other, and define each point $x$ to be equivalent to the point $h(x)$.
		- The quotient space $X$ obtained from this equivalence relation is said to have been obtained by **pasting the edges** of $P$ together according to the given *orientations* and labelling.
		  collapsed:: true
			- Orientations matter!
		- Examples (to gain intuitions) #card
		  collapsed:: true
		  card-last-interval:: 84
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-08-29T01:32:47.014Z
		  card-last-reviewed:: 2023-06-06T01:32:47.015Z
		  card-last-score:: 5
			- ((63eed83b-fcf4-4bd5-88f5-ef10ccafa501))
			  collapsed:: true
				- The unit ball
				- Note that $a$ is nothing special in the space $B^2$, not any kind of boundary. Only an ancillary device to visualize the generation of $B^2$ from polygons.
			- ((63eed843-b814-406c-901b-e7ebbaeda54d))
			  collapsed:: true
				- $S^2$
				- Note that $a$ and $b$ are nothing special in the space $S^2$, not any kind of boundaries. They're only ancillary devices to visualize the generation of $S^2$ from polygons.
		- Convenient notation: Labelling scheme
		  collapsed:: true
			- ((63eed911-bc13-4c34-8089-b7a5a155a035)) Let $P$ be a polygonal region with successive vertices $p_0, \ldots, p_n$, where $p_0=p_n$.
			- For each $k$, let $a_{i_k}$ be the label assigned to the edge $p_{k-1} p_k$, and let $\epsilon_k=+1$ or $-1$ according as the orientation assigned to this edge goes from $p_{k-1}$ to $p_k$ or the reverse. Then the number of edges of $P$, the orientations of the edges, and the labelling are completely specified by the symbol
			  $$
			  w=\left(a_{i_1}\right)^{\epsilon_1}\left(a_{i_2}\right)^{\epsilon_2} \cdots\left(a_{i_n}\right)^{\epsilon_n} .
			  $$
			- Examples
			  collapsed:: true
				- ((63eed843-b814-406c-901b-e7ebbaeda54d)) is $bb^{-1}aa^{-1}$
				- $RP^2$
				  collapsed:: true
					- First thought: Identifying $x$ and $-x$ on $S^1$
					- Expressed by polynomials and labelling schemes is $abab$
				- The [[Mobius Band]]
				  collapsed:: true
					- $abac$
				- Vaguely reminiscent to a freely generated group?
			-
	- n-fold torus #card
	  id:: 63f218b7-eddb-4fe3-bd5e-daff1b591487
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-05-13T11:45:04.428Z
	  card-last-reviewed:: 2023-04-13T11:45:04.428Z
	  card-last-score:: 5
	  collapsed:: true
		- Pasting a $4n$-sided polygon by $\left(a_1 b_1 a_1^{-1} b_1^{-1}\right)\left(a_2 b_2 a_2^{-1} b_2^{-1}\right) \cdots\left(a_n b_n a_n^{-1} b_n^{-1}\right)$
		- What does it mean?
			- Consider the $n=2$ case, ![Image(1).png](../assets/Image(1)_1676811151957_0.png)
				- Prop. All vertices are identified.
				- Therefore, the common part of the two tori is a **circle**.
				- ((63f21c79-2841-4abc-a109-c068df01ff2b))
			- General case: All vertices are identified, but the tori are not connected by a circle. Instead they're connected by an **n-pant**.
	- m-fold projective plane #card
	  id:: 63f21c4d-b959-43e5-889d-90abd29a1092
	  collapsed:: true
	  card-last-interval:: 23.96
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-15T02:29:02.062Z
	  card-last-reviewed:: 2023-03-22T03:29:02.064Z
	  card-last-score:: 5
		- An $2m$-polygon pasted by $\left(a_1 a_1\right)\left(a_2 a_2\right) \cdots\left(a_m a_m\right)$.
			- Also a connected sum of $m$ projective planes.
		- $m=3$ example
			- ![Image(1).png](../assets/Image(1)_1676812325317_0.png){:height 688, :width 847}
			- Each component is a projective plane minus a circle.
	- First [[Homology Group]] #card
	  collapsed:: true
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-01T03:55:56.759Z
	  card-last-reviewed:: 2023-03-08T03:55:56.760Z
	  card-last-score:: 5
		- ((63f95d84-10e7-484d-8591-9e785fbbf5bb)) $H_1(X):=\pi_1\left(X, x_0\right) /\left[\pi_1\left(X, x_0\right), \pi_1\left(X, x_0\right)\right]$
	- Proper labelling scheme
	  collapsed:: true
		- Each label appears exactly twice.
	- Torus type and projective type
		- ((63fabe49-9a20-4104-a118-7a3cb4228e3c)) Let $w$ be a **proper** labelling scheme for a single polygonal region.
		- We say that $w$ is of **torus type** if each label in it appears once with exponent $+1$ and once with exponent $-1$. Otherwise, we say $w$ is of **projective type**.
- # Basic facts
  collapsed:: true
	- ((63eedadc-dcd0-43a1-8515-5bb384b50e50)) Let $X$ be the space obtained from a finite collection of polygonal regions by pasting edges together according to some labelling scheme. Then $X$ is a compact Hausdorff space. #card
	  card-last-interval:: 26.06
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-08T13:07:39.691Z
	  card-last-reviewed:: 2023-03-13T12:07:39.692Z
	  card-last-score:: 5
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
		- This is the case for the [[Torus]], the ((63f218b7-eddb-4fe3-bd5e-daff1b591487)), the ((63f21c4d-b959-43e5-889d-90abd29a1092)) and ((63e86249-c48a-4740-a36d-100aeb1da16c)) . Thus the striking resemblance.
		- The proof directly follows ((63db6326-2852-429b-acc7-21e25d249828)).
- # [[Homology]] of Surfaces
  collapsed:: true
	- Though we've obtained fundamental groups of lots of surfaces, we may not immediately determine whether they're distinct or not.
		- There is no algorithm to determine whether two groups are isomorphic.
	- We may consider $\pi_1 /\left[\pi_1, \pi_1\right]$ , which is abelian, for some inspiration!
	-
	- ((63f96977-bed6-4449-ad50-8114274d72d9))  If $X$ is the ((63f218b7-eddb-4fe3-bd5e-daff1b591487)) then $H_1(X)$ is a free abelian group of rank $2 n$. #card
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-06T01:04:23.811Z
	  card-last-reviewed:: 2023-03-13T01:04:23.814Z
	  card-last-score:: 5
		- As an exercise of the above corollary!
	- ((63f96a7e-89f5-4b82-a31f-2c730b301a80)) If $X$ is the ((63f21c4d-b959-43e5-889d-90abd29a1092)) , then the [[Torsion Group]] $T(X)$ of $H_1(X)$ has order 2, and $H_1(X) / T(X)$ is a free abelian group of rank $m-1$. #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-04-07T11:55:36.298Z
	  card-last-reviewed:: 2023-03-14T11:55:36.298Z
	  card-last-score:: 5
		- Another easy exercise.
		- Recall a theorem that $\pi_1(X)=\pi_1(A)/\langle p(f_0)\rangle$.
		- Moreover, we can that $H_1(X) / T(X)$ is free.
			- Actually we may directly invoke the theorem for finitely-generated abelian groups.
		-
	- Thus we can conclude that $S^2,T_1,T_2,...; P_1,P_2,...$ are topologically distinct!
- # ((63fab983-7e3c-40e1-aad1-2c7eb691fd73)) on labelling schemes
	- Setup
		- A labelling scheme $w_1, \ldots, w_m$ on m polygons, with the quotient space being $X$.
	- The strategy is again ((63fa1061-a719-42a4-8b01-2bd603e394fc))
	-
	- Cutting and Pasting
		- Cutting
		  collapsed:: true
			- ((63fab6e4-190d-40c1-981e-515a552a48ab))
		- Pasting
		  collapsed:: true
			- ((63fab713-7618-4b6c-96a6-693fd18fffe6))
		- Effect of cutting on a labelling scheme of a single polygon
			- Suppose $w=y_0y_1$, form $w_1=y_0 y_1$, where $y_0$ consists of the first $k$ terms of $w_1$ and $y_1$ consists of the remainder.
			- Let $c$ be a new label. Then $Q_1^{\prime}$ has the labelling scheme $y_0 c^{-1}$ and $Q_2$ has the labelling scheme $c y_1$.
	- Relabel
	  collapsed:: true
		- Replace all occurrences of any given label by some othe label that does not appear elsewhere in the scheme.
		- Similarly, one can change the sign of the exponent of all occurrences of a given label $a$; this amounts to reversing the orientations of all the edges labelled $a$.
	- Permute
	  collapsed:: true
		- Replace any **one** of the schemes $w_i$ by a **cyclic** permutation of $w_i$.
		- Intuitively rotating the polygon.
		- Note that permutations of the symbols are trivial. We want to permute the geometrical object.
	- Flip
	  collapsed:: true
		- One can replace one scheme
		  $$
		  w_i=\left(a_{i_1}\right)^{\epsilon_1} \cdots\left(a_{i_n}\right)^{\epsilon_n}
		  $$
		  by its formal inverse
		  $$
		  w_i^{-1}=\left(a_{i_n}\right)^{-\epsilon_n} \cdots\left(a_{i_1}\right)^{-\epsilon_1} .
		  $$
		- Actually reversing the orientation of the polygon, which has no effect on the geometry.
	- Cancel and uncancel
	  collapsed:: true
		- Replace $w_i=y_0 a a^{-1} y_1$ by $y_0y_1$ provided that $a$ doesn't appear elsewhere.
			- Uncancel is the reverse operation.
		- Intuitively, $aa^{-1}$ is a cone (which is topologically trivial), with the bottom pasted to the polygon in question.
-
- # The Classification Theorem
	- ((64b4848e-7e80-4fe8-a1f1-319b6f009d6f))
	- Theorem. If $w$ is a scheme of **projective type**, then $w$ is equivalent to a scheme of the same length having the form
	  card-last-interval:: 21.86
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-03-31T07:01:53.427Z
	  card-last-reviewed:: 2023-03-09T11:01:53.427Z
	  card-last-score:: 5
	  collapsed:: true
	  $$
	  \left(a_1 a_1\right)\left(a_2 a_2\right) \cdots\left(a_k a_k\right) w_1
	  $$
	  where $k \geq 1$ and $w_1$ is either empty or of torus type. #card
		- In plain English, the same edges can all be pushed to the front.
		- Specifically: Let $w$ be a proper scheme of the form
		  id:: 63fabdf6-dd04-4a9c-9d8f-a3635ac7b108
		  $$
		  w=\left[y_0\right] a\left[y_1\right] a\left[y_2\right],
		  $$
		  where some of the $y_i$ may be empty. Then one has the equivalence
		  $$
		  w \sim a a\left[y_0 y_1^{-1} y_2\right]
		  $$
			- An easy exercise. Just proceed concretely to avoid mistakes!
			- Note that there is one extra step. Not obtainable by just one cutting and pasting.
		- Now it suffices to apply the lemma repeatedly.
	- ((63ff145f-7f9e-4b11-8b84-ca36597daf79)) Let $w$ be a proper scheme of the form $w=w_0 w_1$, where $w_1$ is a scheme of **torus type** that does not contain two adjacent terms having the same label. Then $w$ is equivalent to a scheme of the form $w_0 w_2$, where $w_2$ has the same length as $w_1$ and has the form
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-07T00:56:29.783Z
	  card-last-reviewed:: 2023-03-14T00:56:29.784Z
	  card-last-score:: 5
	  $$
	  w_2=a b a^{-1} b^{-1} w_3
	  $$ #card
		- Specifically: If we have
		  $$
		  w=w_0\left[y_1\right] a\left[y_2\right] b\left[y_3\right] a^{-1}\left[y_4\right] b^{-1}\left[y_5\right]
		  $$
		  we can obtain
		  $$
		  w\sim w_0 a b a^{-1} b^{-1}\left[y_1 y_4 y_3 y_2 y_5\right]
		  $$
	- ((63ff1cab-4221-49ab-9d57-42cf9aa3952d)) Let $w$ be a proper scheme of the form
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-08-26T18:36:52.492Z
	  card-last-reviewed:: 2023-07-26T12:36:52.492Z
	  card-last-score:: 5
	  $$
	  w=w_0(c c)\left(a b a^{-1} b^{-1}\right) w_1
	  $$
	  Then $w$ is equivalent to the scheme
	  $$
	  w^{\prime}=w_0(a a b b c c) w_1
	  $$ #card
		- In plain English, this means that a projective type must be torus-free.
		- Proof
			- Hint: Use the [lemma](((63fabdf6-dd04-4a9c-9d8f-a3635ac7b108))) forwards and backwards for several times.
	- ((63ff1f74-71d1-4d4e-b347-d0746b62e728)) (The classification theorem). Let $X$ be a surface formed by a **proper** scheme. Then $X$ is homeomorphic either to $S^2$ (trivial scheme), to the $n$-fold torus $T_n$, or to the $m$-fold projective plane $P_m$. #card
	  card-last-score:: 5
	  card-repeats:: 3
	  card-next-schedule:: 2023-12-08T03:21:18.753Z
	  card-last-interval:: 117.6
	  id:: 6401b892-1a98-4844-89b5-e95da63050da
	  card-ease-factor:: 2.8
	  card-last-reviewed:: 2023-08-12T13:21:18.754Z
		- Note this only works for pasting edges in pairs. Not for, eg. ((63e86249-c48a-4740-a36d-100aeb1da16c)).
		- Collecting the lemmas above!
	-
- # Construct Compact Surfaces
	- Now we'd like to know whether all compact surfaces can be tackled by the classification theorem.
	- [[Triangulation]]
	- ((6407fddd-bfbc-4b68-b54a-ae71c0566d35)) If $X$ is a compact triangulable surface, then $X$ is homeomorphic to a space obtained from a collection of disjoint triangular regions in the plane by pasting their edges together in pairs.
		- Plain English
			- Every triangulable surface falls in the scope of the classification theorem.
		- This is quite obvious. Only needing some work to show pathological cases can't be called surfaces.
	- Theorem. Each connected compact surface can be classified by the [classification theorem](((6401b892-1a98-4844-89b5-e95da63050da))). #card
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-05-25T11:49:52.642Z
	  card-last-reviewed:: 2023-04-25T11:49:52.643Z
	  card-last-score:: 5
		- First, ((6407fc4c-c8f0-405e-9919-d73a637dbe87)).
		- Second, the surface can be obtained by pasting the edges of a set of triangles **in pairs**.
			- We must prove that pasting several edges together isn't allowed.
		- Furthermore, connectedness means that it can be obtained by pasting a polygon (paste the triangles successively to obtain a polygon)
		-
		- Note that a polygon is **not** a surface. The boundary points don't have neighborhoods homeomorphic to an open disk.
	- Exercise. Does the classification theorem work for ((63e86249-c48a-4740-a36d-100aeb1da16c))? #card
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-06-20T00:49:32.220Z
	  card-last-reviewed:: 2023-05-21T00:49:32.220Z
	  card-last-score:: 5
		- **NO**. It is not a surface for $n>2$.
- Exercise. Can we simplify ((63e86249-c48a-4740-a36d-100aeb1da16c)) to a projective plane?
	- eg. 6-fold dunce cap: $aaaaaa \to aaac, c^{-1}aaa \to aaac,a^{-3}c \to cc$ **?**
	- Answer: {{cloze NO. Cancelling can only be applied to a label which doesn't appear elsewhere.}}
- Exercise. The Klein bottle $a b a^{-1} b$ is homeomorphic to the 2-fold projective plane. #card
  card-last-interval:: 25.01
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-04-01T01:00:39.895Z
  card-last-reviewed:: 2023-03-07T01:00:39.896Z
  card-last-score:: 5
	- We define two labelling schemes to be equivalent if {{cloze one can be obtained from another by elementary operations above}}.
	- Try to find the operations by yourself!