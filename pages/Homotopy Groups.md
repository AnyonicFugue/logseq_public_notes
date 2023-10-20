# Function Spaces
	- ((6531eaa7-129c-4bda-8096-c89268ebfe25)) Compact-open topology on function spaces #card
		- Let $X^Y$ denote the set of all continuous functions from $Y$ into $X$. The **compact-open topology** on $X^Y$ is the topology having a sub-basis consisting of all subsets $(K ; U)$, when $K$ is a compact subset of $Y, U$ is an open subset of $X$, and
		  $$
		  (K ; U)=\left\{f \in X^Y: f(K) \subset U\right\} .
		  $$
		- A typical open set in $X^Y$ is thus an arbitrary union of finite intersections of sets of the form $(K ; U)$.
		- Intuitively, functions in $(K;U)$ are 'relatively close to each other' in the sense that their values in the domain $K$ are constrained by $U$.
			- e.g. we may take $X=Y=\mathbb R^n$, $K$ and $U$ smaller and smaller.
	- ((6531ec3b-839a-40e6-93ba-7a53d6b49878)) Associate of functions (# and b) #card
		- If $F: Z \times Y \rightarrow X$ is a function, then its **associate** is the function 
		  $$F^{\#}: Z \rightarrow \operatorname{Hom}(Y, X)$$ defined by $F^{\#}(z)=F(z,-)$
		- Conversely, if $G: Z \rightarrow \operatorname{Hom}(Y, X)$, define 
		  $$G^b: Z \times Y \rightarrow X$$ by $G^b(z, y)=G(z)(y)$.
		- Indeed $\#$ and $b$ is are inverse to each other.
	- Proposition. (Exponential law for sets)
	  $$
	  X^{Z \times Y}=\left(X^Y\right)^Z
	  $$
	- Definition. If $X$ and $Y$ are sets, then the **evaluation map** $e: \operatorname{Hom}(Y, X) \times Y \rightarrow X$ is defined by
	  $$
	  e(f, y)=f(y)
	  $$
	- ((6531f0a0-16c5-4449-b807-321e85e99601)). Let $X$ and $Z$ be topological spaces, let $Y$ be a locally compact Hausdorff space, and let $X^Y$ have the compact-open topology (as usual).
	  (i) The evaluation map $e: X^Y \times Y \rightarrow X$ is continuous.
	  (ii) A function $F: Z \times Y \rightarrow X$ is continuous if and only if its associate $F^{\#}: Z \rightarrow X^Y$ is continuous. #card
		- What's the role of locally compact Hausdorff?
		  background-color:: red
			-
		- (i)
			- What is $e^{-1}(O)$?
				- It is $\{f \times f^{-1}(O)\}$.
			- Recall: ((64b48499-780e-4928-a9d9-e6c5a4b395fe))
				-
			- Proposition.
			  $$e^{-1}(O)=\bigcup_K (K;O) \times \operatorname{Int}K$$
				- Consider any pair $(f,y)$ s.t. $f(y) \in O$. The question is that whether we can find some $K$ such that $f \in (K;O)$ and $y \in \operatorname{Int} K$.
				- The choice is clear: We need only find a $V(y) \in f^{-1}(O)$ as indicated in the above corollary.
		- (ii)
			- p -> q
				- Consider $(K;U) \in X^Y$. Is $(F^\#)^{-1}(K;U) \equiv \{z:F(z,k) \in U \quad \forall k\in K \}$ open in $Z$?
				- Yes. Use the tube lemma and restrict to $Z \times K$.
			- q -> p
				- It is easy to check that $F$ is the composite
				  $$
				  Z \times Y \stackrel{F^* \times 1}{\longrightarrow} X^Y \times Y \stackrel{e}{\longrightarrow} X
				  $$
				- Since $e$ is continuous, it follows that $F$ is continuous.
				-
			-
			-
			-
			-
	-