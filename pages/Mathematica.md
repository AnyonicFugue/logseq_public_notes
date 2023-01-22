alias:: MMA

- # Algebraic Number Theory
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