- Definition
	- Simple object #card
		- Some nonzero $x \in C$ s.t. all ((641a6a23-ca6b-4d29-b1dc-28dab3b2fb6a)) of $x$ are 0 or isomorphisms.
		- What's the intuition behind?
			- 'Simple' means 'no nontrivial sub-thing'
		- In a semisimple category, this is equivalent to $\mathrm{Hom}_{\mathcal{C}}(x,x) \simeq \mathbb C$
	- Pre-semisimple category #card
		- A k-linear cat C, such that 
		  (1) Every object is a direct sum of simple objects
		  (2) $\forall x,y,z \in C$ simple, $\forall f: x \to y, g: y \to z$, $g \circ f \neq 0$
	- ((641a6c67-bd98-4266-bc5d-75ce90e2c7e0)) Semisimple category
		- (1) Finite direct sums always exists
		  (2) There exists a collection of mutually disjoint simple objects such that every object $x \in C$ is a finite direct sum of them.
		- In practice we may define a finite semisimple category as $$\operatorname{Vec}^{\oplus n}$$
		- Note that there are different definitions.
- # Properties
	- [[Schur's Lemma]] for pre-semisimple categories #card
	  id:: 641a6be7-3db1-44a5-be18-92070cdb5125
		- $\forall x,y$ simple, any nonzero Hom $f:x \to y$ is an isomorphism.
		- Proof
			- Note than with a linear structure, prove two things are 'same' <-> prove 0 is mapped to 0.
	- Corollaries of ((641a6be7-3db1-44a5-be18-92070cdb5125)) #card
		- Two simple objects are either isomorphic or disjoint.
		- For some simple $x$, $\mathrm{Hom}_{\mathcal{C}}(x,x)$ is a finite-dimensional division algebra, i.e. each nonzero element has an inverse.
			- Note that when it is C-linear, the division algebra has to be $\mathbb C$.
	- Maschke's Theorem. $\mathrm{Rep}(G)_\mathbb k$ is finite-semisimple iff $|G|$ is invertible in $\mathbb k$. #card
		-
	- Every finite semisimple category is ((636ca217-d22e-42b8-984f-f4f35d530948)). #card
		- The homs can be seen as block-diagonal matrices, because different copies of $$Vec$$ are disjoint.
		- So we need to consider a matrix A with $$A^2=A$$.
		  A familiar exercise in [[Linear Algebra]].
	-
- ((636dfb09-421f-4f06-9084-b2e4bb8af201))
	- In other words, the level of the category of ((636879d9-dfe3-4bdd-a078-587cc9c25350)) only depends on the dimension of the defects, not the dimension of the topo order.