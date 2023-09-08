# Definition
	- Simple object #card
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.46
	  card-next-schedule:: 2023-09-07T13:27:23.410Z
	  card-last-reviewed:: 2023-07-27T13:27:23.411Z
	  card-last-score:: 3
		- Some nonzero $x \in C$ s.t. all ((641a6a23-ca6b-4d29-b1dc-28dab3b2fb6a)) of $x$ are 0 or isomorphisms.
		- What's the intuition behind?
			- 'Simple' means 'no nontrivial sub-thing'
		- In a semisimple category, this is equivalent to $\mathrm{Hom}_{\mathcal{C}}(x,x) \simeq \mathbb C$
	- Pre-semisimple category #card
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.22
	  card-next-schedule:: 2023-10-07T12:55:55.602Z
	  card-last-reviewed:: 2023-08-26T12:55:55.602Z
	  card-last-score:: 3
		- A k-linear cat C, such that 
		  (1) Every object is a direct sum of simple objects
		  (2) $\forall x,y,z \in C$ simple, $\forall f: x \to y, g: y \to z$, $g \circ f \neq 0$
	- ((641a6c67-bd98-4266-bc5d-75ce90e2c7e0)) Semisimple category
		- (1) Finite direct sums always exists
		  (2) There exists a collection of mutually disjoint simple objects such that every object $x \in C$ is a finite direct sum of them.
		- In practice we may define a finite semisimple category as $$\operatorname{Vec}^{\oplus n}$$
		- Note that there are different definitions.
	-
		-
	-
- # Properties
  collapsed:: true
	- [[Schur's Lemma]] for pre-semisimple categories #card
	  id:: 641a6be7-3db1-44a5-be18-92070cdb5125
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-09-06T18:30:59.812Z
	  card-last-reviewed:: 2023-08-06T12:30:59.812Z
	  card-last-score:: 3
		- $\forall x,y$ simple, any nonzero Hom $f:x \to y$ is an isomorphism.
		- Proof
			- Note than with a linear structure, prove two things are 'same' <-> prove 0 is mapped to 0.
	- Corollaries of ((641a6be7-3db1-44a5-be18-92070cdb5125)) #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-07-22T07:28:29.120Z
	  card-last-reviewed:: 2023-06-21T01:28:29.120Z
	  card-last-score:: 3
		- Two simple objects are either isomorphic or disjoint.
		- For some simple $x$, $\mathrm{Hom}_{\mathcal{C}}(x,x)$ is a finite-dimensional division algebra, i.e. each nonzero element has an inverse.
			- Note that when it is C-linear, the division algebra has to be $\mathbb C$.
	- Maschke's Theorem. $\mathrm{Rep}(G)_\mathbb k$ is finite-semisimple iff $|G|$ is invertible in $\mathbb k$. #card
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-21T00:53:10.181Z
	  card-last-reviewed:: 2023-05-22T00:53:10.181Z
	  card-last-score:: 5
		-
	- Every finite semisimple category is ((636ca217-d22e-42b8-984f-f4f35d530948)).
		- The homs can be seen as block-diagonal matrices, because different copies of $$Vec$$ are disjoint.
		- So we need to consider a matrix A with $$A^2=A$$.
		  A familiar exercise in [[Linear Algebra]].
- # Modules
	- Convention. A module category $M$ over a multi-fusion cat $C$ is assumed to be linear, and $\odot: C \otimes M \to M$ is bilinear.
	- Defs
		- Cat of left modules over $A$ in $C$, $\mathrm{LMod}_A(C)$  #card
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-06-22T00:35:23.928Z
		  card-last-reviewed:: 2023-05-23T00:35:23.929Z
		  card-last-score:: 5
			- *To be completed: See Etingof*
			- Objects are modules over $A$ in $C$
			- Morphisms are module homomorphisms
			-
			- Special case (Set version): Cat of left modules over $A$, $\mathrm{LMod}_A(\mathrm{Vec})$
				- Objects are left $A$-modules, i.e. $A$ acting on vector spaces
				- Morphisms are module homomorphisms
				- Special case: $A$ is a division algebra, while $\mathrm{Vec}$ is a vector space over $A$
				  collapsed:: true
					- Theorem. Any finite semisimple $A$-linear category $C$ is equivalent to $\sum_{j=1}^n \mathrm{LMod}_{D_j}(\mathrm{Vec})$, where $D_j$ is the division algebra of $\mathrm{Hom}_{\mathcal{C}}(x_j,x_j)$ #card
					  card-last-interval:: 31.26
					  card-repeats:: 1
					  card-ease-factor:: 2.36
					  card-next-schedule:: 2023-08-25T08:03:39.589Z
					  card-last-reviewed:: 2023-07-25T02:03:39.590Z
					  card-last-score:: 3
						- We know clearly what $C$ is: there are $n$ simple objects. Any object are direct sums of the simple objects and the homs are block-diagonalized (only nonzero between the same $x_j$)
					- What is $\mathrm{LMod}_{D_j}(\mathrm{Vec})$? #card
					  card-last-interval:: 24
					  card-repeats:: 1
					  card-ease-factor:: 2.6
					  card-next-schedule:: 2023-04-21T00:44:32.463Z
					  card-last-reviewed:: 2023-03-28T00:44:32.464Z
					  card-last-score:: 5
						- The action on a one-dimensional VS is equivalent to a number in $D$, which means 'multiplying by the scalar'
						- Special case: $\mathrm{LMod}_\mathbb C(\mathrm{Vec}_\mathbb C )$
							- It is a representation of $\mathbb C$.
							- By Schur's lemma, each element is a multiple of the identity in an irrep.
								- Then it is an automorphism of $\mathbb C$, which must be trivial.
									- Note that it is different from the case of Galois theory, where complex conjugation is allowed; the automorphism should be linear!
							- Thus a general representation must also be trivial.
							- In conclusion, the category is just $\mathrm{Vec}_\mathbb C$
						- Special case: $\mathrm{LMod}_R(\mathrm{Vec}_R )$
							-
						- Special case: $\mathrm{LMod}_k(\mathrm{Vec}_k )$ for some field $k$
							-
						- General case
							-
		- Bimodules #card
			-
		- Semisimple object #card
		  card-last-interval:: 42
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2023-09-12T13:08:31.465Z
		  card-last-reviewed:: 2023-08-01T13:08:31.465Z
		  card-last-score:: 3
			- For $C$ multi-fusion, $A \in C$ is semisimple if $\mathrm{RMod}_A(C)$ is semisimple.
		-
	- Theorem. (Ostrik 03) For $C$ a multi-fusion cat, $M$ finite-semisimple $C$-module.
	  Then there exists $A \in C$ s.t. $M \simeq \mathrm{RMod}_A(C)$ as $C$-modules.
		- #+BEGIN_TIP
		  This also gives insights in topo orders, i.e. we can consider a boundary as **an algebra in the original cat**.
		  #+END_TIP
		- Observation. We can define an equivalence relation on $\mathrm{Irr}(M)$ by $x_i \sim x_j$ if $\exist a \in C, f: a \odot x_i \to x_j$ nonzero
			- Intuitively, act all of $a \in C$ on $x$ repeatedly. All intermediate fusion channels are in the same equivalence class.
			- Exercise. This is indeed an equivalence relation.
		- In this way we can partition $M = \oplus M_\lambda$ (indecomposable equivalence classes)
		- Now we assume $M$ is indecomposable.
			- The decomposable case directly follows.
		- The right adjoint of $C \overset{- \odot x}{\to} M$ is denoted $[x,-]: M \to C$ ('internal hom')
		- We can define a functor $C \to C$ by $T=[x,- \odot x]\simeq - \otimes [x,x]$ by rigidity.
		  We just need to show $M \overset{\exist!}{\to} \mathrm{LMod}_T(C)=\mathrm{RMod}_{[x,x]}(C)$
- ((636dfb09-421f-4f06-9084-b2e4bb8af201))
	- In other words, the level of the category of ((636879d9-dfe3-4bdd-a078-587cc9c25350)) only depends on the dimension of the defects, not the dimension of the topo order.