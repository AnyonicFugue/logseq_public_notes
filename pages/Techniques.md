- # Math
	- ## Integration
	  collapsed:: true
		- [[Feynman parameter]] #Techniques
		  collapsed:: true
		- Exploit Branch Points
			- See [Arfken](((642d0ff2-1702-4be7-9a72-66e3a2f944c0)))
			- Example. $I=\int_0^{\infty} \frac{x^p d x}{x^2+1}, \quad 0<p<1$ #card
			  card-last-interval:: 32.52
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-06-03T23:26:28.235Z
			  card-last-reviewed:: 2023-05-02T11:26:28.236Z
			  card-last-score:: 5
				- Key idea: Regard an integration as 'the extra path in order to avoid encircling the branch point'.
				- Construct a contour without encircling the branch point:
				  ((642d1074-41db-4833-8ff3-a02f25f99b71))
				- The contributions on the two arcs both vanish.
				- $A=I,B=e^{i 2p\pi}$, the total value is the sum of two residues.
				  $$
				  \left(1-e^{2 p \pi i}\right) I=(2 \pi i) \frac{1}{2 i}\left(e^{p \pi i / 2}-e^{3 p \pi i / 2}\right)
				  $$
				-
	- ## Linear Algebra
		- Select a maximal linear independent set
		  id:: 64c66f21-d71f-4cf2-a4d8-44d974454f65
			- The elements could be vectors, operators, subspaces, etc.