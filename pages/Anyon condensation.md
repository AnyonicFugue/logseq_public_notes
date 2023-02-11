- # Mathematical Description
	- ## Condensable bosons
	  id:: 63d873f9-1041-49a2-8b5a-1908f8fa53a8
		- Requirement #card
		  card-last-interval:: 27.15
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-03-08T14:11:36.282Z
		  card-last-reviewed:: 2023-02-09T11:11:36.282Z
		  card-last-score:: 5
			- $R_{a\bar a}^cR_{\bar a a}^c=1$ (bosonic) for **at least one** of the fusion channels of $a \otimes \bar a$
				- Note that it is the **double braiding**.
				- Why? #Learning-TODO
					- Maybe start from Wan's construction and derive a contradiction?
			-
	- ### Three steps
		- Identification
		  collapsed:: true
			- Identify the condensed anyon(s) $\{\gamma_i\}$ to the vacuum
			- Identify several anyons linked by the condensate as well
		- Splitting
		  collapsed:: true
			- If $a \times \bar{a}=1+\gamma_i+\ldots$, then $a\times \bar a$ contains orthogonal copies of the condensate vacuum.
			- This means $a$ must split in the condensed phase.
		- Confinement
			- Only $a$ with **at least one channel** in $a \otimes \gamma_i$ having trivial double braiding can survive.
				- ((63db212c-55c2-4693-a5c8-bb5713898e44))
			- Also, if $N_{\gamma_i, \gamma_i}^c>0$ and $c$ is not a boson, then $c$ is confined in the condensed phase.
				- Note that it is related to the condition of ((63d873f9-1041-49a2-8b5a-1908f8fa53a8))
	- ((63db223b-823d-4c25-8301-f669a6ff09cd))
		-
- # Topics
	- ## Gappability of boundaries
		- An interesting question: Could the boundary (to vacuum or to other phases) be gapped?
			- This turned out to be related to anyon condensation?!
		- Conclusion: Related by TSB <-> exists gappable boundaries
			- See [Burnell2017](((63db2524-002c-41f4-84d1-4a6c2cb6882a))) for some arguments.
				- First step: Use the [[Folding trick]] to reduce general boundaries to edges
			- ((63dc6611-b249-4a6b-9d84-61424d5eb2b0))
	- ## Relation to Domain walls
		-
- # Examples
	- ## ((63da0e16-0074-496a-952b-bd3534890de6)): Double Ising to [[Toric Code]] condensation #card
		- Note: We choose double Ising rather than Ising because $s_\psi=-1$. Pair two $\psi$ cancels the sign.
		- Choose $\psi_1\psi_2$ as the anyon to be condensed.
			- Confined anyons
				- Note 'confined' = Nontrivial double braiding
				- $\sigma_1,\sigma_2,\psi\sigma,\sigma\psi$
			- Deconfined ones
				- $\psi_1,\psi_2,\sigma_1\sigma_2$
			- Determine the new phase
				- [Wan]([[2021_Hu_Huang_Wan_Anyon Condensation]])'s approach
					- Find out the $+1$ eigenvectors for all $W_n(\psi_1\psi_2)$
					- But splitting cannot be obtained?
				- $\sigma_1\sigma_2$ **splits** into two flavors to resolve $\tilde{\sigma} \times \tilde{\sigma}=\tilde{1}+\tilde{1}+\tilde{\psi}+\tilde{\psi}$.
		- Result
			- $\begin{aligned} \tilde{\psi} \times \tilde{\psi}=1, \quad \tilde{\psi} \times \tilde{\sigma}_e=\tilde{\sigma}_m, & \tilde{\psi} \times \tilde{\sigma}_m=\tilde{\sigma}_e \\ \tilde{\sigma}_e \times \tilde{\sigma}_e=\tilde{\sigma}_m \times \tilde{\sigma}_m=1, & \tilde{\sigma}_e \times \tilde{\sigma}_m=\tilde{\psi}\end{aligned}$
			- Just toric code!
		- Splitting is determined by 'violation of fusion rule', which is problematic. #Learning-TODO
		  background-color:: red
- # Comments
	- ((63d87e90-19ca-426a-93d5-77c0b39eac21))
	- Why does the mathematical structure (not being first principles) fit so well with physics? #[[Thoughts/Math and Physics]]
		- Deeper structures behind?
	- ((63d8728e-64bc-4c90-aaf2-63efb1e11fac))
	- ((63d872bb-9d03-495a-8030-e76fb77eb849))
- # Misc
	- A critical point of the condensation
		- ((63aa5ee4-d8ac-4c34-aa3c-fe3a1d5c8ac9)) #Problem
			- Can we obtain the exchange domain wall from the trivial one?
		- ((63a95e51-a8e4-4bd3-bc50-77ce4d2dd60f))
- [[Condensation Completeness]]