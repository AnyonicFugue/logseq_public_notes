alias:: Gauge Theory

- [What is a gauge? | Teherence Tao](https://terrytao.wordpress.com/2008/09/27/what-is-a-gauge/)
- # Motivations
	- When we try to construct theories like $A^\mu A^\nu \partial_\mu A_\nu$ or $A^4$, we would encounter negative norms.
		- The problem is absent in QED because ((640458fa-7092-47a3-a5db-acb4759ce58a)).
		- This follows from [[Ward identity]], which in turn follows from **gauge invariance**. #Learning-TODO/Course
		- Thus it's natural to consider other theories with some sorts of gauge invariance.
	- .3
	-
- # Examples
	- Reconstruct [[QED]] from a viewpoint of gauge invariance
		- It is striking that the covariant derivative, the field $A^\mu$ and subsequently the interaction term could emerge from such a simple principle!
		-
		- Recall that 
		  $\begin{aligned} \mathcal{L}_{\text {QED }} & =\mathcal{L}_{\text {Dirac }}+\mathcal{L}_{\text {Maxwell }}+\mathcal{L}_{\text {int }} \\ & =\bar{\psi}(i \not \partial-m) \psi-\frac{1}{4} F_{\mu \nu} F^{\mu \nu}-e \bar{\psi} \gamma^\mu \psi A_\mu\end{aligned}$
		- It is invariant under a **global** gauge transformation $\psi(x) \rightarrow e^{i \alpha} \psi(x)$, but **not** under a **local** gauge transformation $\psi(x) \rightarrow e^{i \alpha(x)} \psi(x)$.
			- Obviously the problem is that the derivative isn't covariant. $\partial_\mu \psi(x) \rightarrow \partial_\mu\left[e^{i \alpha(x)} \psi(x)\right]=e^{i \alpha(x)}\left[i \partial_\mu \alpha(x)\right] \psi(x)+e^{i \alpha(x)} \partial_\mu \psi(x)$
		- We need a ((640439cc-078f-40ee-9eee-b9677c4ca2d2)) to write useful derivative terms.
			- In differential geometry, 'covariant' means independent of the specific coordinate system. 
			  Similarly, here it means independent of the specific gauge choice.
			- The transformation law shall be $D_\mu \psi(x) \rightarrow e^{i \alpha(x)} D_\mu \psi(x)$.
		- It can be easily constructed if we have a ((640439c2-364e-4189-bae8-743a984441f4)).
			- That is, some $U(y, x)$ transforming as $U(y, x) \longrightarrow e^{i \alpha(y)} U(y, x) e^{-i \alpha(x)}$
				- Exercise. Examine this transformation law indeed produces a covariant derivative. #card
		- A natural choice is to take the integral curve of $A_\mu$.
			- $U(y, x)=\exp \left[-i e \int_\gamma A_\mu(x) d x^\mu\right]$
			  id:: 6404430c-1c1c-40a7-a9f6-977362c15589
				- Obviously $A_\mu$ must also transform.
				- Exercise. Prove its law of transformation. #card
					- Hint: Examine the infinitesimal behavior.
					- Answer: {{cloze $A^\mu(x) \rightarrow A^\mu(x)-\frac{1}{e} \partial^\mu \alpha$}}
			- This also absorbs the interaction term into the derivative!
		- Conclusion
			- $\mathcal L=-\frac{1}{4} F^{\mu \nu} F_{\mu \nu}+\bar{\psi}\left(i \gamma^\mu D_\mu-m\right) \psi$
			- $D^\mu=\partial_\mu+i e A_\mu$
		- Comments
			- $\left[D_\mu, D_\nu\right]=ieF_{\mu\nu}$ is precisely the ((640439ca-6d19-4064-9b93-f90d6ed0948e))!
			- Generally ((6404430c-1c1c-40a7-a9f6-977362c15589)) may not be path-independent. This is directly related to [[Berry Phase]].
			- Moreover, $A_\mu A^\mu$ **cannot** appear without breaking the gauge invariance.
			- In principle there can also be $\varepsilon^{\alpha \beta \mu \nu} F_{\alpha \beta} F_{\mu \nu},\left(F_{\mu \nu} F^{\mu \nu}\right)^2$, etc. But they violate symmetries like $P$ or $T$, or not renormalizable.
			  id:: 64045b5c-6fea-4ab6-8155-7c5cce369a40
	- [[Strong Interaction]]
	- [[Weak Interaction]]
	-
- ez