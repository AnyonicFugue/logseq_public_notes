- Def #card
  card-last-interval:: 25.01
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-02-27T12:20:24.662Z
  card-last-reviewed:: 2023-02-02T12:20:24.662Z
  card-last-score:: 5
	- Let $f: X \rightarrow Y$ and $g: Y \rightarrow X$ be continuous maps. Suppose that the map $g \circ f: X \rightarrow X$ is **homotopic to the identity map** of $X$, and the map $f \circ g: Y \rightarrow Y$ is **homotopic to the identity map** of $Y$.
	- Then the **maps** $f$ and $g$ are called **homotopy equivalences**, and each is said to be a homotopy inverse of the other.
	- Example
		- Inclusion j and deformation retraction r
- Let $h, k: X \rightarrow Y$ be continuous maps; let $h\left(x_0\right)=y_0$ and $k\left(x_0\right)=y_1$. If $h$ and $k$ are **homotopic**, there is a path $\alpha$ in $Y$ from $y_0$ to $y_1$ such that $k_*=\hat{\alpha} \circ h_*$. Indeed, if $H: X \times I \rightarrow Y$ is the homotopy between $h$ and $k$, then $\alpha$ is the path $\alpha(t)=H\left(x_0, t\right)$ #card
  collapsed:: true
  card-last-interval:: 24
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-03-26T00:59:32.591Z
  card-last-reviewed:: 2023-03-02T00:59:32.592Z
  card-last-score:: 5
	- **No need to fix any point in the homotopy; homotopic paths always give the same homomorphism between fundamental groups!**
	- ((63a66686-57f7-43bd-8883-017b1642e7f1))
	- We may construct a path homotopy $G: I\times I \to Y$ by $G(s,t)=(\alpha_t * F(f(s),t) * \alpha_t^{-1})(s)$, where $\alpha_t(s)=H(x_0,st)$
		- $\alpha_t$ is 'the path $\alpha$ truncated at length t'
		- ![Image.png](../assets/Image_1671852973168_0.png)
		-
- ((63a67422-9e04-4af9-8bae-e9bc5903ed6a)) Let $f: X \rightarrow Y$ be continuous; let $f\left(x_0\right)=y_0$. If $f$ is a **homotopy equivalence** then
  card-last-interval:: 26.06
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-02-24T13:05:21.686Z
  card-last-reviewed:: 2023-01-29T12:05:21.687Z
  card-last-score:: 5
  $$
  f_*: \pi_1\left(X, x_0\right) \longrightarrow \pi_1\left(Y, y_0\right)
  $$
  is an **isomorphism**. #card
	- Intuition
		- Homotopy equivalence preserve all info related to paths.
	- Proof
		- Suppose $f\circ g \cong id_Y$, $g \circ f \cong id_X$
		- Now we have explicit inverses to the star maps (up to different base points)!
- ((63a67588-b6c3-48ab-97fb-5f38f7401e4a)) Two spaces $X$ and $Y$ have the **same homotopy type** if and only if they are **homeomorphic to deformation retracts of a single space** $Z$.
-