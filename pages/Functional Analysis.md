# Basics
	- ## Defs
		- Functional derivative
			- Consider a theory involving a tensor field (or collection of tensor fields) defined on a manifold $M$.
			- Let $S[\psi]$ be a functional of $\psi$, let $\psi_\lambda$ be a smooth one parameter family of field configurations starting from $\psi_0$ which satisfy appropriate boundary conditions. We denote $d \psi_\lambda /\left.d \lambda\right|_{\lambda=0}$ by $\delta \psi$. Suppose $d S / d \lambda$ at $\lambda=0$ exists for all such one-parameter families starting from $\psi_0$.
			  Suppose, furthermore, that there exists a smooth tensor field $\chi$ [which is dual to $\psi$, i.e., if $\psi$ is a tensor field of type $(k, l)$, then $\chi$ will be of type $(l, k)]$ such that for all such families we have
			  $$
			  \frac{d S}{d \lambda}=\int_M \chi \delta \psi
			  $$
			  where contraction of all indices in the integral is understood. Then we say that $S$ is **functionally differentiable** at $\psi_0$. We call $\chi$ the functional derivative of $S$ and denote it as
			  $$
			  \chi=\left.\frac{\delta S}{\delta \psi}\right|_{\psi_0}
			  $$
				- Why do we define it in this way? #card
				  card-last-interval:: 31.26
				  card-repeats:: 1
				  card-ease-factor:: 2.6
				  card-next-schedule:: 2023-07-05T07:04:01.005Z
				  card-last-reviewed:: 2023-06-04T01:04:01.005Z
				  card-last-score:: 5
					- First of all, it's common to capture the notion of **variance** by a dual object.
					- We must somehow find a way to define 'an infinitesimal change of the field'.
						- We can't vary $\psi(x)$ because it would break the continuity.
					- Naturally, the next thought is to vary the whole function in a smooth manner, which lead to a one-parameter family.
					- This might also be viewed as selecting a 'direction of variance' on the configuration manifold. 
					  We obtain the tangent vector by differentiating wrt $\lambda$.
					- Smooth one-parameter families are perfectly legitimate, but there bound to be some better ways.
						- Maybe ask category for help?
			- See [Wald](((64297a39-f7ff-4ff6-9670-c0ab2cfbf079)))
			- Note
				- In a Lagrangian formulation, we have the action as an integral over a local function
				  $$S[\psi]=\int_M \mathscr{L}[\psi]$$
				  and the solution is
				  $$
				  \left.\frac{\delta S}{\delta \psi}\right|_{\psi}=0
				  $$
				-
	- ## Examples
		- id:: 643b4ac6-657b-468b-b31e-6c7106b9db20
		  card-last-interval:: 33.94
		  card-repeats:: 2
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-23T10:58:26.923Z
		  card-last-reviewed:: 2023-08-20T12:58:26.923Z
		  card-last-score:: 5
		  $$
		  \frac{\delta}{\delta \varphi(x)}\left(\int d^4 x\mathcal{L}\right)=\frac{\partial \mathcal{L}}{\partial \varphi}-\partial_\mu\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_\mu \varphi\right)}\right)
		  $$ #card
			- We should start from the definition of a functional derivative, which is defined by a parameter.
				- $$
				  \frac{d S}{d \lambda}=\int_M \chi \delta \psi
				  $$
				  We call $\chi$ the functional derivative of $S$ and denote it as
				  $$
				  \chi=\left.\frac{\delta S}{\delta \psi}\right|_{\psi_0}
				  $$
			- Then we set $\phi'(x)=\phi(x)+\lambda f(x)$ and examine $\frac{d S}{d \lambda}$.
			- $\frac{\delta}{\delta \varphi(x)}\left(\int d^4 x\mathcal{L}\right)$ shall be **defined** as $\chi(x)$.
			-