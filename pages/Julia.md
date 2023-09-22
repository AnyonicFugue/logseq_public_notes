# Basic Syntax
	- Functions
		- keyword argument: Place after a semicolon
		- e.g. `function test(a,b;c,d)`
			- a,b are positional
			- c,d are keywords
	- `function func()` and `for` need an `end`
	-
	- ## Logical operators #card
	  card-last-score:: 5
	  card-repeats:: 3
	  card-next-schedule:: 2023-05-03T04:15:01.231Z
	  card-last-interval:: 67.2
	  card-ease-factor:: 2.8
	  card-last-reviewed:: 2023-02-25T00:15:01.232Z
	  collapsed:: true
		- C-style `&&, !, ||`
		- All doubled except `!`
	- ## Multiple File
	  collapsed:: true
		- Use `include("utils.jl")` to include other files.
	- ## Arrays
	  collapsed:: true
		- `zeros(T, dims...)` an `Array` of all zeros
		- `ones(T, dims...)` an `Array` of all ones
		- `A*B` for matrix multiplication.
		- `A'` is complex conjugation
		- `inv(A)` is the inverse
	- ## Specify Types #card
	  card-last-score:: 3
	  card-repeats:: 3
	  card-next-schedule:: 2023-05-10T10:40:26.970Z
	  card-last-interval:: 61.44
	  card-ease-factor:: 2.56
	  card-last-reviewed:: 2023-03-10T00:40:26.971Z
	  collapsed:: true
		- `function Wolff_iterate(StateArr::Array{Int8})`
			- Type **after** the argument
		- `x::Int32=100`
	- ## File Operations
		- ```julia
		  io = open("runoob-file.txt", "a+")
		  
		  # 写入文件内容
		  write(io, "Hello world!\nRunoob Julia Test")
		  close(io)
		  ```
- # Features
	- Parallel computation
		- Multithreading
		  card-last-interval:: 10
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-12-15T12:57:37.498Z
		  card-last-reviewed:: 2022-12-05T12:57:37.498Z
		  card-last-score:: 5
			- Syntax #card
			  card-last-interval:: 297.18
			  card-repeats:: 4
			  card-ease-factor:: 2.66
			  card-next-schedule:: 2024-05-30T17:01:15.998Z
			  card-last-reviewed:: 2023-08-07T13:01:15.999Z
			  card-last-score:: 5
				- Add `--threads=auto`  as a command argument at startup
				- Just add `Threads.@threads`  to parallelize a for loop!
					- ```	 
					  	Threads.@threads for i = 1:10
					         a[i] = Threads.threadid()
					     end
					  ```
			- Potential problems #card
			  card-last-interval:: 117.6
			  card-repeats:: 3
			  card-ease-factor:: 2.8
			  card-next-schedule:: 2023-12-07T02:49:11.881Z
			  card-last-reviewed:: 2023-08-11T12:49:11.881Z
			  card-last-score:: 5
				- Racing
					- Trigger
						- Multiple threads share a same piece of memory and at least one is writing.
						- Especially things like `a+=1` when different threads share the same `a`!
					- Solution
						- Allocate a separate buffer for each thread
						- For shared memory use locks or channels.
				- Overhead at memory allocation
					- Trigger
						- Allocating memory inside threads are extremely inefficient.
					- Solution
						- Preallocate a large array before the loop
						- Use **static arrays** for critical parts of code
		- Multiprocessing
	- Plotting #card
	  card-last-score:: 3
	  card-repeats:: 4
	  card-next-schedule:: 2023-09-07T00:39:24.288Z
	  card-last-interval:: 169.81
	  card-ease-factor:: 2.66
	  card-last-reviewed:: 2023-03-21T05:39:24.289Z
	  collapsed:: true
		- Use PyPlot.
		- Example.
		  
		  ```Julia
		      import PyPlot as plt
		      plt.plot(VolumeArr,EntropyArr,VolumeArr,av*VolumeArr.+bv)
		      plt.title("Entropy vs Volume")
		      plt.grid()
		      plt.show()
		  ```
			- Here I plotted 2 curves, i.e. `EntropyArr` vs `VolumeArr` and `av*VolumeArr.+bv` vs `VolumeArr`
			  Note that each pair of `(x,y)` must be written explicitly, **cannot** ignore!
	- Use @time to analyze a function.
	  collapsed:: true
		- Pay special attention to the memory allocation.
			- #+BEGIN_QUOTE
			  'Unexpected memory allocation is almost always a sign of some problem with your code, usually a problem with type-stability or creating many small temporary arrays. '
			  #+END_QUOTE
		- More generally, the tools [docs.julialang.org/en/v1/manual/performance tips/#tools](https://docs.julialang.org/en/v1/manual/performance-tips/#tools) can help.
	- Finite Field
	  collapsed:: true
		- Correct way to deal with finite fields in Julia by AbstractAlgebra.jl'
			- ```julia
			  F2=AbstractAlgebra.GF(2)
			  un=F2(1)
			  ```
			- Create vectors by `u=zeros(F2,2)` and matrices by `A=zeros(F2,2,2)`. This avoids the Any type to pop up.
			- Assign values by `un` rather than 1.
		- Note that only arithmetic operations, polynomials, norm, etc. (i.e. mainly abstract algebra) are supported.
		- Matrix multiplication is supported, but general linear algebra operations (rank, det, etc.) are **not**. Better implement by myself
- # Common mistakes
  collapsed:: true
	- ## Error Texts
		- > no method matching setindex!(::Bool, ::Bool, ::Int64)
			- Usually it is because I wrote a Python-style indexing of arrays.
				- i.e. The Julia style is `arr[a,b]`, but the Python style is `arr[a][b]`
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
	  card-last-interval:: 353.22
	  card-repeats:: 4
	  card-ease-factor:: 2.9
	  card-next-schedule:: 2024-09-06T05:39:46.583Z
	  card-last-reviewed:: 2023-09-19T00:39:46.583Z
	  card-last-score:: 5
		- Use [i,j], not [i][j] (Different from [[C++]])
		- Use [i,:] to obtain a slicing. **The dummy index must have a colon.**
			- [i] isn't enough; Julia would return only one element.
			- Note that partial slicing is also possible. See document.
		- Especially the sum should be `sum(arr[i,:])`! The colon must be present!
	- Vectorized operations #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-05-04T17:08:18.196Z
	  card-last-reviewed:: 2023-02-26T13:08:18.196Z
	  card-last-score:: 5
		- `arr3=(arr1.+arr2).^2`
		- The dot is necessary. Otherwise only a single element is modified.
			- But no dot before the equality.
- # Performance Tips
  collapsed:: true
	- ## Profiling
		- ```julia
		  Profile.@profile sample_EE(18,12,40,false,true)
		  Profile.print(mincount=800)
		  ```
			- `mincount` excludes many irrelevant function calls.
	- ## Reduce allocation of memory.
		- Allocate a large buffer beforehand, in one line
		- Avoid `push!()`, which is costly.
		  Use a fixed-size buffer and maintain a `arr_size` instead.
		- Use `view()` in slicing, which avoids creating new arrays.
- # Data Structures
  collapsed:: true
	- ## Vector
		- We can create vectors by `v=Vector{T}()`, but it is just an alias for an 1D array.
		- Supported operators are `push()`, `pushfirst()`, `pop()`, `popfirst()`