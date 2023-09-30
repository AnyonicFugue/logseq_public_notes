# Motivating Problems
	- Suppose $G$ and $H$ are matrix Lie groups with Lie algebras $\mathfrak{g}$ and $\mathfrak{h}$, respectively, and suppose $\phi$ : $\mathfrak{g} \rightarrow \mathfrak{h}$ is a Lie algebra homomorphism. Can we construct a Lie group homomorphism $\Phi: G \rightarrow H$ such that 
	  $$\Phi\left(e^X\right)=e^{\phi(X)}$$
	   for all $X$ in $\mathfrak{g}$?
		- We have $\phi([X,Y])=[\phi(X),\phi(Y)]$.
		- We want $\Phi\left(e^Xe^Y\right)=\Phi\left(e^X\right)\Phi\left(e^Y\right)$.
		- The problem is whether they're consistent. That is, if $e^Xe^Y=e^Z$, then whether $RHS=e^{\phi(Z)}$.
- ((640ac8c3-e3b3-475f-9a0d-073dfba14572)) Suppose $X$ and $Y$ are $n \times n$ complex matrices, and that $X$ and $Y$ commute with their commutator:
  $$
  [X,[X, Y]]=[Y,[X, Y]]=0 .
  $$
  Then we have
  $$
  e^X e^Y=e^{X+Y+\frac{1}{2}[X, Y]} .
  $$
	- As an first example.
	-
	- Proof
		- Consider $L(t)=e^{tX}e^{tY}$.
		  $\frac {dL}{dt}=e^{tX}(X+Y)e^{tY}$.
		- By differentiating again, we may show that $RHS=X+Y+t[X,Y]$.
		- Then it is all clear.
	- Note that the process of differentiation can be repeated infinitely and we may obtain the complete form of BCH.
		- Only that we can't directly prove it in this way...
- ((640ad204-613d-408c-9fb4-28e69ad1474d)) (BCH, Integral Version) For all $n \times n$ complex matrices $X$ and $Y$ with $\|X\|$ and $\|Y\|$ sufficiently small, we have
  card-last-score:: 3
  card-repeats:: 2
  card-next-schedule:: 2023-06-18T00:40:38.080Z
  card-last-interval:: 30
  card-ease-factor:: 2.46
  card-last-reviewed:: 2023-05-19T00:40:38.081Z
  $$
  \log \left(e^X e^Y\right)=X+\int_0^1 g\left(e^{\mathrm{ad}_X} e^{t\ \mathrm{ad}_Y}\right)(Y) d t 
  $$
  where $g(z)=\frac{\log z}{1-\frac{1}{z}}$. #card
	- Notes
		- $e^{\operatorname{ad}_X} e^{t \mathrm{ad}_Y}$ and, hence, also $g\left(e^{\operatorname{ad} X} e^{t \mathrm{ad}_Y}\right)$ are linear operators on the space $M_n(\mathbb{C})$ of all $n \times n$ complex matrices. This operator is being applied to the matrix $Y$.
		- The fact that $X$ and $Y$ are small guarantees that $e^{\mathrm{ad} X} e^{t \mathrm{ad} Y}$ is close to the identity operator on $M_n(\mathbb{C})$ for $0 \leq t \leq 1$, so that $g\left(e^{\mathrm{ad} X} e^{t \mathrm{ad} Y}\right)$ is well defined.
	- Intuition
	- Significance
	- Proof