alias:: SSA, Conditional Mutual Information

-
- Statement
	- For any tri-partite state $\rho^{123}$ the following holds
	  collapsed:: true
	  $$
	  S\left(\rho^{123}\right)+S\left(\rho^2\right) \leq S\left(\rho^{12}\right)+S\left(\rho^{23}\right)
	  $$
		- Take *subsystem 2 = empty*, this goes back to ordinary sub-additivity.
- Definition. Conditional mutual information
	- $$
	  I(A: C \mid B)_\rho=S\left(\rho_{A B}\right)+S\left(\rho_{B C}\right)-S\left(\rho_B\right)-S\left(\rho_{A B C}\right)
	  $$
	-
- Corollaries of SSA #card
	- collapsed:: true
	  $$
	  \begin{aligned}
	  & I\left(A A^{\prime}: B B^{\prime}\right) \geq I(A: B) \\
	  & I\left(A A^{\prime}: C C^{\prime} \mid B\right) \geq I(A: C \mid B) \\
	  & I\left(A A^{\prime}: C C^{\prime} \mid B\right) \geq I\left(A: C \mid A^{\prime} B C^{\prime}\right) \\
	  & S_{B C}+S_C-S_B \geq I(A: C) \\
	  & S_{B C}+S_C-S_B \geq I(A: C \mid B) \\
	  & S_{B C}+S_C-S_B \geq S_{B B^{\prime} C}+S_C-S_{B B^{\prime}} \\
	  & S_{B C}+S_{C D}-S_B-S_D \geq I(A: C \mid B) \\
	  & S_{B C}+S_{C D}-S_B-S_D \geq S_{B B^{\prime} C}+S_{C D D^{\prime}}-S_{B B^{\prime}}-S_{D D^{\prime}}
	  \end{aligned}
	  $$
		- Intuitive explanation
		  collapsed:: true
			- 1, 2
			  collapsed:: true
				- Inclusion of regions leads to smaller (conditional) mutual information.
				- "Part of the system can't have more information than the whole system".
			- 3
			  collapsed:: true
				- 'Regions in the conditions' are smaller than 'regions in colons'
			- 4,5
			  collapsed:: true
				- Triangle >= (conditional) mutual information