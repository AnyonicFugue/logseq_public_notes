- # Homogeneous Isotropic Cosmology
	- ## Definitions
	  collapsed:: true
		- Homogeneous
			- A spacetime is said to be (spatially) homogeneous if there exists a one-parameter family of spacelike hypersurfaces $\Sigma_t$ foliating the spacetime, such that:
			   for each $t$ and for any points $p, q \in \Sigma_t$ there exists an isometry of the spacetime metric, $g_{a b}$, which takes $p$ into $q$.
				- Intuitively, all points on the hypersurface are equal.
		- Isotropic
			- A spacetime is said to be (spatially) isotropic at each point if there exists a congruence of timelike curves (i.e., observers), with tangents denoted $u^a$, filling the spacetime and satisfying the following property:
			  Given any point $p$ and any two unit "spatial" tangent vectors $s_1^a, s_2^a \in V_p$ (i.e, vectors at $p$ orthogonal to $u^a$ ), there exists an isometry of $g_{a b}$ which leaves $p$ and $u^a$ at $p$ fixed but rotates $s_1^a$ into $s_2^a$.
				- Intuitively, all directions to the observer are equal.
	- ## Solution: [[FLRW]]
	- ## Question: Is the volume finite?
	  collapsed:: true
		- In the case of a trivial topology:
		  $$V=\int_V \sqrt{{ }^3 g} d^3 x=a^3 \int_0^{2 \pi} d \phi \int_0^\pi \sin \theta d \theta \int_0^{r_k} \frac{r^2 d r}{\sqrt{1-k r^2}}$$
			- Actually integrating over a time slice.
			- $$
			  V=\left\{\begin{array}{cl}
			  \pi^2 a^3 & \text { for } k=1 \\
			  \infty & \text { for } k=0,-1
			  \end{array}\right.
			  $$
		- For a closed solution, the volume must be finite.
		- For flat and open solutions, things can be more complicated.
			- In short, we can produce nontrivial topologies by identifying some points (like making a torus).
			- Thus the space can be made finite by **pasting**.
	- ## Simplest model: Perfect fluid #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-07-08T07:08:20.560Z
	  card-last-reviewed:: 2023-06-07T01:08:20.561Z
	  card-last-score:: 5
	  collapsed:: true
		- Definitions
		  collapsed:: true
			- Critical energy
			  collapsed:: true
				- $$
				  \rho_{\mathrm{c}}^0=\frac{3 H_0^2 c^2}{8 \pi G_{\mathrm{N}}}
				  $$
				- Namely, the density of a flat universe.
				- Since we can observe $H$ experimentally, we can fix $H$ and examine the behavior when $\rho$ changes.
				  collapsed:: true
					- When $\rho > \rho_c, k > 0$.
					- When $\rho < \rho_c, k < 0$.
		- About the Fluid
		  collapsed:: true
			- EM tensor
			  collapsed:: true
			  $$
			  T^{\mu \nu}=(\rho+P) \frac{u^\mu u^\nu}{c^2}+P g^{\mu \nu}
			  $$
				- Note that 'perfect' means no **friction**, not no pressure.
			- Equation of state
			  collapsed:: true
				- The simplest form is 
				  $$
				  P=w \rho
				  $$
				  though others are also possible.
		- ### Friedmann Equations
			- *Wald doesn't have good ways to obtain the Ricci tensor either. Seems we can only calculate the Christoffel symbols by brute force, then contract them.
			- First:
			  collapsed:: true
			  $$
			  H^2=\frac{8 \pi }{3} \rho-\frac{k}{a^2} \quad (1)
			  $$
				- $H= \dot a / a$ is the **Hubble parameter**. 
				  When applied to our universe, it is the **Hubble constant**.
			- Second:
			  collapsed:: true
			  $$
			  \frac{\ddot{a}}{a}=-\frac{4 \pi }{3}(\rho+3 P) \quad (2)
			  $$
				- Note that this means $\ddot a < 0$ for most cases, thus the universe is generally **not static**!
			- Note that we may also use $\nabla_\mu T^{\mu v}=0$ to obtain
			  $$
			  \dot{\rho}=-3 H(\rho+P) \quad (3)
			  $$
			  But these three equations aren't independent; we can use any two equations to obtain the third.
			-
		- ### Solution (Half-Approximated)
			- Conclusion
			  collapsed:: true
				- $$\rho \propto a^{-3(1+w)}$$
				- $$
				  a \propto t^{\frac 2 {3(1+w)}} \quad \text{(approximated)}
				  $$
			- The simplest way is to start from (3):
			  $$\dot \rho=-3(1+w)\rho \ \frac {\dot a} a$$
				- This equation can be immediately integrated to obtain
				  collapsed:: true
				  $$\rho \propto a^{-3(1+w)}$$
					- $$
					  \begin{aligned}
					  & w=0 \quad \rightarrow \quad \rho \propto 1 / a^3 \quad \text { (dust does no work, thus inverse-proportional to the volume) } \\
					  & w=1 / 3 \rightarrow \rho \propto 1 / a^4 \quad \text { (radiation, does positive in expansion, thus decaying faster) } \\
					  & w=-1 \rightarrow \rho=\text { constant } \quad \text { (vacuum energy, does negative work in expansion) } \\
					  &
					  \end{aligned}
					  $$
			- Next plug into (1) and **ignore the k term**.
			  collapsed:: true
				- $$\dot a^2=\frac {8\pi} 3  Ca^{-3(1+w)}$$
				- Obviously the solution is of the form
				  $$
				  a \propto t^\alpha
				  $$
				- Therefore we find
				  $$\alpha=\frac 2 {3(1+w)}$$
		- ### Exact Solutions for Certain Matter Species
		  id:: 646df946-15d9-447b-ac72-2e8efbd6f2ac
		  collapsed:: true
			- Einstein Universe: Dust plus Cosmological Constant
				- $$
				  \begin{aligned}
				  H^2 & =\frac{8 \pi G_{\mathrm{N}}}{3 c^2} \rho+\frac{\Lambda c^2}{3}-\frac{k c^2}{a^2}, \\
				  \frac{\ddot{a}}{a} & =-\frac{4 \pi G_{\mathrm{N}}}{3 c^2}(\rho+3 P)+\frac{\Lambda c^2}{3} .
				  \end{aligned}
				  $$
				- Einstein wants a static universe, i.e. $\dot a=\ddot a=0$,
				  therefore we can obtain an unstable equilibrium
				  $$
				  \rho=\frac{\Lambda c^4}{4 \pi G_{\mathrm{N}}}, \quad a=\frac{1}{\sqrt{\Lambda}}, \quad k=1
				  $$
			- Matter (dust) dominated: $w=0$
			  collapsed:: true
				- Intuitively, dust has no 'pressure', so the gravitational effects cause an open universe to keep expanding and a closed universe to keep contracting.
				- We can use $\rho \propto a^{-3(1+w)}$ to rewrite equation (1):
				  $$
				  \dot{a}^2=\frac{8 \pi G_{\mathrm{N}}}{3 c^2} \frac{C_1}{a}-k c^2
				  $$
				- The rest is algebraic manipulations, refer to [Bambi](((646dfd73-b2fc-46fa-b733-855f0e3886a1))).
				- We can obtain the relation $a$ versus $t$:
				  ((646dfd95-b11d-42aa-9ee3-a057f5dad014))
					- Open and flat universes expand infinitely.
					- Closed universe would reach a maximum and eventually fall back to a point!
			- Radiation dominated: $w=-1/3$
			  collapsed:: true
				- Use $\rho a^4=C_2$ to rewrite equation (1):
				  $$
				  \dot{a}^2=\frac{8 \pi G_{\mathrm{N}}}{3 c^2} \frac{C_2}{a^2}-k c^2
				  $$
				- It could be directly integrated to obtain
				  collapsed:: true
				  $$
				  a=\left[\sqrt{\frac{32 \pi G_{\mathrm{N}} C_2}{3 c^2}} t-k c^2 t^2\right]^{1 / 2}
				  $$
					- Note that the solution corresponds to $a(0)=0$.
				- The evolution is quite similar to a matter-dominated universe,
				  ((646dfe5a-141c-4344-91c2-4b447d21cb33))
			- Energy dominated: $w=-1$
			  collapsed:: true
				- Intuitively, vacuum energy (cosmological constant) has a positive pressure and always pushes the universe to expand.
				- It isn't hard to solve the equations.
				  $$
				  \begin{aligned}
				  & k=1 \rightarrow a=\sqrt{\frac{3 k}{\Lambda}} \cosh \left(\sqrt{\frac{\Lambda}{3}} c t\right) . \\
				  & k=0 \rightarrow a=a(t=0) \exp \left(\sqrt{\frac{\Lambda}{3}} c t\right) . \\
				  & k=-1 \rightarrow a=\sqrt{\frac{-3 k}{\Lambda}} \sinh \left(\sqrt{\frac{\Lambda}{3}} c t\right) .
				  \end{aligned}
				  $$
				- All universes **expand forever**.
				- Moreover, for $k=0,1$ there is **no Big Bang**.
	- ## Primordial Plasma
		- Summary
			- We assume the plasma is at thermal equilibrium and the universe is a grand canonical ensemble,
			  so the density $\rho$ would be determined by $g_{eff},\mu,T$ (effective d.o.f., chemical potential, temperature)
				- Calculated from BE and FD distributions.
				- However, thermal equilibrium is also questionable, since particles become asymptotically free at high energies and the interaction can be quite weak!
				  background-color:: red
			- If we assume that the early universe is dominated by ratiation and $H=1/2t$, then we can obtain a relation between **temperature** and **time** from the Friedmann equation:
			  $$
			  H^2=(\frac 1 {2t})^2=\frac{4 \pi^3 }{45} g_{\mathrm{eff}}\left(k_{\mathrm{B}} T\right)^4-\frac{k c^2}{a^2}
			  $$
				- It's sensible that the early universe is dominated by radiation, since $\rho \propto \frac 1 {a^4}$ and $a$ can be very small in the early universe.
			- In other words, we've found out **how does the universe cool down**!
	- ## Age of the Universe
	  collapsed:: true
		-
		- If we know the matter content (for example, dust -> $\rho=\frac 1 {a^3}$), then $a(t)$ decides $\rho(t)$, which in turn decides $\dot a(t)$ via the Friedmann equation
		  $$
		  H^2=\frac{8 \pi }{3} \rho-\frac{k}{a^2} \quad (1)
		  $$
			- A real universe would contain different species of matters, so we just need to sum their respective contributions.
		- Therefore we can directly integrate 
		  $$\int dt=\int \frac {da}{\dot a}$$
		  and obtain the age.
			- We may set $1+z=\frac {a_0}a$ to simplify the notations a bit.
		- #+BEGIN_NOTE
		  It's surprising that we can obtain the age of our universe from abstract equations and very few observational data!
		  #+END_NOTE
	- ## Destiny of the Universe
		- Question: Would the universe expand forever, or finally collapse into a singularity again?
		- The answer is dependent on the specific matter content.
			- For example, dust and radiation don't alter the essential behaviors (expand infinitely for open universes, collapse for closed ones), while radiation always **pushes** the universe to expand forever.
			- However, when different matters are present simultaneously, their contributions would compete.
			- See ((646df946-15d9-447b-ac72-2e8efbd6f2ac)).
-