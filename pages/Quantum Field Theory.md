alias:: [[QFT]]

- [[References]]
	- ![Schroeder, Daniel V._ Peskin, Michael Edward - An introduction to quantum field theory.pdf](file://C:/Users/yizho/Nutstore/1/sync/我的坚果云/资料/physics/QFT/Schroeder, Daniel V._ Peskin, Michael Edward - An introduction to quantum field theory.pdf) The classical textbook by Peskin
	- ![Introduction_to_Quantum_Field_Theory.pdf](file://D:/Downloads/Courses/Introduction_to_Quantum_Field_Theory.pdf) Satoshi Nawata's lecturenotes
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
	  collapsed:: true
		- ((636af081-5d67-4758-887c-ba004b190b71))
		- ((637b326c-0792-4cf0-b2e5-d861201c971c))
		-
	- [[Helicity]] structure in scattering
	  collapsed:: true
		- High-E limit #card
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.36
		  card-next-schedule:: 2022-12-07T14:22:22.088Z
		  card-last-reviewed:: 2022-11-27T14:22:22.089Z
		  card-last-score:: 3
			- All fermions can be regarded as massless.
			- For $\xi=\left(\begin{array}{l}1 \\ 0\end{array}\right)$, ((6379c82e-aa21-424e-9d43-339a251a9bc2))
				- And the same for spin down.
				- Note $p^3$ is $p^z$. The formula can be verified directly by #TODO
			- ((6379cf92-7252-44e9-b63d-ce792967a710))
				- Note that it is different for fermions and anti-fermions.
			- In other words, now [[Helicity]] and [[Chirality]] becomes identical.
		- Contribution of different helicities
			- Idea: Use the projectors $\frac{1\pm\gamma^5}{2}$ to get certain helicities.
			- ((6379d13b-9ca8-4786-9cf5-265e23751503))
				- $\gamma^5$ anticommutes with any single $\gamma^\mu$
				- LHS determines the helicity of u, while RHS determines v.
			- Proceed by the common process to obtain $|M|^2$ and $\frac{d \sigma}{d \Omega}$, we can obtain all contributions of the different combinations.
				- Exercise: what are the possible combinations for $e^{+} e^{-} \rightarrow \mu^{+} \mu^-$? #card
				  card-last-interval:: 61.44
				  card-repeats:: 3
				  card-ease-factor:: 2.56
				  card-next-schedule:: 2023-02-23T16:08:08.133Z
				  card-last-reviewed:: 2022-12-24T06:08:08.133Z
				  card-last-score:: 5
					- Input and output can be $(++),(--)$ respectively.
					- 4 in total.
	- Crossing symmetry
	  collapsed:: true
		- He claims to easily relate 
		  $e^{+} e^{-} \rightarrow \mu^{+} \mu^{-}$ and $e^{-} \mu^{-} \rightarrow e^{-} \mu^{-}$
		  by a substitution of variable ((6379d42d-2944-458f-9110-e369a7bb0a42))
			- Both of them only have one diagram, with a photon propagator in the middle.
			- The kinetics are similar.
	- [[LSZ Formula]]
	- Properties of the [[S-matrix]]
		- [[Lorentz invariance]]
		- Unitarity
			- [[Optical Theorem]]
- [[Klein-Gordon Theory]]
- [[Yukawa theory]]
- [[Quantum Electrodynamics]]
- [[Classical Field Theory]]
  collapsed:: true
	- Noether's theorem #card
	  card-last-interval:: 11.8
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-12-27T00:22:55.688Z
	  card-last-reviewed:: 2022-12-15T05:22:55.689Z
	  card-last-score:: 5
		- $$\begin{aligned}
		  \partial _{\mu } j^{\mu } (x) & =0,\ \ \text{ for } \ \ j^{\mu } (x)=\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\frac{\delta \phi }{\delta \alpha } -\mathcal{J}^{\mu }
		  \end{aligned}$$
		- Points: EOM, construct full derivative
		-
		- Proof
			- Consider a Lagrangian with sym. $\alpha$
			- L must be inv. under different $\alpha$, up to a 4-divergence $\partial_\mu \mathcal{J}^{\mu }$:
			  $$\begin{aligned}
			  \frac{\delta \mathcal{L}}{\delta \alpha } & =\frac{\partial \mathcal{L}}{\partial \phi }\frac{\delta \phi }{\delta \alpha } +\left(\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\right) \partial _{\mu } (\frac{\delta \phi }{\delta \alpha } )\\
			   & =\partial _{\mu }\left(\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\frac{\delta \phi }{\delta \alpha }\right) +\alpha \left[\frac{\partial \mathcal{L}}{\partial \phi } -\partial _{\mu }\left(\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\right)\right]\frac{\delta \phi }{\delta \alpha }
			  \end{aligned}$$
			- Substitute EOM: We're done.
		- Example
			- [[Energy-momentum Tensor]] 
			  $\mathcal{T}_{\mu \nu}=\sum_{n} \frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{n}\right)} \partial_{\nu} \phi_{n}-g_{\mu \nu} \mathcal{L}$
		- Ref. Peskin, ((63805db9-661f-470f-9403-3ff9ae8aa7dd))
- Causality and Propagators
  collapsed:: true
	- $\langle 0|[\phi(x), \phi(y)]| 0\rangle=0$ for spacelike separation, which preserves [[Causality]].
		- Use some invariance/symmetry to simplify the problem. ([[Lorentz invariance]] in this case) #Trick
	-
	- [[Propagator]], or time-ordered product
		- $$\langle 0|\phi(x) \phi(y)| 0\rangle=\int \frac{d^3 p}{(2\pi)^3} \cdot \frac{1}{2 E_p} \cdot e^{-i p(x-y)}:=D(x-y)$$
		- Feynman propagator
		  id:: 129a2538-6668-4ae1-a5cc-a7cf58e6122b
			- Def
				- $D_{F}( x_{1} ,x_{2}) =\langle 0| T\{\phi _{0}( x_{1}) \phi _{0}( x_{2})\}| 0\rangle =\int \frac{d^{4} k}{(2\pi )^{4}}\frac{i}{k^{2} -m^{2} +i\varepsilon } e^{ik( x_{1} -x_{2})}$
				- Points: Exponential term from $a_p e^{ipx}$; denominator produces singularities.
			-
			- Core point: $$\frac{e^{-iE_{k} \tau } \theta (\tau )+e^{iE _{k} \tau } \theta (-\tau )}{2E_k}=\lim _{\varepsilon \rightarrow 0}\int _{-\infty }^{\infty }\frac{dp_0}{2\pi}\frac{i }{p_0 ^{2} -E _{k}^{2} +i\varepsilon } e^{-ip_0 \tau }$$ 
			  'Phase multiples Heaviside'
			- Note tha $D_F$ is the [[Green Function]] of KG operator, i.e. 
			  $$\left(\partial^\mu \partial_\mu+m^2\right) D_F(x-y)=-i \delta^4(x-y)$$
		- Dirac Propagator
			- Def
				- $$\begin{aligned}
				  &S_F(x-y)=\int \frac{d^4 p}{(2 \pi)^4} \frac{i(\not p+m)}{p^2-m^2+i \epsilon} e^{-i p \cdot(x-y)}\\
				  &=\left\{\begin{aligned}
				  \langle 0|\psi(x) \bar{\psi}(y)| 0\rangle & \text { for } x^0>y^0 \text { (close contour below) } \\
				  -\langle 0|\bar{\psi}(y) \psi(x)| 0\rangle & \text { for } x^0<y^0 \text { (close contour above) }
				  \end{aligned}\right.\\
				  &\equiv\langle 0|T \psi(x) \bar{\psi}(y)| 0\rangle
				  \end{aligned}$$
			- This is $-(i\gamma^\mu p_\mu+m)D_F(x-y)$.
				- With the 'dirac operator' $i\gamma^\mu p_\mu-m$ acting on it, we obtain $(\square+m^2)D_F(x-y)\cdot \mathbb1_4$.
				- The same idea as obtaining KG eq. from Dirac eq.
			-
			- Exercise. The [[Time-ordered product]] gives the correct propagator
				- Tip: Modify $$\frac{e^{-iE_{k} \tau } \theta (\tau )+e^{iE _{k} \tau } \theta (-\tau )}{2E_k}=\lim _{\varepsilon \rightarrow 0}\int _{-\infty }^{\infty }\frac{dp_0}{2\pi}\frac{i }{p_0 ^{2} -E _{k}^{2} +i\varepsilon } e^{-ip_0 \tau }$$
				- Use Lorentz invariance (or change of integration variables)
			-
			- Take care of the minus sign! (Compare ((129a2538-6668-4ae1-a5cc-a7cf58e6122b)) )
	-