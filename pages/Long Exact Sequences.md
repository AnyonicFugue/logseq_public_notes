-
- ## Definitions
	- Chain complex #card
	  collapsed:: true
		- A (chain) complex $(S_*,\partial)$ is a sequence of **abelian** groups and homomorphisms
		  collapsed:: true
		  $$
		  \cdots \longrightarrow S_{n+1} \stackrel{\partial_{n+1}}{\longrightarrow} S_n \stackrel{\partial_n}{\longrightarrow} S_{n-1} \longrightarrow \cdots, \quad n \in \mathbf{Z},
		  $$
		  such that $\partial_n \partial_{n+1}=0$ for each $n \in \mathbf{Z}$.
			- The subscripts could be negative!
		- The homomorphism $\partial_n$ is called the **differentiation** of degree $n$, and $S_n$ is called the **term** of degree $n$.
		- $\operatorname{ker} \partial_n$ is called **the group of n-cycles** and is denoted by $Z_n\left(S_*, \partial\right)$; $\operatorname{im}\partial_{n+1}$ is called the group of **n-boundaries** and is denoted by $B_n\left(S_*, \partial\right)$. 
		  The $n$th **homology group** of this complex is
		  $$
		  H_n\left(S_*, \partial\right)=Z_n\left(S_*, \partial\right) / B_n\left(S_*, \partial\right)
		  $$
		- Note that a ((6454f1b7-f979-485a-aafb-fa39fd34e0af)) is a chain complex, with all negative terms being trivial.
		- #+BEGIN_CAUTION
		  It's as if the spirit of homology (of topological spaces) is extracted and released into a larger universe...
		  But why the spirit is a sequence of abelian groups? Not singular chains?
		  Furthermore, how to **observe** what is the spirit of a theory?
		  #+END_CAUTION
	- Exact sequence #card
	  collapsed:: true
		- Also called an 'acyclic complex'.
		- A sequence of two homomorphisms (of groups) $A \stackrel{f}{\rightarrow} B \stackrel{g}{\rightarrow} C$ is exact at $B$ if im $f=\operatorname{ker} g$. A sequence of abelian groups and homomorphisms
		  $$
		  \cdots \longrightarrow S_{n+1} \stackrel{\partial_{n+1}}{\longrightarrow} S_n \stackrel{\partial_n}{\longrightarrow} S_{n-1} \longrightarrow \cdots
		  $$
		  is exact if it is exact at each $S_n$, that is, im $\partial_{n+1}=\operatorname{ker} \partial_n$ for all $n \in \mathbf{Z}$.
		- Note that being an exact sequence is **stronger** than being a complex: equality (im = ker) implies inclusion (im $\subset \mathrm{ker}$ ).
		-
		- Example. Short exact sequence:
		  A short exact sequence is an exact sequence of the form
		  $$
		  0 \rightarrow A \stackrel{i}{\rightarrow} B \stackrel{p}{\rightarrow} C \rightarrow 0 .
		  $$
	- Chain map #card
	  collapsed:: true
		- Definition. If $\left(S_*^{\prime}, \partial^{\prime}\right)$ and $\left(S_*, \partial\right)$ are complexes, a chain map $f:\left(S_*^{\prime}, \partial^{\prime}\right) \rightarrow\left(S_*, \partial\right)$ is a sequence of homomorphisms $\left\{f_n: S_n^{\prime} \rightarrow S_n\right\}$ such that the following diagram commutes:
		  ((64716a6b-8c2a-4d82-b4e8-1f9067c8679d))
			- A typical definition of homomorphism.
				-
		- One calls $f_n$ the **term of degree n**.
	- Subcomplex #card
	  collapsed:: true
		- $\left(S_*^{\prime}, \partial^{\prime}\right)$ is a subcomplex of $\left(S_*, \partial\right)$ if each $S_n^{\prime}$ is a subgroup of $S_n$ and if each $\partial_n^{\prime}=\partial_n \mid S_n^{\prime}$.
		- Equivalently, a subcomplex is defined by a complex homomorphism where each $f_n$ is an inclusion (to the parent complex).
	- Quotient Complex #card
	  collapsed:: true
		- If $\left(S_*^{\prime}, \partial^{\prime}\right)$ is a subcomplex of $\left(S_*, \partial\right)$, then the quotient complex is the complex
		  $$
		  \cdots \longrightarrow S_n / S_n^{\prime} \stackrel{\bar{\partial}_n}{\longrightarrow} S_{n-1} / S_{n-1}^{\prime} \longrightarrow \cdots,
		  $$
		  where $\bar{\partial}_n: s_n+S_n^{\prime} \mapsto \partial_n\left(s_n\right)+S_{n-1}^{\prime}\left(\bar{\partial}_n\right.$ is well defined because $\left.\partial_n\left(S_n^{\prime}\right) \subset S_{n-1}^{\prime}\right)$.
	- Kernel and Image #card
	  collapsed:: true
		- If $f:\left(S_*, \partial\right) \rightarrow\left(S_*^{\prime \prime}, \partial^{\prime \prime}\right)$ is a chain map, then $\operatorname{ker}f$ is the subcomplex of $S_*$
		  $$
		  \cdots \longrightarrow \operatorname{ker} f_n \stackrel{\partial_n^{\prime}}{\longrightarrow} \operatorname{ker} f_{n-1} \longrightarrow \cdots,
		  $$
		  where $\partial_n^{\prime}$ is the restriction $\partial_n \mid_{\operatorname{ker} f_n}$
		- $\operatorname{Im}f$ is the subcomplex of $S_*^{\prime \prime}$
		  $$
		  \cdots \longrightarrow \operatorname{im} f_n \stackrel{\Delta_n^{\prime \prime}}{\longrightarrow} \operatorname{im} f_{n-1} \longrightarrow \cdots,
		  $$
		  where $\Delta_n^{\prime \prime}$ is the restriction $\partial_n^{\prime \prime}\mid_{\operatorname{im} f_n}$.
		- Exercise. Verify that these two maps are both well-defined.
	- Exactness of a sequence of complexes #card
		- A sequence of complexes and chain maps
		  $$
		  \cdots \longrightarrow A_*^{q+1} \stackrel{f^{q+1}}{\longrightarrow} A_*^q \stackrel{f^q}{\longrightarrow} A_*^{q-1} \longrightarrow \cdots
		  $$
		  is **exact** if im $f^{q+1}=\operatorname{ker} f^q$ for every $q$.
			- This very well illustrates the similarity between $\mathbf{Comp}$ and $\mathrm{Ab}$: Complexes (as well as abelian groups) could be terms of an exact sequence!
		- A short exact sequence of complexes is an exact sequence of the form
		  $$
		  0 \rightarrow S_*^{\prime} \stackrel{i}{\rightarrow} S_* \stackrel{p}{\rightarrow} S_*^{\prime \prime} \rightarrow 0,
		  $$
		  where 0 denotes the zero complex.
			- The full diagram is like
			  ((64716fbb-80b4-4986-931b-12380bae496f))
			- Note that a single column is a term (a complex) in the sequence of complexes!
- ## In the viewpoint of [[Category]]
	- The Category Comp #card
	  collapsed:: true
		- The objects are chain complexes
		- The Homs are chain homomorphisms.
			- Note that each $\mathrm{Hom}(S_{1*},S_{2*})$ is an abelian group.
		- > It is quite similar to the category $\mathbf{Ab}$, since we also have sub-objects, quotient, first isomorphism theorem, etc.
	- For each n, we have a functor 
	  collapsed:: true
	  $$H_n: \mathrm{Comp} \to \mathrm{Ab}$$
		- Theorem. For each $n \in \mathbf{Z}$, the functor $H_n: \mathbf{Comp} \rightarrow \mathbf{A b}$ is **additive**; that is, if $f, g \in \operatorname{Hom}\left(S_*^{\prime}, S_*\right)$, then $H_n(f+g)=H_n(f)+H_n(g)$. #card
			- An exercise to review the concepts.
	- We have a functor
	  $$S_*: \mathrm{Top} \to \mathrm{Comp}$$
	  mapping a topological space to the singular complex.
	  Then 'taking $H_n(X)$' is the composition of functors $H_n \circ S_*$.
	-
- ## Basic Facts
	- Theorem. A complex $\left(S_*, \partial\right)$ is an exact sequence if and only if $H_n\left(S_*, \partial\right)=0$ for every $n$. #card
		- Therefore, the homology groups measure 'how does a complex deviates from being exact'.
		- Thus an exact sequence is called an 'acyclic complex'.
	-
		-