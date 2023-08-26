alias:: Wilson Line

- It is first introduced in the context of gauge theories, but it seems ubiquitous later...
- # Def
	- Wilson Line #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-25T18:57:07.561Z
	  card-last-reviewed:: 2023-08-25T12:57:07.561Z
	  card-last-score:: 5
		- $$
		  U_P(z, y)=P\left\{\exp \left[i g \int {d x^\mu} A_\mu^a t^a\right]\right\}
		  $$
			- Rephrased: The holonomy of the gauge connection
			- Exercise. Show that it indeed transforms as $U_P\left(z, y, A^V\right)=V(z) U_P(z, y, A) V^{\dagger}(y)$, where $A^V$ is the field after gauge transformation. #card
			  card-last-interval:: 30
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-06-16T01:16:14.128Z
			  card-last-reviewed:: 2023-05-17T01:16:14.131Z
			  card-last-score:: 5
				- Hint: ((640ad127-cc23-464b-b796-fb5a07f8049a))
				-
		- Wilson loop
		  card-last-interval:: 27.15
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-04-16T04:28:29.777Z
		  card-last-reviewed:: 2023-03-20T01:28:29.778Z
		  card-last-score:: 5
			- In the nonabelian case, $U(x,x)$ is not gauge-invariant.
			  So we define $\operatorname{tr} U_P(x, x)$ as the **Wilson loop**.
- # Properties
	- Transformation rule
		- ((64b4848f-9d1a-44f4-a9c4-9187e12d1c27))
- Notes
	- $P$ is the path-ordering operator. It is introduced since different generators might be non-commutative.
		- Later matrices (greater values of the parameter) is on the left side.
	- The quantity is path-dependent (due to the prescence of curvature)
	- If $x=y$ it is called a Wilson loop in the abelian case.
		- Use [[Stokes Theorem]], 
		  $$
		  U_P(y, y):=\exp \left[-i e \oint_P d x^\mu A_\mu(x)\right]=\exp \left[-i \frac{e}{2} \int_{\Sigma} d \sigma^{\mu \nu} F_{\mu \nu}\right]
		  $$
			- That is, the total amount of holonomy is equal to the flux on the surface.
	-