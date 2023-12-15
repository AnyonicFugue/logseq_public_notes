alias:: MMA

- # Tutorials
	- [Project Euler (1–10) | Stone Zeng’s Site (stone-zeng.site)](https://stone-zeng.site/2020-08-07-euler-1-10)
- # Basic Syntax
	- Comment
		- Use `(*` and `*)` to enclose comments.
	- Combine multiple expressions into one #card
	  collapsed:: true
		- Use `;`
		- Example. `If[x>50, AppendTo[arr,a]; n=n+1]`
			- If x>50, then the combined expression `AppendTo[arr,a]; n=n+1` would be executed.
	- Prefix and postfix #card
	  collapsed:: true
		- `f[x] == f @ x == x // f`
		- For example, we can write `Eigenvalues[x] // N // Sort`
		- #+BEGIN_TIP
		  This avoids nesting a hundred brackets.
		  #+END_TIP
	- Functions and lists #card
		- Evaluate f on each element of a list
			- `f /@ {a,b,c}` gives `{f[a], f[b], f[c]}`
		- Use a list as arguments of a function
			- `f @@ {x,y,z}` gives `f[x,y,z]`
		-
	- Replacement with a rule `./` #card
	  collapsed:: true
		- Replace a variable with a value / list
			- `{x, x^2, y, z} /. x -> 1` gives `{1, 1, y, z}`
			- `{x, x^2, y, z} /. x -> {a, b}` gives `{{a,b}, {a^2,b^2}, {y,z}}`
		- Replace a function
			- `Sin[x] /. Sin -> Cos` gives `Cos[x]`
		- Replace matching part with a pattern, like regex
			- `1 + x^2 + x^4 /. x^p_ :> f[p]` gives {1 + f[2] + f[4]}
				- Here `x^p_` is a rule
		- Apply a set of rules separately
			- `x /. {{x -> 1}, {x -> 3}, {x -> 7}}` gives `{1,3,7}`
		-
	- Condition `/;` #card
	  collapsed:: true
		- `{6, -7, 3, 2, -1, -2} /. x_ /; x < 0 -> w`
			- Replace `x` by `w` if `x` is negative.
	- Array element #card
		- `arr[[i]]`
		- Note that we need a **double** bracket.
	-
- # Useful Functions
	- Substitutions of `for` and `if`
		- Nestwhile
		- `Select[list, criterion]`
			- Pick out all elements `x` in `list `for which `criterion[x]` is true.
	- ## Plot
	  collapsed:: true
		- Plot a single function
		  collapsed:: true
			- `Plot[f, {x, x_min, x_max}]`
		- Plot multiple functions
		  collapsed:: true
			- `Plot[{f1, f2, f3}, {x, x_min, x_max}]`
		- Further possibilities
		  collapsed:: true
			- Plot legends
			- Label each curve
			- Fill below a curve / between two curves
		- GraphPlot
		  collapsed:: true
			- Plot networks
			- ![](https://reference.wolfram.com/language/howto/Files/PlotAGraph.en/O_6.png){:height 303, :width 385}
		- PolarPlot
		- ### 3D
		  collapsed:: true
			- `Plot[f, {x, x_min, x_max}, {y, y_min, y_max}]`
			- Further possibilities
			  collapsed:: true
				- Density plot
				- SliceContourPlot: Take slices and plot contours.
				- Sphericalplot
		- ### Vector
			- VectorPlot
			- StreamPlot
	- ## Random
		- Note: Generating a random array is much faster than generating the elements one-by-one.
		- `RandomReal[{x_min,x_max}]`
			- Note that the input should be a list.
		- RandomInteger
- # Tricks
	- Suppress output of a line by `;`
- # Interesting Examples
  collapsed:: true
	- ![image.png](../assets/image_1702283625778_0.png){:height 293, :width 395}
	  collapsed:: true
		- `f` generates the wavefunction of the nth level
		- `Evaluate` causes an expression to be evaluated even if it appears as an argument of a function specified to be unevaluated.
		- `@` is the prefix
		- `Append` adds an elements to a list.
			- Here the appended element is $x^2/2$, the potential.
		- `Table` generates a list by applying the expr in the first argument to the following list (or iterator). Similar to `/@`.
		-
	- ![image.png](../assets/image_1702369076614_0.png){:height 744, :width 534}
		- `$` isn't a special symbol in Mathematica. Just a convention to define global variables.
		-
- # Algebraic Number Theory
  collapsed:: true
	- Ref. MMA/guide/AlgebraicNumberTheory
	- ## Useful functions
		- Represent algebraic numbers
			- AlgebraicNumber
				- ![image.png](../assets/image_1673569521240_0.png)
				- Theta can be represented by the function `Root`
				- eg. `AlgebraicNumber[Root[#^3 + # + 1 &, 3], {1, 2, 1}]`
			- ToNumberField
				- Putting different algebraic numbers in a common extension could accelerate computation.
		- Characters
			- AlgebraicNumberNorm
			- AlgebraicNumberTrace
			- AlgebracNumberDenominator
			- NumberFieldDiscriminant
			-