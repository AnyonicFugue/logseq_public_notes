alias:: Quantum Error Correcting Code

- # Comments
	- The key to protect information against errors is redundancy. #Thoughts
	- In any case, we must have assumptions about the possible errors.
	- However, classical strategies encounter difficulties for quantum information.
		- [[No-cloning theorem]] prohibits making copies.
		- Measurement disturbs the state.
		- The possible errors form a continuous set.
		- ((63841f61-37f3-44f3-8a55-fe648303ef87))
- # Codes
	- Three-qubit bit-flip code
	  collapsed:: true
		- Setting
			- Alice wants to send a single qubit $|\psi\rangle=\alpha|0\rangle+\beta|1\rangle$ to Bob.
			- The quantum channel they use may flip any qubit with probability $\epsilon$.
		- Code #card
		  card-last-interval:: 67.2
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-05-17T05:17:59.010Z
		  card-last-reviewed:: 2023-03-11T01:17:59.010Z
		  card-last-score:: 5
			- Encoding
				- $|\psi\rangle=\alpha|0\rangle+\beta|1\rangle \rightarrow \alpha\left|0_L\right\rangle+\beta\left|1_L\right\rangle=\alpha|000\rangle+\beta|111\rangle$
					- ((63842195-9e57-46b6-b34a-6e62c211e353))
					- 'L' means 'logical'.
					- Note that this doesn't violate no-cloning theorem.
			- Decoding
				- Note that Bob can't directly measure the state he receives, because measurement destroys the state.
				- Solution: {{cloze introduce ancillary qubits}}.
					- Measuring the ancillary bits won't destroy the state (If they're separable).
					- A common strategy!
					- The ancillary bits are just explicit measurement devices performing $\sigma_{1z}\sigma_{2z}$.
				- ((63842212-769c-437e-acb8-fa6413a32574))
					- If 1st and 2nd qubits are different, then $x_0$ is flipped. Similar for $x_1$.
					- $x_0$ and $x_1$ are called the *error syndrome*.
					- In logical qubits, the 1st and 2nd qubits shall always be the same. So if $x_0=1$ we know the 1st or 2nd bit has been flipped.
				- Finally, determine which one has been flipped by $x_0$ and $x_1$ and flip it back.
					- Measurement is necessary here to **project** the state onto 'pure errors'. If we use controlled-X instead, the final state would still be a superposition state.
			-
	- Three-qubit phase-flip code
	  collapsed:: true
		- Setting
			- Alice still wants to send a qubit to Bob.
			- This time the channel performs $\sigma_z$ on any qubit with probability $\epsilon$.
		- Code #card
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-12-11T11:51:01.779Z
		  card-last-reviewed:: 2022-12-01T11:51:01.780Z
		  card-last-score:: 5
			- In the Bell basis, phase flip becomes bit flip! Just reuse the bit-flip code.
	- Nine-bit Shor code ((6385ffff-7f73-43a8-8dfe-bc77a21c6feb))
	  id:: 63842469-5dc0-4676-9daa-b5ee2000e5a4
		- The idea is to combine phase-flip and bit-flip codes.
		- Code #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-04-07T11:57:26.624Z
		  card-last-reviewed:: 2023-03-14T11:57:26.624Z
		  card-last-score:: 5
		  collapsed:: true
			- $$
			  \begin{aligned}
			  &|0\rangle \rightarrow\left|0_L\right\rangle \equiv \frac{1}{\sqrt{8}}(|000\rangle+|111\rangle)(|000\rangle+|111\rangle)(|000\rangle+|111\rangle) \\
			  &|1\rangle \rightarrow\left|1_L\right\rangle \equiv \frac{1}{\sqrt{8}}(|000\rangle-|111\rangle)(|000\rangle-|111\rangle)(|000\rangle-|111\rangle)
			  \end{aligned}
			  $$
			- ((6384263e-5907-4281-b9e6-a626b32ffe94))
				- Hadamard generates the Bell basis.
				- The CNOTs 'copy' the qubits.
		- Decode #card
		  card-last-interval:: 201.84
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2023-08-23T08:22:59.959Z
		  card-last-reviewed:: 2023-02-02T12:22:59.960Z
		  card-last-score:: 5
		  collapsed:: true
			- In a word, correct bit-flip errors in a single group and correct phase-flip errors across groups.
			- Spin-flip errors are corrected in the usual way. For example, measure $\sigma_{1z}\sigma_{2z}$ and $\sigma_{1z}\sigma_{3z}$ for the first group.
			- To correct the phase-flip errors, we need 
			  $$y_0=\sigma_1^x \sigma_2^x \sigma_3^x \sigma_4^x \sigma_5^x \sigma_6^x \quad$$ 
			  and 
			  $$\quad y_1=\sigma_1^x \sigma_2^x \sigma_3^x \sigma_7^x \sigma_8^x \sigma_9^x$$
				- Not $\sigma_1^x \sigma_4^x$ or $\sigma_1^x \sigma_7^x$! Intuitively, we must flip all three qubits of a group **simultaneously**.
				- On the other hand, phase flip on a single qubit add a minus to $|111\rangle$ as a whole.
		- Theorem. The code may correct any errors to a single qubit. #card
		  card-last-interval:: 252.3
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2024-02-12T07:42:45.112Z
		  card-last-reviewed:: 2023-06-05T00:42:45.113Z
		  card-last-score:: 5
		  collapsed:: true
			- Essentially, a 'mixed error' would be **projected** to a 'pure error' by a measurement of the syndromes, then easily corrected by the Shor code.
				- Note that elements of $SU(2)$ can be expressed in the form
				  $$
				  A=\left(\begin{array}{cc}
				  \alpha & -\bar{\beta} \\
				  \beta & \bar{\alpha}
				  \end{array}\right)
				  $$
				  with $|\alpha|^2+|\beta|^2=1$.
				- Therefore, a general $SU(2)$ operator can be expressed as a **linear combination** of $\left\{I, \sigma_x, \sigma_y, \sigma_z\right\}$.
			- Remark: A continuous set of errors can be corrected by a discrete code!
		- Prop. it has distance three. #card
		  card-last-score:: 5
		  card-repeats:: 2
		  card-next-schedule:: 2023-02-22T12:04:25.924Z
		  card-last-interval:: 24
		  card-ease-factor:: 2.7
		  card-last-reviewed:: 2023-01-29T12:04:25.925Z
		  collapsed:: true
			- Codes to correct 1-qubit errors must have distance at least 3.
			- $\sigma_z^1\sigma_z^2\sigma_z^3$ flips $|0_L\rangle$ to $|1_L\rangle$.
		- Verify the ((638563b0-97c7-407a-b2b0-dcbe845029c7)) #Learning-TODO
	- The 5-qubit code ((6385fff2-cb39-4467-8cc5-360e7b922045))
	  collapsed:: true
		- It is `[[5,1,3]]`, much better than Shor's `[[9,1,3]]`
		- Stabilizer
		  collapsed:: true
			- Generators  (Hint: Cyc. permute) #card
			  card-last-interval:: 67.2
			  card-repeats:: 3
			  card-ease-factor:: 2.8
			  card-next-schedule:: 2023-06-01T11:50:48.486Z
			  card-last-reviewed:: 2023-03-26T07:50:48.486Z
			  card-last-score:: 5
				- ((638605de-c46e-4b9d-89ea-a69241304577))
					- Here is a typo: 4th of $M_4$ shall be $\sigma_4^x$
					  background-color:: red
				- Why no $M_5$?
					- Because $M_5=M_1M_2M_3M_4$
			- All stabilizers with generators ((638605de-c46e-4b9d-89ea-a69241304577)) #card
			  card-last-interval:: 252.3
			  card-repeats:: 4
			  card-ease-factor:: 2.9
			  card-next-schedule:: 2024-01-17T07:24:23.733Z
			  card-last-reviewed:: 2023-05-10T00:24:23.733Z
			  card-last-score:: 5
				- 4 generators, each can be 0 or 1. $|G|=4^2=16$
				- Aside from M1 and the four operators obtained from it by cyclic permutations, the stabilizer will also contains M1M2 plus its cyclic permutations, and M1M3 plus its cyclic permutations.
				- Note that $M_1M_2M_3M_4M_5=I$, so 3=5-2.
			-
		- Codewords #card
		  card-last-interval:: 201.84
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2023-10-08T21:20:10.813Z
		  card-last-reviewed:: 2023-03-21T01:20:10.819Z
		  card-last-score:: 5
			- Naive construction
				- $|0\rangle \rightarrow\left|0_L\right\rangle \equiv \sum_{M \in \mathcal{S}} M|00000\rangle$
				- $|1\rangle \rightarrow\left|1_L\right\rangle \equiv \sum_{M \in \mathcal{S}} M|11111\rangle$
				- Sum all possible permutations to obtain an invariant form. #Strategy
				  id:: 63c1416d-8273-48d4-8cdf-b3fc6ecdf937
			- Simplification
				- Only sum the actions of the **generators**.
		- Verify that the code is nondegenerate and have length 3. #Learning-TODO
- ## [[Stabilizer Code]]
  id:: 6385c5c5-1c56-413f-ae9d-93d1ca14caf4
	- Example of ((63842469-5dc0-4676-9daa-b5ee2000e5a4)) #card
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-01-21T06:44:11.858Z
	  card-last-reviewed:: 2022-12-28T06:44:11.859Z
	  card-last-score:: 5
		- We measure eight operators to correct the errors.
		  collapsed:: true
			- ((6385d21b-16bd-4dfa-a7cc-6e8a7fadcc16))
		- Prop. They are the generators of the stabilizer of the code in ${G}$.
		  collapsed:: true
			- That is, the operators satisfy $M|0\rangle=|0\rangle$ and $M|1\rangle=|1\rangle$.
			- Note that $G$ is defined to be a discrete group. That is, only I and the Paulis.
			-
			- First of all, the operators in the list must appear.
			- Then we show they're sufficient.
			  collapsed:: true
				- $\sigma_z$ must appear in pairs of two.
				- $\sigma_x$ and $\sigma_y$ must appear in groups of three and the groups must appear in pairs.
		- $M_1$ detects bit flips in qubit one or qubit two by {{cloze anti-commutation, which modifies the eigenvalue from +1 to -1}}.
		  collapsed:: true
			- Similarly for other M.
			- Note that $\sigma_y$ can be expressed as a product of x and z, so we don't consider it separately.
- # General Theory
	- ((63860023-4dc1-4576-aca0-d11763757723))
	- ## Defs
	  collapsed:: true
		- The set of all possible errors $\mathcal{E}=\left\{E_0, \ldots, E_{4^n-1}\right\}$
		  collapsed:: true
			- Note that $\mathcal{E}$ (including the identity), with a possible overall factor of $\pm 1$ or $\pm i$, forms a group ${G}$ under multiplication.
			  collapsed:: true
				- G is a discrete group!
				- ((6385c11b-a6c6-4f79-b5ab-11a31bc4a68d))
		- $\mathcal{E}_c$ the subset of errors correctable by the code
		- Weight of an error #card
		  card-last-interval:: 252.3
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2024-02-10T08:11:42.772Z
		  card-last-reviewed:: 2023-06-03T01:11:42.772Z
		  card-last-score:: 5
		  collapsed:: true
			- The number of qubits on which a given operator differs from the identity
			- eg. The weight of $I_1 \otimes \sigma_2^y \otimes \sigma_3^x \otimes I_4 \otimes \sigma_5^z$ is 3.
		- Distance of a code #card
		  card-last-interval:: 252.3
		  card-repeats:: 4
		  card-ease-factor:: 2.9
		  card-next-schedule:: 2024-01-10T07:44:30.120Z
		  card-last-reviewed:: 2023-05-03T00:44:30.120Z
		  card-last-score:: 5
		  collapsed:: true
			- The smallest distance between two codewords.
			- ((6385c169-71ce-4fd6-9a59-ab5a1ed8f271))
		-
	- ## Basic Facts
		- Prop. Unitary operators on n qubits can be expanded over a set of $4^n$ operators.
		  collapsed:: true
			- $U(2^n)=\otimes^n U(2)$
			- We know $I, \sigma_x, \sigma_y$, and $\sigma_z$ constitute a basis of $U(2)$
	- 2 Necessary conditions for error correction #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-05-03T04:11:09.280Z
	  card-last-reviewed:: 2023-02-25T00:11:09.280Z
	  card-last-score:: 5
	  id:: 638563b0-97c7-407a-b2b0-dcbe845029c7
	  collapsed:: true
		- $\left\langle i_L\left|E_a^{\dagger} E_b\right| j_L\right\rangle=0 \quad$ for $i \neq j$
		  collapsed:: true
			- Different states must be **orthogonal**, otherwise not perfectly correctable.
		- $\left\langle i_L\left|E_a^{\dagger} E_b\right| i_L\right\rangle=C_{a b}$ independent of i
		  collapsed:: true
			- If dependent of i, obtain information about the state <-> collapse of quantum state
		- Put the above two together, we arrive at $\left\langle i_L\left|E_a^{\dagger} E_b\right| j_L\right\rangle=C_{a b} \delta_{i j}$
		  collapsed:: true
			- Actually this is sufficient and necessary.
		- Def. Nondegenerate #card
		  card-last-interval:: 10
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2022-12-22T05:51:21.031Z
		  card-last-reviewed:: 2022-12-12T05:51:21.031Z
		  card-last-score:: 5
		  collapsed:: true
			- $C_{a b}=\delta_{a b}$
			- This means that different errors are **orthogonal**.
	- Scheme for ECC in nondegenerate case #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-07-27T12:55:49.923Z
	  card-last-reviewed:: 2023-05-04T12:55:49.924Z
	  card-last-score:: 5
		- Input: $|\psi\rang$
		- After error: $\sum_{E_k \in \mathcal{E}_c} E_k|\psi\rangle\left|e_k\right\rangle_E$
			- Not only acted on by error operators, but also entangle with the environment!
		- Perform projective measurement, collapse to $E_{\bar{k}}|\psi\rangle\left|e_{\bar{k}}\right\rangle_E$
		  collapsed:: true
			- Note that nondegeneracy ensures this.
		- Perform the necessary correction operation by the syndromes.
	- Quantum Hamming Bound #card
	  collapsed:: true
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-06-20T00:46:02.436Z
	  card-last-reviewed:: 2023-05-21T00:46:02.437Z
	  card-last-score:: 5
		- Theorem. $\sum_{j=0}^t\left(\begin{array}{l}n \\ j\end{array}\right) 3^j 2^k \leq 2^n$
		  collapsed:: true
			- n is the total number of qubits
			- t is the max number of erroneous qubits
			- k is the number of logical qubits
			- t stands for the number of errors taking place
		- Proof.
		  collapsed:: true
			- Each qubit has 3 possible errors, that is, the Pauli matrices. Thus $3^j$.
			- Each error must correspond to a subspace of dimension at least $2^k$ to restore the full info of k logical qubits.
		- Note that this only applies to nondegenerate codes.
- Decoherence-free subspaces ((6385f720-bcc2-4404-962c-18a8ea0939d0))
  collapsed:: true
	- This differs from ((6385c5c5-1c56-413f-ae9d-93d1ca14caf4)), because we don't take any action to correct the errors.
	- Simple example
		- Collective dephasing: $|0\rangle_j \rightarrow|0\rangle_j, \quad|1\rangle_j \rightarrow e^{i \phi}|1\rangle_j$ for each qubit.
		- Obviously $\left|0_L\right\rangle \equiv|01\rangle, \quad\left|1_L\right\rangle \equiv|10\rangle$ are invariant (up to a global phase) under dephasing.
	- General theory
		- Defs
			- Decoherence-free
				- The evolution inside is unitary. ((6385f9a1-7eeb-4350-b08b-ec2c5fffa96b))
					- Then the simple example above seems meaningless, because it is unitary in any (invariant) subspace?
					- But the definition has an advantage, that is we can recover all necessary information by reversing the evolution.
			-
- [[Quantum Zeno Effect]]
	- In short, infinitely frequent projective measurements would freeze the evolution of the system.
		- See Principles of QC and Cohen.