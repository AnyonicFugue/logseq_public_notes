- Formulae for Gaussian integrals of positive-definite biforms #card
  card-last-interval:: 24
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2023-01-20T06:19:47.988Z
  card-last-reviewed:: 2022-12-27T06:19:47.988Z
  card-last-score:: 5
	- $\int_{R^N} d^{N} \vec{v} \cdot e^{-\frac{1}{2} v^{T} A v}=(2 \pi)^{\frac{N}{2}}(\operatorname{det} A)^{-\frac{1}{2}}$
	- $\int_{R^{N}} d^{N} \vec{v} e^{-\frac{1}{2} v^{T} A v+j^{T} v}=(2 \pi)^{\frac{N}{2}}(\operatorname{det} A)^{-\frac{1}{2}} e^{\frac{1}{2} j^{T} A^{-1} j}$
	-
	- Proof: Diagonalize A and everything else follows.
-
- [[Wick's Theorem]] for Gaussian integrals #card
  card-last-interval:: 67.2
  card-repeats:: 3
  card-ease-factor:: 2.8
  card-next-schedule:: 2023-04-28T16:02:04.732Z
  card-last-reviewed:: 2023-02-20T12:02:04.733Z
  card-last-score:: 5
	- $\left\langle v_{m} v_{n}\right\rangle=A_{m n}^{-1}$
	- $\left\langle v_{i_{1}} v_{i_{2}} \ldots v_{i_{2 n}}\right\rangle=\sum\limits_{\substack{\text { pairings of } \\\left\{i_{1}, \ldots, i_{2 n}\right\}}} A_{i_{k_{1}} i_{k_{2}}}^{-1} \ldots A_{i_{k_{2 n-1}}^{-1} i_{k_{2 n}}}$
	-
	- Proof: Apply derivatives to $j_m$.
	- This is a common but extremely interesting trick: Apply derivative to some "parameter" #Thoughts
	  id:: 63c14166-98ea-48ae-a115-b91b991489e8
-