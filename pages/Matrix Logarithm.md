- Def #card
	- $\log A=\sum_{m=1}^{\infty}(-1)^{m+1} \frac{(A-I)^m}{m}$
	- The strategy is to define it near $I_n$, since we can't have it globally.
	-
	- Theorem. It is defined and continuous on all matrices s.t. $\|A-I\|<1$
		- Use $\left\|(A-I)^m\right\| \leq\|(A-I)\|^m$.
		- We can slightly modify the condition in a variety of ways. The idea is always to avoid multiple values.
	-
	- Theorem. (Partial Inverse of [[Matrix Exponential]] )
	  id:: 63c14167-8540-43ba-9aa0-4d1c2bc7cf64
		- For all $A \in M_n(\mathbb{C})$ with $\|A-I\|<1$,
		  $$
		  e^{\log A}=A .
		  $$
		- For all $X \in M_n(\mathbb{C})$ with $\|X\|<\log 2,\left\|e^X-I\right\|<1$ and
		  $$
		  \log e^X=X
		  $$
-