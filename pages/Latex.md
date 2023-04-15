- Basic signs
	- 'Big' things are obtained by {{cloze capitalizing the first letter}}.
		- $\Rightarrow$ = `\Rightarrow`
	- $\subset$ and $\subseteq$ #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-03-05T11:10:11.393Z
	  card-last-reviewed:: 2023-02-09T11:10:11.394Z
	  card-last-score:: 5
		- `\sub` and `\subseteq`
- Lists and Tables
- Text Alignment
- Paragraph Formatting
	- Equation numbering
	  collapsed:: true
		- Single equation
			- `\begin{equation}`
		- Multiple equations one number
			- ```
			  \begin{equation}
			  \begin{aligned}
			  \end{aligned}
			  \end{equation}
			  ```
		- Multiple equations multiple numbers
			- `\begin{align}`
		- No numbering
			- `\begin{equation*}`
				- The star always removes numbering
			- `\nonumber`
	- Multi-column
		- `\package{multicols}{n}`
	-
- Citation and Bib
	- Summary
		- First, create a `.bib` file
		- Add items to the file
			- They can be exported in arXiv
		- Use `\bibliography{file}` to include it
		- Use `\cite{Kitaev_2006}` to cite specific articles
- # Warnings #card
	- #+BEGIN_CAUTION
	  Latex is quite old and decentralized, so there are many strange bugs. 
	  #+END_CAUTION
	- Don't use `$$$$` to create multi-line formulae. Use `\begin{equation}` to avoid potential problems.
	-