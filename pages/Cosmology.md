- # Homogeneous Isotropic Cosmology
	- Definitions
		- Homogeneous
			- A spacetime is said to be (spatially) homogeneous if there exists a one-parameter family of spacelike hypersurfaces $\Sigma_t$ foliating the spacetime, such that:
			   for each $t$ and for any points $p, q \in \Sigma_t$ there exists an isometry of the spacetime metric, $g_{a b}$, which takes $p$ into $q$.
				- Intuitively, all points on the hypersurface are equal.
		- Isotropic
			- A spacetime is said to be (spatially) isotropic at each point if there exists a congruence of timelike curves (i.e., observers), with tangents denoted $u^a$, filling the spacetime and satisfying the following property:
			  Given any point $p$ and any two unit "spatial" tangent vectors $s_1^a, s_2^a \in V_p$ (i.e, vectors at $p$ orthogonal to $u^a$ ), there exists an isometry of $g_{a b}$ which leaves $p$ and $u^a$ at $p$ fixed but rotates $s_1^a$ into $s_2^a$.
				- Intuitively, all directions to the observer are equal.
	- Solution: [[FLRW]] metric
		- $$
		  d s^2=-c^2 d t^2+a^2(t)\left(\frac{d r^2}{1-k r^2}+r^2 d \theta^2+r^2 \sin ^2 \theta d \phi^2\right)
		  $$
			- $a$ is called the scale factor
		- We can always rescale $r$ such that $k=-1,0,1$.
			- $k=1$ is called **closed**, since each 3-hypersurface is a 3-sphere.
			- $k=0$ is **flat**, since each 3-hypersurface is $\mathbb R^3$.
				- Note that the 4-spacetime is **not** flat, since $a$ depends on $t$!
			- $k=-1$ is **open**, since each 3-hypersurface is a hyperboloid.
		- Proof
			- By the definition of isotropic, we can decompose the metric as
			  $$
			  g_{a b}=-u_a u_b+h_{a b}(t)
			  $$
				- $u_a$ is the tangent vector of the observer
				- $h_{ab}$ is the induced metric on the 3-surface.
			- Proposition. A homogeneous, isotropic 3-hypersurface could only be a 3-sphere, $\mathbb R^3$ or a hyperboloid.
			- Therefore
			  $$d s^2=-d \tau^2+a^2(\tau)\left\{\begin{array}{l}
			  d \psi^2+\sin ^2 \psi\left(d \theta^2+\sin ^2 \theta d \phi^2\right) \\
			  d x^2+d y^2+d z^2 \\
			  d \psi^2+\sinh ^2 \psi\left(d \theta^2+\sin ^2 \theta d \phi^2\right)
			  \end{array}\right.$$
				- For a 3-sphere, we can write
				  $$x=\cos \psi, y=\sin \psi \cos \theta, z=\sin \psi \sin \theta \cos \phi, w=z=\sin \psi \sin \theta \sin \phi$$
				- For a 3-hyperboloid we just replace $\cos \psi$ by $\cosh \psi$ and $\sin \psi$ by $\sinh \psi$