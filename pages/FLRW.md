- # Solution
	- collapsed:: true
	  $$
	  d s^2=-c^2 d t^2+a^2(t)\left(\frac{d r^2}{1-k r^2}+r^2 d \theta^2+r^2 \sin ^2 \theta d \phi^2\right)
	  $$
		- $a$ is called the **scale factor**.
		  collapsed:: true
			- Intuitively, the universe expands when $a$ becomes larger,
			  since humans on fixed locations of the time slices would find others drifting farther and farther away.
	- We can always rescale $r$ such that $k=-1,0,1$.
	  collapsed:: true
		- $k=1$ is called **closed**, since each 3-hypersurface is a 3-sphere.
		- $k=0$ is **flat**, since each 3-hypersurface is $\mathbb R^3$.
		  collapsed:: true
			- Note that the 4-spacetime is **not** flat, since $a$ depends on $t$!
		- $k=-1$ is **open**, since each 3-hypersurface is a hyperboloid.
	- Proof
	  collapsed:: true
		- By the definition of isotropic, we can decompose the metric as
		  collapsed:: true
		  $$
		  g_{a b}=-u_a u_b+h_{a b}(t)
		  $$
			- $u_a$ is the tangent vector of the observer
			- $h_{ab}$ is the induced metric on the 3-surface.
		- Proposition. A homogeneous, isotropic 3-hypersurface could only be a 3-sphere, $\mathbb R^3$ or a hyperboloid.
		- Therefore
		  collapsed:: true
		  $$d s^2=-d \tau^2+a^2(\tau)\left\{\begin{array}{l}
		  d \psi^2+\sin ^2 \psi\left(d \theta^2+\sin ^2 \theta d \phi^2\right) \\
		  d x^2+d y^2+d z^2 \\
		  d \psi^2+\sinh ^2 \psi\left(d \theta^2+\sin ^2 \theta d \phi^2\right)
		  \end{array}\right.$$
			- For a 3-sphere, we can write
			  $$x=\cos \psi, y=\sin \psi \cos \theta, z=\sin \psi \sin \theta \cos \phi, w=z=\sin \psi \sin \theta \sin \phi$$
			- For a 3-hyperboloid we just replace $\cos \psi$ by $\cosh \psi$ and $\sin \psi$ by $\sinh \psi$
		- This is just the above form when we have $x = \sin \psi$ (sphere) or $x= \sinh \psi$ (hyperboloid)
- # Physical Effects
	- ## Cosmological Redshift
		- Rough argument
			- For radiation, $\rho \propto \frac 1 {a^4}$, while the volume $V \propto {a^3}$.
			- Since the number of photons doesn't change and $E=\rho V$, we conclude that $E \propto \frac 1 a$.
		- Strategy
			- Invoke homogeneity to establish the existence of 3 orthogonal spatial Killing fields.
			- Use the property that $k_a \xi^a$ keeps constant.
		- Solution
			- $E = -k_a u^a$, so we want to calculate how does $E$ change along a geodesic.
			- Without loss of generality, suppose initially $k_a \xi_2^a = k_a \xi_3^a=0$, i.e. the projection of $k$ to the 3-surface is proportional to $\xi_1^a$.
			- Therefore, $k_a \xi_2^a = k_a \xi_3^a=0$ holds at any point on the geodesic.
			  Then we may write
			  $$k_a= (\frac {k_b \xi_1^b}{\xi_1^b \xi_{1b}}) \xi_1^a +(\frac {k_b u^b}{u^b u_{b}}) u^a$$
			- Moreover, since $k_a k^a=0$, we have
			  $$\frac {(k_b \xi_1^b)^2}{\xi_1^b \xi_{1b}}-(k_b u^b)^2=0$$
			  therefore
			  $$k_b u^b \propto \frac 1 {\sqrt {\xi_1^b \xi_{1b}}}$$
			- Now it's obvious $\xi_1^b \xi_{1b} \propto a^2$ (take the example of a flat space: the coordinates at different times are identical, just the scale factor changed)
			  therefore
			  $$k_b u^b \propto \frac 1 {a}$$
			-
	- ## Particle Horizon
	  collapsed:: true
		- Motivating question: How much of the universe is causally connected?
		- Strategy
			- Consider a photon (which has the upper bound of causal speed) travelling from $t=0$ to $t=T$.
			  The distance corresponds to the causally connected region.
		- Calculation
			- Obviously 
			  $$r(t)=\int_0^T \frac {dt}{a(t)}$$
			- If we take the approximation where $a \propto t^\alpha$,
			  we find 
			  $$r(t) \propto \frac{t^{1-\alpha}}{1-\alpha} \propto \frac {t}{a(t)(1-\alpha)}$$
			- If we take the proper distance $s = ar$, then
			  $$s(t) \propto \frac{t}{1-\alpha}$$
			  which means the proper causal diameter grows linearly with time.
			-
			-