- The Lemma. #card
  card-last-score:: 5
  card-repeats:: 4
  card-next-schedule:: 2024-08-11T17:56:32.795Z
  card-last-interval:: 353.22
  card-ease-factor:: 2.9
  card-last-reviewed:: 2023-08-24T12:56:32.796Z
	- ((638de986-e9a0-45a2-bba8-d698da5b3ed1)) Let $\mathcal{A}$ be an open covering of the metric space $(X, d)$. If $X$ is compact, there is a $\delta>0$ such that for each subset of $X$ having diameter less than $\delta$, there exists an element of $\mathcal{A}$ **containing** it.
	  The number $\delta$ is called a Lebesgue number for the covering $\mathcal{A}$.
		- This grants some convenient constructions. Essentially, we have a lower bound for the 'lengths'.
			- We may divide an interval into finite pieces.
	- Intuition
		- It suffices to consider connected X.
		- The open sets must intersect to cover X. Moreover, the intersection can't be infinitely small.
	- Proof
		- Construct a function $f(x)=\frac{1}{n} \sum_{i=1}^n d\left(x, C_i\right)$, where $C_i=X-O_i$. #Techniques
			- i.e. The distance to the boundary.
			- The trick of constructing a function is remarkable
		- Since $x$ is in some $O_i$, the distance must be greater than zero.
		- f is continuous, X is compact -> f has a minimum $\delta$, which is our required number.
-