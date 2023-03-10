- # Peskin Version
	- Thought
	  collapsed:: true
		- For 2->n Green functions, we have poles at $p^2=m^2$.
		  collapsed:: true
			- Example. $\int d^4 x e^{i p \cdot x}\langle\Omega|T \phi(x) \phi(0)| \Omega\rangle \underset{p^2 \rightarrow m^2}{\sim} \frac{i Z}{p^2-m^2+i \epsilon}$ up to some phase or non-singular terms
		- Take the limit where all particles are on shell, the coefficient (residue) of the multiple pole is an S-matrix element.
	- Simple case: Examine $\int d^4 x e^{i p \cdot x}\left\langle\Omega\left|T\left\{\phi(x) \phi\left(z_1\right) \phi\left(z_2\right) \cdots\right\}\right| \Omega\right\rangle$. #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-04-01T01:35:22.928Z
	  card-last-reviewed:: 2023-03-07T01:35:22.928Z
	  card-last-score:: 5
		- Key points
			- Divide the integral into three regions 
			  $$\int d x^0=\int_{T_{+}}^{\infty} d x^0+\int_{T_{-}}^{T_{+}} d x^0+\int_{-\infty}^{T_{-}} d x^0$$.
			  The asymptotic regions are easy to analyze, while **the finite region has no contribution** to the singularity structure.
			- Insert completeness relation.
		- First region
			- $$I_1=\int_{T_{+}}^{\infty} d x^0 \int d^3 x e^{i p^0 x^0} e^{-i \mathbf{p} \cdot \mathbf{x}} \sum_\lambda \int \frac{d^3 q}{(2 \pi)^3}  \frac{1}{2 E_{\mathbf{q}}(\lambda)}\left\langle\Omega|\phi(x)| \lambda_{\mathbf{q}}\right\rangle  \times\left\langle\lambda_{\mathbf{q}}\left|T\left\{\phi\left(z_1\right) \phi\left(z_2\right) \cdots\right\}\right| \Omega\right\rangle$$ (Insert completeness)
			- Use $\left\langle\Omega|\phi(x)| \lambda_{\mathbf{q}}\right\rangle=\left.\left\langle\Omega|\phi(0)| \lambda_0\right\rangle e^{-i q \cdot x}\right|_{q^0=E_{\mathbf{q}}(\lambda)}$ (translation and Lorentz invariance)
			- Introduce a factor $e^{-\epsilon x^0}$ to make the integral well-defined (familiar trick), we obtain
			  $$
			  I_1=\sum_\lambda \frac{1}{2 E_{\mathbf{p}}(\lambda)} \frac{i e^{i\left(p^0-E_{\mathbf{p}}+i \epsilon\right) T_{+}}}{p^0-E_{\mathbf{p}}(\lambda)+i \epsilon}\left\langle\Omega|\phi(0)| \lambda_0\right\rangle\left\langle\lambda_{\mathbf{p}}\left|T\left\{\phi\left(z_1\right) \cdots\right\}\right| \Omega\right\rangle .
			  $$
			- We recognize $\left\langle\Omega|\phi(0)| \lambda_0\right\rangle=\sqrt Z$ up to a phase. Moreover, since the field is free, we only need to consider the 1-particle part.
			-
			- **Conclusion**
				- id:: 640000d5-4226-4b33-b898-933b0e843e33
				  collapsed:: true
				  $$\begin{aligned} \int d^4 x e^{i p \cdot x} & \left\langle\Omega\left|T\left\{\phi(x) \phi\left(z_1\right) \cdots\right\}\right| \Omega\right\rangle \\ \underset{p^0 \rightarrow+E_{\mathbf{p}}}{\sim} & \frac{i}{p^2-m^2+i \epsilon} \sqrt{Z}\left\langle\mathbf{p}\left|T\left\{\phi\left(z_1\right) \cdots\right\}\right| \Omega\right\rangle\end{aligned}$$
					- Note that the third region has no contribution to this pole, so we may comfortably write $\int d^4 x$ instead of $\int_{T_{+}}^{\infty} d x^0 \int d^3 x$.
				- This is a hint: If we change $e^{i p \cdot x}$ to $e^{-i p \cdot x}$, $p$ would be replaced by $-p$ and the singularity would appear at $p^0 \rightarrow-E_{\mathbf{p}}$ instead.
				  id:: 6400015d-d4a2-4a2d-9f97-66dc51abe1a7
		- Third region
		  collapsed:: true
			- The analysis is completely similar.
			- **Conclusion**
			  collapsed:: true
				- $$
				  \begin{aligned}
				  & \int d^4 x e^{i p \cdot x}\left\langle\Omega\left|T\left\{\phi(x) \phi\left(z_1\right) \cdots\right\}\right| \Omega\right\rangle \\
				  & \underset{p^0 \rightarrow-E_{\mathbf{p}}}{\sim}\left\langle\Omega\left|T\left\{\phi\left(z_1\right) \cdots\right\}\right|-\mathbf{p}\right\rangle \sqrt{Z} \frac{i}{p^2-m^2+i \epsilon}
				  \end{aligned}
				  $$
				- The [hint](((6400015d-d4a2-4a2d-9f97-66dc51abe1a7))) still holds, that is, we should use $e^{-ipx}$ if we want $p^0 \rightarrow E_{\mathbf{p}}$.
	- General case: perform the above operation to all coordinates.
		- Extra subtleties when dealing with $\left\langle\lambda_{\mathbf{p}}\left|T\left\{\phi\left(z_1\right)\phi\left(z_2\right) \cdots\right\}\right| \Omega\right\rangle$
			- After inserting the completeness relation, we would obtain $\left\langle\lambda_{1\mathbf{q_1}}|\phi(x)| \lambda_{2\mathbf{q_2}}\right\rangle\times\left\langle\lambda_{2\mathbf{q_2}}\left|T\left\{\phi\left(z_1\right) \phi\left(z_2\right) \cdots\right\}\right| \Omega\right\rangle$. We should explain why the first term is still $\sqrt Z$ and why $\lambda_p$ is 'adding one more asymptotic state to $\lambda_q$'.
			- The first term is $e^{i(q_1-q_2)x}\left\langle\lambda_{1,\mathbf{q_1}}|\phi(0)| \lambda_{2,\mathbf{q_2}}\right\rangle$
			  id:: 6400044b-7905-409a-9984-4b346e597800
			-
			- When integrating over $p$, the delta function and the singularity would appear at $p=q_1-q_2$, which means adding a particle.
			- Moreover, we can use Lorentz invariance to change to a frame where $\vec q_2=\vec q_1$.
				- Argument: Since the new particle is **independent** from the old ones at asymptotic time, $\left\langle\lambda_{1,\mathbf{q_1}}|\phi(0)| \lambda_{2,\mathbf{q_1}}\right\rangle=\sqrt Z$.
				- Proof
					-
			-
		- Each coordinates gives $\frac{i}{p^2-m^2+i \epsilon} \sqrt{Z}$.
		-
		- We can choose to integrate wrt $e^{ipx}$ or $e^{-ipx}$.
			- For incoming particles we choose $e^{-ipx}$, so the singularity is in the third region and particles comes to the right of the matrix element.
			- For outgoing particles we choose $e^{ipx}$, so the singularity is in the first region and particles comes to the left of the matrix element.
- Statement #card
	- $$
	  \begin{array}{r}
	  \prod_1^n \int d^4 x_i e^{i p_i \cdot x_i} \prod_1^m \int d^4 y_j e^{-i k_j \cdot y_j}\left\langle\Omega\left|T\left\{\phi\left(x_1\right) \cdots \phi\left(x_n\right) \phi\left(y_1\right) \cdots \phi\left(y_m\right)\right\}\right| \Omega\right\rangle \\ \\
	  \underset{\begin{array}{c}
	  \text { each } p_i^0 \rightarrow+E_{\mathbf{p}_i} \\
	  \text { each } k_j^0 \rightarrow+E_{\mathbf{k}_j}
	  \end{array}}{\large\sim}\left(\prod_{i=1}^n \frac{\sqrt{Z} i}{p_i^2-m^2+i \epsilon}\right)\left(\prod_{j=1}^m \frac{\sqrt{Z} i}{k_j^2-m^2+i \epsilon}\right)\left\langle\mathbf{p}_1 \cdots \mathbf{p}_n|S| \mathbf{k}_1 \cdots \mathbf{k}_m\right\rangle .
	  \end{array}
	  $$
		- Here the fields are free fields.
	- The expression should be up to a phase?
	  background-color:: red
		- So in principle we do not need to write $i$. Is it a device to remind ourselves of the propagators?
		-