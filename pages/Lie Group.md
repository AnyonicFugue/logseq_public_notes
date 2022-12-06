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
		  id:: 6382c5bc-957b-4756-8adc-146cca7d1a16
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-12-13T07:02:48.388Z
		  card-last-reviewed:: 2022-12-03T07:02:48.388Z
		  card-last-score:: 5
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
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-12-13T07:05:18.224Z
		  card-last-reviewed:: 2022-12-03T07:05:18.224Z
		  card-last-score:: 5
			- We may construct a homeomorphism to $S^3$
		- ((639330f5-2eca-4f75-93cf-3fd1f6f9fe12)) There is a continuous bijection between $\mathrm{SO}(3)$ and $\mathbb{R} P^3$, thus $SO(3)$ isn't simply connected. #card
		  card-last-score:: 5
		  card-repeats:: 2
		  card-next-schedule:: 2022-12-19T12:57:30.399Z
		  card-last-interval:: 10
		  card-ease-factor:: 2.7
		  card-last-reviewed:: 2022-12-09T12:57:30.400Z
			- Note that $\mathbb{R} P^3$ is obtained by identifying points in $\mathbb R^4$.
			- Intuition
				- A rotation always has a principle axis. Thus the topological structure of $SO(3)$ is analogous to a 'direction' and an 'angle'.
				- The latter is isomorphic to $S_1$.
	- [[Norms of Matrices]]
		- Hilbert–Schmidt norm, or Frobenius norm
			- $\|X\|=\left(\sum_{j, k=1}^n\left|X_{j k}\right|^2\right)^{1 / 2}$
			- See X as an $n^2$-dimensional vector.
			- Properties
				- $\left\|(A-I)^m\right\| \leq\|(A-I)\|^m$
	- [[Matrix Exponential]]
		- Def
			- $e^X=\sum_{m=0}^{\infty} \frac{X^m}{m !}$
			- It it convergent and continuous on all $X\in M_n(\mathbb C)$
		- Here is a useful decomposition of ((6381c0cf-5886-4962-856d-b14589f1bdbf)).
		- Notable properties #card
		  card-last-interval:: 10
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2022-12-16T07:48:02.114Z
		  card-last-reviewed:: 2022-12-06T07:48:02.114Z
		  card-last-score:: 5
			- $e^{C X C^{-1}}=C e^X C^{-1}$
			  id:: 6381c0a3-1e80-48b1-ba45-9844cd8aabd7
			- $e^{X+Y}=\lim _{m \rightarrow \infty}\left(e^{\frac{X}{m}} e^{\frac{Y}{m}}\right)^m$
			  id:: 6381ca36-6077-413b-8665-7fbbb620d7db
				- Provable by taking log of $e^{\frac{X}{m}} e^{\frac{Y}{m}}$
			- $\operatorname{det}\left(e^X\right)=e^{\operatorname{trace}(X)}$
			- Theorem (One-Parameter Subgroups). If $A(\cdot)$ is a one-parameter subgroup of $\mathrm{GL}(n ; \mathbb{C})$, there exists a unique $n \times n$ complex matrix $X$ such that
			  $$
			  A(t)=e^{t X} \text {. }
			  $$
				- Provable by PDE.
				- Intuitively, a 1-para group must be an integral curve of a constant vector.
			-
	- [[Matrix Logarithm]]
		- We hope to define something as an inverse of the matrix exponential.
		  However, a bit knowledge in [[Complex Analysis]] would show that it is impossible to have a global one.
		- Def #card
			- $\log A=\sum_{m=1}^{\infty}(-1)^{m+1} \frac{(A-I)^m}{m}$
			- The strategy is to define it near $I_n$, since we can't have it globally.\
			-
			- Theorem. It is defined and continuous on all matrices s.t. $\|A-I\|<1$
				- Use $\left\|(A-I)^m\right\| \leq\|(A-I)\|^m$.
				- We can slightly modify the condition in a variety of ways. The idea is always to avoid multiple values.
				-
	-
- Exapmles
	- General Linear Group, $GL(n,\mathbb C)$
	- Special Unitary Group
	  id:: 6381bfb5-10ab-4876-94a6-21f10a02b058
		- ((6381bed0-deb1-4cab-94d7-e1e4837c83e8))
		-
	-