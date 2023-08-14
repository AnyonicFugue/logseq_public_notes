- ![Entanglement Negativity at Measurement-Induced Criticality.pdf](file://zotero_link/Entanglement Negativity at Measurement-Induced Criticality.pdf)
- # Basic Facts
  collapsed:: true
	- For stabilizer circuits, the entanglement measures do not depend on the Renyi indices or
	  the measurement outcomes.
		- Intuitively, all measurement outcomes could be flipped by single-qubit operators.
	- The state is alway a direct product of GHZ states, each supported on a subset of qubits, where
	  the subsets form a partition (which changes over time) of Q.
		- Intuitively, the subset is stabilized by a set of **locally anti-commutating** stabilizers.
- # The Majorana Loop Representation
  collapsed:: true
	- $$
	  \begin{aligned}
	  \gamma_{2 j-1} & =\left(\prod_{i<j} X_i\right) Z_j, 1 \leq j \leq L \\
	  \gamma_{2 j} & =\left(\prod_{i<j} X_i\right) Y_j, 1 \leq j \leq L
	  \end{aligned}
	  $$
		- Note that the convention of JW transformation is a bit different from mine.
	- $$
	  \begin{aligned}
	  i \gamma_{2 j-1} \gamma_{2 j} & =X_j \\
	  i \gamma_{2 j} \gamma_{2 j+1} & =Z_j Z_{j+1}
	  \end{aligned}
	  $$
	- ((64d4e9de-65a1-49a2-b45a-5d88bd1994f7))
	- ((64d4e9ec-db9d-46b0-8ecf-b0215abe5477))
		- The loops at the upper boundary indicates the initial configuration, i.e. the configuration specified by the arc stabilizers.
	- ## Braiding
		- $$
		  \begin{aligned}
		  & U_1^M: \gamma_{2 j-1} \leftrightarrow \gamma_{2 j} \quad \Leftrightarrow_{J W} \quad U_1^S: Z_j \leftrightarrow Y_j \\
		  & U_2^M: \gamma_{2 j} \leftrightarrow \gamma_{2 j+1} \quad \Leftrightarrow_{J W} \quad U_2^S: Y_j I_{j+1} \leftrightarrow X_j Z_{j+1} . \\
		  &
		  \end{aligned}
		  $$
		-
- # Physical Quantities
	- Entanglement Entropy
		- Easily calculated by counting stabilizers (here counting majorana strings)
	- Mutual information
		- $$
		  I_{A B}=S_A+S_B-S_{A \cup B}
		  $$
		- Again by counting string.
		- As a result, $I_{AB}=0$ iff the two regions have intersection in the same GHZ cluster.
		- ((64d532b0-9386-4e5a-b3ce-ba6f75e426ea))
	- Mutual Negativity
		- Again, we start by focusing on the simple case when $|A|=|B|=1$.
			- From the state decomposition in Eq. (25), we see that $A$ and $B$ has MN $N_{A, B}=\ln 2$ if these two qubits constitute a two-qubit GHZ state (i.e. an EPR pair; see Fig. 2(f)) but unentangled from everything else; but zero otherwise - either when $A$ and $B$ are not in the same cluster (Fig. 2(d)), or they are in a cluster with at least three qubits (Fig. 2(e)).
		-