- # Math
	- ## Integration
		- [[Feynman parameter]] #Trick
		  collapsed:: true
			- ((63e38a70-4b41-476b-b989-2419e008da6d))
			- Idea: {{cloze Introduce auxiliary parameters to simplify the expression, then change the order of integration.}}
				- The trick is usually followed by changing the order of integrations and shifting integration variables (To complete the square).
				- So there's the inherent problem: Can we really exchange the order of integration? #Thoughts
				  collapsed:: true
					- Similar problems abound. For example, lots of things don't converge absolutely.
			- $$
			  \frac{1}{A B}=\int_0^1 d x \frac{1}{[x A+(1-x) B]^2}=\int_0^1 d x d y \delta(x+y-1) \frac{1}{[x A+y B]^2}
			  $$
			- card-last-score:: 5
			  card-repeats:: 4
			  card-next-schedule:: 2023-09-08T03:36:46.375Z
			  card-last-interval:: 188.16
			  card-ease-factor:: 2.8
			  card-last-reviewed:: 2023-03-04T00:36:46.376Z
			  $$
			  \frac{1}{A B^n}=\int_0^1 d x d y \delta(x+y-1) \frac{n y^{n-1}}{[x A+y B]^{n+1}}
			  $$
			   #card
				- Proof. Differentiate the first identity wrt B
			- card-last-score:: 5
			  card-repeats:: 3
			  card-next-schedule:: 2023-03-11T22:55:33.729Z
			  card-last-interval:: 61.44
			  card-ease-factor:: 2.56
			  card-last-reviewed:: 2023-01-09T12:55:33.730Z
			  $$
			  \frac{1}{A_1 A_2 \cdots A_n}=\int_0^1 d x_1 \cdots d x_n \delta\left(\sum x_i-1\right) \frac{(n-1) !}{\left[x_1 A_1+x_2 A_2+\cdots x_n A_n\right]^n}
			  $$
			  #card
				- Core: It turns an awkward product into a summation.
				- The proof is to be completed.
		- Exploit Branch Points
			- See [Arfken](((642d0ff2-1702-4be7-9a72-66e3a2f944c0)))
			- Example. $I=\int_0^{\infty} \frac{x^p d x}{x^2+1}, \quad 0<p<1$ #card
				- Construct a contour without encircling the branch point:
				  ((642d1074-41db-4833-8ff3-a02f25f99b71))
				- The contributions on the two arcs both vanish.
				- $A=I,B=e^{i 2p\pi}$, the total value is the sum of two residues.
				  $$
				  \left(1-e^{2 p \pi i}\right) I=(2 \pi i) \frac{1}{2 i}\left(e^{p \pi i / 2}-e^{3 p \pi i / 2}\right)
				  $$
				-