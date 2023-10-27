# Definitions
	- ((653334b3-01a6-45cd-a0b6-48dd55b9c729)) $\operatorname{Ext}(A, G)$ #card
		- For each abelian group $A$, choose an exact sequence $0 \rightarrow R \stackrel{i}{\rightarrow} F \rightarrow$ $A \rightarrow 0$ with $F$ (and hence $R$ ) **free abelian**.
			- This is perfectly OK.
			  For example, $\mathbb Z$ and $\mathbb{nZ}$ are both free abelian, but $\mathbb Z/\mathbb{nZ}$ is the familiar $\mathbb Z_n$.
		- For any abelian group $G$, define
		  $$
		  \operatorname{Ext}(A, G)=\operatorname{coker} i^{\#}=\operatorname{Hom}(R, G) / i^{\#} \operatorname{Hom}(F, G) .
		  $$
	- Definition. An abelian group $G$ is **divisible** if, for every $x \in G$ and every integer $n>0$, there exists $y \in G$ with $n y=x$.
	-
	- Many properties can be found in a textbook for homological algebra.
		- [Ext 1]. If $0 \rightarrow A^{\prime} \rightarrow A \rightarrow A^{\prime \prime} \rightarrow 0$ is a short exact sequence, then there is an exact sequence
		  $$
		  0 \rightarrow \operatorname{Hom}\left(A^{\prime \prime}, G\right) \rightarrow \operatorname{Hom}(A, G) \rightarrow \operatorname{Hom}\left(A^{\prime}, G\right) \rightarrow \operatorname{Ext}\left(A^{\prime \prime}, G\right) \rightarrow \operatorname{Ext}(A, G) \rightarrow \operatorname{Ext}\left(A^{\prime}, G\right) \rightarrow 0 .
		  $$
		- [Ext 1']. If $0 \rightarrow G^{\prime} \rightarrow G \rightarrow G^{\prime \prime} \rightarrow 0$ is a short exact sequence, then there is an exact sequence
		  $$
		  0 \rightarrow \operatorname{Hom}\left(A, G^{\prime}\right) \rightarrow \operatorname{Hom}(A, G) \rightarrow \operatorname{Hom}\left(A, G^{\prime \prime}\right) \rightarrow \operatorname{Ext}\left(A, G^{\prime}\right) \rightarrow \operatorname{Ext}(A, G) \rightarrow \operatorname{Ext}\left(A, G^{\prime \prime}\right) \rightarrow 0 .
		  $$
		- [Ext 2]. If $F$ is free abelian, then
		  $$
		  \operatorname{Ext}(F, G)=0 .
		  $$
		- [Ext 2']. If $D$ is divisible, then
		  $$
		  \operatorname{Ext}(A, D)=0
		  $$
		- If $\left\{A_j: j \in J\right\}$ is a family of abelian groups, then $\prod A_j$ is the abelian group whose elements are all $J$-tuples $\left(a_j\right)$ under coordinatewise addition (thus, $\sum A_j$ is the subgroup of $\prod A_j$ consisting of all $J$-tuples with only finitely many nonzero coordinates). When the index set $J$ is finite, $\sum A_j=\prod A_j$.
		- [Ext 3]. $\operatorname{Ext}\left(\sum A_j, G\right) \cong \prod \operatorname{Ext}\left(A_j, G\right)$.
		- [Ext 3']. $\cdot \operatorname{Ext}\left(A, \prod G_j\right) \cong \prod \operatorname{Ext}\left(A, G_j\right)$.
		- [Ext 4]. $\operatorname{Ext}(\mathbf{Z} / m \mathbf{Z}, G) \cong G / m G$.
- # Homology
	-
- # Cohomology
	- Lemma. There is a natural map
	  collapsed:: true
	  $$
	  \left.\beta: H^n\left(\operatorname{Hom}\left(S_*, G\right)\right) \rightarrow \operatorname{Hom}\left(H_n\left(S_*\right), G\right)\right)
	  $$
	  defined by
	  $$
	  \beta: \operatorname{cls} \varphi \mapsto \varphi^{\prime},
	  $$
	  where $\varphi^{\prime}\left(z_n+B_n\right)=\varphi\left(z_n\right)$. #card
		- First, let $\varphi$ be an $n$-cocycle, that is, $\varphi \in \operatorname{Hom}\left(S_n, G\right)$ and $0=\delta(\varphi)=\varphi \partial_{n+1}$.
		- Now $\varphi: S_n \rightarrow G$ and $0=\varphi\left(\operatorname{im} \partial_{n+1}\right)=\varphi\left(B_n\right)$. Thus $\varphi$ induces a homomorphism $S_n / B_n \rightarrow G$, and hence a homomorphism $\varphi^{\prime}: H_n\left(S_*\right)=Z_n / B_n \rightarrow G$, namely, $z_n+B_n \mapsto \varphi\left(z_n\right)$.
		- Rephrased: cocycle -> maps boundary to zero (by a partial)
		-
		- Moreover, if $\varphi$ is an $n$-coboundary, that is, $\varphi=\delta(\psi)=\psi \partial$, then $\varphi$ induces the map $z_n+B_n \mapsto \varphi\left(z_n\right)=\psi \partial\left(z_n\right)=0$ (because $z_n$ is a cycle).
		- Rephrased: Difference by a coboundary doesn't matter, since it is zero when acting on a cycle.
		-
		-
	- ((65333d1e-b692-49f4-9105-5564cdb8989b)) (Universal Coefficients) 
	  (i) For every space $X$ and every abelian group $G$, there are exact sequences for all $n \geq 0$ :
	  $$
	  0 \rightarrow \operatorname{Ext}\left(H_{n-1}(X), G\right) \rightarrow H^n(X ; G) \stackrel{\beta}{\rightarrow} \operatorname{Hom}\left(H_n(X), G\right) \rightarrow 0,
	  $$
	  where $\beta$ is the map defined above.
	  (ii) This sequence **splits**; that is, there are isomorphisms for all $n \geq 0$,
	  $$
	  H^n(X ; G) \cong \operatorname{Hom}\left(H_n(X), G\right) \oplus \operatorname{Ext}\left(H_{n-1}(X), G\right)
	  $$ #card
		- Note that splitting is nontrivial.
		  For example, we have an exact sequence
		  $$0 \rightarrow \mathbb Z \rightarrow \mathbb Z \rightarrow \mathbb Z_n \rightarrow 0$$
		  which doesn't split.
		-
		- Intuition
			- First note that $\beta$ is onto, since any element in $\operatorname{Hom}\left(H_n(X), G\right)$ naturally gives rise to an element of $H^n \left(X, G\right)$.
			- However, there is still **redundancy** because we $\operatorname{Hom}\left(S_n(X), G\right)$ contains information about all of $S_n(X)$, but $\operatorname{Hom}\left(H_n(X), G\right)$ only contains information about $Z_n(X)$.
			- Therefore the redundancy is approximately captured by 
			  $$\operatorname{Hom}\left(S_n(X)/Z_n(X), G\right) \simeq \operatorname{Hom}\left(S_n(X), G\right)/ \operatorname{Hom}\left(Z_n(X), G\right)$$
			  Note that $S_n(X)$ is freely generated.
		-
		- The full proof should be completed.