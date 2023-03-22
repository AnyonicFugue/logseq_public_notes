- Evolution #card
  card-last-interval:: 26.02
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-04-16T01:55:06.618Z
  card-last-reviewed:: 2023-03-21T01:55:06.619Z
  card-last-score:: 5
	- $$\begin{aligned} & i \frac{\partial}{\partial t} O_I(t)=\left[O_I, H_0\right] \\ & i \frac{\partial}{\partial t}|\psi(t)\rangle_I=V_I|\psi(t)\rangle_I\end{aligned}$$
		- $H_0$ is the free Hamiltonian, $V_I$ is the interaction.
	- Note that $V_I$ also evolves with time.
		- This is a small exercise.
	-
	- Evolution operator
		- $U(t,t_0):=T\{\exp[-i\int^{t}_{t_0}dt' V_I(t')]\}$
		- Note that we must **fix** $t_0$ and define $U_(t_2,t_1):=U(t_2,t_0)U^\dag(t_1,t_0)$. Otherwise the operators won't compose properly.
- # Examples
	- [[Klein-Gordon Theory]]
		- $$
		  \mathcal{L}=\frac{1}{2} \partial_\mu \phi \partial^\mu \phi-j^\mu \partial_\mu \phi
		  $$
		- Summary #card
			- First obtain $\pi$ and $\mathcal H=\pi \dot{\phi}-\mathcal{L}$
				- Note that we shall express $\dot\phi$ by $\pi$.
			- Separate $H_0$ and $V$.
			- Replace $\pi$ by $\dot\phi$ (free field) in $V$ to obtain $V_I$.
			- Finally $V_I=\dot{\phi} j^0+\vec{j} \cdot \nabla \phi+\frac{1}{2}\left(j^0\right)^2=j^\mu \partial_\mu \phi+\frac{1}{2}\left(j^0\right)^2$
				- Note that upper and lower indices can directly contract without metrics!
				  background-color:: yellow
			- #+BEGIN_CAUTION
			  Generally this procedure might not work. For example, the effective theory $$\mathcal{L}_{\mathrm{eff}}(x)=\frac{1}{2}\left[\partial_\mu \phi(x)\right]\left[\partial^\mu \phi(x)\right]-\frac{1}{2} m^2 \phi^2(x)-\frac{1}{4}[1+C \phi(x)] F_{\mu \nu}(x) F^{\mu \nu}(x)$$.
			  The path integral formulation could be more useful.
			  #+END_CAUTION
	- [[Proca Theory]] with interaction #Learning-TODO/Course
		- $$
		  \mathcal{L}=-\frac{1}{4} F_{\mu \nu} F^{\mu \nu}+\frac{1}{2} m^2 A_\mu A^\mu-j_\mu A^\mu
		  $$
			- $\pi^i=F^{i 0}, \pi^0=0$
		- What should we replace? Just replace $\dot A^\nu$ or $\partial_{\mu} A^\nu$?
		  background-color:: red
			- It seems that $\partial_0 A^\mu$ (time derivatives) are replaced while other derivatives are kept intact.
		- Official solution
			- E-L equation: $\partial_\mu F^{\mu \nu}+m^2 A^\nu=j^\nu$
				- Thus $A^0=\left(-\nabla \cdot \vec{\pi}+j^0\right) / m^2$.
			- Moreover, $\pi^i=F^{i 0}\equiv\partial^iA^0-\partial^0A^i$, thus $\vec{\pi}=-\dot{\vec{A}}-\nabla A^0=-\dot{\vec{A}}+\nabla\left(\nabla \cdot \vec{\pi}-j^0\right) / m^2$.
			  So $\dot{\vec{A}}=\nabla\left(\nabla \cdot \vec{\pi}-j^0\right) / m^2-\vec{\pi}$.
				- In principle we could have different equalities by manipulating the above relations repeatedly. So where shall we stop and how to determine the 'right' form?
			- Then he set out to attack the Hamiltonian.
				- $H=\pi^\mu \dot{A}_\mu-\mathcal{L}=-\vec{\pi} \cdot \dot{\vec{A}}-\mathcal{L}$
				- $\begin{aligned} & \frac{1}{2} F_{0 i} F^{02}=-\frac{1}{2} \vec{\pi}^2 \\ & \frac{1}{4} F_{i j} F^{i j}=\frac{1}{2}(\nabla \times \vec{A})^2\end{aligned}$
				- He concluded that 
				  $$
				  \begin{aligned}
				  \frac{1}{2} \vec{\pi}^2+\frac{1}{2}(\nabla \times \vec{A})^2+\frac{1}{2 m^2}(\nabla \cdot \vec{\pi})^2+\frac{1}{2} m^2|\vec{A}|^2 & \equiv H_0 \\
				  -\vec{j} \cdot \vec{A}-\frac{1}{m^2} j^0(\nabla \cdot \vec{\pi})+\frac{1}{2 m^2} j^{0^2} & \equiv V
				  \end{aligned}
				  $$
			- Conclusion. The desired interaction part is
			  $$\begin{aligned} V_I & =-\vec{j} \cdot \vec{A}+j^0 A^0+\frac{1}{2 m^2} j^{0^2} \\ & =j^\mu A_\mu+\frac{1}{2 m^2}\left(j^0\right)^2\end{aligned}$$
				- Not directly $\mathcal H_{int}=-\mathcal L_{int}$!
				  background-color:: red
			- This all seem to be black art to me...