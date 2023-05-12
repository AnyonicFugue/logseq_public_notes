- ![2022_Xu_Zheng_Zhai_Topological Micromotion of Floquet Quantum Systems.pdf](file://zotero_link/Research/Floquet/Floquet and Topology/2022_Xu_Zheng_Zhai_Topological Micromotion of Floquet Quantum Systems.pdf)
- # Setup
	- Effective Hamiltonian
		- $$
		  e^{-i \hat{H}_{\mathrm{F}}\left(\alpha_1\right) T}=\hat{\mathcal{T}} e^{-i \int_{\alpha_1 / \omega}^{\left(2 \pi+\alpha_1\right) / \omega} \hat{H}(t) d t}
		  $$
			- $\alpha_1$ is the chosen start time of a cycle.
	- Micromotion
		- $$
		  \hat{H}_{\mathrm{F}}\left(\alpha_1\right)=\hat{U}^{\dagger}\left(\alpha_2, \alpha_1\right) \hat{H}_{\mathrm{F}}\left(\alpha_2\right) \hat{U}\left(\alpha_2, \alpha_1\right)
		  $$
		- Physically, the difference between effective Hamiltonians if we select different start times.
- # General Theory
	- Key idea #card
		- The idea is to take the parameter $\alpha$ as yet another momentum (adding a dimension!) and calculate the topological invariants of the Brillouin zone.
			- For example, we can construct a map $BZ \to S^2$ by 
			  $$
			  \mathbf{n}(\mathbf{k})=\left\langle\varphi_{\mathbf{k}}|\sigma| \varphi_{\mathbf{k}}\right\rangle
			  $$
			  and the map can be classified by $\pi_3(S^2)$.
			- In principle we can also examine higher spheres and higher homotopy groups, but our space has only three dimensions, so such effort would not be too fruitful.
		- To summarize, the topological invariants of the $(n+1)-d$ Hamiltonian of the $nd$ system could protect $(n-1)d$ edge states.