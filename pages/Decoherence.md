- [[To be recorded]]
- Def
	- Interaction with the environment destroys the superposition.
- Kraus operator
  collapsed:: true
	- ((6371e60d-7b26-47f7-b159-0c11111473aa))
	  Where U is some evolution of the **total** system.
	- ((6371e616-f41d-4b6c-b9dd-e8d497df9ebf))
		- The map $$S:\rho_1 \mapsto \rho_1'$$ is called ((6371e68c-e4f9-4b7b-870e-5a144d39cb75))
		- The map always maps a [[Density operator]] to another one. #Exercise
	- ((6371e642-3c01-46d2-a2c0-96edf6427116))
	-
	- The superoperator may not be unique for a certain evolution process.
	  collapsed:: true
		- ((6371e911-0164-4324-ae66-8e5cbf37235c))
		-
- Unitary representatin
	- The Kraus operator describes the evolution of a part of the total system. Conversely, every Kraus operator can be realized by some auxiliary system.
	- ((6371e7d3-d374-47c1-a89b-ce34438d0fde))
		- It's easy to verify that U preserves the inner product.
		- Since it's unitary on a subspace, it can be extended to a unitary on the whole space.
	- Explanation:
	  It is a classical mix of different $$E_k|\psi\rang_1$$, with probability given by the norms.
		- $E_k$ isn't unitary. So the probabilities may not be equal.
		-
- How many real parameters do we need?
  collapsed:: true
	- The space of $$N\times N$$ hermitian matrices is $$N^2$$ dimensional, so the operators have a $$N^4$$ dimensional.
	- The condition $$\sum_k E_k^{\dagger} E_k=I_1$$ gives $$N^2$$ constraints.
- ((6371e882-ad08-48df-88ac-75d509d76dd3))
	- This means that some information are lost during the evolution. We can't invert the course.
-
- Summary things above
  collapsed:: true
	- ((6371ea3c-0625-4214-81ab-33b4686111af))
		- ((6371ea71-a3bc-411d-bcf4-a811275e20dd))
		- ((6371ecae-1cc5-4b1d-b7e1-96e4620bd9eb))
			- This means that we can trace out the environment, write down the superoperator of the first system, then happily invoke the fundamental theorem.
	- Thus we have 3 equivalent forms of representation.
-
- A simple example: ((6371ef6a-5e46-4055-b681-c39202268236))
	- Setting
		- Environment=System=Single qubit
		- $$|\psi\rangle=\alpha|0\rangle+\beta|1\rangle$$
		  $$\rho=\left[\begin{array}{cc}
		  |\alpha|^2 & \alpha \beta^{\star} \\
		  \alpha^{\star} \beta & |\beta|^2
		  \end{array}\right]$$
			- Diagonal term -> 'populations',
			  Off-diagonal terms -> 'coherences'
	- After a CNOT between the system and the environment:
	  collapsed:: true
	  $$\left|\Psi^{\prime}\right\rangle=\alpha|00\rangle+\beta|11\rangle$$
	  $$\rho^{\prime}=\operatorname{Tr}_{\mathrm{env}}\left[\left|\Psi^{\prime}\right\rangle\left\langle\Psi^{\prime}\right|\right]=\left[\begin{array}{cc}
	  |\alpha|^2 & 0 \\
	  0 & |\beta|^2
	  \end{array}\right]$$
		- The coherences are destroyed. The system becomes a classical probabilistic superposition.
		- The system becomes entangled with the environment.
		- Some information is leaked into the environment. We can't extract all initial information only from the system.
	- Quantum black box: Invoke [[Bloch sphere]]
	  collapsed:: true
		- ((6371f1af-be03-465f-816d-7246f0494a66))
		- ((6371f1b9-067f-4072-b19e-3b787cd465c9))
		  Called the **affine map**.
		-
		- #+BEGIN_NOTE
		  M might not be orthogonal, i.e. not a rotation.
		  By SVD, nevertheless, it is a rotation plus a inhomogeneous scaling.
		  #+END_NOTE
		-
		-
	- We may use a quantum circuit to simulate a given type of noise.
		- ((6371f38f-c95e-4d59-a4d8-237a069a12e7))
			- System is rho. Ancillary bit is psi.
			- Intuitively, the 3 controlled gates changes the 3 coordinates of the Bloch sphere respectively.
				- #+BEGIN_WARNING
				  No cross terms. Only rescale 3 coordinates independently.
				  Therefore, not all noises can be realized by the circuit.
				  #+END_WARNING
		- Effect
		  collapsed:: true
			-
			- ((6371f3bf-7f5d-4f59-aa03-954d582fd946))
			- ((6371f3c9-1faf-4ec3-b235-c6b1e94836d4))
			- Then: 
			  $$U=\left[\begin{array}{cccc}
			  \sigma_x & 0 & 0 & 0 \\
			  0 & \sigma_y & 0 & 0 \\
			  0 & 0 & \sigma_z & 0 \\
			  0 & 0 & 0 & I
			  \end{array}\right]$$
			- ((6371f40b-e654-45ae-b11a-896899fd070f))
		- Some channels
			- Rule:
			  **Entanglement with the environment -> Classical probability within the system**
			- Bit-flip
			  collapsed:: true
				- ((6371fb39-a453-44c0-8971-ed5e450e6787))
				- Flip z direction with probability $$|\alpha|^2$$
			- Phase-flip
				- $$\alpha=\beta=0$$
				- Add a relative phase
			- Bit-phase flip
			  collapsed:: true
				- $$\alpha=\gamma=0$$
				- Note 
				  $$\sigma_y=\left(\begin{array}{cc}
				  0 & i \\
				  -i & 0
				  \end{array}\right)$$
			- Depolarization
			  collapsed:: true
				- $$|\alpha|^2=|\beta|^2=|\gamma|^2=p / 3$$
				- Reverse each direction probabilistically.
				  When $$p=3/4$$, $$\boldsymbol{r}^{\prime}=(0,0,0) \text { for any } \boldsymbol{r}$$
				- #+BEGIN_NOTE
				  The condition is $$|\alpha|^2=|\beta|^2=|\gamma|^2=1/4$$, not $$1/2$$. 
				  Because $$\sigma_x$$ doesn't affect x (only add $$\pi$$ to the relative phase), but add a minus to both y and z.
				  #+END_NOTE
				-
			- Amplitude damping
			  collapsed:: true
				- ((6371fe7e-8fc1-482f-b505-582cb00d99cc))
					- Intuitively: $$|0\rangle\lang0|$$ is always retained, while $$|1\rangle\lang1|$$ is flipped with probability p.
				- ((6371fea4-5d43-4319-8730-5a36d3d746fe))
				- Thus p represents the probability that $$|1\rangle \text { decays to }|0\rangle$$
				-
			- Phase damping
			  collapsed:: true
				- The same as phase-flip
			- *De-[[Entanglement]] (actually 2-qubit)
				- ((63720490-57d6-4fac-acdf-f0227800dd0a))
				- When $$\theta=\pi/2$$, the operation makes the Bell state a classical mix, which is 'de-entangle'.
					- Intuitively: $$F_0$$ selects the second bit being 0,
					  id:: 637204c0-0117-40dc-8aa6-2edd3de193c7
					  while $$F_1$$ selects the second bit being 1.