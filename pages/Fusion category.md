- Almost customized for [[Topological Order]]...
- # Definition
- # Separable algebra
	- Def #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-12-17T06:42:26.379Z
	  card-last-reviewed:: 2023-11-16T00:42:26.380Z
	  card-last-score:: 3
		- An algebra $(A, \mu, \eta) \in C$ is separable if there is an $A$-$A$-bimodule homomorphism $\delta: A \to A \otimes A$, with
			- $\mu \circ \delta =\mathrm{id}_A$
			- Frobenius conditions
	- A fusion cat $C$ is separable if {{cloze C is a separable C-C-bimodule}}. #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-08-29T18:43:07.315Z
	  card-last-reviewed:: 2023-07-29T12:43:07.315Z
	  card-last-score:: 3
		- Remark: $\mathrm{Fun}_{C|C}(C,C) \simeq Z(C)$ is semisimple, thus the center $Z(C)$ is a braided fusion cat.
	- Examples
		- $M_n(\mathbb k)$ is separable with $\mu := E_{ij} \mapsto \frac 1 n \sum_k E_{ik} \otimes E_{kj}$
			- This map is defined componentwise. The whole map is obtained by linearity.
	- Lemma. $C$ is a multi-fusion cat. If $A \in C$ is separable, then $\mathrm{RMod}_A(C)$ is finit-semisimple.
	- Proposition. For a multi-fusion cat $C$ and $A \in C$ semisimple, $M := \mathrm{RMod}_A(C)$, the following are equivalent:
	  (1) $A$ is separable
	  (2) There is a separable algebra $B \in C$ s.t. $M \simeq \mathrm{RMod}_B(C)$
	  (3) For all finite-semisimple left C-module $N$, $\mathrm{Fun}_C(M,N)$ is separable
	  (4) $\mathrm{Fun}_C(M,M)$ is separable
	  (5) $\mathrm{BMod}_{A|A}(C)$ is semisimple
		-
	-
	-
	- Multi-fusion category #card
	  card-last-interval:: 24
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-25T00:58:03.267Z
	  card-last-reviewed:: 2023-04-01T00:58:03.267Z
	  card-last-score:: 5
		- A $\mathbb k$-linear rigid monoidal finite-semisimple category.
		- It is called a fusion category if the tensor unit $1$ is simple.
	- Fusion ring
		- ((636e0d2a-d931-4220-90a4-a37c3f69e41e))
		- ((636e0d3b-65a3-4d18-b098-ae64e774612c))
			- Example. ((636e074a-e3f3-4c93-8ee1-d5b97e7c05ea)).
				- Same fusion rules, different 'signs'
			- The [[Fusion rules]] cannot uniquely determine the [[Topological Order]]!
- # [[Invertible]]
  collapsed:: true
	- Def #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-08-17T18:57:05.329Z
	  card-last-reviewed:: 2023-07-17T12:57:05.329Z
	  card-last-score:: 5
		- An object is invertible if it satisfies the conditions
			- ((63745ee5-d4fe-4d02-a3b8-3582f373a546)) #card
			  card-last-interval:: 672.13
			  card-repeats:: 5
			  card-ease-factor:: 2.52
			  card-next-schedule:: 2025-09-27T03:49:28.312Z
			  card-last-reviewed:: 2023-11-25T00:49:28.313Z
			  card-last-score:: 5
				- The proof invokes interesting properties of [[Fusion rules]] and [[Quantum dimension]].
				- id:: 63c14165-542f-4aff-bb7f-063784718de9
				- The 'algebraic characters' can provide lots of info! No need to know all information of the object under investigation!
				-
			- Especially, each fusion channel is **simple**.
- [[Pointed]]
	- Def
		- Each object is invertible.
	- Link with $$Vec_G$$
	  collapsed:: true
		- ((63758a42-5bb4-4254-93c4-66cd7abf562f))
			- Note that $$C\simeq Vec_G$$ only as ((C)). No [[Fusion]] or [[Braiding]] structure here.
		- ((63758b5a-8776-4206-979e-96075d0182c0))
			- Braiding -> $$a \otimes b \simeq b \otimes a$$ -> They belong to the same isomorphism class.
	- [[Quadratic form]]
	  collapsed:: true
		- ((63758e18-557b-4c6d-9137-02eaff42e1d2))
			- 'Quadratic' seems to mean 'doesn't depend on the sign'
			- [[Bicharacter]]
		- [[Pre-metric group]]
			- ((63758e5a-b10b-466b-b999-f1b71dbe26f9))
		- As a identifying character of [[Pointed]] braided fusion categories
			- ((63758ee8-0b06-41a1-aadf-c8f51356931b))
			- ((63758e7c-60cc-40e9-b084-11a02caa988e))
			- ((63758e98-b014-4e85-8dc5-92fd585adc8d))
	- [[Abelian topological order]]
	-
- # Properties
	-