- ![2016_Qualls_Lectures on Conformal Field Theory.pdf](file://zotero_link/Physics/CFT/2016_Qualls_Lectures on Conformal Field Theory.pdf)
- # Significance
	- Critical phenomena
		- At the critical point correlation length diverge, thus we have a **scale-invariant theory**.
			- But it is still a daunting leap to formulate the property as the fundamental principle of a brand-new theory -- though it appears so natural in retrospect.
	- Fixed point of QFT
		- Roughly speaking, a scale invariant theory corresponds to a theory exactly marginal under RG.
	- We can solve a theory without writing down a Lagrangian, by bootstrap.
		- There are even theories without a Lagrangian, e.g. 6d (2,0) SCFT #[[Research/To Be Investigated]]
		-
- # Definitions
	- Conformal invariance #card
	  card-last-interval:: -1
	  card-repeats:: 1
	  card-ease-factor:: 2.5
	  card-next-schedule:: 2023-10-20T16:00:00.000Z
	  card-last-reviewed:: 2023-10-20T00:54:05.594Z
	  card-last-score:: 1
		- Intuitively, transformations that keep angles (but not necessarily distance) preserved.
		- Formally, the spacetime metric transforms as 
		  $$\eta(x) \mapsto f(x) \eta(x)$$
			- The definition is strikingly simple, thus I'm compelled to ponder why it is so defined and why so much structure could lurk behind the simple expression!
			- First answer: In a spacetime where there is no translation invariance, we could only define angle by **inner product**, which in turn relies on a metric.
				- The next question: Why should inner product be defined by metric? What kind of leap do we need from the traditional Euclidean case to the language of tangent space?
- # Examples
	- Note that scale invariance implies conformal invariance under some reasonable assumptions.
	- ## Classical Conformal Invariance
		- Maxwell equations
		- Dirac equation
		- Yang-Mills theory
		- Massless $\phi^4$
		- Common character of the theories: **Massless**.
			- In short, mass provides a length scale (in natural units) which cannot be invariant under scaling.
		- Some classical conformal invariant theories are not **quantum** conformal invariant.
			- QED is not scale-invariant, massive scalars are not scale-invariant,
			  Yang-Mills theory is not scale invariant, ...
			- In short, there is a coupling constant which runs with scale.
				- The statement is simple, but it still strikes me somewhat. Renormalization calculations seem to be nonsense, but the result -- running couplings -- is nontrivial and correct (and even accurate to some extent).
			- Put in another way, to obtain sensible low-energy effective theories we must introduce an energy scale.
			-
			- Free theories usually continue to be conformal invariant when quantized.