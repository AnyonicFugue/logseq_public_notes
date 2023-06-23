- Assumptions of Landau Theory of Fermi Liquids #card
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-06-06T18:01:23.668Z
  card-last-reviewed:: 2023-05-06T12:01:23.668Z
  card-last-score:: 5
	- There is still a fermi surface of some shape
	- There are quasiparticle excitations near the fermi surface, which might decay.
	- Energy functional
		- $$
		  \delta E=\sum_{k \sigma} \varepsilon_k^0 \delta n_0(k)+\frac{1}{2 v} \sum_{k_1 k_2 \sigma_1 \sigma_2} f_{\sigma_1, \sigma_2}\left(k_1, k_2\right) \delta n_{\sigma_1}\left(\vec{k}_1\right) \delta n_{\sigma_2}\left(\vec{k}_2\right)
		  $$
		- The first term is 1-body energy.
			- $\varepsilon_k^0=\frac{k_F}{m^*}\left(k-k_F\right)$, where $m*$ is the ^^effective mass^^.
		- The second term is 2-body part.
			- $$
			  \begin{aligned}
			  & f_{\uparrow \uparrow}\left(\vec{k}, \overrightarrow{k^{\prime}}\right)=f^s(\vec{k}, \vec{k'})+f^a\left(\vec{k}, \overrightarrow{k^{\prime}}\right) \\
			  & f_{\downarrow \uparrow}\left(\vec{k}, \overrightarrow{k^{\prime}}\right)=f^s-f^a
			  \end{aligned}
			  $$
			- We may expand by Legendre polynomials (which is a complete set):
			  $$
			  f^{a / s}\left(\vec{k}_1, \vec{k}_2\right)=\sum_{l=0}^{\infty} f_l^{\alpha / s} P_l(\cos \theta)
			  $$
		- Also could be comprehended as a series expansion.
- Square law of lifetime #card
  card-last-interval:: 30
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-06-28T13:57:21.438Z
  card-last-reviewed:: 2023-05-29T13:57:21.439Z
  card-last-score:: 5
	- Consider some electron with energy $\epsilon$ above the fermi surface. 
	  It could decay by scattering with another electron slightly below the fermi surface.
	- $$\frac{1}{\tau } \varpropto \Gamma \varpropto |u|^{2}\int d^{3}\vec{p}_{1} d^{3}\vec{p}_{2}F(p_1,p_2)[1-f( \varepsilon _{p_{1}})] f( \varepsilon _{p_{2}})[ 1-f( \varepsilon _{p-p_{1} +p_{2}})] \delta (\Sigma\varepsilon )$$
		- $f$ is the occupation number. $F$ is the cross section between $p_1$ and $p_2$.
		- $$(p,p_2) \to (p_1,p-p_1+p_2)$$
	- Obviously the volume of the phase space is proportional to $\epsilon^2$.
- Calculate physical quantities
	- Heat capacity at low temperatures #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-07-28T12:05:20.771Z
	  card-last-reviewed:: 2023-05-05T12:05:20.772Z
	  card-last-score:: 5
		- First calculate the energy of a certain configuration. The heat capacity would be known once the state density is known.
			- $$\begin{aligned}
			  \delta E^{(2)} & =\frac{1}{2V}\sum _{\theta _{1} \theta _{2} \sigma _{1} \sigma _{2}} f_{\sigma _{1} \sigma _{2}( \theta _{1} ,\theta _{2})}\sum _{| \vec{k}_{1}| | \vec{k}_{2}| } \delta n_{\sigma _{1}}(\vec{k}_{1}) \delta n_{\sigma _{2}}(\vec{k}_{2})\\
			   & =\frac{1}{2V}\sum _{\theta _{1} \theta _{2} \sigma _{1} \sigma _{2}} f_{\sigma _{1} \sigma _{2}}( \theta _{1} ,\theta _{2})\left[\sum _{| \vec{k}_{1}| } \delta n_{\sigma _{1}}(\vec{k}_{1})\right]\left[\sum _{| \vec{k}_{2}| } \delta n_{\sigma _{2}}(\vec{k}_{2})\right]
			  \end{aligned}$$
				- Approx: At low temperature $k_1,k_2$ would be close to the fermi surface, thus $f$ only depends on the angles, not the norms.
			- Therefore the 2-body part is zero, only the 1-body part remains.
			- The heat capacity can be calculated like free fermions (by inserting the effective mass).
			  background-color:: yellow
		- Note that Fermi-Dirac distribution shall be used since we're dealing with fermions!
		  background-color:: red
			- Never see anything like $e^{-\beta E}$.
		- Experimentalists often use this method to obtain the effective mass.
	- Susceptibility #card
	  card-last-interval:: 117.6
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-10-13T15:08:24.741Z
	  card-last-reviewed:: 2023-06-18T01:08:24.742Z
	  card-last-score:: 5
		- Idea
			- First obtain the dependence of $E_0$ on $m$.
			- Since $E=E_0-m\cdot h$, m would be obtained by minimizing the total energy.
				- $\frac{\partial E}{\partial m}=m(h) \cdot \frac{\partial^2 E}{\partial m^2} {=} h$.
				- Note that $\frac {\partial E}{\partial m}=0$ when $m=0$.
			- $\chi$ could be obtained by $m=h\cdot \chi$.
				- $\chi=\left(\frac{\partial^2 E}{\partial m^2}\right)^{-1}$
		- With external field, $N_{\uparrow } \neq N_{\downarrow } ,\ \ N_{\uparrow } +N_{\downarrow } =N$
		- Suppose the fermi surface shifts from the original one by $\delta_k$
			- $$M=\mu_B \cdot\left(\delta N_{\uparrow}-\delta N_\downarrow\right) \Rightarrow \delta k_F=\frac{\lambda^2 M}{\mu_B k_F^2 V}$$
			- Take $V=1$ for simplicity.
		- Obviously the energy shift $\delta E \sim \delta k_F^2$
			- $\delta E_1$ can be calculated like free fermions, just inserting the effective mass.
			- $\delta E^{(2)}=\frac{1}{2 V} \Sigma f_{\sigma_1 \sigma_2}\left(k_1, k_2\right) \delta n_{k_1 \sigma_1} \delta n_{k_2 \sigma_2}$
				- Insert the expansion by Legendre polynomials, $\delta E_2=V\left(\frac{k_f^2}{2 \pi^2}\right)^2\left(\delta k_f\right)^2 \cdot 2 f_0^a=\frac{f_0^a}{\mu_B^2} \frac{M^2}{2 V}$
				- $\mu_B$ is the Bohr magneton, the magnetic moment of a single electron.
			-
- Fermi surface nesting
	- Large segments of a Fermi surface that can be connected to another large segment of another Fermi surface via the reciprocal lattice vector.
	- ![](https://pica.zhimg.com/80/v2-3f777e9aeff5c939327564d80d4b7b4b_720w.webp?source=1940ef5c)
	-