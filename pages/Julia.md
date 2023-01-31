- Frequently used features
	- Logical operators #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-02-21T07:05:59.852Z
	  card-last-reviewed:: 2023-01-28T07:05:59.852Z
	  card-last-score:: 5
		- C-style `&&, !, ||`
		- All doubled except `!`
	- Parallel computation
		- Multithreading
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-12-15T12:57:37.498Z
		  card-last-reviewed:: 2022-12-05T12:57:37.498Z
		  card-last-score:: 5
			- Syntax #card
			  card-last-interval:: 10
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2022-12-16T07:42:51.041Z
			  card-last-reviewed:: 2022-12-06T07:42:51.042Z
			  card-last-score:: 5
				- Add `--threads=auto`  as a command argument at startup
				- Just add `Threads.@threads`  to parallelize a for loop!
					- ```	 
					  	Threads.@threads for i = 1:10
					         a[i] = Threads.threadid()
					     end
					  ```
			- Potential problems #card
			  card-last-interval:: 10.42
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2022-12-23T16:28:00.325Z
			  card-last-reviewed:: 2022-12-13T06:28:00.325Z
			  card-last-score:: 5
				- Racing
					- Avoid modifying (including +=) one piece of data from multiple threads.
				- Overhead at memory allocation
					- Preallocate buffers
					- Use static arrays for critical parts of code
		- Multiprocessing
	- Plotting #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-03-03T08:16:52.075Z
	  card-last-reviewed:: 2022-12-26T04:16:52.075Z
	  card-last-score:: 5
		- Temporary solution: Use GR.jl to plot and use readline() to block the program.
		- ```
		    GR.xlabel("\$tL^{1/v}\$")
		    GR.ylabel("\$ML^{ (D-2+\\eta)/ 2}\$")
		    GR.scatter(vec(x_list),vec(y_list)) #Scattered points
		    a=readline()
		  
		    GR.xlabel("T")
		    GR.ylabel("Binder cumulant")
		    GR.plot(T_list, Binder_para_list[1,:]) #Points connected by lines
		  ```
		- Essentially, store the data into arrays then plot them.
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
	  card-last-interval:: 10
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2022-12-14T06:09:02.065Z
	  card-last-reviewed:: 2022-12-04T06:09:02.065Z
	  card-last-score:: 5
		- `function Wolff_iterate(StateArr::Array{Int8})`
- Common mistakes
	- Usage of range #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-03-08T11:08:09.696Z
	  card-last-reviewed:: 2022-12-31T07:08:09.697Z
	  card-last-score:: 5
		- `range(1,10)`
		- I must specify the beginning.
		- It is comma instead of colons (Different from [[Python]])
	- Access and slice multidimensional arrays #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-02-05T00:27:44.849Z
	  card-last-reviewed:: 2023-01-12T00:27:44.849Z
	  card-last-score:: 5
		- Use [i,j] instead of [i][j] (Different from [[C++]])
		- Use [i,:] to obtain a slicing. **The dummy index must have a colon.**
			- [i] isn't enough; Julia would return only one element.
			- Note that partial slicing is also possible. See document.
	- Vectorized operations #card
	  card-last-interval:: 10
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-12-13T07:02:21.115Z
	  card-last-reviewed:: 2022-12-03T07:02:21.115Z
	  card-last-score:: 5
		- `arr=arr.^2`
		- The dot is necessary.