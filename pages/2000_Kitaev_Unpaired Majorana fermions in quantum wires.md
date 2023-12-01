- ![2000_Kitaev_Unpaired Majorana fermions in quantum wires.pdf](file://zotero_link/Physics/Kitaev/2000_Kitaev_Unpaired Majorana fermions in quantum wires.pdf)
- # Questions and Problems
	- Why is a gap necessary?
		- ((65616a95-5ca6-4864-972e-f5b6ebfc61fe))
- # Motivation #card
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-12-30T07:32:38.889Z
  card-last-reviewed:: 2023-11-29T01:32:38.889Z
  card-last-score:: 5
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
		  H_1=\sum_{j=1}^{L-1}\left(-w\left(a_j^{\dagger} a_{j+1}+a_{j+1}^{\dagger} a_j\right)-\mu\left(a_j^{\dagger} a_j-\frac{1}{2}\right)+\Delta a_j a_{j+1}+\Delta^* a_{j+1}^{\dagger} a_j^{\dagger}\right)
		  $$
		- The first term is hopping.
		- The second term is the chemical potential.
		- The third and the last term break the $U(1)$ symmetry, which is the induced superconducting gap in BCS theory.
		-
		- Note that we can also choose to hide the phase dependence of $\Delta$ in the definition of majorana operators:
		   $$
		  c_{2 j-1}=e^{i \frac{\theta}{2}} a_j+e^{-i \frac{\theta}{2}} a_j^{\dagger}, \quad c_{2 j}=-i e^{i \frac{\theta}{2}} a_j+i e^{-i \frac{\theta}{2}} a_j^{\dagger} \\
		  H_1=\frac{i}{2} \sum_{j=1}^{L-1}\left(-\mu c_{2 j-1} c_{2 j}+(w+|\Delta|) c_{2 j} c_{2 j+1}+(-w+|\Delta|) c_{2 j-1} c_{2 j+2}+h.c. \right)
		  $$
- # Solution
  collapsed:: true
	- ## Two Special Cases
		- Trivial case: $w=|\Delta|=0$
		  collapsed:: true
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
		- ### Further investigation into the nontrivial case
			- Two free majorana modes corresponds one free fermionic mode.
			- Therefore the system has two ground states, with the same energy but **different fermionic parity**.
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
  collapsed:: true
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
		  collapsed:: true
			- The specific form of $A$ could be written down:
				- \begin{align*}
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
			- The bulk solution
				- Therefore, if $\vec{u} =\sum _{j}( x_{2j-1}\vec{e}_{2j-1} +x_{2j}\vec{e}_{2j})$, then
				  \begin{align*}
				  A\vec{u} & =\sum _{j}[ -( w+|\Delta |) x_{2j-2} -\mu x_{2j} +( -w+|\Delta |)x_{2j+2}]\vec{e}_{2j-1}\\
				  & -\sum _{j}[( -w+|\Delta |)x_{2j-3} -\mu x_{2j-1} -( w+|\Delta |) x_{2j+1}]\vec{e}_{2j}
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
				  \lambda=\frac{-\mu \pm \sqrt{4|\Delta |^{2} +\mu ^{2} -4w^{2}}}{2( |\Delta |+w)}
				  \end{equation*}
				  which is precisely Kitaev's equation ((65604cd9-1dcf-468f-9331-831171f13f06))
				-
				- If $2|w|<|\mu|$, we have one of $|\lambda_+|,|\lambda_-|$ larger than 1 and the other smaller than 1.
					- For $|\lambda>1|$, the mode is localized at the other end of the chain. 
					  For $|\lambda<1|$, the mode is localized at the same end.
					- Therefore, only one of the coefficients $\alpha_{+}^{\prime},\alpha_{-}^{\prime}\text{ (or }\alpha_{+}^{\prime\prime},\alpha_{-}^{\prime\prime})$ (in Kitaev's notation) could be nonzero in order to have localized modes.
				- If $2|w|>|\mu|$, both $|\lambda_+|,|\lambda_-|$ are larger than 1.
					- Therefore, both coefficients could be nonzero!
				- It seems the chain always exhibits zero modes. What's the condition that the chain doesn't have zero modes at all?
				  background-color:: red
					- First, if the chain does always exhibit zero modes, the fact isn't unacceptable since it might be a boundary effect.
			- The boundary conditions
				- Note that the conditions to be satisfied at the ends of the chain is different from that in the bulk.
				- We could rephrase the boundary condition into the following form: #card
					- $x_{-1}=x_0=0,x_{2L+1}=x_{2L+2}=0$
					- In other words, 'the matrix element is zero beyond the boundary' could be rephrased by setting the corresponding variables beyond the boundary to zero.
				- #+BEGIN_IMPORTANT
				  To satisfy the boundary condition, we must allow both coefficients to be nonzero.
				  #+END_IMPORTANT
				- Therefore, only the case $2|w| > |\mu|$ allows unpaired boundary modes.
	- ## Finite-Size effect
		- When the size of the chain is finite, the eigenvectors are not exact and the 'unpaired modes' are actually weakly interacting.
			- Note that the boundary conditions should actually be $x_0=x_{-1}=0,x_{2L+1}=x_{2L+2}=0$, which could not be all satisfied simultaneously.
		- The interaction could be described by
		  $$H_{\mathrm{eff}}=\frac{i}{2}tb'b'',\quad\quad t\propto e^{-L/l_0},$$
		-
- id:: 65583334-e2d6-4205-a4cc-fb3ff0212e44
  collapsed:: true
  #+BEGIN_Warning
  What to study after constructing the interesting model? What good questions are to be raised?
  #+END_Warning
	- An average physicist might stop at page 5 of his paper: Voila! Here is a chain with unpaired Majorana modes! But we should always look further.
	- Also, there are hundreds of rubbish papers produced every day. At first sight I might also miss the gold buried in this paper.
	  So the problem is: How to find gold hidden in seemingly easy phenomena?
	- Possible questions
		- A criteria for whether a system exhibits unpaired modes
		- Higher dimensions
		- A definition of 'equivalence' and classification
	-
- # Zero modes in general Hamiltonians
	- ## Setup
		- Majorana number
		  collapsed:: true
			- $$\mathcal{M}=\mathcal{M}(H)=\pm1$$
			- $M(H)=-1$ means that there are unpaired majorana modes for $H$ when $L \to \infty$.
		- Basic properties
			- $$P(H)=\operatorname{sgn}\det W=\operatorname{sgn}\operatorname{Pf}A$$
			- $$\mathcal{M}(H^{\prime}\boxtimes H^{\prime\prime})=\mathcal{M}(H^{\prime})\mathcal{M}(H^{\prime\prime})$$
			- When we close chains into loops,
			  $$P(H(L_1+L_2))=\mathcal{M}(H)P(H(L_1))P(H(L_2))$$
				- ((65616f5a-d59b-4067-ab1e-76ff91e62e06))
				- The boundary mode would pair up and exactly one of them would be occupied.
		- Translational-invariant chain
			- There are $L$ unit cells with $n$ fermionic sites in each cell.
			- $$H=\frac{i}{4}\sum_{l,m}\sum_{\alpha,\beta}B_{\alpha\beta}(m-l)c_{l\alpha}c_{m\beta}$$
				- $m,l$ labels the unit cell while $\alpha,\beta$ labels the majorana operator inside the cell.
				- Translational invariance manifests itself in $B$'s dependence on $m-l$, instead of $m$ and $l$ individually.
	- ## Compute the parity of the ground state #card
		- Observation. $[P,H]=0$, thus we can find common eigenstates of the two operators.
		- Idea
			- We could determine the existence of majorana modes by investigating the parity of ground states.
		- Fourier transformation
			- $$\tilde{B}_{\alpha\beta}(q)=\sum_je^{iqj}B_{\alpha\beta}(j),\quad q=2\pi\frac{k}{L}\pmod{2\pi},k=0,\ldots,N-1$$
				- The transformation works for a finite chain, so the momentum is discrete.
			- $$\tilde{B}^\dagger(q)=-\tilde{B}(q)=\tilde{B}^T(-q)$$
		- Proposition. 
		  $$\operatorname{Pf}B=\left(\prod_{q=-q}\operatorname{Pf}\tilde{B}(q)\right)\left(\prod_{q\neq-q}\operatorname{det}\tilde{B}(q)\right)$$
			- The first step is to use Fourier transformation of **majorana operators** to diagonalize the Hamiltonian.
				- $$\begin{align*}
				  c_{m\alpha } & =\sum _{p} e^{-ipm} c_{p\alpha }\\
				  H & =\frac{i}{2}\sum _{\alpha \beta }\sum _{ml} B_{\alpha \beta }( m-l) c_{m\alpha } c_{l\beta }\\
				   & =\frac{i}{2}\sum _{\alpha \beta }\sum _{ml} B_{\alpha \beta }( m-l)\sum _{p}\sum _{q} e^{-ipm} e^{-iql} c_{p\alpha } c_{q\beta }\\
				   & =\frac{i}{2}\sum _{\alpha \beta }\sum _{p}\sum _{q}\sum _{l} e^{-i( p+q) l}\sum _{m-l} B_{\alpha \beta }( m-l) e^{-ip( m-l)} c_{p\alpha } c_{q\beta }\\
				   & =\frac{i}{2}\sum _{\alpha \beta }\sum _{p}\sum _{q} N\delta _{pq}\left\{\sum _{m-l} B_{\alpha \beta }( m-l) e^{-ip( m-l)}\right\} c_{p\alpha } c_{q\beta }\\
				   & =\frac{i}{2} N\sum _{\alpha \beta }\sum _{q} B_{\alpha \beta }( q) c_{q\alpha } c_{q\beta }
				  \end{align*}$$
			- #+BEGIN_NOTE
			  Fourier transformation of the operators would finally lead to the Fourier transformation of the bilinear Hamiltonian.
			  #+END_NOTE
			- Therefore if we denote the Discrete Fourier transformation by $F$, then
			  $$\tilde B=FBF^T=FBF$$
				- $$\begin{aligned}W=\frac1{\sqrt{N}}\begin{bmatrix}1&1&1&1&\cdots&1\\1&\omega&\omega^2&\omega^3&\cdots&\omega^{N-1}\\1&\omega^2&\omega^4&\omega^6&\cdots&\omega^{2(N-1)}\\1&\omega^3&\omega^6&\omega^9&\cdots&\omega^{3(N-1)}\\\vdots&\vdots&\vdots&\vdots&\ddots&\vdots\\1&\omega^{N-1}&\omega^{2(N-1)}&\omega^{3(N-1)}&\cdots&\omega^{(N-1)(N-1)}\end{bmatrix},\end{aligned}$$
				- Note that for transformations of the majorana operator, the corrrect operation is **transposition** rather than **complex conjugation**.
			- $$\operatorname{Pf} \tilde B=\operatorname{Pf} B \operatorname{det} F$$
			- Proposition. The determinant of the Fourier transformation is one.
				- Note that
-