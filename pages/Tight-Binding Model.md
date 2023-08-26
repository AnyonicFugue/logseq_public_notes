# Definition
	- Only adjacent hopping terms after second quantization
- # Certain Cases
	- ## 1D Chain
	- ## Square Lattice
		- $$
		  \hat{H}=-t \sum_{\left\langle ij \right\rangle}\left(\hat{c}_i^{\dagger} c_j+c . c .\right)
		  $$
		- By Fourier transformation, we can diagonalize the Hamiltonian and obtain $E_{\vec{k}}=-2 t\left[\cos \left(k_x a\right)+\cos \left(k_y a\right)\right]$.
	- ## Hexagonal Lattice
	  id:: 64e25c74-5efe-4b19-888d-d81eabc1c273
		- $$
		  \hat{H}=- \sum_{\left\langle ij \right\rangle}t_\alpha \left(\hat{c}_i^{\dagger} c_j+c . c .\right)
		  $$
			- $t_x,t_y,t_z$ are the couplings on x,y,z edges respectively.
		- Solution
			- Step 1. Divide the lattice into unit cells
				- Use Kitaev's convention: ((64c2c028-bfa3-41b9-bc70-d5f70b943a13))
			- Step 2. Perform the Fourier transformation
				- \begin{aligned}
				  c_{i\mu } & =\frac{1}{\sqrt{N}}\sum _{p} e^{ip\cdot r_{i}} c_{p\mu }\\
				  c_{i\mu }^{\dagger } & =\frac{1}{\sqrt{N}}\sum _{p} e^{-ip\cdot r_{i}} c_{p\mu }^{\dagger }\\
				  H & =-\sum _{< mn> } t_{\alpha }\left(\hat{c}_{m}^{\dagger } c_{n} +h.c.\right)\\
				  &  \begin{array}{l}
				  =-\sum _{i}\left\{t_{z}\left(\hat{c}_{i1}^{\dagger } c_{i2} +h.c.\right) +t_{x}\left(\hat{c}_{i1}^{\dagger } c_{i+n_{1} ,2} +h.c.\right) +t_{y}\left(\hat{c}_{i1}^{\dagger } c_{i+n_{2} ,2} +h.c.\right)\right\}\\
				  \text{Change to sum over unit cells and upper connections
				  - 1 stands for white and 2 stands for black}
				  \end{array}\\
				  & =-\sum _{i}\left\{\left[ t_{z}\hat{c}_{i1}^{\dagger } c_{i2} +t_{x}\hat{c}_{i1}^{\dagger } c_{i+n_{1} ,2} +t_{y}\hat{c}_{i1}^{\dagger } c_{i+n_{2} ,2}\right] +h.c.\right\}\\
				  & =-\sum _{i}\{[ t_{z}\left(\frac{1}{\sqrt{N}}\sum _{p} e^{-ip\cdot r_{i}} c_{p1}^{\dagger }\right)\left(\frac{1}{\sqrt{N}}\sum _{q} e^{iq\cdot r_{i}} c_{q2}\right) +t_{x}\left(\frac{1}{\sqrt{N}}\sum _{p} e^{-ip\cdot r_{i}} c_{p1}^{\dagger }\right)\left(\frac{1}{\sqrt{N}}\sum _{q} e^{iq\cdot ( r_{i} +n_{1})} c_{q2}\right)\\
				  & +t_{y}\left(\frac{1}{\sqrt{N}}\sum _{p} e^{-ip\cdot r_{i}} c_{p1}^{\dagger }\right)\left(\frac{1}{\sqrt{N}}\sum _{q} e^{iq\cdot ( r_{i} +n_{2})} c_{q2}\right)] +h.c.\}\\
				  & =-\frac{1}{N}\sum _{i}\sum _{p}\sum _{q}\left\{\left[ t_{z} e^{-ip\cdot r_{i}} e^{iq\cdot r_{i}} +t_{x} e^{-ip\cdot r_{i}} e^{iq\cdot ( r_{i} +n_{1})} +t_{y} e^{-ip\cdot r_{i}} e^{iq\cdot ( r_{i} +n_{2})}\right] c_{p1}^{\dagger } c_{q2} +h.c.\right\}\\
				  &  \begin{array}{l}
				  =-\frac{1}{N}\sum _{i}\sum _{p}\sum _{q}\left\{e^{-i( p-q) \cdot r_{i}}\left[ t_{z} +t_{x} e^{iq\cdot n_{1}} +t_{y} e^{iq\cdot n_{2}}\right] c_{p1}^{\dagger } c_{q2} +h.c.\right\} \ \ \\
				  \text{Extract the common exponential factor}
				  \end{array}\\
				  & =-\frac{1}{N}\sum _{p}\sum _{q}\left\{N\delta ( p-q)\left[ t_{z} +t_{x} e^{iq\cdot n_{1}} +t_{y} e^{iq\cdot n_{2}}\right] c_{p1}^{\dagger } c_{q2} +h.c.\right\} \ \ \text{Sum over i}\\
				  & =-\sum _{p}\left\{\left[ t_{z} +t_{x} e^{ip\cdot n_{1}} +t_{y} e^{ip\cdot n_{2}}\right] c_{p1}^{\dagger } c_{p2} +h.c.\right\} \ \ \text{Sum over q}
				  \end{aligned}
			- Step 3. Bogoliubov Transformation and obtain the spectrum
				- $$\mathbf{H}( p) =\begin{bmatrix}
				  0 & f( p)\\
				  f( p)^{*} & 0
				  \end{bmatrix}$$
				- id:: 64e41128-6e00-4aa8-baae-ad44016e1821
				  $$ \begin{array}{l}
				  f( p) =-\left[ t_{z} +t_{x} e^{ip\cdot n_{1}} +t_{y} e^{ip\cdot n_{2}}\right]\\
				  \varepsilon ( p) =\pm |f( p) |
				  \end{array}$$
				- Similar to Kitaev Honeycomb, pluggin in $x=f(p)$,
				  $$\begin{align*}
				  b_{p,\pm }^{\dagger } & =\frac{1}{\sqrt{2}}\left( c_{p,1}^{\dagger } \pm {\frac{f^{*}( p)}{|f( p)|}} c_{p,2}^{\dagger }\right)
				  \end{align*}$$
					- Note that there is a singularity iff $f(p)=0$.
				- It is always the minus mode (minus eigenvalue) to be occupied and the plus mode empty.
					-
				-
				- The result is almost exactly the same as Kitaev honeycomb... amazing.
	-