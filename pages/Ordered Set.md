- # Defs
	- Partially ordered set
		- A partially ordered set $(X, \leqq)$ or just $X$, is an ordered pair of a set $X$ and a binary relation (the partial order) $\leqq$ on $X$, that is **reflexive** $(x \leqq x)$, **transitive** $(x \leqq y, y \leqq z$ implies $x \leqq z)$, and **antisymmetric** $(x \leqq y$, $y \leqq x$ implies $x=y$ ).
		- A **total** order relation also has $x \leqq y$ or $y \leqq x$, for every $x, y \in X$; then $X$ is totally ordered.
	- Upper Bound
		- An upper bound of $C$ in $X$ is an element $b$ of $X$ such that $x \leqq b$ for all $x \in C$.
		- Notes
			- Could be outside the subset
			- Stronger than maximal, since it requires that >= always exists.
	- Maximal Element
		- A maximal element of $S \sub X$ is some $s \in S$ such that there is no $x \in S$ s.t. $s < x$
		- Notes
			- The maximal element must be inside the subset
			- Only 'nothing > $s$', which is weaker than '$s$ >= everything'.
	- Chain
	  collapsed:: true
		- A subset $C$ of $X$ such that at least one of the statements $x \leqq y$, $y \leqq x$ holds for every $x, y \in C$.
	- Chain conditions
	  collapsed:: true
		- Ascending
			- Proposition. For a partially ordered set $X$ the following conditions are equivalent:
			  (1) every infinite ascending sequence $x_1 \leqq x_2 \leqq \cdots \leqq x_n \leqq x_{n+1} \leqq \cdots$ of elements of $X$ terminates (is eventually stationary): there exists $N>0$ such that $x_n=x_N$ for all $n \geqq N$
			  (2) there is no infinite strictly ascending sequence $x_1<x_2<\cdots<x_n<$ $x_{n+1}<\cdots$ of elements of $X$;
			  (3) every nonempty subset $S$ of $X$ has a maximal element.
		- Descending
			- Completely similar.
			- Proposition. For a partially ordered set $X$ the following conditions are equivalent:
			  (1) every infinite descending sequence $x_1 \geqq x_2 \geqq \cdots \geqq x_n \geqq x_{n+1} \geqq \cdots$ of elements of $X$ terminates: there exists $N>0$ such that $x_n=x_N$ for all $n \geqq N$;
			  (2) there is no infinite strictly descending sequence $x_1>x_2>\cdots>x_n>$ $x_{n+1}>\cdots$ of elements of $X$;
			  (3) every nonempty subset $S$ of $X$ has a minimal element.
-