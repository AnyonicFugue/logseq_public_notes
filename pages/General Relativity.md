alias:: GR

- # Principles
	- General Covariance #card
		- The metric of space is the only quantity pertaining to space that can appear in the laws of physics.
		- Specifically, there are no preferred vector fields or preferred bases of vector fields pertaining only to the structure of space which appear in any law of physics.
			- As a consequence, the (undifferentiated) Christoffel symbol cannot appear in physical laws since it implies a preferred frame.
		- See ((64267a67-8dfa-44a6-a52c-4f86ebc81214))
	- Special Covariance #card
		- All physical measurements are equally possible in different inertial frames and all physical laws are the same.
- # Special Relativity
	- Lorentz transformation #card
		- $$
		  \left\|\Lambda_x{ }^\mu{ }_\nu\right\|=\left(\begin{array}{cccc}
		  \gamma & -\gamma & 0 & 0 \\
		  -\gamma \beta & \gamma & 0 & 0 \\
		  0 & 0 & 1 & 0 \\
		  0 & 0 & 0 & 1
		  \end{array}\right)
		  $$
		- A quick way to rederive it: Take $\tilde t=ict$, then the metric becomes Euclidean.
		  We can first write down a rotation in the Euclidean space, then insert $i$ back.
- # Elements of Differential Geometry
	- Christoffel symbol #card
		- $$\Gamma_{a b}^c=\frac{1}{2} g^{c d}\left\{\partial_a g_{b d}+\partial_b g_{a d}-\partial_d g_{a b}\right\}$$
		- Quick memorization: Two plus and a minus, raised by a metric, symmetric positive at the two lower indices
	- Geodesic equation #card
		- $$
		  \frac{d^2 x^\mu}{d t^2}+ \Gamma_{\sigma \nu}^\mu \frac{d x^\sigma}{d t} \frac{d x^\nu}{d t}=0
		  $$
			- Note that this only holds for an affine parameter. For a different parameter $\lambda'$ we have instead $\left(\ddot{x}^\mu+\Gamma_{v \rho}^\mu \dot{x}^\nu \dot{x}^\rho\right)\left(\frac{d \lambda^{\prime}}{d \lambda}\right)^2=-\dot{x}^\mu \frac{d^2 \lambda^{\prime}}{d \lambda^2}$. (Exercise)
		- Can be derived from minimizing $S=\frac{1}{2} m \int_{\gamma} g_{ab}(x) \dot{x}^a \dot{x}^b d t$ and writing down the EL equation
-