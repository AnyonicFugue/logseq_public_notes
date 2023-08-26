alias:: [[Ising]]

- # Quantum
	- $H_I=-J g \sum_i \hat{\sigma}_i^x-J \sum_{\langle i j\rangle} \hat{\sigma}_i^z \hat{\sigma}_j^z$
- # Map to $\phi^4$ Theory
	- See ((64e76507-d1d7-4ed7-98af-a55ca862caa7)) in Altland.
	- Summary
	  collapsed:: true
		- Start from the classical partition function
		  $$
		  \mathcal{Z}=\sum_{\left\{S_i\right\}} e^{\sum_{i j} S_i K_{i j} S_j+\sum_i h_i S_i}
		  $$
		- Remove the interaction at the cost of introducing a new field (i.e. a Gaussian integration)
	- Derivation
		- Proposition. Fat unity:
		  $$
		  1=\mathcal{N} \int D \psi e^{-\frac{1}{4} \sum_{i j} \psi_i\left(K^{-1}\right)_{i j} \psi_j}
		  $$ #card
			- The technique of 'inserting a unity' #Techniques
			- Note that $\psi$ is a n-component field.
		- Shift the integration variables in the fat unity to cancel spin-spin interactions
		  collapsed:: true
			- $$
			  \psi_i \rightarrow \psi_i-2 \sum_j K_{i j} \mathbf{S}_j
			  $$
			- $$
			  1=\mathcal{N} \int D \psi e^{-\frac{1}{4} \sum_{i j} \psi_i\left(K^{-1}\right)_{i j} \psi_j+\sum_i S_i \psi_i-\sum_{i j} S_i K_{i j} S_j}
			  $$
		- Insert the fat unity into the spin sum in the classical partition function:
		  collapsed:: true
		  $$
		  \begin{aligned}
		  \mathcal{Z}&=\mathcal{N} \int D \psi \sum_{\left\{S_i\right\}} e^{-\frac{1}{4} \sum_{i j} \psi_i\left(K^{-1}\right)_{i j} \psi_j+\sum_i S_i\left(\psi_i+h_i\right)} \\
		  & =\mathcal{N} \int D \psi e^{-\frac{1}{4} \sum_{i j} \psi_i\left(K^{-1}\right)_{i j} \psi_j} \prod_i\left(2 \cosh \left(\psi_i+h_i\right)\right) \\
		  & =\mathcal{N} \int D \psi e^{-\frac{1}{4} \sum_{i j}\left(\psi_i-h_i\right)\left(K^{-1}\right)_{i j}\left(\psi_j-h_j\right)+\sum_i \ln \left(\cosh \psi_i\right)}
		  \end{aligned}
		  $$
			- In the last step we shifted the field $\psi_i \to \psi_i-h_i$
			- Also we threw away unimportant factors of 2.
		- Change the interaction variable from $\psi_i$ to $\phi_i \equiv \frac{1}{2} \sum_j\left[K^{-1}\right]_{i j} \psi_j$:
		  $$
		  \mathcal{Z}=\mathcal{N} \int D \phi e^{-\sum_{i j} \phi_i K_{i j} \phi_j+\sum_i \phi_i h_i+\sum_i \ln \cosh \left(2 \sum_j K_{i j} \phi_j\right)}
		  $$
		- The following is making approximations and perform the Fourier transformation.
			- Low-temperature limit: $\beta \to \infty$
			- we switch to a Fourier representation, 
			  $$\phi _{i} =\frac{1}{\sqrt{N}}\sum _{\mathbf{k}} e^{-i\mathbf{k} \cdot \mathbf{r}_{i}} \phi (\mathbf{k} ),K_{ij} =\frac{1}{N}\sum _{\mathbf{k}} e^{-i\mathbf{k} \cdot (\mathbf{r}_{i} -\mathbf{r}_{j})} K(\mathbf{k} )$$
				- Expand $\ln\cosh (x)=$ $\frac{1}{2} x^{2} -\frac{1}{12} x^{4} +\cdots$.
				- Noting that $(K\phi )(\mathbf{k} )=K(\mathbf{k} )\phi (\mathbf{k} )=K(0)\phi (\mathbf{k} )+\frac{1}{2}\mathbf{k}^{2} K^{\prime \prime } (0)\phi (\mathbf{k} )+\mathcal{O}\left(\mathbf{k}^{4}\right)$.
			- collapsed:: true
			  $$\begin{aligned}
			  S[\phi ] & =\sum _{\mathbf{k}}[ \phi _{\mathbf{k}}( c_{1} +c_{2}\mathbf{k} \cdot \mathbf{k}) \phi _{-\mathbf{k}} +c_{3} \phi _{\mathbf{k}} h_{-\mathbf{k}}]\\
			   & +\frac{c_{4}}{N}\sum _{\mathbf{k}_{1} ,\dotsc ,\mathbf{k}_{4}} \phi _{\mathbf{k}_{1}} \phi _{\mathbf{k}_{2}} \phi _{\mathbf{k}_{3}} \phi _{\mathbf{k}_{4}} \delta _{\mathbf{k}_{1} +\mathbf{k}_{2} +\mathbf{k}_{3} +\mathbf{k}_{4} ,\mathbf{0}} +\mathcal{O}\left(\mathbf{k}^{4} ,h^{2} ,\phi ^{6}\right)
			  \end{aligned}$$
				- Proof
					- \begin{equation*}
					  \begin{aligned}
					  \mathcal{Z} & =\mathcal{N}\int D\phi e^{-\sum _{ij} \phi _{i} K_{ij} \phi _{j} +\sum _{i} \phi _{i} h_{i} +\sum _{i}\ln\cosh\left( 2\sum _{j} K_{ij} \phi _{j}\right)}\\
					  S[ \phi ] & =-\sum _{ij} \phi _{i} K_{ij} \phi _{j} +\sum _{i} \phi _{i} h_{i} +\sum _{i}\ln\cosh\left( 2\sum _{j} K_{ij} \phi _{j}\right)\\
					  \sum _{ij} \phi _{i} K_{ij} \phi _{j} & =\sum _{k_{1} k_{2} k_{3}}\frac{1}{\sqrt{N}} e^{-i\mathbf{k}_{1} \cdot \mathbf{r}_{i}} \phi (\mathbf{k}_{1} )\frac{1}{N} e^{-i\mathbf{k}_{2} \cdot (\mathbf{r}_{i} -\mathbf{r}_{j})} K(\mathbf{k}_{2} )\frac{1}{\sqrt{N}} e^{-i\mathbf{k}_{3} \cdot \mathbf{r}_{j}} \phi (\mathbf{k}_{3} )\\
					  & =\frac{1}{N^{2}}\sum _{k_{1} k_{2} k_{3}} e^{-i(\mathbf{k}_{1} +\mathbf{k}_{2}) \cdot \mathbf{r}_{i}} e^{-i(\mathbf{k}_{3} -\mathbf{k}_{2}) \cdot \mathbf{r}_{j}} \phi (\mathbf{k}_{1} )K(\mathbf{k}_{2} )\phi (\mathbf{k}_{3} )\\
					  & =\sum _{k} \phi (-\mathbf{k} )K(\mathbf{k} )\phi (\mathbf{k} )\\
					  & \text{Similar for other terms.}
					  \end{aligned}
					  \end{equation*}
	- The final result is 
	  \begin{equation*}
	  S[\phi ] =\int d^{d} x\left( c_{2} (\partial \phi )^{2} +c_{1} \phi ^{2} +c_{3} \phi h+c_{4} \phi ^{4}\right)
	  \end{equation*}
		- The coefficients $c_{i}$ are given by $c_{1} =K(0)(1-2K(0)),c_{2} =\frac{1}{2} K^{\prime \prime } (0)(1-$ $4K(0)),c_{3} =1,c_{4} =\frac{4K(0)^{4}}{3}$
		-