- [[Julia]]
- [[Python]]
- [[Latex]]
- [[Markdown]]
- [[Mathematica]]
- ((64b9da3c-0d34-4e01-bf64-5082a3b1336e))
-
- # Common Mistakes #card
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-10-23T06:57:43.936Z
  card-last-reviewed:: 2023-09-22T00:57:43.936Z
  card-last-score:: 3
	- Boundary Conditions #card
		- Example. Compute the upper vertex of a given vertex
			- Be very careful about the **range** of the variables (coordinates in this case).
				- Could it be 0? Be `L`?
			- How to avoid?
				- Test the boundary values `0,1,L-1,L`
				- Use indexes starting from `0`. Much simpler when taking mod.
	- The variable just modified
	  collapsed:: true
		- ```julia
		  for j in cur:n
		    # Omit some irrelevant code
		    found=true
		    cur+=1 # The vector at cur has a nonzero i-th component. So for the next component we start the search from cur+1.
		    break
		    
		  end
		  
		  # Eliminate the i-th component of the rest vectors.
		  if(found)  
		    for j in cur:n
		      if Vecs[j,i]==true
		        
		        # The important part is here!
		        
		        Vecs[j,:]=Vecs[j,:] .⊻ Vecs[cur-1,:]
		        Coefficients[j,:]=Coefficients[j,:] .⊻ Coefficients[cur-1,:]
		      end
		    end
		  end
		  
		  ```
		- We often use a *cursor variable* to control the position where we are working on.
		  Thus when we add or subtract 1, we must take care in the code follows.
	- Apply 'Swapping variables' to the same variable
		- Wrong example.
		  
		  ```julia
		  @inline function swaprows!(v::Matrix{Bool},i::Int64,j::Int64)
		      # The function swaps the rows of a matrix, v[i,:] and v[j,:].
		      # The function is inlined to avoid the overhead of function call.
		      v[i,:]=v[i,:] .⊻ v[j,:]
		      v[j,:]=v[i,:] .⊻ v[j,:]
		      v[i,:]=v[i,:] .⊻ v[j,:]
		  end
		  
		  if (Vecs[j,i]==true)
		    swaprows!(Vecs,cur,j)
		    swaprows!(Coefficients,cur,j)
		  
		    found=true
		    cur+=1 # The vector at cur has a nonzero i-th component. So for the next component we start the search from cur+1.
		  end
		  ```
		- It's wrong because when `cur=j` the swapping breaks down.
		  In other words, the trick of *xor swapping* only works for distinct variables.
		- Corrected Version.
		  ```julia
		  
		  if (Vecs[j,i]==true)&&(found==false)
		    if(j!=cur)
		      swaprows!(Vecs,cur,j)
		      swaprows!(Coefficients,cur,j)
		    end
		    
		    found=true
		    cur+=1 # The vector at cur has a nonzero i-th component. So for the next component we start the search from cur+1.
		  end
		  
		  ```
- # Tips against Bugs #card
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-09-21T19:14:56.177Z
  card-last-reviewed:: 2023-08-21T13:14:56.178Z
  card-last-score:: 3
	- Use your strong geometric intuition to remember definitions of variables.
		- Visualize data conventions as diagrams.
	- When modifying handling of certain variables, modify all related points.
		- Use 'search all references' of the IDE.