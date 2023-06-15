- # Def
	- Actually an algebra over $\mathbb C$, where any two elements **anticommute**.
	- Complex conjugation
		- $$
		  (\theta \eta)^* \equiv \eta^* \theta^*=-\theta^* \eta^*
		  $$
		- Note that $\theta$ and $\theta^*$ are treated as **independent** variables in integrations.
		- For higher-dimensional integrations:
		  $$
		  d^N \zeta d^N \zeta^*:=d \zeta_1 d \zeta_1^* \ldots d \zeta_N d \zeta_N^*
		  $$
		-
	-
- # Integration
	- Intuitions
		- To define functional integrations, we only need to define the analog of $\int^\infty_{-\infty} dx$.
		- We wish that the integration has some good properties:
			- (1) A linear map of functions
			- (2) Integrals of total derivatives should vanish
			- (3) Better that the integral is invariant under a shift of the integral variable
	- Def. 
	  $$\int d\theta \cdot 1 =0, \int d\theta \cdot \theta =1, \int d\theta \int d\eta \ \eta\theta = 1$$
		- This is a **definition**, not derivable from other principles.
		- Note that the integral over an arbitrary function $f(\theta)$ can be completely determined by the coefficient of its linear term.
	- Generalization to higher orders:
		- Take
		  $$
		  f(\zeta)=f_0+f_1^i \zeta_i+f_2^{i j} \zeta_i \zeta_j+\cdots+f_N \zeta_N \zeta_{N-1} \cdots \zeta_1
		  $$
		- We obtain 
		  $$\int d^{N} \zeta f(\zeta )=\left\{\begin{array}{ c l }
		  +f_{N} & f_{N} :c\text{-number }\\
		  (-1)^{N} f_{N} & f_{N} :\text{ Grassmann number }
		  \end{array}\right. $$
			- Note that $d^N \zeta := d\zeta_1 ... d\zeta_N$. Each integration variable must appear exactly once, so only $f_N$ survives.
			- $(-1)^n$ arises from moving $f_N$ to the rightmost.
	- Prop. Translation invariance: $\int d^N \zeta f\left(\zeta+\eta_{\xi}\right) = \int d^N \zeta f(\zeta)$ #card
		- $$
		  \begin{aligned}
		  \int d^N \zeta f\left(\zeta+\eta_{\xi}\right) & =\int d^N \zeta f_N\left(\zeta_N+\eta_N\right) \cdots\left(\zeta_1+z_1\right) \\
		  & =\int d^N \zeta f_N \zeta_N \cdots \zeta_1 \\
		  & =\int d^N \zeta f(\zeta)
		  \end{aligned}
		  $$
	- Prop. Gaussian Integration:
	  $$\int d^{N} \zeta d^{N} \zeta ^{*} e^{\zeta ^{\dagger} A\zeta } =\operatorname{det} A$$ #card
		- \begin{aligned}
		  \int d^{N} \zeta d^{N} \zeta ^{*} e^{\zeta ^{\dagger } A\zeta } & \underset{\zeta ^{\prime } =A\zeta }{=}\int d^{N} \zeta ^{\prime } d^{N} \zeta ^{*}\left\Vert \frac{d\zeta }{d\zeta^{\prime }}\right\Vert e^{\zeta ^{\dagger } \zeta ^{\prime }}\\
		   & =\operatorname{det} A\int d^{N} \zeta ^{\prime } d^{N} \zeta ^{*}\frac{1}{N!}\left( \zeta ^{\dagger } \zeta ^{\prime }\right)^{N}\\
		   & =\operatorname{det} A\int d^{N} \zeta ^{\prime } d^{N} \zeta ^{*} \zeta _{N}^{*} \zeta _{N}^{\prime } \cdots \zeta _{1}^{*} \zeta _{1}^{\prime }\\
		   & =\operatorname{det} A
		  \end{aligned}
		- $\exp$ shall be expanded to $N^{th}$ order to obtain each integration variable exactly once.
		- The third line uses the fact that there are exactly $N!$ such pairings.
		- Pairs of Grassmann numbers always commute.
		- This formula, similar to the Gaussian integration, would be frequently used.
		  background-color:: yellow
	- ## Examples
		- $$\int d\theta ^{*} d\theta e^{-\theta ^{*} b\theta } =b$$
			- $$
			  \int d \theta^* d \theta e^{-\theta^* b \theta}=\int d \theta^* d \theta\left(1-\theta^* b \theta\right)=\int d \theta^* d \theta\left(1+\theta \theta^* b\right)=b
			  $$
			- Note that in ordinary integrations we would obtain something like $1/b$. This is a difference!
		- $$
		  \int d \theta^* d \theta \ \theta \theta^* e^{-\theta^* b \theta}=1
		  $$ #card
			- $$e^{-\theta ^{*} b\theta } =1-\theta ^{*} b\theta $$
			- The key point is $\theta^2=0$, which cancels the term linear in $b$.
		-
		-
	-
- # Differentiation
	- Note that we can have different choices, since $d\theta$ can be multiplied before or after $f(\theta)$.
	- We choose the **right differentiation**,
	  $$f(\theta+d\theta)=f(\theta)+f'(\theta)d\theta$$
	- Leibniz rule of differentiation
		- $$\frac{\partial }{\partial \theta }( f( \theta ) g( \theta )) =( -1)^{|g|} f'( \theta ) g( \theta ) +f( \theta ) g'( \theta )$$
		- $|g|$ is 0 if $g(\theta)$ is a complex number and 1 if $g(\theta)$ is a Grassmann number.
		-
- # Transformation of Variables
	- Consider $\theta_i^{\prime}=U_{i j} \theta_j$, we have
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-06-09T00:31:40.661Z
	  card-last-reviewed:: 2023-05-10T00:31:40.662Z
	  card-last-score:: 3
	  $$\prod _{i} \theta _{i}^{\prime } =(\operatorname{det} U)\left(\prod _{i} \theta _{i}\right)\\
	  \prod _{i} d\theta _{i}^{\prime } =(\operatorname{det} U)^{-1}\left(\prod _{i} d\theta _{i}\right)
	  $$ #card
		- $$\begin{aligned}
		  \prod _{i} \theta _{i}^{\prime } & =\frac{1}{n!} \epsilon ^{ij\dotsc l} \theta _{i}^{\prime } \theta _{j}^{\prime } \dotsc \theta _{l}^{\prime }\\
		   & =\frac{1}{n!} \epsilon ^{ij\dotsc l} U_{ii^{\prime }} \theta _{i^{\prime }} U_{jj^{\prime }} \theta _{j^{\prime }} \dotsc U_{ll^{\prime }} \theta _{l^{\prime }}\\
		   & =\frac{1}{n!} \epsilon ^{ij\dotsc l} U_{ii^{\prime }} U_{jj^{\prime }} \dotsc U_{ll^{\prime }} \epsilon ^{i^{\prime } j^{\prime } \dotsc l^{\prime }}\left(\prod _{i} \theta _{i}\right)\\
		   & =(\operatorname{det} U)\left(\prod _{i} \theta _{i}\right)
		  \end{aligned}$$
			- The first line is anti-symmetrization with summation
			- The second-last line is just relabeling the variables and fixing the order of $\{\theta_i\}_i$.
		- The second rule is derived again from $\int d\theta \ \theta=1$.
		  Also it leaves the integration invariant under a change of measures.
		-
- # Basic facts
	- $\theta^2=0$
		- Since it anticommutes with itself.
	- Function in one Grassmann variable $\theta$
		- Only $a+b\theta$.
	- Linear transformation of variables
		- Single variable
			- Consider $\zeta'=a\zeta$ , we'd have $\Bigl|\frac{d\zeta }{d\zeta '}\Bigl| =a$ (contrary to common integrals)
				- $$
				   1=\int d \zeta \zeta=\frac{1}{a} \int d \zeta \zeta^{\prime}=\frac{1}{a} \int d \zeta^{\prime}\left\|\frac{d \zeta}{d \zeta^{\prime}}\right\| \zeta^{\prime}
				  			$$
			- This is due to the definition $\int d\theta \ \theta=1$ , which fixes lots of things
	-