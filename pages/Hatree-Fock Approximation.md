- ## Idea
	- Use the variation principle to find out the ground state energy.
	- However, we **fix** the levels to be occupied and **vary the states**.
## Expand the Hamiltonian as 1 and 2 body operators
	- $\hat{h}_{1} =-\frac{\hbar ^{2}}{2m} \Delta +V (\mathbf{r} )$
	- $\hat{h}_2=\frac{e^{2}}{| \mathbf{r}_{1} -\mathbf{r}_{2}| }$
	- Therefore $\hat H_1=\sum_{\nu \lambda}\langle\nu|\widehat{h}(1)| \lambda\rangle a_\nu^{\dagger} a_\lambda$, $\hat H_2=\frac{1}{2} \sum_{\nu \lambda \alpha \beta}\left\langle\nu \lambda\left|\frac{e^2}{\left|\mathbf{r}_1-\mathbf{r}_2\right|}\right| \alpha \beta\right\rangle a_\nu^{\dagger} a_\lambda^{\dagger} a_\beta a_\alpha$
	-
## Generalized [[Wick's Theorem]]
id:: 64085b6c-2d37-476b-92d3-3527157ccbbf
	- Examples
		- card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-15T17:39:08.044Z
		  card-last-reviewed:: 2023-04-14T11:39:08.044Z
		  card-last-score:: 5
		  $$\left< a_{\nu }^{\dagger } a_{\lambda }^{\dagger } a_{\beta } a_{\alpha }\right> :=\left< \psi _{0} |a_{\nu }^{\dagger } a_{\lambda }^{\dagger } a_{\beta } a_{\alpha } |\psi _{0}\right> =( \delta _{\nu \alpha } \delta _{\lambda \beta } -\delta _{\nu \beta } \delta _{\lambda \alpha })< \hat{n}_{\alpha }> < \hat{n}_{\beta }> .$$
		  Where $|\psi _{0}> =\prod _{a\in A} c_{a}^{\dagger } |0\rangle$ #card
			- The inner operators must pair up to have nonzero amplitudes.
			- The two kronecker deltas corresponds to two contractions.
## Evaluate Energy Expectations
	- $$< \hat{H}_{1}> =\sum _{kl} H_{kl}^{(1)}\left< \psi _{0}\left| \hat{a}_{k}^{\dagger }\hat{a}_{l}\right| \psi _{0}\right>=\sum _{k} H_{kk}^{(1)} n_{k}$$
		- The second equality follows ((64085b6c-2d37-476b-92d3-3527157ccbbf))
	- $$\begin{aligned}
	  < \hat{H}_{2}>  & =\frac{1}{2}\sum _{k_{1} l_{1} l_{2} k_{2}} H_{k_{1} l_{l} l_{2} k_{2}}^{(2)} < \hat{a}_{k_{1}}^{\dagger }\hat{a}_{l1}^{\dagger }\hat{a}_{l2}\hat{a}_{k_{2}}  >\\
	   & =\frac{1}{2}\sum _{kl}( U_{kl} -J_{kl}) n_{k} n_{l}
	  \end{aligned}$$
		- The first term is **diagonal** and the second term is **exchange**.
	- Express in the position representation,
	  $$
	  \begin{equation*}
	  H_{kk}^{(1)} =\int d^{3} r\ \psi _{k}^{*} (r)\left[ -\frac{\hbar ^{2}}{2m} \Delta +V(r)\right] \psi _{k} (r)
	  \end{equation*}
	  \\
	  \begin{equation*}
	  \begin{aligned}
	   & U_{kl} =\int d^{3} r_{1} d^{3} r_{2} \psi _{k}^{*}( r_{1}) \psi _{l}^{*}( r_{2})\frac{e^{2}}{\mid \overrightarrow{r_{1}} -\vec{r}_{2} \mid } \psi _{l}( r_{2}) \psi _{k}( r_{1})\\
	   & J_{kl} =\int d^{3} r_{1} d^{3} r_{2} \ \ \psi _{k}^{*}( r_{1}) \psi _{l}^{*}( r_{2})\frac{e^{2}}{\mid \overrightarrow{r_{1}} -\vec{r}_{2} \mid } \psi _{l}( r_{1}) \psi _{k}( r_{2})
	  \end{aligned}
	  \end{equation*}$$
	-
## Functional Derivative
	- Minimize wrt wavefunctions $\phi_k(r)$, with the constraint of normalization enforced by a Lagrangian multiplier.
		- $$\frac{\delta \left( E_{\mathrm{HF}} -\lambda \int d^{3}\mathrm{r} \ \phi _{k}^{*}( r) \phi _{k}( r)\right)}{\delta \phi _{v}^{*} (\mathbf{r} )} =0$$
	- $$
	  \begin{aligned}
	  {\left[\frac{-\hbar^2}{2 m} \nabla^2+\widehat{V}(\mathbf{r})+\sum_\lambda \int \mathrm{d} \mathbf{r}^{\prime} n_\lambda\left(\mathbf{r}^{\prime}\right) \frac{e^2}{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|}\right] \phi_\nu(\mathbf{r}) } \\
	  -\sum \int d\mathbf{r}^{\prime} \phi_\lambda^*\left(\mathbf{r}^{\prime}\right) \phi_\nu\left(\mathbf{r}^{\prime}\right) \frac{e^2}{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|} \phi_\lambda(\mathbf{r})=\lambda \phi_\nu(\mathbf{r})
	  \end{aligned}
	  $$
	-