type:: paper_reading

- ![Simon_Topological Quantum.pdf](file://zotero_link/Physics/Topological order/Intros and Reviews/Simon_Topological Quantum.pdf)
-
- # Main Points
	- ## ((63c2176e-689e-4871-9dcb-d820669e68ac))
	  collapsed:: true
		- ### ((63c21788-4217-4cb3-8a20-099a3cfa23ba)) ; Diagrams and Physical Quantities #card
			- Define toric code by local dancing rules (similar to 2017_Wen)
				- Isotopy, adding/removing contractable loops, reconnection
			- Strange operation: Detect the total charge of a disk of [[Toric code]] by an annulus surrounding it
				- #+BEGIN_NOTE
				  The name 'Tube' originated from its topology, which is the same as an annulus.
				  #+END_NOTE
				- **This is a bit mysterious... almost a bulk-boundary relation.**
				- Set the stage
					- We don't specify the details of the lattice.
					- We use the spin-up and spin-down basis and represent them by blue lines and nothing separately.
				- Idea
					- First, the presence of e charge can be detected by a nontrivial string
					- The presence of m charge can be detected by the phase difference between the trivial homotopy type on the annulus and the nontrivial loop
				- Details: Projectors
					- The subscripts denote the particle types.
					- ((63c24f08-74e0-47d7-8c28-bf0217916833))
					- ((63c24f10-c712-4262-860c-c34cdf9a69a1))
				- More properties
					- Annuli can be multiplied.
						- The annulus to be multiplied must both have or both not have strings connecting the boundaries.
						- The loops are multiplied mod 2.
					- We may define a [[Anyon Basis]] for the torus.
					  collapsed:: true
						- Two points of view
							- Obtain a certain element from the trivial element by running the anyon
							- Glue two boundaries of the annulus (and multiply the strings) to obtain a ground state.
								- The 'anyon' is the charge detected by the string configuration on the annulus.
					- Determine the [[Twist]] of the anyons
					  id:: 63c2532f-fd97-4a25-86ac-27fc600589ee
					  collapsed:: true
						- ((63c25463-4c00-47de-8b21-3c9b5f2740ef)) (Dehn twist)
						-
						- For I and e, a rotation for a whole round is certainly trivial.
						- For m and f, ((63c25382-8f46-4fd5-973a-ae5042a11520))
						- Thus $\theta_m=1, \theta_f=-1$
						- **There got to be something deeper inside.**
					- Determine the [[S-matrix]]
					  collapsed:: true
						- ((63c2552b-3d48-4a77-9891-ca7aca3817a7))
						- Making a basis transformation, we obtain our familiar S-matrix!
			- Generalization: Determine general braidings and fusions by a **double-punctured disk**
			  collapsed:: true
				- [[Braiding]]
					- ((63c25660-8f63-48ee-b221-4ecceea3314b))
						- $f \otimes f$
					- Then use the three moves to simplify the lower line
				- [[Fusion]]
					- Essentially merging the holes
					- ((63c25681-7b53-4c30-99c8-9af8bd2fda8a))
						- $e \otimes f$
			- **Also easily generalizable to other string-net models!**
				- There is an example of $Z_n$ on topobook
			- ((63c24f85-b229-4920-88cf-78b0207f7682))
				- There are two sets of solutions to the hexagons of the $Z_2$ planar algebra
	- ## ((63c356c2-2dfd-480e-a0a4-49e6db63d25f))
		- Quantum Double
		- Double semion
		- Levin-Wen