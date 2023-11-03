- Definition #card
  card-last-interval:: 29.95
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-10-18T22:50:43.245Z
  card-last-reviewed:: 2023-09-19T00:50:43.245Z
  card-last-score:: 5
  collapsed:: true
	- Idea
	  collapsed:: true
		- A spin has two levels, which could be regarded as a fermionic mode (i.e. $|\uparrow \rangle \mapsto |1\rangle$, $|\downarrow \rangle \mapsto |0\rangle$)
	- $$
	  \begin{aligned}
	  \sigma_j^+=\left(\sigma_j^x+i \sigma_j^y\right) / 2 \equiv f_j^{\dagger} \\
	  \sigma_j^-=\left(\sigma_j^x-i \sigma_j^y\right) / 2 \equiv f_j
	  \end{aligned}
	  $$
		- However, $f$ between different sites commute rather than anti-commute. We should fix this by adding the phase manually.
	- $$
	  \begin{aligned}
	  & a_j^{\dagger}=e^{\left(i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)} \cdot f_j^{\dagger} =f_j^{\dagger} \prod_{k=1}^{j-1}\sigma_k^z\\
	  & a_j=e^{\left(i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)} \cdot f_j=f_j \prod_{k=1}^{j-1}\sigma_k^z
	  \end{aligned}
	  $$
		- Note that the transformation is **highly nonlocal**.
		  i.e. *Bosonic* and *fermionic* differs by a highly nonlocal transformation!
	- Inverse transformation
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
- Generalized Version
	- Fradkin-Kadanoff transformation
	  id:: 654311c4-28f4-4c33-a815-5082745b7412
		- This relates the $2 L$ parafermion operators $\chi_l$ to clock operators $\sigma_j$ and $\tau_j, j=1, \ldots, L$.
		- Clock operators
		  collapsed:: true
			- They commute off-site,
			  $$
			  \left[\tau_i, \tau_j\right]=\left[\sigma_i, \sigma_j\right]=\left[\tau_i, \sigma_j\right]=0, \quad i \neq j,
			  $$
			- On the same lattice site they satisfy
			  $$
			  \sigma_j^3=\tau_j^3=1, \quad \sigma_j^{\dagger}=\sigma_j^2, \quad \tau_j^{\dagger}=\tau_j^2, \quad \sigma_j \tau_j=\omega \tau_j \sigma_j, \quad \omega=e^{2 \pi \mathrm{i} / 3}
			  $$
		- Parafermion operators:
		  $$
		  \chi_{2 j-1}=\left(\prod_{k=1}^{j-1} \tau_k\right) \sigma_j, \quad \chi_{2 j}=\left(\prod_{k=1}^{j-1} \tau_k\right) \sigma_j \tau_j=\chi_{2 j-1} \tau_j
		  $$
		- Compare to [[Majorana Representation]]
		  collapsed:: true
			- Let's map $\sigma_k \equiv c_{2k-1} \to \sigma_k^x$, $\tau_k \equiv c_{2k} \to \sigma_k^z$
			- Then
			  $$
			  \gamma_{2 j-1}=\left(\prod_{k=1}^{j-1} c_{2k}\right) c_{2j-1} \to \left(\prod_{k=1}^{j-1} \sigma_k^z \right)\sigma_j^x \\ 
			  \gamma_{2 j}=\left(\prod_{k=1}^{j-1} c_{2k}\right) c_{2j-1} c_{2j} \to \left(\prod_{k=1}^{j-1} \sigma_k^z \right)\sigma_j^x \sigma_j^z
			  $$
			  which is precisely the original JW transformation.
			-
		- ((6544541f-5a45-40d8-9d4a-319f96c9cd51))