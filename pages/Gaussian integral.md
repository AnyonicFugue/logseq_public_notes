- Formulae for Gaussian integrals of positive-definite biforms #card
  card-last-interval:: 117.6
  card-repeats:: 3
  card-ease-factor:: 2.8
  card-next-schedule:: 2023-12-03T03:02:27.651Z
  card-last-reviewed:: 2023-08-07T13:02:27.651Z
  card-last-score:: 5
	- $$\int_{R^N} d^{N} \vec{v} \cdot e^{-\frac{1}{2} v^{T} A v}=(2 \pi)^{\frac{N}{2}}(\operatorname{det} A)^{-\frac{1}{2}}$$
	- $$\int_{R^{N}} d^{N} \vec{v} e^{-\frac{1}{2} v^{T} A v+j^{T} v}=(2 \pi)^{\frac{N}{2}}(\operatorname{det} A)^{-\frac{1}{2}} e^{\frac{1}{2} j^{T} A^{-1} j}$$
		- Wick's theorem follows.
	-
	- Proof: Diagonalize A and everything else follows.
-
- [[Wick's Theorem]] for Gaussian integrals #card
  card-last-interval:: 353.22
  card-repeats:: 4
  card-ease-factor:: 2.9
  card-next-schedule:: 2024-06-06T06:10:17.261Z
  card-last-reviewed:: 2023-06-19T01:10:17.262Z
  card-last-score:: 5
	- $\left\langle v_{m} v_{n}\right\rangle=A_{m n}^{-1}$
	- $\left\langle v_{i_{1}} v_{i_{2}} \ldots v_{i_{2 n}}\right\rangle=\sum\limits_{\substack{\text { pairings of } \\\left\{i_{1}, \ldots, i_{2 n}\right\}}} A_{i_{k_{1}} i_{k_{2}}}^{-1} \ldots A_{i_{k_{2 n-1}}^{-1} i_{k_{2 n}}}$
	-
	- Proof: Apply derivatives to $j_m$.
	- This is a common but extremely interesting trick: Apply derivative to some "parameter" #Observations
	  id:: 63c14166-98ea-48ae-a115-b91b991489e8
-