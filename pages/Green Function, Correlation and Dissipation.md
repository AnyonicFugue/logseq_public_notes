- # Definitions
	- [[Green Function]] #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-06T18:04:27.576Z
	  card-last-reviewed:: 2023-05-06T12:04:27.577Z
	  card-last-score:: 5
		- ((640be051-94a7-40d3-bcc0-581ee03f5cdb)) 
		  $$G_\sigma\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right):=-\mathrm{i} T\left\langle\psi_\sigma(\mathbf{r}, t) \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\rangle$$
			- T is the time ordering, where 
			  $$
			  T\left(a\left(t_1\right) b\left(t_2\right)\right)= \begin{cases}a\left(t_1\right) b\left(t_2\right), & t_1>t_2, \\ (-1)^P b\left(t_2\right) a\left(t_1\right), & t_2>t_1,\end{cases}
			  $$
			- Don't forget the minus for fermions!
		- Retarded
			- $$G_\sigma^{\mathrm{R}}\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right) :=-\mathrm{i} \theta\left(t-t^{\prime}\right)\left\langle\left\{\psi_\sigma(\mathbf{r}, t), \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\}\right\rangle=-\frac{i}{\hbar} \theta(t)\left\langle\left\{c_k(t), \hat{c}_k^{\dagger}(0)\right\}\right\rangle$$
			- $$\chi_{B A}^{ret}\left(t, t^{\prime}\right)=\frac{i}{\hbar} \theta\left(t, t^{\prime}\right)\left\langle\left[\hat{B}(t), \hat{A}\left(t^{\prime}\right)\right]\right\rangle$$
				- This follows ((6410762b-de4a-479c-961f-baa5532f6a5d)).
			- Only retarded (from the earlier time $t'$ to the later time $t$) part.
		- Advanced
			- $$G_\sigma^{\mathrm{A}}\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right)=\mathrm{i} \theta\left(t^{\prime}-t\right)\left\langle\left\{\psi_\sigma(\mathbf{r}, t), \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\}\right\rangle$$
			- Only advanced (from the later time $t'$ to the earlier time $t$) part.
		- Fourier transformed
			- $$G^R(k,\omega)=\int dt \ e^{i\omega t} G^R(k,t)$$
				- Note that the exponent is $+i \omega t$ rather than $-i \omega t$!
	- Correlation function
	- Spectral function
		- ((640be0e1-63f2-426b-96be-b5b698e93cdb)) 
		  $$A(k, \omega):=\frac{1}{2 \pi} \int d t e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle$$
			- Quite analogous to the ((6401b89c-e517-4e8f-ad4e-f98d5b166921))
	-
- # Relations
	- Green function and spectral function #card
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-29T01:18:23.357Z
	  card-last-reviewed:: 2023-05-30T01:18:23.358Z
	  card-last-score:: 5
		- $$A(\vec{k}, \omega) :=\frac{1}{2 \pi} \int d t e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle =-\frac{1}{\pi} \operatorname{Im} G^R(k, \omega)$$
			- Note that the exponent is $+i \omega t$ rather than $-i \omega t$!
			- Start from the definition
			  $$G^R(k,t)=-\frac{i}{\hbar} \theta(t)\left\langle\left\{c_k(t), \hat{c}_k^{\dagger}(0)\right\}\right\rangle$$
				- Note that there is an **anti-commutator** in the retarded Green function!
			- $A=(G^R-\overline{G^R})/(2i)$, which completes the integral to the whole real axis.
		- $$G^R(\vec{k}, \omega)=\int d \omega^{\prime} \frac{A\left(k, \omega^{\prime}\right)}{\omega-\omega^{\prime}+i \varepsilon}
		  $$
			- Prop. 
			  $$\begin{aligned} & \int_{-\infty}^{\infty} d \omega^{\prime} f\left(\omega^{\prime}\right)\left\{P \frac{1}{\omega^{\prime}-\omega}+i \pi \delta\left(\omega^{\prime}-\omega\right)\right\} \\ & =\int_{-\infty}^{\infty} d \omega^{\prime} f\left(\omega^{\prime}\right) \frac{1}{\omega^{\prime}-\omega-i \epsilon}\end{aligned}$$
				- The delta function adds back the imaginary part.
			- Invoke ((6401b89c-a4af-4f0c-b59f-d44a3c164ff6)): $\chi_1(\omega)=\frac{1}{\pi} \mathcal{P} \int_{-\infty}^{\infty} \frac{\chi_2\left(\omega^{\prime}\right)}{\omega^{\prime}-\omega} d \omega^{\prime}$
				- Note that there is an extra minus in the definition of $A$, thus the denominator of the integrand is also minused.
			-
	- Green function and Matsubara Green function
		- card-last-score:: 5
		  card-repeats:: 2
		  card-next-schedule:: 2023-06-29T12:12:44.470Z
		  card-last-interval:: 30
		  card-ease-factor:: 2.7
		  card-last-reviewed:: 2023-05-30T12:12:44.471Z
		  $$
		  \mathcal{G}_\sigma\left(\omega_n, \mathbf{p}\right)=G_\sigma^{\mathrm{R}}\left(\mathrm{i} \omega_n, \mathbf{p}\right), \quad \omega_n>0
		  $$
		  which means we can obtain the retarded Green function by substituting every $i\omega_n$ by $\omega$ #card
			- Summary
				- Obtain the expectation by brute-force sum over the Boltzmann ensemble (spectral representation).
			- \begin{gather*}
			   \\
			  \begin{aligned}
			  G_{AB}( \omega _{n}) & =\int _{0}^{\beta } d\tau G_{AB} (\tau )e^{i\omega _{n} \tau }\\
			   & =-\int _{0}^{\beta } d\tau \langle T\{A(\tau )B(0)\}\rangle e^{i\omega _{n} \tau }\\
			   & =-\int _{0}^{\beta } d\tau \sum _{\alpha \beta }\frac{1}{Z} e^{-\beta E_{\alpha }}\left< \alpha \left| e^{H\tau } Ae^{-H\tau }\right| \beta \right> < \beta |B|\alpha > e^{i\omega _{n} \tau }\\
			   & =-\frac{1}{Z}\sum_{\alpha \beta } e^{-\beta E_{\alpha }}< \alpha | A| \beta > < \beta |B|\alpha > \int _{0}^{\beta } d\tau e^{( i\omega _{n} +E_{\alpha } -E_{\beta }) \tau }\\
			   & 
			  \end{aligned}\\
			  \end{gather*}
			- On the other hand,
			  \begin{equation*}
			  \int _{0}^{\beta } d\tau e^{( i\omega _{n} +E_{\alpha } -E_{\beta }) \tau } =\frac{e^{( i\omega _{n} +E_{\alpha } -E_{\beta }) \beta } -1}{i\omega _{n} +E_{\alpha } -E_{\beta }} =\frac{\eta e^{( E_{\alpha } -E_{\beta }) \beta } -1}{i\omega _{n} +E_{\alpha } -E_{\beta }}
			  \end{equation*}
			  Thus
			  \begin{equation*}
			  G_{AB}( \omega _{n}) =-\frac{1}{Z}\sum{}_{\alpha \beta } e^{-\beta E_{\alpha }}< \alpha | A| \beta > < \beta |B|\alpha > \frac{\eta e^{( E_{\alpha } -E_{\beta }) \beta } -1}{i\omega _{n} +E_{\alpha } -E_{\beta }}
			  \end{equation*}
			- Comparing with
			  \begin{equation*}
			  \begin{aligned}
			  A_{AB} (\omega ) & =\int _{R} dt\ e^{-i\omega t} \langle A(0)B(t)\rangle \\
			   & =\frac{1}{Z}\sum _{\alpha \beta }\left( e^{-\beta E_{\alpha }} -\eta e^{-\beta E_{\beta }}\right) \langle\alpha |A|\beta \rangle \langle \beta |B|\alpha \rangle \delta ( \omega +E_{\alpha } -E_{\beta })
			  \end{aligned}
			  \end{equation*}
			  finishes the proof.
		-
- # Examples
	- Free fermions
	  id:: 64238eab-5b4c-48b1-ac8a-33fe14061048
		- card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.36
		  card-next-schedule:: 2023-06-29T02:05:41.925Z
		  card-last-reviewed:: 2023-05-30T02:05:41.926Z
		  card-last-score:: 3
		  $$
		  G^R(\vec{k}, \omega)=\int d \omega^{\prime} \frac{A\left(\vec{k}, \omega^{\prime}\right)}{\omega-\omega^{\prime}+i\epsilon}=\frac{1}{\omega-\xi_k+i\epsilon}
		  $$ #card
			- id:: 64113383-8089-4db4-8a8b-ebc74bfc5ab7
			  $$
			  \begin{aligned}
			  A(\vec{k}, \omega) & \stackrel{\text { def }}{=} \frac{1}{2 \pi} \int d t e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle \\
			  & =\frac{1}{2 \pi} \int d t e^{i \omega t} e^{-i \xi_k t} 1=\frac{1}{2 \pi} \cdot 2 \pi \delta\left(\omega-\xi_k\right)
			  \end{aligned}
			  $$
				- Note that the time exponent is $e^{i \omega t}$ in the first line (contrary to the conventional $e^{-i \omega t}$), which is crucial to the correctness of the result!
				- Otherwise I would obtain $\delta(\omega + \xi_k)$, which is wrong.
			-
- # Matsubara Green Function
  id:: 642f7907-397a-4fd1-b504-e0060ac5a8be
	- Idea
		- Introduce an imaginary time to make things easier.
		- Go back to real time by analytical continuation.
	- Def #card
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-06-29T02:26:33.458Z
	  card-last-reviewed:: 2023-05-30T02:26:33.459Z
	  card-last-score:: 3
		- $$
		  G_{A B}\left(\tau_1, \tau_2\right):=-\frac{1}{\hbar}T\left\langle A\left(\tau_1\right) B\left(\tau_2\right)\right\rangle
		  $$
		  where $\tau=it$
			- Note that here is no symmetrization, different from the definition of retarded Green functions!
		- $$
		  G_{AB}\left(\omega_n, \mathbf{p}\right)=\int_0^{\beta \hbar} \mathrm{e}^{\mathrm{i} \omega_n \tau} G_{AB}(\tau, \mathbf{p}) \mathrm{d} \tau
		  $$
	- Prop. $G_{AB} (\tau )=\eta G_{AB} (\tau +\beta )$ #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-30T18:14:05.441Z
	  card-last-reviewed:: 2023-05-30T12:14:05.441Z
	  card-last-score:: 5
		- \begin{equation*}
		  \begin{aligned}
		  G_{AB} (\tau ) & =-\operatorname{Tr}\left\{\frac{1}{z} e^{-\beta H} e^{H\tau } Ae^{-H\tau } B\right\}\\
		  G_{AB} (\tau +\beta ) & =-\operatorname{Tr}\left\{\frac{1}{z} e^{-\beta H} e^{(\tau +\beta ) H} Ae^{-(\beta +\tau )H} B\right\}\\
		   & =-\operatorname{Tr}\left\{\frac{1}{z} e^{\tau H} Ae^{-\tau H} \cdot e^{-\beta H} B\right\}\\
		   & =-\operatorname{Tr}\left\{\frac{1}{z} e^{-\beta H} B \cdot e^{\tau H} Ae^{-\tau H}\right\}
		  \end{aligned}
		  \end{equation*}
		- Exchange $B$ and $e^{\tau H} Ae^{-\tau H}$ leads to a factor of $\eta$ (1 for bosons, -1 for fermions)
			- Seems there's an implicit assumption: $A,B$ are both linear combinations of bosonic or fermionic operators.
		- The function is periodical, therefore:
			- Boson. 
			  \begin{equation*}
			  G_{AB}( \omega _{n}) =\int _{0}^{\beta } d\tau G_{AB} (\tau )e^{i\omega _{n} \tau } ,\omega _{n} =\frac{2\pi }{\beta } n
			  \end{equation*}
			- Fermion.
			  \begin{equation*}
			  G_{AB}( \omega _{n}) =\int _{0}^{\beta } d\tau G_{AB} (\tau )e^{i\omega _{n} \tau } ,\omega _{n} =\frac{\pi }{\beta } \cdot ( 2n+1)
			  \end{equation*}
	- Analytical continuation
		- On the upper half plane:
		  $$
		  \mathcal{G}_\sigma\left(\omega_n, \mathbf{p}\right)=G_\sigma^{\mathrm{R}}\left(\mathrm{i} \omega_n, \mathbf{p}\right), \quad \omega_n>0
		  $$
			- This is Philips's notation, where LHS is the Matsubara Green function and RHS is the retarded Green function.
		- On the lower half plane:
		  $$
		  \mathcal{G}_\sigma\left(\omega_n, \mathbf{p}\right)=G_\sigma^{\mathrm{A}}\left(\mathrm{i} \omega_n, \mathbf{p}\right), \quad \omega_n<0
		  $$
		- Proof
			- Can be done by spectral representation, i.e. express average $\langle A \rangle$ as 
			  $$\sum_\alpha e^{-\beta E_\alpha} \langle \alpha | A | \alpha \rangle$$
			  then compare to the spectral function and invoke the KK relation.
	- Example. Calculate the particle-number correlation
		-
-