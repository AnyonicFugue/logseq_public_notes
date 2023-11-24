- ![2000_Kitaev_Unpaired Majorana fermions in quantum wires.pdf](file://zotero_link/Physics/Kitaev/2000_Kitaev_Unpaired Majorana fermions in quantum wires.pdf)
- # Motivation #card
  collapsed:: true
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
- # Symmetry condition for unpaired majorana fermions
  collapsed:: true
	- The $U(1)$ symmetry must be broken to a $Z_2$ symmetry.
	  background-color:: red
		- If this is true, we must consider superconducting systems.
		- Review on the $U(1)$ symmetry
		  collapsed:: true
			- Action on operators: 
			  $$
			  a_j \mapsto e^{i \phi} a_j
			  $$
			- Proposition.
			  $$e^{-i\theta N_{j}} a_{j} e^{i\theta N_{j}} =e^{i\theta } a_{j}$$
				- The proof is easy. Just take a derivative to $\theta$, as common in Lie algebras.
				- The key point is that the $Z_2$ symmetry is a special case, with $\theta=\pi$.
				- A continuous symmetry could always be obtained by exponentiating generators, which is precisely the thought of Lie algebras.
		- The $Z_2$ symmetry
		  collapsed:: true
			- Operator level:
			  $$
			  a_j \mapsto-a_j
			  $$
			- State level:
			  $$N=(-1)^{\sum_i a_i^\dagger a_i}=\prod_i (1-2a_i^\dagger a_i)$$
			- Proposition. These two levels match,
			  $$\begin{align*}
			  \left( 1-2a_{j}^{\dagger } a_{j}\right) a_{j}\left( 1-2a_{j}^{\dagger } a_{j}\right) & =-a_{j}\\
			  \left( 1-2a_{j}^{\dagger } a_{j}\right) a_{j}^{\dagger }\left( 1-2a_{j}^{\dagger } a_{j}\right) & =-a_{j}^{\dagger }
			  \end{align*}$$
		- Proposition. The symmetry mixes a majorana operator with its pair.
			- Proposition. If $j\neq k$, then $[ N_{j} ,\gamma _{2k-1}] =[ N_{j} ,\gamma _{2k}] =0$
			- \begin{equation*}
			  e^{-i\theta \sum _{j} N_{j}} \gamma _{2k-1} e^{i\theta \sum _{j} N_{j}} =e^{-i\theta N_{k}} \gamma _{2k-1} e^{i\theta N_{k}} =e^{-i\theta \frac{\mathbf{1} +i\gamma _{2k-1} \gamma _{2k}}{2}} \gamma _{2k-1} e^{i\theta \frac{\mathbf{1} +i\gamma _{2k-1} \gamma _{2k}}{2}}
			  \end{equation*}
		- But what would the problem that would follow?
		  background-color:: red
- # Setup
  collapsed:: true
	- The Hamiltonian
		- $$
		  H_1=\sum_j\left(-w\left(a_j^{\dagger} a_{j+1}+a_{j+1}^{\dagger} a_j\right)-\mu\left(a_j^{\dagger} a_j-\frac{1}{2}\right)+\Delta a_j a_{j+1}+\Delta^* a_{j+1}^{\dagger} a_j^{\dagger}\right)
		  $$
		- The first term is hopping.
		- The second term is the chemical potential.
		- The third and the last term break the $U(1)$ symmetry, which is the induced superconducting gap in BCS theory.
		-
		- Note that we can also choose to hide the phase dependence of $\Delta$ in the definition of majorana operators:
		   $$
		  c_{2 j-1}=e^{i \frac{\theta}{2}} a_j+e^{-i \frac{\theta}{2}} a_j^{\dagger}, \quad c_{2 j}=-i e^{i \frac{\theta}{2}} a_j+i e^{-i \frac{\theta}{2}} a_j^{\dagger} \\
		  H_1=\frac{i}{2} \sum_j\left(-\mu c_{2 j-1} c_{2 j}+(w+|\Delta|) c_{2 j} c_{2 j+1}+(-w+|\Delta|) c_{2 j-1} c_{2 j+2}\right)
		  $$
- # Solution
  collapsed:: true
	- ## Two Special Cases
	  collapsed:: true
		- Trivial case: $w=|\Delta|=0$
			- The system has only chemical potential and no interaction.
			- In the majorana representation, 
			  $$
			  H=\frac{i}{2}(-\mu) \sum_j c_{2 j-1} c_{2 j}
			  $$
			  i.e. majoranas from the same site pair up.
				- ((655832d0-ee28-45c6-8091-04cb1f4fbaf8))
		- Desired case: $w=|\Delta|>0, \mu=0$
			- $$
			  H=i w \sum_j c_{2 j} c_{2 j+1}
			  $$
			- Majoranas from adjacent sites pair up (similar to [[AKLT Model]]).
				- ((655832c2-2fa9-4620-9d01-0f73076e20d8))
			- Those at the ends of the chain are free!
			-
	- ## General Solution
	  collapsed:: true
		- The spectrum could be found via Fourier transformation,
		  $$
		  \epsilon(q)= \pm \sqrt{(2 w \cos q+\mu)^2+4|\Delta|^2 \sin ^2 q}, \quad-\pi \leq q \leq \pi
		  $$
			- Obviously, the necessary and sufficient condition for the chain to be gapless is
			  $$
			  2|w|>|\mu|, \Delta = 0
			  $$
			- Note that a Fourier transformation corresponds to an infinitely long chain, i.e. only the bulk property matters.
		- Conjecture. The trivial phase occurs at $2|w|<|\mu|$ while the nontrivial phase occupies the domain $2|w|>|\mu|, \Delta \neq 0$.
- # Zero modes for general parameters
	- ## Energies and eigen modes from the A matrix
		- ### What is a zero mode, or an unpaired mode?
		  collapsed:: true
			- First note that $H=\frac{i}{2}\sum A_{ij} c_{i} c_{j}$. To find the spectrum, we need to quasi-diagonalize the skew-symmetric matrix,
			  \begin{equation*}
			  \left(\begin{array}{ c }
			  b_{1} '\\
			  b_{1} ''\\
			  \vdots \\
			  b_{N} '\\
			  b_{N} ''\\
			  b_{N} ''
			  \end{array}\right) =W\left(\begin{array}{ c }
			  c_{1}\\
			  c_{2}\\
			  \vdots \\
			  c_{2N-1}\\
			  c_{2N}
			  \end{array}\right) ,\ \ WAW^{T} =\left(\begin{array}{ c c c c c }
			  0 & \epsilon _{1} &  &  & \\
			  -\epsilon _{1} & 0 &  &  & \\
			  & \ddots  &  &  & \\
			  &  & 0 & \epsilon _{N} & \\
			  &  & -\epsilon _{N} & 0 & 
			  \end{array}\right)
			  \end{equation*}
			- A zero-mode is a block with $\varepsilon _{m} =0$, which means that $b'_{m}$ and $b''_{m}$ are not paired with any other majorana operator.
			- Rephrased in matrix term, if we write $b'_{m} =\sum _{j}( x_{2j-1} c_{2j-1} +x_{2j} c_{2j})$ and arrange the coefficients into a vector $\vec{u} =( x_{1} ,x_{2} ,...,x_{2N-1} ,x_{2N})$, then we should have
			  \begin{equation*}
			  A\vec{u} =0
			  \end{equation*}
		- ### Find the zero mode from the A matrix
			- The specific form of $A$ could be written down:
			  \begin{align*}
			  H_{1} & =\frac{i}{2}\sum _{j}\{-\mu c_{2j-1} c_{2j} +(w+|\Delta |)c_{2j} c_{2j+1} +(-w+|\Delta |)c_{2j-1} c_{2j+2}\}\\
			  A & =\sum _{j}\{-\mu e_{2j-1,2j} +(w+|\Delta |)e_{2j,2j+1} +( -w+|\Delta |)e_{2j-1,2j+2}\} +skew.sym.
			  \end{align*}
			- $$A=\left(\begin{array}{ c c c c c c c c }
			  ... &  &  &  &  &  &  & \\
			   &  & -\mu  &  & ( -w+|\Delta |) &  &  & \\
			   & \mu  &  & w+|\Delta | &  &  &  & \\
			   &  & -( w+|\Delta |) &  & -\mu  &  & ( -w+|\Delta |) & \\
			   & -( -w+|\Delta |) &  & \mu  &  & w+|\Delta | &  & \\
			   &  &  &  & -( w+|\Delta |) &  & -\mu  & \\
			   &  &  & -( -w+|\Delta |) &  & \mu  &  & \\
			   &  &  &  &  &  &  & ...
			  \end{array}\right)
			  $$
			-
			- Therefore, if $\vec{u} =\sum _{j}( x_{2j-1}\vec{e}_{2j-1} +x_{2j}\vec{e}_{2j})$, then
			  \begin{align*}
			  A\vec{u} & =\sum _{j}[ -( w+|\Delta |) x_{2j-2} -\mu x_{2j} +( -w+|\Delta |)x_{2j+2}]\vec{e}_{2j-1}\\
			  & -\sum _{j}[( -w+|\Delta |)x_{2j-3} -\mu x_{2j-1} -( w+|\Delta |) x_{2j}]\vec{e}_{2j}
			  \end{align*}
				- After imposing $A\vec{u} =0$, this is two decoupled recursive series.
			- The solution is standard: Find an eigenvector of the series, i.e. find a combination $x_{n-1} +px_{n}$ s.t.
			  \begin{equation*}
			  ( x_{n-1} +px_{n}) -\lambda ( x_{n} +px_{n+1}) =0
			  \end{equation*}
			  For $ax_{n-1} +bx_{n} +cx_{n+1} =0$, we could solve
			  \begin{equation*}
			  \lambda =-\frac{b\pm \sqrt{b^{2} -4ac}}{2a}
			  \end{equation*}
			- Plug it into Mathematica, we find
			  \begin{equation*}
			  x=\frac{-\mu \pm \sqrt{4|\Delta |^{2} +\mu ^{2} -4w^{2}}}{2( |\Delta |+w)}
			  \end{equation*}
			  which is precisely Kitaev's equation ((65604cd9-1dcf-468f-9331-831171f13f06))
- id:: 65583334-e2d6-4205-a4cc-fb3ff0212e44
  collapsed:: true
  #+BEGIN_Warning
  What to study after constructing the interesting model? What good questions are to be raised?
  #+END_Warning
	- An average physicist might stop at page 5 of his paper: Voila! Here is a chain with unpaired Majorana modes! But we should always look further.
	- A criteria for whether a system exhibits unpaired modes
	- A definition of 'equivalence' and classification
	-
- # Further investigation into the nontrivial case
  collapsed:: true
	- Two free majorana modes corresponds one free fermionic mode.
	- Therefore the system has two ground states, with the same energy but **different fermionic parity**.
	-