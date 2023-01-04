- Basic signs
	- 'Big' things are obtained by {{cloze capitalizing the first letter}}.
		- $\Rightarrow$ = `\Rightarrow`
	- $\subset$ and $\subseteq$ #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-01-20T06:35:17.440Z
	  card-last-reviewed:: 2022-12-26T06:35:17.440Z
	  card-last-score:: 5
		- `\sub` and `\subseteq`
- Lists and Tables
- Text Alignment
- Paragraph Formatting
	- Equation numbering
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