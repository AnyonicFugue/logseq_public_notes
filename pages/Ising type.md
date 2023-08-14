# Data
id:: 63da100c-a77b-4c42-8e86-5bc90cce4cbd
	- Fusion rules
		- $\psi \otimes \psi=\mathbb{1}, \psi \otimes \sigma=\sigma, \sigma \otimes \sigma=\mathbb{1} \oplus \psi$
	- Braidings and topo spins
		- $$
		  R_1^{\sigma \sigma}=e^{-\pi i / 8}, R_\psi^{\sigma \sigma}=e^{3 \pi i / 8}, R_1^{\psi \psi}=-1, R_\sigma^{\sigma \psi}=i
		  $$
		- $s_\psi=-1, \quad s_\sigma=e^{i \pi / 8}$
		- This is the case for $\xi=e^{-i\pi/8}$
	- 16-fold way
		- 8 braiding structures (can be divided into 2 classes of monoidal structures), 2 spherical structures
		- ((63744cc7-0cd4-48ac-9efc-987e92a2b210))
		- Nontrivial associators
		  collapsed:: true
			- $\begin{gathered}\alpha_{\psi, \sigma, \psi}:(\psi \otimes \sigma) \otimes \sigma=\sigma \stackrel{-1}{\longrightarrow} \sigma=\psi \otimes(\sigma \otimes \psi), \\ \alpha_{\sigma, \psi, \sigma}:(\sigma \otimes \psi) \otimes \sigma=\mathbb{1} \oplus \psi \stackrel{1 \oplus-1}{\longrightarrow} \mathbb{1} \oplus \psi=\sigma \otimes(\psi \otimes \sigma), \\ \alpha_{\sigma, \sigma, \sigma}:(\sigma \otimes \sigma) \otimes \sigma=(\mathbb{1} \otimes \sigma) \oplus(\psi \otimes \sigma) \stackrel{A_{+}}{\longrightarrow}(\sigma \otimes \mathbb{1}) \oplus(\sigma \otimes \psi)=\sigma \otimes(\sigma \otimes \sigma),\end{gathered}$
				- $A_{\pm}=\frac{\pm 1}{\sqrt{2}}\left(\begin{array}{rr}1 & 1 \\ 1 & -1\end{array}\right)$ corresponds to two monoidal structures.
		- Braidings
			- $$
			  \begin{gathered}
			  c_{\psi, \psi}: \psi \otimes \psi=\mathbb{1} \stackrel{-1}{\longrightarrow} \mathbb{1}=\psi \otimes \psi, \\
			  c_{\sigma, \sigma}: \sigma \otimes \sigma=\mathbb{1} \oplus \psi \stackrel{\zeta \oplus \zeta^{-3}}{\longrightarrow} \mathbb{1} \oplus \psi=\sigma \otimes \sigma, \\
			  c_{\psi, \sigma}: \psi \otimes \sigma=\sigma \stackrel{\zeta^4}{\longrightarrow} \sigma=\sigma \otimes \psi, \\
			  c_{\sigma, \psi}: \sigma \otimes \psi=\sigma \stackrel{\zeta^4}{\longrightarrow} \sigma=\psi \otimes \sigma .
			  \end{gathered}
			  $$
			- $\zeta^8=-1$ with $\zeta^2+\zeta^{-2}=\pm \sqrt{2}$
			  id:: 63da0fe6-366f-4fad-902a-59220239c51e
				- The sign tells monoidal structures.
		- If only consider the unitary modular tensor categories: $S=\left(\begin{array}{ccc}1 & 1 & \sqrt{2} \\ 1 & 1 & -\sqrt{2} \\ \sqrt{2} & -\sqrt{2} & 0\end{array}\right)$
		  collapsed:: true
			- Generally, 
			  $$
			  S=\left(\begin{array}{ccc}
			  1 & 1 & \epsilon\left(\zeta^2+\zeta^{-2}\right) \\
			  1 & 1 & -\epsilon\left(\zeta^2+\zeta^{-2}\right) \\
			  \epsilon\left(\zeta^2+\zeta^{-2}\right) & -\epsilon\left(\zeta^2+\zeta^{-2}\right) & 0
			  \end{array}\right)
			  $$
			  where $\epsilon$ tells the spherical structures.
	- See ((63744c99-ad88-49b3-961c-f37d7b3aca41)).
- # Relation to Majorana Anyons
	- Interprete $\sigma \leftrightarrow \gamma$.
	- $\psi$ corresponds to $i\gamma_{2j-1}\gamma_{2j}=1$, i.e. occupation number = 1 for the j^{th} fermion.
	- $1$ corresponds to $i\gamma_{2j-1}\gamma_{2j}=-1$, i.e. occupation number = 0 for the j^{th} fermion.