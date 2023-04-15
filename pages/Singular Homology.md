- # Defs
	- ## About Orientations
		- Orientation
		  id:: 642578ff-9703-449c-b3df-41ffc344e641
			- An orientation of $\Delta^n=\left[e_0, e_1, \ldots, e_n\right]$ is a linear ordering of its vertices.
				- For a line segment, it is an ordering of the two endpoints
		- Identification of orientations
			- Two orientations of $\Delta^n$ are the same if, as permutations of $\left\{e_0, e_1, \ldots, e_n\right\}$, they have the same parity (i.e., both are even or both are odd); otherwise the orientations are opposite.
		- Induced orientation
			- Given an orientation of $\Delta^n$, there is an induced orientation of its faces defined by orienting the $i$ th face in the sense $(-1)^i\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$
		- Example. Verify the induced orientation of $\Delta^2$, $[e_0,e_1,e_2]$, is compatible with the original one.
		  ![image.png](../assets/image_1681440654144_0.png){:height 336, :width 409}
			- The boundary of $\Delta^2$ is
			  $$
			  \left[e_1, e_2\right] \cup\left[e_0, e_2\right] \cup\left[e_0, e_1\right]=\left[\hat{e}_0, e_1, e_2\right] \cup\left[e_0, \hat{e}_1, e_2\right] \cup\left[e_0, e_1, \hat{e}_2\right] .
			  $$
			  The oriented boundary of $\Delta^2$ is
			  $$
			  \left[\hat{e}_0, e_1, e_2\right] \cup-\left[e_0, \hat{e}_1, e_2\right] \cup\left[e_0, e_1, \hat{e}_2\right]=\left[e_1, e_2\right] \cup\left[e_2, e_0\right] \cup\left[e_0, e_1\right] .
			  $$
			- More generally, the boundary of $\Delta^n=\left[e_0, \ldots, e_n\right]$ is $\bigcup_{i=0}^n\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$ and the oriented boundary of $\Delta^n$ is $\bigcup_{i=0}^n(-1)^i\left[e_0, \ldots, \hat{e}_i, \ldots, e_n\right]$.
			-
			-
-