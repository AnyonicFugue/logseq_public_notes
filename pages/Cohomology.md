- Start point
	- Consider the category $\mathbf {Ab}$.
	  $\mathbf{Ab}(-,G)$ is a contravariant functor.
	- Could we extend the functor to a complex...?
- # Definition
	- ((65323c20-b312-4f6f-86a7-a710f612d718)) Cohomology Groups #card
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
	- Comparing basic facts of homology and cohomology #card
		- Common features
			- Functoriality
				- ((64b48496-7607-4075-8451-d120e228dafc))
				- ((65323c6e-8ef2-4c74-bdc2-84d19146566e))
			- Dimension axiom
				- ((6454f1b7-5d36-4a76-b56c-aa3dc7b2515d))
				- ((65324131-a2a4-47ba-b58b-6b4585d3cf8f))
			- Homotopy axiom
				- ((6532434c-4b75-4d01-8f70-dbe2ff7f036d))
				- ((6498e102-758e-44db-bbcb-a7c679b43a90))
		- Differences
			-
	- ((6532394c-e8b9-4752-9500-74081018a669)). If $\left(S_*(X), \partial\right)$ is a complex, then, for every abelian group $G$,
	  collapsed:: true
	  $$
	  0 \longrightarrow \operatorname{Hom}\left(S_0(X), G\right) \stackrel{\partial_1^*}{\longrightarrow} \operatorname{Hom}\left(S_1(X), G\right) \stackrel{\partial_2^*}{\longrightarrow} \operatorname{Hom}\left(S_2(X), G\right) \longrightarrow \cdots
	  $$
	  is a complex (denoted by $\operatorname{Hom}\left(S_*(X), G\right)$). #card
		- The lemma is extremely simple technically, but what's the insight behind?
		  background-color:: red
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
	- ((65324366-e806-4d87-a9bf-65ac108b78fb)) (Homotopy Axiom). If $f, g: X \rightarrow Y$ are homotopic, then they induce the same homomorphisms $H^n(Y ; G) \rightarrow H^n(X ; G)$ for all $n \geq 0$.
	  id:: 6532434c-4b75-4d01-8f70-dbe2ff7f036d