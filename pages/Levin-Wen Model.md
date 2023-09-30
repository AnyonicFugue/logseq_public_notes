- Seems to be directly motivated from planar algebras?
- # Mathematical Descriptions
	- Input: a spherical tensor category $C$
		- ((63e84dee-bee0-4b90-aace-679bc17deab5))
			- This is the case for the [[Double Semion Model]], but not for [[Toric Code]].
				- Semions correspond to the fermonic braiding of $Z_2$, thus modular.
				- However, diagrammatic rules of TC have bosonic braidings, where the nontrivial particle is **transparent**, thus not modular.
			-
		- ((63e84ee7-70c8-46ae-843c-8a87f2643564))
	- Output: a topo order corresponding to the Drinfeld center $\mathfrak Z_1(C)$
- # Setup #card
  collapsed:: true
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-07-07T07:39:27.059Z
  card-last-reviewed:: 2023-06-06T01:39:27.059Z
  card-last-score:: 3
	- ## Fat Lattice
		- Trivalent, with a direction on each edge
			- Why does the lattice need to be trivalent? #Learning-TODO
				- Fusion multiplicity is also defined for multiple particles fusion together
		- Each edge is labeled by a simple object of the input tensor category
			- Reversing the direction of an edge changes the particle to its dual
				- ((63e85270-994b-4bc9-b5b0-621fe43c45f2))
		- In the middle of each plaquette there is a $\times$, which indicates we cannot contract loops on the plaquettes.
	- ## Hamiltonian
		- $$H=-\sum_v A_v-\sum_p B_p$$
		- Vertex operators enforce the fusion rules, i.e. $A_v=1$ iff $\left(N_{a b c}=N_{a b}^{\bar{c}}>0\right)$
		- Plaquette operators add $\tilde \Omega$ loops on the plaquette
			- ((63e85457-40a3-4f6a-9c79-3cdee0efc747))
				- The precise definition is as follows:
					- ((63f1dc64-debc-421e-b334-2cfc0e75207c))
						- ((63f1ddd2-9f0d-4e7e-a23b-94ab139e161f)) #card
						  card-last-interval:: 31.26
						  card-repeats:: 1
						  card-ease-factor:: 2.36
						  card-next-schedule:: 2023-07-22T07:28:14.669Z
						  card-last-reviewed:: 2023-06-21T01:28:14.670Z
						  card-last-score:: 3
							- Note that ((63f1ddff-4d6d-4e9c-8703-eeac52e3bfb5)), incoming particle as positive
					- Sum over all possible fusion channels.
				- ((63e85493-7abb-4406-95d9-6059dbada06e))
		- Proposition. $A_v^2=A_v,B_p^2=B_p, [A_v,B_p]=0$ #card
		  card-last-interval:: 42
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2023-09-13T12:51:20.461Z
		  card-last-reviewed:: 2023-08-02T12:51:20.461Z
		  card-last-score:: 3
			- (1) is obvious.
			- (2) Let's prove the handle-slide property by explicitly writing the loop and using F-move (on the vacuum): ((63f1dfaa-c3ef-4c6a-8cac-1c5a9aafbdc8))
			- (3): Note that adding a loop keeps the fusion rule.
- # Solution
	- ## Ground states
	  collapsed:: true
		- Note that we may freely use diagrammatic rules and contract loops in ground states. #card
		  collapsed:: true
		  card-last-interval:: 117.6
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-12-11T02:52:45.874Z
		  card-last-reviewed:: 2023-08-15T12:52:45.874Z
		  card-last-score:: 5
			- Ground states are eigen to $B_p$. So we can first add a $\tilde \Omega$ by $B_p$, use the handle-slide property to move across the puncture, then remove the $\tilde \Omega$.
		- Prop. The ground space is topological. #card
		  card-last-interval:: 42
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2023-09-22T12:55:36.000Z
		  card-last-reviewed:: 2023-08-11T12:55:36.001Z
		  card-last-score:: 3
			- ((63fa1061-a719-42a4-8b01-2bd603e394fc))
			- ((63f1e575-e066-4e22-9614-a8f2a6fd2ab6))
				- Note that not only the quantum numbers are changed, but also the underlying lattice structure.
			- ((63f1e581-4ebb-4a66-85a3-0af2aa11c759))
				- Solve this as an exercise!
			- Use the moves to transform a square to a triangle as an exercise!
				- Simple exercise: ![Image(1).png](../assets/Image(1)_1676798114616_0.png)
				- Hard exercise: Try to add more plaquettes to a torus.
					- But here comes a question: How to define the discrete version of torus? #Learning-TODO
						- It should actually be a [[Triangulation]], involving simplices
		- The ground space is nondegenerate on a sphere. #card
		  card-last-interval:: 42
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2023-09-13T12:45:56.777Z
		  card-last-reviewed:: 2023-08-02T12:45:56.777Z
		  card-last-score:: 3
			- Prove this by investigating a minimal lattice!
	- ## Quasiparticles
		- General constructions of quasiparticles can be difficult, but easier for a braided input category.
	- String operators can be found in [topobook](((63f2ce3a-202d-4bb4-8c39-a923cda51c6e))).
- # Examples
  collapsed:: true
	- ## ((63f2cb2c-5abf-4881-bac9-403813ff05dd))
		- Diagrammatic rules
			- ((63f2cc10-b805-49a9-8d6d-370366dd60ad))
				- As an exercise, determine the GSD on a torus. #card
				  card-last-interval:: 32.57
				  card-repeats:: 1
				  card-ease-factor:: 2.6
				  card-next-schedule:: 2023-09-13T01:51:34.040Z
				  card-last-reviewed:: 2023-08-11T12:51:34.041Z
				  card-last-score:: 5
					- The answer is four. The theory is indeed doubled.
				- As another exercise, find out the S-matrix. #card
				  card-last-interval:: 31.2
				  card-repeats:: 1
				  card-ease-factor:: 2.6
				  card-next-schedule:: 2023-10-29T04:48:06.241Z
				  card-last-reviewed:: 2023-09-28T00:48:06.241Z
				  card-last-score:: 5
					- $$
					  S=\frac{1}{\mathcal{D}}\left(\begin{array}{ll}
					  1 & \phi \\
					  \phi & y
					  \end{array}\right)
					  $$
					- Solve by F-move and R-move. Not so hard.
					- Don't forget the prefactor for a unitary S-matrix!
			- The first two are F-move.
			- The third is the quantum dimension. The last is the so called 'quantum dimension'.
		- The twists and braidings can be obtained by diagrammatic rules.
- # Topics
	- ## Relations to Math Axioms
		- ((63d1e7c7-5e46-4a7e-a93a-80eea0451f8c)) #card #[[Research/To Be Investigated]]
		  card-last-interval:: 30
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2023-05-12T11:35:45.237Z
		  card-last-reviewed:: 2023-04-12T11:35:45.238Z
		  card-last-score:: 3
			- Very interesting. Obtain categories from physical requirements!
		- ((63d1e83a-5d36-44b8-93b5-e746f7860e6c)) #[[Research/To Be Investigated]]
		-
	- ## Boundary
		- ((63d1e82c-08cb-4054-a1be-0e6a97026652))
		  id:: 63d1e825-ac40-4e31-b268-0241a194b40f
	-
- # Comments