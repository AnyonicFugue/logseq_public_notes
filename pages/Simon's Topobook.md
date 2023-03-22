type:: paper_reading

- ![Simon_Topological Quantum.pdf](file://zotero_link/Physics/Topological order/Intros and Reviews/Simon_Topological Quantum.pdf)
-
-
- # ((63c2176e-689e-4871-9dcb-d820669e68ac))
  collapsed:: true
	- ### ((63c21788-4217-4cb3-8a20-099a3cfa23ba)) ; Diagrams and Physical Quantities #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-04-15T03:18:31.963Z
	  card-last-reviewed:: 2023-03-22T03:18:31.964Z
	  card-last-score:: 5
		- Define toric code by local dancing rules (similar to 2017_Wen)
			- Isotopy, adding/removing contractable loops, reconnection
		- Strange operation: Detect the total charge of a disk of [[Toric Code]] by an annulus surrounding it
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
- # ((63c356c2-2dfd-480e-a0a4-49e6db63d25f))
	- Quantum Double
	- [[Double Semion Model]]
		-
- # ((63f5d393-9003-4c31-b6de-5dc05564fdec))
- # ((63f5d3a0-24c4-49f6-bbd6-905c87ee21f8))
- # ((63f2cf5d-e5e1-423f-9ad7-90214e40392f))
- # ((63f6d9c3-7d19-4d5c-9c5c-3ac52297b388))
  collapsed:: true
	- ## Relation to [[Anyon Condensation]]
		- ((63f6db13-324a-405f-a76a-0110f0aacaa6)).
		- ((63f6db1b-ee95-4073-a8f5-374de40ae98b))
	- ## Examples
		- Toric code: Exchange $e$ and $m$
			- Could be obtained by condensing $\text{Ising} \times \overline{\text{Ising}}$
			- Duality mapping
				- Map to the dual lattice to exchange $e$ and $m$
			- Equalizing mapping
			  collapsed:: true
				- ((63f6dc5b-cb2c-4479-b282-9adf540020c9))
				- A further transformation is needed: apply $\sigma_y$ on the east and west corners of the green diamonds, 
				  $$
				  \begin{aligned}
				  \sigma_x & \rightarrow \sigma_z \\
				  \sigma_z & \rightarrow \sigma_x \\
				  \sigma_y & \rightarrow \sigma_y
				  \end{aligned}
				  $$
				- **Plaquette and vertex operators are identified in the new lattice!**
					- $$
					  H_{\text {toric code }}=-\frac{\Delta}{2} \sum_{\text {diamonds } q} \sigma_z^{q_N} \sigma_x^{q_E} \sigma_z^{q_S} \sigma_x^{q_W}
					  $$
					- N,E,S,W are the directions
				- However, one can only move on the pink plaquettes while the other can only move on the green plaquettes.
					- Like the chessboards.
			- Dislocation defect and the exchange domain wall
				- ((63f9a8bb-5e68-43a6-8cf2-c8686b577d49)) #[[Research/To Be Investigated]]
					- Each dislocation **traps** a [[Majorana Zero Mode]]!
					- TODO Also investigate the thing in terms of the dual diamond lattice.
						- Also Exercise 32.4.
					-
- # ((63f9a9a2-190e-4948-b6a5-faa1ad08eb83))
  collapsed:: true
	- Idea of [[Topological Entanglement Entropy]]
		- We would like to relate entanglement quantities to the boundary of two subsystems, which is kind of similar to [[Bulk-Boundary Relation]].
		- Moreover, we expect it to be somewhat topological in topo phases.
	- Example: [[TEE]] in [[Toric Code]] #card
	  collapsed:: true
		- ((63f9ab7a-5493-4741-8119-f9751148f6a8))
			- The correlation, corresponding to the blue strings, are generally nonlocal and topological.
		- Now we calculate TEE of a certain **ground state**.
			- That is, we can fix a homotopy class.
			- Do so for excited states. [[Research/To Be Investigated]]
		- We need to decompose the ground state into $|\psi\rangle:=\sum c_i \cdot\left|\psi_{A i}\right\rangle \cdot|\alpha\rangle \cdot\left|\psi_{B i}\right\rangle$
			- The three terms corresponds to A, boundary and B.
			- In principle all configs in B have independent contributions to the reduced density matrix of A. But we may take $\psi_B$ to be a superposition state.
		- **Observations**
			- Allowed configurations inside a region is only dependent on the boundary config, not on the config of the other region.
			- Inside a region, each action of $B_p$ would create a new valid config (from the reference config). Moreover, they're all independent.
				- Therefore the weights of all boundary configs are equal!
			- Different boundary configs always generate independent configs in A and B.
		- Therefore, we only need to count the allowed boundary configs. They're all of equal weight.
			- We must have an even number of blue strings crossing the boundary.
			- $N=\sum_{k}C_{L}^{2k}$, where L is the length of the boundary.
			- By some combinatoric, we obtain $N=2^{L-1}$.
		- Thus,
		  $$S=(L-1)\ln 2$$
			- The constant term $-\ln2$ is related to the quantum dimension of TC.
			- It is worth noting that if region $A$ has two boundaries as in Fig. $33.4$ we will get instead
			  $$
			  \mathcal{S}_{A, B}=(M-2) \log 2
			  $$
				- In other words, each piece of boundary adds a constraint.
				- Could we investigate other topologically nontrivial boundaries? #Possibility
					- Moreover, we may investigate higher dimensional topo orders with higher dimensional boundaries.
					- Reminiscent of [[Homology]] :)
	- General case
		- The technique is still counting boundary states (see [topobook](((63fec44a-15d9-4e69-a1cd-e966b65798a7))) for reference)
		- The entropy would be 
		  $$
		  \mathcal{S}_{A, B}=\alpha L-\gamma+\ldots
		  $$
			- $\alpha$ is a constant.
			- $\gamma=\log \mathcal{D}$ is the so-called topo contribution.
	- ## Robustness
		- Would TEE still be topological with some perturbations to the Hamiltonian, or in different models?
		- A possible argument: Divide the surface into four regions to cancel the boundary terms. #card
			- *To be completed.*
			- ((63fec57c-f224-4f78-9201-a8d052e816e5))
			- $\begin{aligned} \mathcal{S}_{\text {top }}:= & \left(\mathcal{S}_{A, B C D}+\mathcal{S}_{B, A C D}+\mathcal{S}_{C, A B D}+\mathcal{S}_{D, A B C}\right) \\ & -\left(\mathcal{S}_{A B, C D}+\mathcal{S}_{A C, B D}+\mathcal{S}_{A D . B C}\right)\end{aligned}$
				- We are going to prove $\mathcal{S}_{t o p}=-\gamma$
			-
			- First we prove that S doesn't depend on the geometry of the boundary, i.e. we may freely deform it.
			- Then prove a local change in the Hamiltonian far from the boundary has no effect.
			- Finally, any local change in the Hamiltonian can be 'encircled' by deforming the boundary.
- # ((63fec6f9-50a7-4f7d-b378-5110f39f0bde))
	-
-