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
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-03-19T00:25:55.604Z
		  card-last-reviewed:: 2023-02-23T00:25:55.605Z
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
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-03-24T00:44:52.397Z
	  card-last-reviewed:: 2023-02-28T00:44:52.397Z
	  card-last-score:: 5
	  collapsed:: true
		- Let K be the intersection of $S^2$ with the first octant $$\left\{\left(x_1, x_2, x_3\right) \mid x_1 \geq 0 \text { and } x_2 \geq 0 \text { and } x_3 \geq 0\right\}$$.
		- Obviously $K \cong B^2$.
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
		- Polygonal region
		  collapsed:: true
			- Roughly speaking, we have a set of points $\{a_n\}$equaldistant to the center $c$. $P$ is the intersection of the closed half-planes created by the lines $a_{i-1}a_i$
		- Orientation
		  collapsed:: true
			- An ordering of the two end points of a line segment
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
			  card-last-interval:: 25.01
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-03-25T13:40:42.351Z
			  card-last-reviewed:: 2023-02-28T13:40:42.351Z
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
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-21T00:09:19.238Z
		  card-last-reviewed:: 2023-02-25T00:09:19.239Z
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
			- An $2m$-polygon pasted by $\left(a_1 a_1\right)\left(a_2 a_2\right) \cdots\left(a_m a_m\right)$.
			- $m=3$ example
				- ![Image(1).png](../assets/Image(1)_1676812325317_0.png){:height 688, :width 847}
				- Each component is a projective plane minus a circle.
		- First [[Homology Group]] #card
		  collapsed:: true
			- ((63f95d84-10e7-484d-8591-9e785fbbf5bb)) $H_1(X):=\pi_1\left(X, x_0\right) /\left[\pi_1\left(X, x_0\right), \pi_1\left(X, x_0\right)\right]$
		- Proper labelling scheme
		  collapsed:: true
			- Each label appears exactly twice.
		- Torus type and projective type
			- ((63fabe49-9a20-4104-a118-7a3cb4228e3c)) Let $w$ be a **proper** labelling scheme for a single polygonal region.
			- We say that $w$ is of **torus type** if each label in it appears once with exponent $+1$ and once with exponent $-1$. Otherwise, we say $w$ is of **projective type**.
	- Basic facts
	  collapsed:: true
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
			- This is the case for the [[Torus]], the ((63f218b7-eddb-4fe3-bd5e-daff1b591487)), the ((63f21c4d-b959-43e5-889d-90abd29a1092)) and ((63e86249-c48a-4740-a36d-100aeb1da16c)) . Thus the striking resemblance.
			- The proof directly follows ((63db6326-2852-429b-acc7-21e25d249828)).
	- [[Homology]] of Surfaces
	  collapsed:: true
		- Though we've obtained fundamental groups of lots of surfaces, we may not immediately determine whether they're distinct or not.
			- There is no algorithm to determine whether two groups are isomorphic.
		- We may consider $\pi_1 /\left[\pi_1, \pi_1\right]$ , which is abelian, for some inspiration!
		-
		- Prop. The isomorphism between $\pi_1(X,a)$ and $\pi_1(X,b)$ induced by different paths are identical when projected to $H_1(X,a)$ and $H_1(X,b)$ #card
			- Consider two paths $\alpha$ and $\beta$, and the isomorphism induced by $\gamma:=\alpha \beta^{-1}$.
			- $f \mapsto \gamma f \gamma^{-1}$.
			- Obviously it is still $f$ in the abelianized quotient.
		- ((63f9607e-52d2-4362-81b9-9392cd5509e1)) Theorem 75.1. Let $F$ be a group; let $N$ be a normal subgroup of $F$; let $G:=F/N$. The projection homomorphism
		  collapsed:: true
		  card-last-interval:: 23.96
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-22T12:05:09.640Z
		  card-last-reviewed:: 2023-02-26T13:05:09.641Z
		  card-last-score:: 5
		  $$
		  p: F \rightarrow F /[F, F]
		  $$
		  induces an **isomorphism**
		  $$
		  \phi: G /[G, G] \rightarrow p(F) / p(N) .
		  $$ #card
			- Intuition
				- Elements in LHS are of the form $(x\cdot N) \cdot \{aba^{-1}b^{-1} \cdot N  \}_{ab}$
				- Elements in RHS are $(x\cdot [F,F]) \cdot (N \cdot [F,F])$
				- We may construct an explicit isomorphism and find out when would $x_1~x_2$ (which of course coincides for LHS and RHS), but this is ugly.
			- Official
				- ((63f96759-3738-48a8-8e1d-6fa03d6d2e5d))
		- ((63f967c8-2ec0-44a3-ad3f-4a9a9d1cc739)) Let $F$ be a free group with free generators $\alpha_1, \ldots, \alpha_n$; let $N$ be the least normal subgroup of $F$ containing the element $x$ of $F$; let $G=F / N$. 
		  collapsed:: true
		  Let $p:F \rightarrow F /[F, F]$ be projection. Then $G /[G, G]$ is **isomorphic** to the quotient of $F /[F, F]$ (which is **free abelian** with basis $p\left(\alpha_1\right), \ldots, p\left(\alpha_n\right)$) by the subgroup generated by $p(x)$. #card
			- We know that $G/[G,G]\cong p(F)/p(N)$. Moreover, $F/[F,F]$ is abelian with the same basis.
			-
		- ((63f96977-bed6-4449-ad50-8114274d72d9))  If $X$ is the ((63f218b7-eddb-4fe3-bd5e-daff1b591487)) then $H_1(X)$ is a free abelian group of rank $2 n$. #card
			- As an exercise of the above corollary!
		- ((63f96a7e-89f5-4b82-a31f-2c730b301a80)) If $X$ is the ((63f21c4d-b959-43e5-889d-90abd29a1092)) , then the [[Torsion Group]] $T(X)$ of $H_1(X)$ has order 2, and $H_1(X) / T(X)$ is a free abelian group of rank $m-1$. #card
			- Another easy exercise.
		- Thus we can conclude that $S^2,T_1,T_2,...; P_1,P_2,...$ are topologically distinct!
	- Cutting and Pasting
	  collapsed:: true
		- Cutting
		  collapsed:: true
			- ((63fab6e4-190d-40c1-981e-515a552a48ab))
		- Pasting
		  collapsed:: true
			- ((63fab713-7618-4b6c-96a6-693fd18fffe6))
		- Effect of cutting on a labelling scheme of a single polygon
			- Suppose $w=y_0y_1$, form $w_1=y_0 y_1$, where $y_0$ consists of the first $k$ terms of $w_1$ and $y_1$ consists of the remainder.
			- Let $c$ be a new label. Then $Q_1^{\prime}$ has the labelling scheme $y_0 c^{-1}$ and $Q_2$ has the labelling scheme $c y_1$.
	- ((63fab983-7e3c-40e1-aad1-2c7eb691fd73)) on labelling schemes
		- Setup
			- A labelling scheme $w_1, \ldots, w_m$ on m polygons, with the quotient space being $X$.
		- The strategy is again ((63fa1061-a719-42a4-8b01-2bd603e394fc))
		-
		- Cut
		- Paste
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
	- Exercise. The Klein bottle $a b a^{-1} b$ is homeomorphic to the 2-fold projective plane. #card
	  collapsed:: true
		- We define two labelling schemes to be equivalent if {{cloze one can be obtained from another by elementary operations above}}.
		- Try to find the operations by yourself!
	- Towards The Classification Theorem
		- Simplify the representation into some canonical form. #Strategy #card
		- Theorem. If $w$ is a scheme of projective type, then $w$ is equivalent to a scheme of the same length having the form
		  $$
		  \left(a_1 a_1\right)\left(a_2 a_2\right) \cdots\left(a_k a_k\right) w_1
		  $$
		  where $k \geq 1$ and $w_1$ is either empty or of torus type. #card
			- In plain English, the same edges can all be pushed to the front.
			- ((63ff1367-a528-454e-aee9-bb1d36897060)) Let $w$ be a proper scheme of the form
			  id:: 63fabdf6-dd04-4a9c-9d8f-a3635ac7b108
			  collapsed:: true
			  $$
			  w=\left[y_0\right] a\left[y_1\right] a\left[y_2\right],
			  $$
			  where some of the $y_i$ may be empty. Then one has the equivalence
			  $$
			  w \sim a a\left[y_0 y_1^{-1} y_2\right]
			  $$
				- An easy exercise. Just proceed concretely to avoid mistakes!
			- Now it suffices to apply the lemma repeatedly.
		- ((63ff145f-7f9e-4b11-8b84-ca36597daf79)) Let $w$ be a proper scheme of the form $w=w_0 w_1$, where $w_1$ is a scheme of torus type that does not contain two adjacent terms having the same label. Then $w$ is equivalent to a scheme of the form $w_0 w_2$, where $w_2$ has the same length as $w_1$ and has the form
		  $$
		  w_2=a b a^{-1} b^{-1} w_3
		  $$ #card
			- This is an elaborate proof, so ignore it for now.
		- ((63ff1cab-4221-49ab-9d57-42cf9aa3952d)) Let $w$ be a proper scheme of the form
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
		- ((63ff1f74-71d1-4d4e-b347-d0746b62e728)) (The classification theorem). Let $X$ be a surface formed by a proper scheme. Then $X$ is homeomorphic either to $S^2$, to the $n$-fold torus $T_n$, or to the $m$-fold projective plane $P_m$. #card
			- Note this only works for pasting edges in pairs. Not for, eg. ((63e86249-c48a-4740-a36d-100aeb1da16c)).
			- Collecting the lemmas above!
		-
-