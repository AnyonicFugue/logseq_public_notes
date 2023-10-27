type:: [[Course]]

-
- Exercises #Learning-TODO
	- Prove that [[Completely Positive]] is stronger than positive.
		- $|\psi\rangle_{S E}=\frac{1}{\sqrt{2}}\left(|0\rangle_S|1\rangle_E+|1\rangle_S|0\rangle_E\right)$
		- The partial trace $T_s\left(\rho_s\right)=\rho_s^{T}$ is positive but not completely positive.
		- Note that writing out the density matrix is the simplest here.
- Def
	- Interaction with the environment destroys the superposition.
	- In short, when tracing out the environment, the superposition degenerates to a classical probability.
- Kraus operator
  id:: 63840eb6-970a-4787-ad25-13a3cc29ece5
	- Def #card
	  card-last-interval:: 252.3
	  card-repeats:: 4
	  card-ease-factor:: 2.9
	  card-next-schedule:: 2024-01-07T07:55:26.428Z
	  card-last-reviewed:: 2023-04-30T00:55:26.429Z
	  card-last-score:: 5
		- $E_k \equiv{ }_2\langle k|U| 0\rangle_2$
			- U is some evolution of the **total** system.
			- 0 is the initial state of the environment
		- $\rho_1^{\prime}=\sum_k E_k \rho_1 E_k^{\dagger}$
			- Essentially tracing out the environment.
			- For a pure state $|\psi\rang$, the final state is a classical mix of $E_k|\psi\rang$
			- The map $$S:\rho_1 \mapsto \rho_1'$$ is called ((6371e68c-e4f9-4b7b-870e-5a144d39cb75))
			- The map always maps a [[Density operator]] to another one. #Exercise
		- $\sum_k E_k^{\dagger} E_k=\sum_k{ }_2\left\langle 0\left|U^{\dagger}\right| k\right\rangle_2{ }_2\langle k|U| 0\rangle_2={ }_2\left\langle 0\left|U^{\dagger} U\right| 0\right\rangle_2=I_1$
	- Equivalence of 2 sets of Kraus operators #card
	  card-last-interval:: 329.28
	  card-repeats:: 4
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2024-07-16T19:00:42.729Z
	  card-last-reviewed:: 2023-08-22T13:00:42.730Z
	  card-last-score:: 5
		- Two superoperators $\mathbb{S}\left(\rho_1\right)=\sum_k E_k \rho_1 E_k^{\dagger}$ and $\mathbb{S}^{\prime}\left(\rho_1\right)=\sum_k F_k \rho_1 F_k^{\dagger}$ are equivalent if and only if there exists a **unitary** matrix $W$ such that $F_i=\sum_j W_{i j} E_j$.
			- Essentially, W is the basis transformation between two bases of the environment.
- Unitary representation
  collapsed:: true
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
  collapsed:: true
	- This means that some information are lost during the evolution. We can't invert the course.
-
- Summary things above
	- The Kraus representation theorem #card
	  card-last-interval:: 297.18
	  card-repeats:: 4
	  card-ease-factor:: 2.66
	  card-next-schedule:: 2024-08-14T04:39:51.583Z
	  card-last-reviewed:: 2023-10-22T00:39:51.583Z
	  card-last-score:: 3
		- ((6371ea3c-0625-4214-81ab-33b4686111af))
			- [[Completely Positive]] means $\mathbb{S} \otimes \mathbb{I}_E$ is positive for arbitrary E, which is stronger than positive.
			- ((6371ecae-1cc5-4b1d-b7e1-96e4620bd9eb))
				- This means that we can trace out the environment, write down the superoperator of the first system, then happily invoke the fundamental theorem.
	- Thus we have 3 equivalent forms of representation.
- Noisy quantum channels ((6371ef6a-5e46-4055-b681-c39202268236))
  collapsed:: true
	- Setting
	  collapsed:: true
		- Environment=System=Single qubit
		- $$|\psi\rangle=\alpha|0\rangle+\beta|1\rangle$$
		  $$\rho=\left[\begin{array}{cc}
		  |\alpha|^2 & \alpha \beta^{\star} \\
		  \alpha^{\star} \beta & |\beta|^2
		  \end{array}\right]$$
			- Diagonal term -> 'populations',
			  Off-diagonal terms -> 'coherences'
	- After a CNOT between the system and the environment:
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
	  collapsed:: true
		- ((6371f38f-c95e-4d59-a4d8-237a069a12e7))
			- System is rho. Ancillary bit is psi.
			- Intuitively, the 3 controlled gates changes the 3 coordinates of the Bloch sphere respectively.
				- #+BEGIN_WARNING
				  No cross terms. Only rescale 3 coordinates independently.
				  Therefore, not all noises can be realized by the circuit.
				  #+END_WARNING
		- Effect
			- Generally, $\mathcal{E}\left(\rho_S\right)=(1-p) \rho_S+p U \rho_S U^\dag$
				- U is the controlled operation.
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
		  **Entanglement with the environment ->** {{cloze Classical probability within the system}}
		- Bit-flip #card
		  card-last-interval:: 353.22
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2024-07-29T17:43:48.356Z
		  card-last-reviewed:: 2023-08-11T12:43:48.357Z
		  card-last-score:: 5
			- Controlled-X with the environment bit being $\alpha |1\rang+\beta |0\rangle$
			- Flip z direction with probability $$|\alpha|^2$$
		- Phase-flip #card
		  card-last-interval:: 84
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-07-03T11:11:12.726Z
		  card-last-reviewed:: 2023-04-10T11:11:12.728Z
		  card-last-score:: 5
			- Controlled-Z with the environment in superposition
			- Add a relative phase
		- Bit-phase flip
			- $$\alpha=\gamma=0$$
			- Note 
			  $$\sigma_y=\left(\begin{array}{cc}
			  0 & i \\
			  -i & 0
			  \end{array}\right)$$
		- Depolarization #card
		  card-last-interval:: 117.6
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-11-07T03:40:42.888Z
		  card-last-reviewed:: 2023-07-12T13:40:42.889Z
		  card-last-score:: 5
			- ((6371f38f-c95e-4d59-a4d8-237a069a12e7))
				- Note that this channel needs two control bits to flip 3 directions **independently**.
			- ((6371f3bf-7f5d-4f59-aa03-954d582fd946))
			- $$|\alpha|^2=|\beta|^2=|\gamma|^2=p / 3$$
				- Reverse each direction probabilistically.
				  When $$p=3/4$$, $$\boldsymbol{r}^{\prime}=(0,0,0) \text { for any } \boldsymbol{r}$$
				- #+BEGIN_NOTE
				  The condition is $$|\alpha|^2=|\beta|^2=|\gamma|^2=1/4$$, not $$1/2$$. 
				  Because $$\sigma_x$$ doesn't affect x (only add $$\pi$$ to the relative phase), but add a minus to both y and z.
				  #+END_NOTE
			- Wan's explanation
				- $\rho_s^{\prime}=(1-p) \rho_s+p \frac{\mathbb{1}_s}{2}$
					- The 1/2 factor is to keep unit trace.
		- Amplitude damping #card
		  card-last-interval:: 252.3
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2024-01-30T07:42:57.989Z
		  card-last-reviewed:: 2023-05-23T00:42:57.989Z
		  card-last-score:: 5
			- ((6371fe7e-8fc1-482f-b505-582cb00d99cc))
				- Intuitively: $$|0\rangle\lang0|$$ is always retained, while $$|1\rangle\lang1|$$ is flipped with probability p.
			- ((6371fea4-5d43-4319-8730-5a36d3d746fe))
			- Thus p represents the probability that $$|1\rangle \text { decays to }|0\rangle$$
			-
		- Phase damping #card
		  card-last-interval:: 32.57
		  card-repeats:: 2
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-03T02:06:43.751Z
		  card-last-reviewed:: 2023-08-01T13:06:43.751Z
		  card-last-score:: 5
			- Simple version: The same as phase-flip, which causes the **diagonal** terms to vanish.
			- Complicated version: Add a Gaussian-distributed relative phase.
				- $p(\theta)=\frac{1}{\sqrt{4 \pi \lambda}} e^{-\frac{\theta^2}{4 \lambda}}$
				- $$\rho^{\prime}=\int_{-\infty}^{+\infty} d \theta\ p(\theta) R_z(\theta) \rho R_z^{\dagger}(\theta)=\left(\begin{array}{cc}
				  1+z & e^{-\lambda}(x-i y) \\
				  e^{-\lambda}(x+i y) & 1-z
				  \end{array}\right)$$
		- ## Strange feature of amplitude damping and phase damping
		  heading:: 2
			- Repeated application would arrive at 'pure cases'.
			- For the former, the density operator becomes $|0\rangle\lang 0|$; for the latter it becomes a purely classical mix.
			-
		- *De-[[Entanglement]] (actually 2-qubit)
			- ((63720490-57d6-4fac-acdf-f0227800dd0a))
			- When $$\theta=\pi/2$$, the operation makes the Bell state a classical mix, which is 'de-entangle'.
				- Intuitively: $$F_0$$ selects the second bit being 0,
				  while $$F_1$$ selects the second bit being 1.
- The master equation
  collapsed:: true
	- The textbook's way
	  collapsed:: true
		- Setting the stage
			- ((63830b21-378b-4e2a-b249-fb9973ae2eb0))
			  collapsed:: true
				- R means reservoir.
			- Use interaction picture and obtain ((63830b3b-4513-4772-8e43-8f53dae0527a))
		- Simplifications
		  card-last-score:: 5
		  card-repeats:: 3
		  card-next-schedule:: 2023-06-02T22:13:56.482Z
		  card-last-interval:: 61.44
		  card-ease-factor:: 2.56
		  card-last-reviewed:: 2023-04-02T12:13:56.483Z
		  collapsed:: true
			- ((63830b80-1527-4610-b040-b1121e92a009))
				- The initial state is unentangled.
			- Initially ((63830ba9-d176-4634-9c4b-6e78e37a5dc6))
			  collapsed:: true
				- Select a ((63830cc6-78cb-4d60-937e-898078f15681)) $\{\sigma_i\}$, $H_{S R}=\sum_{i=0}^{M-1} \sigma_i B_i$
				- Then it is easy to obtain the initial condition and the desired substitution.
			- ((63830bb8-bc07-4352-a0d9-97a69af9dafd))
			  collapsed:: true
				- The reservoir is big and unaffected by the system.
				- Thus ((63830c03-241d-4e17-a129-1c70225f8090)) ((63830c0a-6066-46b5-bbde-7e76dee55586))
			- ((63830be8-7298-42ab-b88d-1391d1b1045c))
			  collapsed:: true
				- Replace $\tilde{\rho}(\tau) \rightarrow \tilde{\rho}(t)$ in last equation.
				- The equation now becomes purely differential ($\rho$ isn't integrated over).
		- We finally obtain ((63830d27-bbb4-41f7-b322-443a6778d318))
		- Lindblad operators #card
		  card-last-interval:: 67.2
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-04-08T17:08:43.817Z
		  card-last-reviewed:: 2023-01-31T13:08:43.818Z
		  card-last-score:: 5
			- In short, write the evolution of the system plus the environment as Kraus operators.
			  Different formalisms could provide different viewpoints!
			- $E_0=I+\frac{1}{\hbar}(-i H+K) d t$
			  $E_k=L_k \sqrt{d t}, \quad(k=1, \ldots, M-1)$
				- K is hermitian, denoting the 'deviation from isolated evolution'
			- Why $E_0$ is different?
				- collapsed:: true
				  1. They're not all independent.
					- ((63830f97-5b80-4cd8-8e4e-e90a3e4d74d3))
				- 2. Initially the environment is in $|0\rangle$. With time $dt$ the change is infinitesimal.
	- An alternative derivation by ((63840eb6-970a-4787-ad25-13a3cc29ece5))
	  collapsed:: true
		- We may start from an infinitesimal evolution.
			- $E_0=I+\frac{1}{\hbar}(-i H+K) d t$
			  $E_k=L_k \sqrt{d t}, \quad(k=1, \ldots, M-1)$
			- Note that $E_0$ is special.
		- By plugging into the constraint and the evolution equation, we obtain $\dot{\rho}=-\frac{i}{\hbar}[H, \rho]+\sum_{k=1}^{M-1}\left(L_k \rho L_k^{\dagger}-\frac{1}{2} L_k^{\dagger} L_k \rho-\frac{1}{2} \rho L_k^{\dagger} L_k\right)$.
		- However, $L_k$ is in general time-dependent, since the environment won't always stay the same.
		  The time dependence is ignored by ((63830bb8-bc07-4352-a0d9-97a69af9dafd)).
		-
	- GKLS master equation #card
	  card-last-interval:: 297.18
	  card-repeats:: 4
	  card-ease-factor:: 2.66
	  card-next-schedule:: 2024-07-21T04:52:51.114Z
	  card-last-reviewed:: 2023-09-28T00:52:51.115Z
	  card-last-score:: 5
	  id:: 63840eb6-312d-4a41-a9d9-a1c754156965
		- $\dot{\rho}=-\frac{i}{\hbar}[H, \rho]+\sum_{k=1}^{M-1}\left(L_k \rho L_k^{\dagger}-\frac{1}{2} L_k^{\dagger} L_k \rho-\frac{1}{2} \rho L_k^{\dagger} L_k\right)$
		- Note again that it is only possible under ((63830be8-7298-42ab-b88d-1391d1b1045c)).
	- Examples.
		- Note that we don't seem to obtain $L_k$ from first principles. Instead, we directly give their forms (by intuition or magic) and explore the physical consequences.
		- ((63831039-a335-4415-a13c-ff6f038a2b50))
			- ((6383107a-f021-434c-ba4a-115ab9e80907))
		- Spontaneous Emission
		  collapsed:: true
			- Setting
				- $H=-\frac{\omega_0}{2} \sigma_z$
				- a single Lindblad operator $L=\sqrt{\Gamma}\left(\begin{array}{ll}0 & 1 \\ 0 & 0\end{array}\right)$
					- Obviously this corresponds to flipping from $|1\rangle$ to $|0\rangle$
			- Solution
				- Plug into ((63840eb6-312d-4a41-a9d9-a1c754156965))
				- $$
				  \frac{\partial}{\partial t}\left(\begin{array}{ll}
				  \rho_{00} & \rho_{01} \\
				  \rho_{10} & \rho_{11}
				  \end{array}\right)=i \omega_0\left(\begin{array}{cc}
				  0 & \rho_{01} \\
				  -\rho_{10} & 0
				  \end{array}\right)+\Gamma\left(\begin{array}{cc}
				  \rho_{11} & -\frac{1}{2} \rho_{01} \\
				  -\frac{1}{2} \rho_{10} & -\rho_{11}
				  \end{array}\right)
				  $$
				- The solution is
				  $$
				  \left(\begin{array}{ll}
				  \rho_{00}(0)+\rho_{11}(0)\left(1-e^{-\Gamma t}\right) & \rho_{01}(0) e^{\left(i \omega_0-\frac{r}{2}\right) \tau} \\
				  \rho_{10}(0) e^{\left(-i \omega_0-\frac{\Gamma}{2}\right) t} & \rho_{11}(0) e^{-\Gamma t}
				  \end{array}\right)
				  $$
					- We can read off two time scales from the solution #card
					  card-last-interval:: 67.2
					  card-repeats:: 3
					  card-ease-factor:: 2.8
					  card-next-schedule:: 2023-05-10T04:42:43.533Z
					  card-last-reviewed:: 2023-03-04T00:42:43.533Z
					  card-last-score:: 5
						- Amplitude dampening time (diagonal) $t_1 \sim 1/\Gamma$
						- Decoherence time (off-diagonal) $t_2 \sim 2/\Gamma$
				-
			-
		- NMR
			- Setting
			  card-last-interval:: 24
			  card-repeats:: 2
			  card-ease-factor:: 2.7
			  card-next-schedule:: 2023-04-06T12:11:35.690Z
			  card-last-reviewed:: 2023-03-13T12:11:35.691Z
			  card-last-score:: 5
				- $H=-\frac{\omega_0}{2} \sigma_z$
				- $L_{+}=\sqrt{\Gamma_{+}}\left(\begin{array}{ll}0 & 1 \\ 0 & 0\end{array}\right)$
					- 0 -> 1 flip
				- $L_{-}=\sqrt{\Gamma_{-}}\left(\begin{array}{ll}0 & 0 \\ 1 & 0\end{array}\right)$
					- 1 -> 0 flip
				- $L_z=\sqrt{\Gamma_z}\left(\begin{array}{cc}1 & 0 \\ 0 & -1\end{array}\right)$
					- Dephase
			- Solution
				- $\left(\begin{array}{cc}\rho_{00}^{e q}+\left(\rho_{00}-\rho_{00}^{e q}\right) e^{-t / T_1} & \rho_{01} e^{i \omega_0 t-t / T_2} \\ \rho_{10} e^{-i \omega_0 t-t / T_2} & \rho_{11}^{e q}+\left(\rho_{11}-\rho_{11}^{e q}\right) e^{-t / T_1}\end{array}\right)$
				- $T_1^{-1}=\Gamma_{+}+\Gamma_{-} \quad T_2^{-1}=\frac{1}{2}\left(\Gamma_{+}+\Gamma_{-}\right)+2 \Gamma_3$
				-
- Quantum to classical transition
  collapsed:: true
	- Example. [[Schrodinger's Cat]]
		- In short, if the system has interaction with the environment, quantum superposition becomes classical probability.
	- Example. Collapse of a 1-Dim particle under an external perturbation
		- Summary #card
		  card-last-interval:: 252.3
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2024-02-13T08:36:22.329Z
		  card-last-reviewed:: 2023-06-06T01:36:22.329Z
		  card-last-score:: 5
			- Interaction (eg scattering) -> Superposition of entangled final states (system and environment) -> Classical mix after tracing out the environment
			- [[Entanglement]]
				- Here's still a fundamental problem: Why 'tracing out the environment' could model a partial [[Measurement]]?
				- In other words, we still cannot explain why the system collapses to an eigenstate after the measurement.
		-
- Decoherence and [[Measurement]]
  collapsed:: true
	- ((6383134f-370f-4c58-9218-dfad0ee59843))
	- Premeasurement
		- In this stage we establish quantum correlation between the system and the apparatus.
			- If there's no entanglement between the system and the apparatus, than what we read off from the device won't affect the system.
	- ((638315e1-26ad-4fa4-9a8d-fd6110eccb25))
		- That is, the entanglement makes the apparatus a classical probability.
	- ((6383166f-59ce-4002-85c1-1cb3a5039552))
	- Weak measurement
		- Idea
			- Perform a measurement which perturbs the system very weakly, but sufficient to obtain necessary information (after many repetitions).
		- Example of two qubits
			- System: $\alpha|0\rangle_S+\beta|1\rangle_S$
			- Ancillary qubit: $\cos \frac{\theta}{2}|0\rangle_A+\sin \frac{\theta}{2}|1\rangle_A$
			- Measurement: CNOT with the system as control and the ancilla as target.
			- When $\theta\approx\pi/2$, the measurement almost doesn't change the system.
			- Exercise
				- Calculate the partial density matrices #Learning-TODO
				- Prove $\left\langle\sigma_z\right\rangle_A=\left(|\alpha|^2-|\beta|^2\right) \cos \theta$ and obtain polarization.
				-
	- Summary #card
	  card-last-interval:: 169.81
	  card-repeats:: 4
	  card-ease-factor:: 2.66
	  card-next-schedule:: 2023-08-19T19:33:51.044Z
	  card-last-reviewed:: 2023-03-03T00:33:51.045Z
	  card-last-score:: 5
		- First, the apparatus establishes entanglement with the system. Then interaction with the environment destroys the coherence.