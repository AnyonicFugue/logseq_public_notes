- Basic signs
	- 'Big' things are obtained by {{cloze capitalizing the first letter}}.
		- $\Rightarrow$ = `\Rightarrow`
	- $\subset$ and $\subseteq$ #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-07-25T11:20:23.029Z
	  card-last-reviewed:: 2023-05-02T11:20:23.030Z
	  card-last-score:: 5
		- `\sub` and `\subseteq`
	- $\hookrightarrow$
	-
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
  card-last-interval:: 30
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-06-26T01:00:03.251Z
  card-last-reviewed:: 2023-05-27T01:00:03.251Z
  card-last-score:: 3
	- #+BEGIN_CAUTION
	  Latex is quite old and decentralized, so there are many strange bugs. 
	  #+END_CAUTION
	- Don't use `$$$$` to create multi-line formulae. Use `\begin{equation}` to avoid potential problems.
	- Avoid using `Shift+Enter` to create a new line in formulae. Use `\begin{aligned}`.
	-