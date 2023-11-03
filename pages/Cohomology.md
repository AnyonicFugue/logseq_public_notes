- Start point
	- Consider the category $\mathbf {Ab}$.
	  $\mathbf{Ab}(-,G)$ is a contravariant functor.
	- Could we extend the functor to a complex...?
- # Definition
	- ((65323c20-b312-4f6f-86a7-a710f612d718)) Cohomology Groups #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-11-25T06:31:52.523Z
	  card-last-reviewed:: 2023-10-25T00:31:52.524Z
	  card-last-score:: 5
	  collapsed:: true
		- Let $G$ be an abelian group. If $n \geq 0$, then the group of (singular) $n$-cochains in $X$ with coefficients $G$ is $\operatorname{Hom}\left(S_n(X), G\right)$.
		- Denote 
		  $$
		  \delta^n=\partial_{n+1}^{\#}
		  $$
		- The group of $n$-cocycles is $\operatorname{ker} \delta^n$ and is denoted by $Z^n(X ; G)$; the group of $n$-coboundaries is im $\delta^{n-1}$ and is denoted by $B^n(X ; G)$. The $n$th cohomology group of $X$ with coefficients $G$ is
		  $$
		  H^n(X ; G)=Z^n(X ; G) / B^n(X ; G)=\operatorname{ker} \delta^n / \operatorname{im} \delta^{n-1}=\operatorname{ker} \partial_{n+1}^{\#} / \operatorname{im} \partial_n^{\#}
		  $$
- # Basic Facts
  collapsed:: true
	- Comparing basic facts of homology and cohomology #card
	  collapsed:: true
		- Common features
			- Functoriality
				- ((64b48496-7607-4075-8451-d120e228dafc))
				- ((65323c6e-8ef2-4c74-bdc2-84d19146566e))
			- Dimension axiom
				- ((6454f1b7-5d36-4a76-b56c-aa3dc7b2515d))
				- ((65324131-a2a4-47ba-b58b-6b4585d3cf8f))
			- Homotopy axiom
				- ((6498e102-758e-44db-bbcb-a7c679b43a90))
				- ((6532434c-4b75-4d01-8f70-dbe2ff7f036d))
		- Differences
			-
	- ((6532394c-e8b9-4752-9500-74081018a669)). If $\left(S_*(X), \partial\right)$ is a complex, then, for every abelian group $G$,
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-12-02T06:58:08.307Z
	  card-last-reviewed:: 2023-11-01T00:58:08.308Z
	  card-last-score:: 5
	  $$
	  0 \longrightarrow \operatorname{Hom}\left(S_0(X), G\right) \stackrel{\partial_1^*}{\longrightarrow} \operatorname{Hom}\left(S_1(X), G\right) \stackrel{\partial_2^*}{\longrightarrow} \operatorname{Hom}\left(S_2(X), G\right) \longrightarrow \cdots
	  $$
	  is a complex (denoted by $\operatorname{Hom}\left(S_*(X), G\right)$). #card
		- The lemma is extremely simple technically, but what's the insight behind?
		  background-color:: red
			- The functor is 'left exact', which is obvious for the composition?
		-
		- First of all, note that $\mathbf{Ab}(A,B)$ is itself an abelian group, with the addition given by
		  $$(f+g)(a)=f(a)+g(a)$$
			- For non-abelian groups it become a non-commutative multiplication.
		- Also, $\partial_n^*$ is the morphism $\mathbf{Ab}(-,G)(\partial_n)$, so it is naturally a group homomorphism.
		- The proof is simply
		  $$
		  \partial_{n+1}^{\#} \partial_n^{\#}=\left(\partial_n \partial_{n+1}\right)^{\#}=0^{\#}=0
		  $$
		  from the functoriality (so elegant!).
		- If written explicitly,
		  $$\partial_n^* f=S_n \stackrel{\partial_n}{\longrightarrow} S_{n-1}\stackrel{f}{\longrightarrow} G$$
		  $$\partial_{n+1}^* \partial_n^* f=S_{n+1} \stackrel{\partial_{n+1}}{\longrightarrow} S_n \stackrel{\partial_n}{\longrightarrow} S_{n-1}\stackrel{f}{\longrightarrow} G$$
		-
	- ((65323d0f-f8db-4f1d-9e3a-db122825b330)) For each fixed $n \geq 0$ and each abelian group $G$, cohomology is a contravariant functor
	  id:: 65323c6e-8ef2-4c74-bdc2-84d19146566e
	  collapsed:: true
	  $$
	  H^n(-,G): \mathbf{T o p} \rightarrow \mathbf{A b}
	  $$ #card
		- Here we take an categorical approach:
		  First note that $S_*$ is a functor $\mathbf{Top} \to \mathbf{Comp}$ ($\partial f_\#=f_\# \partial$). The next step is to show that $H^n(-,G)$ is a functor $\mathbf{Comp} \to \mathbf{Ab}$.
		- This part is not categorical, but completely analogous to that in homology.
	- ((65324137-b9c9-41d7-b1ac-0fdcaaeaaa34)) (Dimension Axiom). If $X$ is a one-point space, then
	  id:: 65324131-a2a4-47ba-b58b-6b4585d3cf8f
	  collapsed:: true
	  $$
	  H^p(X ; G)= \begin{cases}G & \text { if } p=0 \\ 0 & \text { if } p>0\end{cases}
	  $$ #card
		- First note that every $S_n(X) \cong \mathbb{Z}$ and $\operatorname{Hom}(\mathbb Z,G) \simeq G$.
		- The rest is completely analogous to the case of homology.
	- ((65324366-e806-4d87-a9bf-65ac108b78fb)) (Homotopy Axiom). If $f, g: X \rightarrow Y$ are homotopic, then they induce the same homomorphisms $H^n(Y ; G) \rightarrow H^n(X ; G)$ for all $n \geq 0$. #card
	  id:: 6532434c-4b75-4d01-8f70-dbe2ff7f036d
	  collapsed:: true
		- The strategy is very similar:
		- First we have the standard property
		  $$
		  f_{\#}-g_{\#}=\partial_{n+1}^{\prime} P_n+P_{n-1} \partial_n .
		  $$.
		- Then we plug it into the cohomology functor and show that
		  $$f^\# - g^\#=0$$
	- ((653327cf-4d81-4481-b020-e512c5b9cc84)) (Left exactness) Let $G$ be an abelian group. If $A^{\prime} \stackrel{i}{\rightarrow} A \stackrel{p}{\rightarrow} A^{\prime \prime} \rightarrow 0$ is an exact sequence of abelian groups, then there is an exact sequence
	  $$
	  0 \longrightarrow \operatorname{Hom}\left(A^{\prime \prime}, G\right) \stackrel{p^*}{\longrightarrow} \operatorname{Hom}(A, G) \stackrel{i^*}{\longrightarrow} \operatorname{Hom}\left(A^{\prime}, G\right) .
	  $$
		- Stated loosely, 'applying $\operatorname{Hom}(-,G) produces an exact sequence with reversed arrows'.
		- The proof process is easy, just drawing some diagrams to show the composition of maps. But the underlying thought is elusive.
	- Corollary. Let $G$ be an abelian group.
	  (i) $\operatorname{Hom}(\mathbf{Z}, G) \cong G$.
	  (ii) $\operatorname{Hom}(\mathbf{Z} / m \mathbf{Z}, G) \cong G[m]=\{x \in G: m x=0\}$.
	  (iii) $\operatorname{Hom}(\mathbf{Z} / m \mathbf{Z}, \mathbf{Z} / n \mathbf{Z}) \cong \mathbf{Z} / d \mathbf{Z}$, where $d=\operatorname{gcd}\{m, n\}$. #card
		- (i) is well-known.
		- (ii) Apply $\operatorname{Hom}(-, G)$ to the exact sequence
		  $$
		  0 \rightarrow \mathbf{Z} \stackrel{m}{\rightarrow} \mathbf{Z} \stackrel{p}{\rightarrow} \mathbf{Z} / m \mathbf{Z} \rightarrow 0,
		  $$
		  we obtain
		  $$
		  0 \longrightarrow \operatorname{Hom}(\mathbf{Z} / m \mathbf{Z}, G) \stackrel{p^*}{\longrightarrow} \operatorname{Hom}(\mathbf{Z}, G) \stackrel{m^*}{\longrightarrow} \operatorname{Hom}(\mathbf{Z}, G)
		  $$
		- Then we see
		  $$\operatorname{Hom}(\mathbf{Z} / m \mathbf{Z}, G) \simeq \operatorname{Im} p^* \simeq \operatorname{Ker} m^* =G[m] $$
	- Corollary. Since both functors $\operatorname{Hom}(-, B)$ and $\operatorname{Hom}(A, -)$ preserve direct sums, we can decompose any f.g. abelian group into 
	  $$
	  G=F \oplus C_1 \oplus \cdots \oplus C_k
	  $$
	  to calculate $\operatorname{Hom}(A,B)$.
- # Relative Cohomology
  collapsed:: true
	- ((65333051-fda2-476a-bf0d-ee5dabba4eea)) Let $G$ be an abelian group and let $A$ be a subspace of a space $X$. For every $n \geq 0$, there is an exact sequence of abelian groups
	  collapsed:: true
	  $$
	  0 \rightarrow \operatorname{Hom}\left(S_n(X) / S_n(A), G\right) \rightarrow \operatorname{Hom}\left(S_n(X), G\right) \rightarrow \operatorname{Hom}\left(S_n(A), G\right) \rightarrow 0 .
	  $$
	  Hence there is a short exact sequence of complexes
	  $$
	  0 \rightarrow \operatorname{Hom}\left(S_*(X) / S_*(A), G\right) \rightarrow \operatorname{Hom}\left(S_*(X), G\right) \rightarrow \operatorname{Hom}\left(S_*(A), G\right) \rightarrow 0
	  $$
		- The first step is simply applying the functor $\operatorname{Hom}(-,G)$ to the short exact sequence
		  $$
		  0 \rightarrow S_n(A) \rightarrow S_n(X) \rightarrow S_n(X) / S_n(A) \rightarrow 0
		  $$
		- Since the original short exact sequence extends to a short exact sequence of complexes, the new one also does due to functoriality.
			- i.e. The blocks still commute after applying the functor.
	- Definition. If $A$ is a subspace of $X$ and if $G$ is an abelian group, then the $n$th relative cohomology group with coefficients $G$ is
	  $$
	  \left.H^n(X, A ; G)=H_n \operatorname{Hom}\left(S_*(X) / S_*(A), G\right)\right)
	  $$
	-
	- Now more lemmas apply analogously...
	-
	- Theorem. If $A$ is a subspace of $X$ and if $G$ is an abelian group, there is an exact sequence
	  $$
	  0 \rightarrow H^0(X, A ; G) \rightarrow H^0(X ; G) \rightarrow H^0(A ; G) \stackrel{d}{\rightarrow} H^1(X, A ; G) \rightarrow H^1(X ; G) \rightarrow \cdots .
	  $$
	  where the connecting homomorphisms $d$ are natural. #card
		- Just apply the [exact triangle](((64b48492-3720-4903-af07-d9b768a34a2f))).
	- ((65333345-d64e-4d16-8bea-203a1c630f50)). (Excision) . Let $X_1$ and $X_2$ be subspaces of $X$ with $X=X_1^\circ \cup X_2^\circ$. Then the inclusion $j:\left(X_1, X_1 \cap X_2\right) \hookrightarrow\left(X, X_2\right)$ induces isomorphisms for all $n \geq 0$,
	  $$
	  j^*: H^n\left(X, X_2 ; G\right) \simeq H^n\left(X_1, X_1 \cap X_2 ; G\right)
	  $$ #card
		- Exercise. Just mimic the excision for homology.
	-