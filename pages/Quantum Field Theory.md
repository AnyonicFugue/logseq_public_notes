alias:: QFT

- [[References]
	- ![Peskin](file://C:\Users\10309\Nutstore\1\sync\我的坚果云\资料\physics\QFT\Schroeder, Daniel V._ Peskin, Michael Edward - An introduction to quantum field theory.pdf)
	- ![Introduction_to_Quantum_Field_Theory.pdf](file://D:/Downloads/Courses/Introduction_to_Quantum_Field_Theory.pdf)
	-
- [[Interaction, Feynman diagrams and S-matrix]]
	- [[Feynman rules]]
	- A fundamental difficulty: We need the states to be asymptotic in the **interaction theory**. However, we only knows how to create **free** plane waves.
	  collapsed:: true
		- ((63675402-6c64-443b-b71c-90c3a99a4842))
		- For the vacuum we use ((636753ab-e737-4f19-a1d8-e33ab15c71fc)), which used the property that the vacuum has the lowest energy.
		- Not so good for general states.
	- Feynman rules for fermions
		- Generalize TOP and normal-ordering
		- Generalized Wick's [TODO]
	- Mandelstam variables
		- ((636af081-5d67-4758-887c-ba004b190b71))
		- ((637b326c-0792-4cf0-b2e5-d861201c971c))
		-
	- [[Helicity]] structure in scattering
		- High-E limit #card
		  collapsed:: true
			- All fermions can be regarded as massless.
			- For $\xi=\left(\begin{array}{l}1 \\ 0\end{array}\right)$, ((6379c82e-aa21-424e-9d43-339a251a9bc2))
				- And the same for spin down.
				- Note $p^3$ stands for $p\cdot \sigma^3$
			- ((6379cf92-7252-44e9-b63d-ce792967a710))
				- Note that it is different for fermions and anti-fermions.
			- In other words, now [[Helicity]] and [[Chirality]] becomes identical.
		- Contribution of different helicities
		  collapsed:: true
			- Idea: Use the projectors $\frac{1\pm\gamma^5}{2}$ to get certain helicities.
			- ((6379d13b-9ca8-4786-9cf5-265e23751503))
				- $\gamma^5$ anticommutes with any single $\gamma^\mu$
				- LHS determines the helicity of u, while RHS determines v.
			- Proceed by the common process to obtain $|M|^2$ and $\frac{d \sigma}{d \Omega}$, we can obtain all contributions of the different combinations.
				- Exercise: what are the possible combinations for $e^{+} e^{-} \rightarrow \mu^{+} \mu^-$? #card
					- Input and output can be $(++),(--)$ respectively.
					- 4 in total.
	- Crossing symmetry
		- He claims to easily relate 
		  $e^{+} e^{-} \rightarrow \mu^{+} \mu^{-}$ and $e^{-} \mu^{-} \rightarrow e^{-} \mu^{-}$
		  by a substitution of variable ((6379d42d-2944-458f-9110-e369a7bb0a42))
			- Both of them only have one diagram, with a photon propagator in the middle.
			- The kinetics are similar.
- [[Yukawa theory]]
- [[Quantum Electrodynamics]]
-