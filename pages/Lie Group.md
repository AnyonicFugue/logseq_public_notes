- Def
	- A group that is also a finite-dimensional smooth [[Manifold]], such that the multiplication and inversion are both smooth.
	- We may further require that the manifold is **closed**, which gives many good properties.
	- Matrix Lie group
		- ((6381bb48-3345-4b06-bbe2-aac3d6c38dde))
		- ((6381bb1b-bd7f-4e67-8380-1a111a50408c)). However, most Lie groups we consider do have this property.
		- A general Lie group might not be a matrix Lie group. But we hardly need to consider such exotic groups :p
	-
		-
- Basic Theory
	- Mainly Chapter 2 of Hall.
	- Defs
		- Identity component
		  id:: 6381bc92-5f90-4322-9a1b-0cbbf9128acc
			- The path component with the identity
		- Lie group homomorphism #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-02-08T01:09:09.988Z
		  card-last-reviewed:: 2023-01-15T01:09:09.988Z
		  card-last-score:: 5
		  id:: 6382c5bc-957b-4756-8adc-146cca7d1a16
			- ((6381bdc6-e0b4-4d4d-91e3-aeb15dce7e60))
			  To be an isomorphism, the inverse map must also be continuous.
			- All structures must correspond.
			-
	- Connectedness
	  collapsed:: true
		- In Lie groups, [[Connected]] is equivalent to [[Path Connected]]
		- The ((6381bc92-5f90-4322-9a1b-0cbbf9128acc)) is a normal subgroup. #card
			- A simple exercise. Directly construct the path.
		- $SU(2)$ is [[Simply connected]]. #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-03-05T11:20:00.269Z
		  card-last-reviewed:: 2023-02-09T11:20:00.269Z
		  card-last-score:: 5
			- We may construct a homeomorphism to $S^3$ by 
			  $$
			  A=\left(\begin{array}{cc}
			  \alpha & -\bar{\beta} \\
			  \beta & \bar{\alpha}
			  \end{array}\right)
			  $$
				- $\alpha$ and $\beta$ are arbitrary complex numbers satisfying $|\alpha|^2+|\beta|^2=1$
		- ((639330f5-2eca-4f75-93cf-3fd1f6f9fe12)) There is a continuous bijection between $\mathrm{SO}(3)$ and $\mathbb{R} P^3$, thus $SO(3)$ isn't simply connected. #card
		  card-last-score:: 5
		  card-repeats:: 3
		  card-next-schedule:: 2023-03-01T16:56:34.620Z
		  card-last-interval:: 67.2
		  card-ease-factor:: 2.8
		  card-last-reviewed:: 2022-12-24T12:56:34.621Z
			- Note that $\mathbb{R} P^3$ is obtained by identifying points in $\mathbb R^4$.
			- Intuition
				- A rotation always has a principle axis. Thus the topological structure of $SO(3)$ is analogous to a 'direction' and an 'angle'.
				- The latter is isomorphic to $S_1$.
	- [[Norms of Matrices]]
	  collapsed:: true
		- Hilbert–Schmidt norm, or Frobenius norm
			- $\|X\|=\left(\sum_{j, k=1}^n\left|X_{j k}\right|^2\right)^{1 / 2}$
			- See X as an $n^2$-dimensional vector.
			- Properties
				- $\left\|(A-I)^m\right\| \leq\|(A-I)\|^m$
	- [[Matrix Exponential]]
	- [[Matrix Logarithm]]
		- We hope to define something as an inverse of the matrix exponential.
		  However, a bit knowledge in [[Complex Analysis]] would show that it is impossible to have a global one.
	-
- Exapmles
	- General Linear Group, $GL(n,\mathbb C)$
	- Special Unitary Group
		- ((6381bed0-deb1-4cab-94d7-e1e4837c83e8))
		-
	-