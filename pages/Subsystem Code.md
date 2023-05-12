- Ref
	- Original article: [Stabilizer Formalism for Operator Quantum Error Correction](https://arxiv.org/pdf/quant-ph/0508131.pdf)
		- PRL, concise but short of details
	- Useful review: Bombin 2020
- # Idea
	- Error-correcting relies on redundance.
	- We may add redundance in the obvious way: Consider the space $A \otimes B$. $A$ stores the logical information, while $B$ is completely free.
		- We say that B is the **gauge subsystem**.
		- This leads us to rethink:
- # Problems
	- Can we always find a set of generators of $G$ in the form $\{X_1,...,X_l;X_{l+1},Z_{l+1},...,X_{l+g},Z_{l+g}\}$?
		- If this holds, then $S=C(G)$ and the gauge part is $L=G/C(G)$ follows easily.
		- To generalize: For a set of operators satisfying $P^2=\pm 1$, $P_i P_j= \pm P_j P_i$, can we always find such generators?
- # Formulation
	-
- # Facts
	- An abelian gauge group corresponds to the conventional stabilizer code.
		- i.e. The gauge group can be regarded as part of the stabilizer group.
	- Necessary and sufficient error-correction conditions are, for all errors $E_a, E_b$ in the error set $\mathcal{E}$,
	  $$
	  P E_a^{\dagger} E_b P=I_{\mathrm{A}} \otimes g_{a b}^{\mathrm{B}}
	  $$
	  where $P$ is a projector onto the codespace $\mathrm{C}\equiv A \otimes B$, and $g_{a b}^{\mathrm{B}}$ is an arbitrary operator on the gauge subsystem.