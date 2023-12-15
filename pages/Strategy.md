# What this page is used for
	- Make them into flashcards. Thus I'll have an arsenal when facing new problems.
		- Understanding the strategies of the previous masters is quite delightful.
	- Extract [[System/Math and Physics]].
- # General Strategies
	- Divide a big problem into subproblems. #card
	  collapsed:: true
		- Decompose a large space into a direct sum / path components / union of parts.
		  id:: 649b9c9e-6796-4991-9241-b012ae76ccee
	- Equivalent formulations, different viewpoints. #card
	  id:: 6393f445-3a3c-4366-a1d1-bbc1587873a0
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2024-01-14T06:59:55.023Z
	  card-last-reviewed:: 2023-12-14T00:59:55.024Z
	  card-last-score:: 3
	  collapsed:: true
		- Sometimes, one formulation would be significantly simpler than another.
		  id:: 63c1416f-3871-4985-9009-5731e43864e6
	- Embed the object under investigation into better spaces. #card
	  id:: 63c1416f-d51b-4487-865b-f9d3cf9b5918
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-12-17T06:40:09.836Z
	  card-last-reviewed:: 2023-11-16T00:40:09.837Z
	  card-last-score:: 5
		- Finiteness
		- Algebraic structure
			- Inverse
			- Algebraic completeness
			- Semisimplicity
		- Topological structure
			- Compactness
	- Attack from the reversed direction, i.e. find necessary/sufficient conditions.
	  id:: 654603c4-b600-4a67-9708-3275bdf5a61c
	- Simplify the problem by adding conditions.
	  id:: 64c66feb-f6e4-4adf-88cb-64ecf551e7e9
	  collapsed:: true
		- Linear independence, orthogonality, compactness, etc.
	- Dirty way: Install a basis/coordinate and verify things directly. #card
	  id:: 63860946-8380-45c7-b564-1c08f9e7cc70
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-05T19:07:05.446Z
	  card-last-reviewed:: 2023-08-05T13:07:05.446Z
	  card-last-score:: 5
		- Actually not so dirty, since $\mathbb R^n$ and $\mathbb C^n$ do have very good properties.
	- Simplify the representation into some canonical form. #card
	  card-last-score:: 5
	  card-repeats:: 2
	  card-next-schedule:: 2023-09-11T12:30:29.807Z
	  card-last-interval:: 42
	  card-ease-factor:: 2.7
	  card-last-reviewed:: 2023-07-31T12:30:29.808Z
	  id:: 64b4848e-7e80-4fe8-a1f1-319b6f009d6f
	- Compare to situations where the theorem/conjecture fails and observe which conditions are essential.
	  id:: 65425a62-2e8d-4e18-916f-712a4b35c506
	-
	- ## Classification Problems #card
	  card-last-interval:: 32.51
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-13T00:58:46.845Z
	  card-last-reviewed:: 2023-08-11T12:58:46.845Z
	  card-last-score:: 5
		- Find a characteristic. If it is different for two objects, then they must be different.
		  id:: 63c14160-28c9-4f15-82dc-977a38e0993b
		  collapsed:: true
			- The same for trace, determinant, cardinality and the [[Fundamental Group]].
			- Actually [simplifying the information](((64116664-78ea-458f-b45f-db085090d9cf))) to make things easier.
				- eg. First homology: Abelian groups are easier than general ones.
		- Study a weaker equivalence relation.
		  id:: 64d8228a-d665-487e-a919-bd1fd00e7825
		  collapsed:: true
			- Homeomorphism is too strong.
			- Homotopy is much easier to deal with.
	- ## Invariance Problems
		- Find an independent/invariant construction and prove the equivalence to that.
		  id:: 65459f47-ac98-40a4-a2ce-280815a295c1
			- Usually the manifestly invariant construction would be more intrinsic and natural.
		- Use a set of elementary moves. Prove invariance under each element of the set.
		  id:: 63fa1061-a719-42a4-8b01-2bd603e394fc
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-06-21T00:52:25.604Z
		  card-last-reviewed:: 2023-05-22T00:52:25.604Z
		  card-last-score:: 5
			- Quite interesting. So useful in classification and invariance (equivalence) problems.
		-
- # [[Algebraic Topology]]
	- Prove nulhomotopy by rescale the shape (in particular, curve) with a parameter $t\in [0,1]$
		- Especially useful for shapes embeddable into $R^n$
- # Physics
	- By analyzing the only possible quantities (allowed by symmetry, Lorentz invariance, etc.) and dependences, we can obtain some nontrivial relations.
	  id:: 63e86244-9e83-4bd6-bf03-aa29c6f1ee0e
	- ## Solve a Model
		- Observe conserved quantities (i.e. operators commuting with the Hamiltonian) to divide the space into sectors.
		  id:: 64b2f633-ff39-4862-92e9-a8827906ea71
	- Introduce a set of operators satisfying some nontrivial relations.
	  id:: 64b4a3a2-5a8e-4828-8059-2d5fdb0ec212
		- e.g. Fermionic operators satisfying anti-commutation relations in Kitaev honeycomb.