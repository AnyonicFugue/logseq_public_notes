-
- Ref. Peskin, 7.4
-
- Statement #card
  card-last-interval:: 24
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2023-04-07T11:55:53.353Z
  card-last-reviewed:: 2023-03-14T11:55:53.353Z
  card-last-score:: 5
	- Often, in the literature, the terms Ward identity, current conservation, and gauge invariance are used interchangeably.
	- Ward identity
		- If $\mathcal{M}(k)=\epsilon_\mu(k) \mathcal{M}^\mu(k)$ is the amplitude for some QED process involving an external photon with momentum $k$, then this amplitude vanishes if we replace $\epsilon_\mu$ with $k_\mu$ :
		  $$
		  k_\mu \mathcal{M}^\mu(k)=0 .
		  $$
- Peskin's approach
	- ((639c19fd-0bc8-4158-b306-449808d8cc43))
	- ((639c1a34-720a-4d01-9557-a61654f6da69))
		- ((639c1ae8-fbe6-495f-a51d-be6713390636))
			- Why not general electron lines?
			  background-color:: red
			- Electron lines must be 'one in one out'. So they either end at external points or form loops.
		- ((639c1a49-f37f-43bb-8509-d84f56eaa040))
	- The insertion to external lines
		- ((639c1ca9-d209-4386-9b6a-98adbe8a45cb))
		- ((639c1c8e-84c0-47cd-b43c-63c454b77a8c))
		- ((639c1c9b-7ebd-4dbd-b6cf-023a1da51739))
		- ((639c1cb4-5bf9-4b83-9e1e-7d7509eae389))
			- ((639c1cdf-53ff-4aeb-8be6-2bd17a1bb8e4))
		- ((639c1d0a-3c14-4a60-b2e4-b0423d65c57e)) #Learning-TODO
			- ((639c1d1a-49ff-4733-9331-55f5be67f5e9))
		- ((639c1d9c-f2b6-4816-a9db-475dc983e7af))
			- ((639c1db7-2982-4b0c-bb8d-90bfdd9e4111))
		-
	- The insertion to electron loops
		- The technique is similar: insertions at adjacent lines always cancel the adjacent terms.
		- Everything is cancelled since loops have no endpoints.
	- Example of usage
		- ((639c1ef4-a31a-46bd-b64e-db0bfba92723))
			- Right side are **exact** photon propagators. $S(p)=\frac{i}{\not p-m-\Sigma(p)}$
		- ((639c1f57-6e0a-416d-80d8-25daf677d731))
		- ((639c1f66-e1b0-47d9-9b7a-182e3b35fbbc))
			- Equivalently, ((639c1f7f-0a10-4225-b252-863044e988db))
		- Relation to renormalization factors
			- $\Gamma^\mu(p+k, p) \rightarrow Z_1^{-1} \gamma^\mu$ #Learning-TODO
			- $S(p) \sim \frac{i Z_2}{\not p-m}$
			- ((639c1fcb-ea18-4fb5-80d8-c9169634cca4)) 
			  $$
			  \begin{aligned}
			  -i Z_1^{-1} \not k & =i Z_2^{-1} \not k \\
			  Z_1 & =Z_2
			  \end{aligned}
			  $$
				- This doesn't seem so elegant as Satoshi claims?
- Satoshi's approach
	- $$
	  j_\mu=e \bar{\psi} \gamma_\mu \psi, \quad \partial_\mu j^\mu=0
	  $$
	- Quantity of interest:
		- $$
		  \partial_x^\mu\left\langle 0\left|T j_\mu(x) \psi\left(x_1\right) \bar{\psi}\left(y_1\right) \cdots \psi\left(x_n\right) \bar{\psi}\left(y_n\right) A_{v_1}\left(z_1\right) \cdots A_{v_p}\left(z_p\right)\right| 0\right\rangle
		  $$
		- Why we are interested in this?
		  background-color:: red
			- In QFT, everything can be obtained from correlation functions.
			- $\partial$ is the momentum operator in position space
	- ((639c26b2-9024-40b8-83d1-bbdc1e38189f))
	- On the other hand, 
	  $$
	  \begin{aligned}
	  & {\left[j_0(x), \psi\left(x^{\prime}\right)\right] \delta\left(x^0-x^{\prime 0}\right)=-e \psi(x) \delta^{(4)}\left(x-x^{\prime}\right)} \\
	  & {\left[j_0(x), \bar{\psi}\left(x^{\prime}\right)\right] \delta\left(x^0-x^{\prime 0}\right)=e \bar{\psi}(x) \delta^{(4)}\left(x-x^{\prime}\right)} \\
	  & {\left[j_0(x), A_\mu\left(x^{\prime}\right)\right] \delta\left(x^0-x^{\prime 0}\right)=0}
	  \end{aligned}
	  $$
		- Directly from CCR
		- ((639c26f7-b208-49c8-a94b-7075007f4ac6))
	- ## Final result: Ward-Takahashi identity
		- $$
		  \begin{aligned}
		  & \partial_x^\mu\left\langle 0\left|T j_\mu(x) \psi\left(x_1\right) \cdots \bar{\psi}\left(y_n\right) A_{v_1}\left(z_1\right) \cdots A_{v_p}\left(z_p\right)\right| 0\right\rangle \\
		  = & e\left\langle 0\left|T \psi\left(x_1\right) \cdots A_{v_p}\left(z_p\right)\right| 0\right\rangle \sum_{i=1}^n\left[\delta^{(4)}\left(x-y_i\right)-\delta^{(4)}\left(x-x_i\right)\right]
		  \end{aligned}
		  $$
			- $\bar\psi$ creates positive charge, $\psi$ creates negative charge
			-
	- #+BEGIN_EXAMPLE
	  Example of Usage
	  #+END_EXAMPLE
		- $n=0,p=1$: photon propagator
			- ((639c282f-4856-49bc-bfd1-3bd48c4fb75d))
				- First, what does 'apply the green function' mean?
				- Second, what does the second diagram mean?
		- $n=1, p=0$: [[Electron Vertex Function]]
		-
- [[To be recorded]]
	- Merge with [[Ward-Takahashi Identity]]
- Since the matrix element shall be covariant and depend linearly on the polarization of the photon, we have ((637ae3b2-dbda-4df2-99bd-8898eb7feb07))
	- Also derivable from the Feynman rules.
- Theorem #card
  card-last-score:: 5
  card-repeats:: 3
  card-next-schedule:: 2023-04-13T21:07:05.045Z
  card-last-interval:: 61.44
  card-ease-factor:: 2.56
  card-last-reviewed:: 2023-02-11T11:07:05.045Z
	- ((637ae474-2d53-4e11-b973-cd140e269b7f)) for photons.
		- Note that this also holds for off-shell [[Photon]]!
		-