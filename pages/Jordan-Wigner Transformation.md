- Definition #card
	- Idea
	  collapsed:: true
		- A spin has two levels, which could be regarded as a fermionic mode (i.e. $|\uparrow \rangle \mapsto |1\rangle$, $|\downarrow \rangle \mapsto |0\rangle$)
	- collapsed:: true
	  $$
	  \begin{aligned}
	  \sigma_j^+=\left(\sigma_j^x+i \sigma_j^y\right) / 2 \equiv f_j^{\dagger} \\
	  \sigma_j^-=\left(\sigma_j^x-i \sigma_j^y\right) / 2 \equiv f_j
	  \end{aligned}
	  $$
		- However, $f$ between different sites commute rather than anti-commute. We should fix this by adding the phase manually/
	- $$
	  \begin{aligned}
	  & a_j^{\dagger}=e^{\left(i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)} \cdot f_j^{\dagger} \\
	  & a_j=e^{\left(i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)} \cdot f_j
	  \end{aligned}
	  $$
		- The phase could also be represented as 
		  collapsed:: true
		  $$
		  e^{\left( \pm i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)}=\prod_{k=1}^{j-1} e^{ \pm i \pi f_k^{\dagger} f_k}=\prod_{k=1}^{j-1} e^{ \pm i \pi \frac{\sigma_k^z+I}{2}}=\prod_{k=1}^{j-1}\left(-\sigma_k^z\right)
		  $$
			- The minus means spin-up is regarded as occupied.
		- Note that the transformation is **highly nonlocal**.
		  i.e. *Bosonic* and *fermionic* differs by a highly nonlocal transformation!
	- Inverse transformation
	  collapsed:: true
		- $$\begin{aligned}
		  & \sigma_j^{+}=e^{\left(-i \pi \sum_{k=1}^{j-1} a_k^{\dagger} a_k\right)} \cdot a_j^{\dagger} \\
		  & \sigma_j^{-}=e^{\left(+i \pi \sum_{k=1}^{j-1} a_k^{\dagger} a_k\right)} \cdot a_j \\
		  & \sigma_j^z=2 a_j^{\dagger} a_j-I
		  \end{aligned}$$
	- Properties
		- $$
		  \left\{a_i^{\dagger}, a_i\right\}=1,\left\{a_i^{\dagger}, a_j^{\dagger}\right\}=0,\left\{a_i, a_j\right\}=0
		  $$
		- collapsed:: true
		  $$
		  \sigma_j^z=2 f_j^{\dagger} f_j-I
		  $$
			- Indeed 'particle number' corresponds to the spin.
		- $$
		  a_j^{\dagger} a_j=f_j^{\dagger} f_j
		  $$
-