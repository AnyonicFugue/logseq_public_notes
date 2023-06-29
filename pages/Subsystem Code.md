- Ref
	- Original article: [Stabilizer Formalism for Operator Quantum Error Correction](https://arxiv.org/pdf/quant-ph/0508131.pdf)
		- PRL, concise but short of details
	- Useful review: Bombin 2020
- # Idea
	- Error-correcting relies on redundance.
	- We may add redundance in the obvious way: Consider the space $A \otimes B$. $A$ stores the logical information, while $B$ is completely free.
		- We say that B is the **gauge subsystem**.
		-
- # Problems
	- Can we always find a set of generators of $G$ in the form $\{X_1,...,X_l;X_{l+1},Z_{l+1},...,X_{l+g},Z_{l+g}\}$?
		- If this holds, then $S=C(G)$ and the gauge part is $L=G/C(G)$ follows easily.
		- To generalize: For a set of operators satisfying $P^2=\pm 1$, $P_i P_j= \pm P_j P_i$, can we always find such generators?
- # Restrictions
	- The state must always be separable.
		- For example, if there is a state $|0\rangle \otimes |0\rangle + |1\rangle \otimes |1\rangle$, then the gauge operators would have nontrivial effects.
		- In other words, there could never be entanglement.
		-
	-
- # Tensor Product in a Matrix Viewpoint
	- $$V:=A \otimes B$$
		- $A$ is the logical part while $B$ is the gauge part.
	- ## Labelling of Basis
		- First, select a basis $\{e_i\}$ for $A$ and a basis $\{f_j\}$ for $B$.
		- A basis for $V$ is $\{v_{ij}:=e_i \otimes f_j\}$
		-
	- ## Gauge Operators
		- $$\begin{align*}
		  ( I\otimes T) v_{ij} & =( I\otimes T)( e_{i} \otimes f_{j})\\
		   & =( Ie_{i}) \otimes ( Tf_{j})\\
		   & =e_{i} \otimes \left(\sum _{k} T_{kj} f_{k}\right)\\
		   & =\sum _{k} T_{kj} v_{ik}
		  \end{align*}$$
		- We can say the decomposition is kept the same (line 3),
		  or the gauge operators acts in a manner independent of index i (position inside a block), only depending on the index k (the number of the block).