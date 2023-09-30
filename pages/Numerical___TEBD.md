# iTEBD
	- [[2008_Classical simulation of infinite-size quantum]]
- # Idea
	- With the Hamiltonian written as a sum of local terms, we could divide it into non-intersecting groups and use the [[Trotter-Suzuki Decomposition]].
		- For example, the quantum Ising could be written as
		  $$\hat{H}=\hat{H}_{\text {even }}+\hat{H}_{\text {odd }}$$
		- Then the imaginary time-evolution could be written as
		  $$
		  \begin{aligned}
		  \hat{U}^{\text {exact }}(\delta) & =e^{-\mathrm{i} \delta \hat{H}} \\
		  & =e^{-\mathrm{i} \delta \hat{H}_{\text {even }}} e^{-\mathrm{i} \delta \hat{H}_{\text {odd }}} e^{-\mathrm{i} \delta^2\left[\hat{H}_{\text {even }}, \hat{H}_{\text {odd }}\right]} \\
		  & \approx e^{-\mathrm{i} \delta \hat{H}_{\text {even }}} e^{-\mathrm{i} \delta \hat{H}_{\text {odd }}} \\
		  & \equiv \hat{U}^{\mathrm{TEBD} 1}(\delta)
		  \end{aligned}
		  $$
		- We could also use [[BCH Formula]] to expand to higher orders,
		  $$
		  \hat{U}^{\mathrm{TEBD} 2}(\delta) \equiv e^{-\mathrm{i} \frac{\delta}{2} \hat{H}_{\text {even }}} e^{-\mathrm{i} \delta \hat{H}_{\text {odd }}} e^{-\mathrm{i} \frac{\delta}{2} \hat{H}_{\text {even }}}
		  $$
	-
-