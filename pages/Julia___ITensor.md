- [Introduction · ITensors.jl](https://itensor.github.io/ITensors.jl/dev/index.html)
- # Constructions
  id:: 651397dd-de98-4904-a3eb-afc5949b701e
	- ITensor
		- ```julia
		  i = Index(2,"index_i")
		  j = Index(4,"index_j")
		  k = Index(3,"index_k")
		  
		  A = ITensor(i,j)
		  B = ITensor(ComplexF64,k,j)
		  ```
			- The default type is `Float64`
			-
- # Tensor Indices
	- Idea
		- We regard indices as objects (connected legs between two tensors) rather than a simple index of an array.
		- Therefore when we contract two tensors, the program knows which legs to contract (i.e. legs having the same index object).
	- ((651397dd-de98-4904-a3eb-afc5949b701e))
		- ```julia
		  i = Index(2; tags="l", plev=1)
		  ```
			- i is an index object with dimension 2
			- `tags` sets tags
			- `plev` sets the prime level.
-
- # DMRG
  collapsed:: true
	- Example. We are interested in finding the ground state of
	  $$
	  H=\sum_{j=1}^{N-1} \mathbf{S}_j \cdot \mathbf{S}_{j+1}=\sum_{j=1}^{N-1} S_j^z S_{j+1}^z+\frac{1}{2} S_j^{+} S_{j+1}^{-}+\frac{1}{2} S_j^{-} S_{j+1}^{+}
	  $$
	- collapsed:: true
	  ```julia
	  using ITensors
	  
	    N = 100
	    sites = siteinds("S=1",N)
	  
	    os = OpSum()
	    for j=1:N-1
	      os += "Sz",j,"Sz",j+1
	      os += 1/2,"S+",j,"S-",j+1
	      os += 1/2,"S-",j,"S+",j+1
	    end
	    H = MPO(os,sites)
	  
	    psi0 = randomMPS(sites,10)
	  
	    nsweeps = 5
	    maxdim = [10,20,100,100,200]
	    cutoff = [1E-10]
	  
	    energy, psi = dmrg(H,psi0; nsweeps, maxdim, cutoff)
	  
	    return
	  end
	  ```
		- ```julia
		  N = 100
		  sites = siteinds("S=1",N)
		  ```
			- It makes an array of indices with the properties of $S=1$ spins. The program knows it will be a 3-dimensional space.
				- ```julia
				  @show sites[1]
				  (dim=3|id=73|"S=1,Site,n=1")
				  
				  ```
		- ```julia
		  os = OpSum()
		  for j=1:N-1
		    os += "Sz",j,"Sz",j+1
		    os += 1/2,"S+",j,"S-",j+1
		    os += 1/2,"S-",j,"S+",j+1
		  end
		  H = MPO(os,sites)
		  ```
			- An `opsum` is an object which records the Hamiltonian terms.
			- The last line constructs the Hamiltonian.
		- ```julia
		  psi0 = randomMPS(sites,10)
		  ```
			- The line constructs a random MPS with physical indices `sites` and bond dimension 10.
		- ```julia
		  nsweeps = 5
		  maxdim = [10,20,100,100,200]
		  cutoff = [1E-10]
		  ```
			- This line controls the parameters, including maximum bond dimensions and maximum truncation error.
		- ```julia
		  energy, psi = dmrg(H,psi0; nsweeps, maxdim, cutoff)
		  ```
			- The line finally runs DMRG and return the optimized MPS and energy.
	- ## Quantum Number Conserving
		- For example, I could require that all fluxes be 0 in [[Kitaev Honeycomb]].
		  This reduces complexity.
		- Not much modification of the code is needed. Just add a few lines to conserve quantum numbers.
		-
- # Basic ITensor Operations
	- ## Factoring
		- SVD
			- `U,S,V = svd(T,(i,k))`
				- This means that we group $j$ and $k$ as a single index.
			- ![](https://itensor.github.io/ITensors.jl/dev/examples/itensor_factorization_figures/SVD_Ex1.png){:height 73, :width 408}
		- Truncated SVD
			- Available accuracy factors
				- `cutoff` -- real number $\epsilon$. Discard the smallest singular values $\lambda_n$ such that the truncation error is less than $\epsilon$:
				  $$\frac{\sum_{n \in \text { discarded }} \lambda_n^2}{\sum_n \lambda_n^2}<\epsilon$$.
				- `maxdim` -- integer $M$. If the number of singular values exceeds $M$, only the largest $\mathrm{M}$ will be retained.
				- `mindim` -- integer $m$. At least $m$ singular values will be retained, even if some fall below the cutoff
			-