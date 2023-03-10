- ((63ba6c1b-ec02-4407-839d-f3522cc4abb9)) Let $C$ be a **compact** subspace of $S^2$; let $b$ be a point of $S^2-C$; and let $h$ be a homeomorphism of $S^2-b$ with $\mathbb{R}^2$. Suppose $U$ is a component of $S^2-C$. If $U$ does not contain $b$, then $h(U)$ is a **bounded** component of $\mathbb{R}^2-h(C)$. If $U$ contains $b$, then $h(U-b)$ is the **unbounded** **component** of $\mathbb{R}^2-h(C)$. In particular, if $S^2-C$ has $n$ components, then $\mathbb{R}^2-h(C)$ has $n$ components.
  id:: 63ba6c1e-488e-40e1-993b-729fc59ffccb
  collapsed:: true
	- The intuition is very clear: $h(C)$ is compact, thus closed and bounded; b is mapped into inf.
	- Step1. If $U$ is a **component** of $S^2-C$, then $U-b$ is **connected**.
	  collapsed:: true
		- Intuitively, U can't be broken into 2 parts by removing a single point.
			- This might not hold for general spaces, but it holds for $S^2-C$.
		- Proof
			- Suppose $U-b=A\cup B$.
			- Since C is compact thus closed, we may take some neighborhood $W(b)$ disjoint from C s.t. $W$ is homeomorphic to an open ball of $\mathbb{R}^2$.
				- The requirement of 'homeomorphic to an open ball' is stronger, but reasonable on $S^2$.
			- Then $W-b$ is connected, thus entirely lies in A.
			- Now $A\cup b$ and $B$ forms a separation, since W entirely lies in $A \cup b$.
	- Step2. Let $\left\{U_\alpha\right\}$ be the set of components of $S^2-C$; let $V_\alpha=h\left(U_\alpha-b\right)$.
		- Since $S^2-C$ is **locally connected**, the sets $U_\alpha$ are connected, disjoint, **open** subsets of $S^2$. Therefore, the sets $V_\alpha$ are connected, disjoint, open subsets of $\mathbb{R}^2-h(C)$, so the sets $V_\alpha$ are the components of $\mathbb{R}^2-h(C)$.
		- The point is **open**, which is preserved by h.
	- Step3. Invoke the [[One-Point Compactification]].
		- Another common [[Strategy]!
		  id:: 63c14167-6109-4d3b-a9cc-0b33bb63e764
			- ((63c1416f-d51b-4487-865b-f9d3cf9b5918))
		- Then b is mapped to $\infty$.
		- The neighborhoods of $\infty$ are $\mathbb R \cap \infty -C$. Compact <-> Closed and bounded.
		-
- ((63ba7047-d03a-4029-8daf-5787e7eabe4f)) Let $a$ and $b$ be points of $S^2$. Let $A$ be a compact space, and let $f: A \longrightarrow S^2-a-b$ be a continuous map. If $a$ and $b$ lie in the same component of $S^2-f(A)$, then $f$ is nulhomotopic. #card
  id:: 63ba704a-2fd3-4833-b52a-2e3ee5a134a8
  collapsed:: true
  card-last-interval:: 26.06
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-03-07T12:19:49.493Z
  card-last-reviewed:: 2023-02-09T11:19:49.494Z
  card-last-score:: 3
	- Intuitively, we need two 'holes' to prevent some loop on $S^2$ to be contractible.
		- A bit more precisely, $f(A)$ is compact, thus closed. So each component of $S^2-f(A)$ is open. We may gradually expand the components to squeeze $f(A)$ into a single point.
		- The loop itself may have multiple 'holes'.
	- Proof
		- Step1. Choose an equivalent formulation.. Place $a$ at 0, $b$ at $\infty$. $g: A \rightarrow \mathbb{R}^2-\mathbf{0}$
		- Step2. Choose a large disk B and a point $p \notin B$.
		- ### Central construction: $H(x, t)=\operatorname{tg}(x)-p$
			- Essentially, zoom the shape $g(A)$ finally to a point.
				- This can be generalized to lots of strange shapes as long as they're bounded.
			- The 'shift' $p$ grants that the homotopy won't intersect the origin.
			- Path-connectedness grants that the final path is homotopic to the initial one after the shift.
-
- Statement
	- ((63ba7757-abc4-4455-8a09-b5fba5a4b80d)) A simple closed curve $C$ separates $S^2$, i.e. $S^2-C$ isn't connected. #card
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-04-01T03:53:06.479Z
	  card-last-reviewed:: 2023-03-08T03:53:06.479Z
	  card-last-score:: 3
		- Summary of the scheme
			- Write $C$ as the union of 2 arcs $A_1$ and $A_2$, which only intersect at endpoints $a$ and $b$.
			- Write $U=S^2-A_1$, $V=S^2-A_2$, $X=U \cup V$.
			- If we **assume** $U \cap V$ to be connected, then by ((63b186e0-b1f4-4b2d-9772-895775842ded))
			- However, we show that $i_*$ and $j_*$ are **trivial**, while $X=S^2-a-b$ isn't simply connected, which derives a **contradiction**.
		- Details
			- Since $A_1$ and $A_2$ are connected, ((63ba704a-2fd3-4833-b52a-2e3ee5a134a8)) applies. So any loop in U or V is nulhomotopic.
			-
	-