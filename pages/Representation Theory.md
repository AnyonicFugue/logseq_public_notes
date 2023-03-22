alias:: Representation

-
- [[Representation Theory/Lie Algebras and Lie Groups]]
- [[Representation Theory/Group]]
- 'Self-consistency' often implies {{cloze representations of certain groups}}.
	- Three components: A set of operations, compose, **self-consistent** (associativity)
		- Different sets of operation lead to different algebraic structures
	- eg Particles under [Lorentz transformation](../../Miscellaneous/Basic Concepts/Lorentz transformation.md); Paths classified by homotopy
- # Definitions
  collapsed:: true
	- A homomorphism $G \rightarrow GL(V)$
	-
	- Equivalent representations
		- We say that two linear representations$$T_{1} :G\rightarrow \mathrm{GL}( V_{1})   \text{ and }   T_{2} :G\rightarrow \mathrm{GL}( V_{2}) ,$$ are **equivalent**, and write $T_{1} \simeq T_{2}$, if there exists an isomorphism $\sigma :V_{1}\rightarrow V_{2}$ such that $\sigma T_{1} (g)=T_{2} (g)\sigma$ for all $g\in G$.
	- Irreducible
		- $T:G\rightarrow \operatorname{GL} (V)$ is said to be irreducible if there are no nontrivial (i.e., different from 0 and $V$) subspaces $U\subset V$ invariant under $T$.
	- Unitary representation
		- Representation operators are unitary
	- Completely reducible #card
		- Every invariant subspace $U\subset V$ has an invariant complement $W$. (Recall that $W$ is called a COMPLEMENT of $U$ if $V=U\oplus W$.)
		- That is, can be decomposed into a sum of invariant reps.
	- ## Produce new reps from old ones
		- With every invariant subspace $U$ we can associate two linear representations of  $G$, acting on the spaces  $U$ and  $V/U$ respectively.
		- Tensor product
			- The tensor product of $T$ and $S$ is the representation $T\otimes S$ of the group $G\times H$ in the space $V\otimes U$, defined by the rule 
			  $$\begin{array}{l}
			  (T\otimes S)(g,h)=T(g)\otimes S(h)\end{array}$$
			- Matrix wise:$$\left( T\otimes T^{\prime }\right)( g_{1} ,g_{2}) X=T( g_{1}) XT( g_{2})^{-1}$$
		- Product representation
			- The PRODUCT OF $T$ AND $S$ is the representation $TS$ of $G$ in the space $V\otimes U$ defined by the rule 
			  $$\begin{equation*}
			  TS(g)=T(g)\otimes S(g).
			  \end{equation*}$$
			- For an element $x=\sum x_{i j}\left(e_{i} \otimes f_{j}\right)$:
			  $$X\mapsto T_{(e)} (g)XS_{(f)} (g)$$
		- Subrepresentation
			- Obtained by restricting the operators  $T(g)$ to a subspace $U$ :
				- $T_{U} (g)= T(g)| _{U}$ for all $g\in G$.
		- Quotient representation
			- Quotient of $T$, denoted by $T_{V/U}$, is defined as $T_{V/U} (x+U)=T(g)x+U$.
		- Dual representation #card
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-04-02T10:50:43.780Z
		  card-last-reviewed:: 2023-03-09T10:50:43.782Z
		  card-last-score:: 5
			- The representation space is the dual vector space.
			- $$\left( T^{\prime } (g)f\right) (x)=f\left( T(g)^{-1} x\right)$$
			- Matrix-wise: We select the dual basis $f_i(e_j)=\delta_{ij}$, then obtain
			  $$T'(g)_{ij}=T(g^{-1})_{ji}$$
		- Complexification
			- Extend the underlying field
			- $T_C(g)(u+iv)=T(g)u+iT(g)v$
			-
			- Connecting Abstract algebra and rep. theory
	- Regular representation #card 
	  id:: 1e9f6e33-36ec-4362-9505-3b42540bb3a7
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-04-14T01:21:46.953Z
	  card-last-reviewed:: 2023-03-21T01:21:46.954Z
	  card-last-score:: 5
		- $$\left(\operatorname{Reg}( g_{1} ,g_{2}) f\right) (g)=f\left( g_{2}^{-1} gg_{1}\right),f\in M(T)$$
			- The definition ensures Associativity:
			  $(L(g_1)L(g_2)f)(g)=L(g_1)f(gg_2)=f((gg_1)g_2)=f(gg_1g_2)$
			- $f$ usually taken to be $f_g(h)=\delta_{gh}$
		-
		- Maybe linked to differential geometry:
		  A definition by pushforward.
		- Obviously we can generalize to higher-rank tensors, which are tensor products of the regular representation.
	- Character #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-01T01:03:51.863Z
	  card-last-reviewed:: 2023-03-07T01:03:51.863Z
	  card-last-score:: 5
		- $\chi_T(g)=Tr(T(g))$ trace of the rep. operator
		- Automatically basis independent, thus a good def.
	- Inner product of matrix elements #card
		- $$( f_{1} ,f_{2}) =\frac{1}{|G|}\sum _{g\in G} f_{1} (g)\overline{f_{2} (g)}$$
	- Central function #card 
	  id:: c444aad8-769e-4048-b5d7-6a01a193068c
	  card-last-interval:: 29.48
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-03T22:14:00.208Z
	  card-last-reviewed:: 2023-03-05T11:14:00.209Z
	  card-last-score:: 5
		- $f\in \mathbf{C}[G]$ s.t.  $f(gxg^{-1})=f(x)$
		- eg [Character](../Representation theory/Basic Definitions/Character.md): since trace allows cycle permutation
		-
		- Space of central function $\mathbf{C}[G]^\#$
-
-
-
-