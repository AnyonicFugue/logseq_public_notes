- ![2000_Kitaev_Unpaired Majorana fermions in quantum wires.pdf](file://zotero_link/Physics/Kitaev/2000_Kitaev_Unpaired Majorana fermions in quantum wires.pdf)
- # Motivation #card
	- We desire to achieve fault-tolerant quantum computation, but we need to deal with errors of both type $\sigma_x$ and $\sigma_z$.
	- After switching to a fermionic view, the first becomes $a_j+a_j^{\dagger}$ and the second becomes $a_j^{\dagger} a_j$.
	-
	- The first might be prevented by charge or fermion parity conservation (e.g. in superconducting systems).
		- Thus single errors cannot happen.
		- They may happen in pairs, but it can be prevented by placing fermions far away and creating an energy gap in wires connecting them.
	- Note that $a_j^{\dagger} a_j=\frac{1}{2}\left(1+i c_{2 j-1} c_{2 j}\right)$.
	- Therefore, the second error might be prevented by placing majorana fermions far away and introduce a gap!
	-
	- To have unpaired majorana fermions, we might ask the following Hamiltonian:
	  $$
	  H=\frac{i}{4} \sum_{l, m} A_{l m} c_l c_m
	  $$
	- Key idea: ((65571999-a1f2-4787-bccc-7be5e150c2d2))
- # Necessary conditions for unpaired majorana fermions
	- The $U(1)$ symmetry must be broken to a $Z_2$ symmetry.
		- Review on the $U(1)$ symmetry
			- Action on operators: 
			  $$
			  a_j \mapsto e^{i \phi} a_j
			  $$
			- Could we extend it to a symmetry acting on states?
		- The $Z_2$ symmetry
			- Operator level:
			  $$
			  a_j \mapsto-a_j
			  $$
			- State level:
			  $$N=(-1)^{\sum_i a_i^\dagger a_i}$$
			- Do they match?