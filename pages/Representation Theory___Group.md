- # Basic Facts
	- Theorem. If $V=U\oplus W$, then  $T_{W}$ and $T_{V/U}$ are isomorphic.
	  collapsed:: true
		- We can select vectors of W as representatives.
		- Can be used on "The remaining part of the sum"
	- ## Decomposition into Minimal invariant subspaces
		- Theorem. Let $T:G\rightarrow \mathrm{GL} (V)$ be a linear representation. Let $V=V_{1} +V_{2} +\dotsc +V_{m}$ be a decomposition of the space $V$ into a (**not necessarily direct**) sum of minimal invariant subspace. 
		  card-last-interval:: 23.96
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-20T00:54:11.987Z
		  card-last-reviewed:: 2023-02-24T01:54:11.987Z
		  card-last-score:: 5
		  Then for every invariant subspace $U$ there exist indices $i_{1} ,\dotsc ,i_{p}$ such that $V=U\oplus V_{i_{1}} \oplus \dotsc \oplus V_{i_{p}}$  #card
			- For a $U$: we use a common construction.
			- "Maximal LI list $\{U,V_{i1},...V_{ip}\}$"  #Trick
			- We show this must span V.
			-
			- Intersect with any "Min invsp outside":
			  collapsed:: true
				- Min ⇒ the intersection must be 0 or full space.
		- Theorem. Suppose the representation $T:G\rightarrow \mathrm{GL} (V)$ is isomorphic to a sum of irreducible representations $T_{i} :G\rightarrow \operatorname{GL}( V_{i}) ,i=1,\dotsc ,m$. 
		  collapsed:: true
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-14T09:23:29.466Z
		  card-last-reviewed:: 2023-02-18T09:23:29.467Z
		  card-last-score:: 5
		  Then every subrepresentation of $T$ ,as well as every quotient representation of $T$ is isomorphic to a sum of some of the representations $T_{i}$ #card
			- Invoke  Theorem 3. Let $T:G\rightarrow \mathrm{GL} (V)$ be a linear Representation. Let $V=V_{1} +V_{2} +\dotsc +V_{m}$ be a decomposition of the space V into a (not necessarily direct) sum of minimal invariant subspace. 
			  Then for every invariant subspace  U there exist indices $i_{1} ,\dotsc ,i_{p}$ such that $V=U\oplus V_{i_{1}} \oplus \dotsc \oplus V_{i_{p}}$
			- Consider a subrep $T_U$: $$T_U\simeq T_{V/({V_{i_{1}} \oplus \dotsc \oplus V_{i_{p}}})}\simeq T_{sum\ of\ the\ remaining\ V_j }$$
			- Isomorphism is the best we can obtain, without more conditions.
			- i.e. Decomposition isn't unique.
			-
			- Corollary. Let $T:G\rightarrow \mathrm{GL} (V)$ be a linear representation. Let $V_{1} ,\dotsc ,V_{m}$ be minimal invariant subspaces such that the representations $T_{i} =T_{V_{i}}$ are **pairwise nonisomorphic**(New condition). Then $V_{1} ,\dotsc ,V_{m}$ are linearly independent.
			  id:: 4b39adbd-96d1-4605-8870-8ce25437e6f7
		- Theorem. Let $T$ be a linear representation. If $$T\simeq T_{1} +\dotsc +T_{m} \simeq S_{1} +\dotsc +S_{p}$$ where $T_{i}$ and $S_{j}$ are irreducible representations, then $m=p$ and, for a suitable labeling, $T_{i} \simeq S_{i}$. #card
		  collapsed:: true
		  card-last-interval:: 23.96
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-20T00:53:18.474Z
		  card-last-reviewed:: 2023-02-24T01:53:18.474Z
		  card-last-score:: 5
			- By induction.
			- For m=2 case: invoke [Theorem 3. Suppose the representation T:G\rightarrow \mathrm{GL} (V) is isomorphic to a sum of Irreducible representations T_{i} :G\rightarrow \operatorname{GL}( V_{i}) ,i=1,\dotsc ,m. 
			  Then every Subrepresentation of T ,as well as every Quotient representation of T is Isomorphic to a sum of some of the representations T_{i}.  ](../Representation theory/Preliminary results/Decomposition into Minimal invariant subspaces/Theorem 3. Suppose the representation T_G_rightarrow _mathrm{GL} (V) is isomorphic to a sum of Irreducible representations T_{i} _G_rightarrow _operatorname{GL}( V_{i}) ,i=1,_dotsc ,m. 
			  Then every Sub.md)
			-
			- The decomposition of representations is only unique up to isomorphism.  #Remark
	-
	- ## Inner product and reducibility
		- Proposition. Every orthogonal or unitary representation is completely reducible. #card
			- U inv ⇒ Complement of U inv.
		- Theorem. Every real (complex) linear representation of a finite group is isomorphic to an orthogonal (unitary) representation. #card
		  collapsed:: true
			- Construct an invariant inner product by summing:  #Trick
			- Given any inner product $f_0(\cdot,\cdot)$, define $f(u,v)=\sum_{g}f_0(T(g)u,T(g)v)$
		- Theorem. Every real (complex) linear representation of a compact topological group is orthogonal (respectively, unitary). #card
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-16T11:53:25.978Z
		  card-last-reviewed:: 2023-02-20T11:53:25.980Z
		  card-last-score:: 5
			- The point is an invariant integration on the group manifold.
			- From the point of view of the theory of (continuous) linear representations, compact topological groups are similar to discrete ones. #[[Thoughts/Math and Physics]]
		- Lemma. Let $f$ and $f_{0}$ be two inner products in the complex vector space $V$. Then there exists a linear operator $\sigma$ such that $f(x,y)=f_{0} (\sigma x,y)$  for all $x,y\in V$.
		- Theorem. Let $T:G\rightarrow \operatorname{GL} (V)$ be an irreducible unitary representation. Then the $T$-invariant inner product in $V$ is unique up to a constant factor.  #card
		  collapsed:: true
			- [[Lemma. Let f and f_{0} be two inner products in the complex vector space V. Then there exists a linear operator \sigma such that f(x,y)=f_{0} (\sigma x,y)  for all x,y\in V.]]
			- $\sigma$ is a self-intertwining map. #Exercise
			-
			- This allows some construction of inner products.  #Remark
			- [[Make full use of every definition (Write its immediate consequences） ]]
		-
	-
	- ## Complexification
	  collapsed:: true
		-
		- Two finite-dimensional real representations are isomorphic if and only if their [[Complexification]] are isomorphic. #card
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-20T01:48:58.817Z
		  card-last-reviewed:: 2023-02-24T01:48:58.818Z
		  card-last-score:: 5
		  collapsed:: true
			- p⇒q is obvious.
			- q⇒p: The matrix equation is $T_{1C}S=ST_{2C}$, which is linear.
			  We can take complex conjugate of both sides, then $S^*$ is also a solution.
			  Then $(S+S^*)$, which is real, is also a solution.
		-
		- Theorem 6. Let $T:G\rightarrow \operatorname{GL} (V)$ be an [[Irreducible]] real linear representation. Then $T_{\mathbf{C}}$ is ^^either irreducible, or the sum of two irreducible representations^^. 
		  collapsed:: true
		  In the second case $V_{\mathbf{C}}$ decomposes into the direct sum of two complex-conjugate minimal invariant subspaces. #[[Complexification]]   #card
			- Obviously, for any $W\sub V$, $V=W+\overline{W}$
			- $u+iv \in W$ ⇒ $u-iv\in \overline{W}$ . Given $u \ and\ iv$ , since T is irreducible, the whole space can be covered.
			-
			- Consider a [[Minimal invariant subspace]] W:
			- $W\cap \overline{W}=0\ or\ W$
	-
	- ## Lift and factoring of representation #card
		- Def
			- For a rep. of quotient group $G/N$, $S:G/N\rightarrow \operatorname{GL} (V)$  and $p:G\rightarrow G/N$:
			  $$(S\circ p)(h)=\varepsilon   \text{ for all } h\in N$$ is a lift of S.
		-
		- Conversely, every linear representation $T$ of $G$ whose kernel contains $N$ 
		  can be **factored** through $p$, i.e., $T=S\circ p$
		-
		- We thus establish a one-to-one correspondence between the **Linear representations of the quotient group**  and those **linear representations of ** $G$ whose kernel contains $N$.
			- Can be used to simplify some problems.
	-
	- ## On tensor products of reps
	  collapsed:: true
		- Theorem. Let $T$ be an complex irreducible representation of the group $G$ in the space $V$, and let $I$ be the trivial representation of $G$ in the space $U$. Then every minimal subspace $W\subset V\otimes U$ invariant under the product representation $TI$ has the form $V\otimes u_{0}$, where $u_{0} \in U$.  #card
		  id:: 4746422f-8ebd-4b6e-b09a-a6d71742468b
			- A wrong attempt
			  collapsed:: true
				- Directly construction: Consider some $v_0\otimes u_{0} \in W$
				- $TI$ will make it to  $V\otimes u_{0}$
			- The vectors in $V\otimes U$ are $\sum{c_{ij}\ e_i\otimes f_j}$ !
			-
			- We can rewrite it as $\sum_j{v_j \otimes f_j}$
			- Construct "coordinate functions" $\sigma_i:W\rightarrow V\otimes f_i$
			-
			- $\sigma_i$ is a Morphism between $TI\big|_W$and  $TI\big|_{V \otimes f_i}$ , while $TI\big|_{V \otimes f_i}$ can be identified with T!
			  collapsed:: true
				- Try to identify some reps, to make use of [[Schur's Lemma]]  #Remark
			- By Schur's: All $\sigma_i$ are proportional, $\sigma_i=c_i\sigma_0$
			- $w=c_1\sigma_0(w)\otimes f_1+...+c_n\sigma_0(w)\otimes f_n=\sigma_0(w)\otimes (c_1f_1+...+c_nf_n)$
			-
			-
		- Theorem. The tensor product of two irreducible complex representations $T:G\rightarrow \operatorname{GL} (V)$ and $S:H\rightarrow \operatorname{GL} (U)$ of the groups $G$ and $H$ 
		  collapsed:: true
		  card-last-interval:: 27.15
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-19T15:03:27.457Z
		  card-last-reviewed:: 2023-02-20T12:03:27.458Z
		  card-last-score:: 5
		  is an **irreducible** representation of $G\times H$.  #card
			- Invoke ((4746422f-8ebd-4b6e-b09a-a6d71742468b)).
			-
			- Consider W inv under $T\otimes S$:
			- W must be inv under $TI$ and $IS$.
			-
			- Split W into min invsp. of TI and IS separately:
			- $W=(V\otimes u_1)\oplus...\oplus(V\otimes u_m)=(v_1\otimes U)\oplus...\oplus(v_n\otimes U)$
			- Obviously $W=V\otimes U$
	-
	-
	- ## About Matrix Elements
		- Def
			- The functions $T_{ij} \in \mathbf{C} [G]$
			- $M(T)$ is the linear span of the matrix elements of $T$ (relative to some basis).
		- Proposition.  $M(T)$ is basis independent and invariant under translations.  #card
		  card-last-interval:: 24
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-12T11:37:59.951Z
		  card-last-reviewed:: 2023-02-16T11:37:59.952Z
		  card-last-score:: 5
			- Just prove: One set can be expressed by linear combinations of another, and vice versa. #Trick
			-
			- Basis independent: $T_{ij}$ under any basis can be expressed as linear combinations of another basis.
			- Invariance: Similar.
		-
		- We can express any f in $M(T)$ invariantly:
			- $f=\sum_{i, j} c_{i j} T_{i j} \in \mathbf{C}[G] \quad\left(c_{i j} \in \mathbf{C}\right)$
		- Write in matrix form, $[c_{ji}]=\xi$ :
		  $$\begin{aligned}
		  \mu :\mathrm{L} (V)&\rightarrow \mathbf{C} [G]\\
		  \mu(\xi )(g)&=\operatorname{tr} \xi T(g)\ \ (\xi \in \mathrm{L} (V))
		  \end{aligned}$$
			- Prop. $\mu$ is an **isomorphism** of $T\otimes T^{\prime }$ and the ((1e9f6e33-36ec-4362-9505-3b42540bb3a7)) $Reg_{M(T)}$ #card
			  collapsed:: true
				- Prop1. $\mu$ is a morphism
					- Use matrix: $f\left( g_{2}^{-1} gg_{1}\right) =\operatorname{tr} \xi T\left( g_{2}^{-1} gg_{1}\right) =\operatorname{tr} \xi T( g_{2})^{-1} T(g)T( g_{1})$ $=\operatorname{tr}\left( T( g_{1}) \xi T( g_{2})^{-1}\right) T(g)=\operatorname{tr} \eta T(q)$
					- $$\eta =T( g_{1}) \xi T( g_{2})^{-1} =\left( T\otimes T^{\prime }\right)( g_{1} ,g_{2}) \xi$$
						- $(T\otimes T')(g_1,g_2)(X)=T(g_1)XT(g_2^{-1})$
					- So $\mu \circ (T\otimes T')=Reg\circ \mu$
				- ![1.png](../assets/1_1676528377752_0.png)
					- Graph is good!
					- Here we identified $L(V)$ and $V\otimes V'$
					- Not enough. We still need to prove it's bijective.
				-
				- Note that $T\otimes T^{\prime }$ is irreducible.
				- Therefore, $Ker\ \mu \subset L(V)$ is either 0 or $L(V)$
				- $Im\ \mu=M(T)$ , therefore $Ker\ \mu=0$
				-
				- The same man in different mirrors by isomorphisms. #[[Thoughts/Math and Physics]]
			-
			- Corollary 1. $\operatorname{dim}\mathrm{M} (T)=n^{2}$, where  $n=\operatorname{dim} V$. #card
			- Corollary 2. The map $\mu$ establishes an isomorphism of $IT^{\prime }$ and $L_{\mathrm{M} (T)}$ as well as→$TI^{\prime }$ and $R_{\mathrm{M} (T)}$.
			- Corollary 3. $L_{\mathrm{M} (T)} \simeq nT^{\prime }$ and  $R_{\mathrm{M} (T)} \simeq nT$. 
			  id:: caeeba62-511c-4014-abcc-0317e98b10e8
				- $IT'\simeq nT^{\prime }$
			- Corollary 4. Let $T_{1}$ and $T_{2}$ be nonisomorphic irreducible complex representations of the group $G$. 
			  id:: 0e1d7f6e-d7fc-4bb8-bc17-e7506829c273
			  Then $\operatorname{Reg}_{\mathrm{M}( T_{1})}$ and $\operatorname{Reg}_{\mathrm{M}( T_{2})}$ are not isomorphic. #card
				- 【Proof by restricting the group】
				- If $\operatorname{Reg}_{\mathrm{M}( T_{2})}\simeq \operatorname{Reg}_{\mathrm{M}( T_{1})}$ , then $\operatorname{L}_{\mathrm{M}( T_{1})}\simeq \operatorname{L}_{\mathrm{M}( T_{2})}$
				- By [Corollary 3](((caeeba62-511c-4014-abcc-0317e98b10e8))) , which is a contradiction.
				-
				- Corollary.  Let $T_{1}$ and $T_{2}$ be nonisomorphic irreducible complex representations of the group $G$, 
				  then $T_1\otimes T_1'$ isn't isomorphic to $T_2\otimes T_2'$ .
			- Corollary 5. Let $T_{1} ,\dotsc ,T_{q}$ be pairwise nonisomorphic irreducible complex representations of the group $G$. 
			  Then the subspaces $\mathrm{M}( T_{1}) ,\dotsc ,\mathrm{M}( T_{q})$ of $\mathbf{C} [G]$ are linearly independent.  #card
				- By [Corollary 4](((0e1d7f6e-d7fc-4bb8-bc17-e7506829c273))), $\mathrm{M}( T_{1}) ,\dotsc ,\mathrm{M}( T_{q})$ are invariant and pairwise nonisomorphic.
				-
				- Invoke the common trick: 
				  Select a  __maximal LI list__ ,  and  __intersect with the remainers__ .
				-
				- ((4b39adbd-96d1-4605-8870-8ce25437e6f7))
			- Theorem. $\mathbf{C} [G]=\mathrm{M}( T_{1}) \oplus \dotsc \oplus \mathrm{M}( T_{q})$ #card
			  card-last-interval:: 24
			  card-repeats:: 1
			  card-ease-factor:: 2.36
			  card-next-schedule:: 2023-03-24T13:54:45.818Z
			  card-last-reviewed:: 2023-02-28T13:54:45.818Z
			  card-last-score:: 3
				- Linear independence: Since they're pairwise nonisomorphic.
				-
				- Spanning: we use the dirty way i.e. matrix
				- Select a basis $\{f_j\}$ of  $\mathbf{C} [G]$
				- $f_j(g)=R(g)f_j(e)=\sum_iR_{ij}(g)f_i(e)$
				- Therefore $f_j=\sum_if_i(e)R_{ij}$
				-
				- View $f_i(e)$ as coefficients: Any $f_j$ can be generated by $\{R_{ij}\}$
				- Since each irrep is a subrep of R, $\{R_{ij}\}\sub span\{M(T_k)\}$
				- Thus $\{M(T_k)\}$ is spanning.
				- **Q.E.D.**
			- Corollary. $n_{1}^{2} +\dotsc +n_{q}^{2} =|G|$.
			- Corollary. $L\simeq R\simeq \sum n_{k} T_{k}$
			-
			- Theorem.  The characters of the irreducible representations constitute a **basis** for the space of ((c444aad8-769e-4048-b5d7-6a01a193068c)) #card
				- Central ⇔ $Reg(g,g)f=f$
				- Since $M(T_k)$ are inv under Reg: we can find the basis vectors in the $M(T_k)$
				-
				- To prove: in $M(T_k)$, only $\chi_{T_k}$ is central.
				- ${(Reg(g,g)f)(x)=Tr(\xi T(gxg^{-1})) }\overset{Cycle\ perm\ of\ trace }{=}Tr((T(g^{-1})\xi T(g)T(x))$
				- Therefore, $\xi=T(g^{-1})\xi T(g)$
				-
				- By Schur's Lemma, $\xi=\lambda I$
			- Corollary.  Number of irreducible representations = Number of conjugacy classes (Equals number of central functions)
			- Corollary. The traces of irreducible representations are distinct.
		-
		-
	-
-