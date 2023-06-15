- # Setup
	- The underlying lattice is Kitaev's honeycomb.
		- The XX, YY and ZZ operators on the edges are called **check operators**.
	- As a quantum error correcting code, the **stabilizers** are the **plaquette operators** and the **logical operators** are nontrivial loops around the torus.
		- A plaquette operator is the product of six check operators around a plaquette.
		- A logical operator is the product of all check operators along a nontrivial loop.
		- ![Image(1).png](../assets/Image(1)_1686812529964_0.png){:height 256, :width 267}
		  As shown in the picture.
- # Method of Performing Measurement
	- We measure the checks in distinct rounds, measuring first all checks labeled by 0, then by 1, then by 2, repeating, so that in the $r$-th round we measure checks labeled by $r \bmod 3$.
	- Labelling of the egdes
	  collapsed:: true
		- First, color the plaquettes by 3 colors 0,1,2.
		- Label the edges by 0,1,2 by the rules that every edge with label $a$ connects two nearest plaquettes with label $a$.
			- ![20230605-092310.jpg](../assets/20230605-092310_1685928302341_0.jpg){:height 424, :width 404}
			- Orange edges are 0, blue edges are 1, purple edges are 2/
- # Important facts
	- Product of checks on a loop commute with any single check.
		- Therefore, both plaquette operators and logical operators commute with checks, which means the eigenvalues don't change during measurements or under the action of check operators.
	- Each single-site Pauli error flips the eigenvalues of two adjacent plaquette operators, depending on the type of the error.
		- For example, an Pauli-X error on the cite with a red circle flips the plaquettes marked with 1 and 2, i.e. the plaquettes sharing the X-edge.
		  ![Image(1).png](../assets/Image(1)_1686813149586_0.png){:height 342, :width 326}
- # Error Detection and Correction
	- First, map the lattice to the triangular dual lattice.
	  Each error could be represented by a red edge, which flips the two adjacent vertices (corresponding to plaquettes in the original lattice)
	- ![Image(1).png](../assets/Image(1)_1686813331528_0.png){:height 269, :width 209}
	- Proposition. Errors of trivial loops (in the dual lattice) could not be detected, but they don't affect the logical qubit (as they commute with the logical operator).
		- It's manifest they cannot be detected.
		- To prove they don't affect logical qubit, note that trivial loops in the dual lattice must be products of check operators in the original lattice.
			- Check operators commute with the logical operator.
	- Therefore, any error could be determined by the plaquette stabilizers (up to products of checks) and corrected.