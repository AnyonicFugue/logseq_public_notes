- Frequently used features
  id:: 6378d89e-e3e2-4c22-b277-bc66afece232
	- Logical operators #card
		- C-style `&&, !, ||`
	- Parallel computation
		- Multithreading #card
			- Add `--threads=auto`  as a command argument at startup
			- Just add `Threads.@threads`  to parallelize a for loop!
				- ```	 
				  	Threads.@threads for i = 1:10
				           a[i] = Threads.threadid()
				       end
				  ```
			- Potential problems
				- Racing
					- Avoid modifying (including +=) one piece of data from multiple threads.
				- Overhead at memory allocation
					- Preallocate buffers
					- Use static arrays for critical parts of code
		- Multiprocessing
	- Plotting #card
		- Temporary solution: Use GR.jl to plot and use readline() to block the program.
	- Matrix operations
	  collapsed:: true
		- A' is complex conjugation
		- inv(A) is the inverse
	- Use @time to analyze a function.
		- Pay special attention to the memory allocation.
			- #+BEGIN_QUOTE
			  'Unexpected memory allocation is almost always a sign of some problem with your code, usually a problem with type-stability or creating many small temporary arrays. '
			  #+END_QUOTE
		- More generally, the tools [docs.julialang.org/en/v1/manual/performance tips/#tools](https://docs.julialang.org/en/v1/manual/performance-tips/#tools) can help.
	- Specify the type when declaring a function #card
		- `function Wolff_iterate(StateArr::Array{Int8})`
- Common mistakes
	- Usage of range #card
		- `range(1,10)`
		- I must specify the beginning.
		- It is comma instead of colons (Different from [[Python]])
	- Access and slice multidimensional arrays #card
		- Use [i,j] instead of [i][j] (Different from [[C++]])
		- Use [i,:] to obtain a slicing. **The dummy index must have a colon.**
			- [i] isn't enough; Julia would return only one element.
			- Note that partial slicing is also possible. See document.
	- Vectorized operations #card
		- `arr=arr.^2`
		- The dot is necessary.