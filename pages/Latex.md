- Basic signs
  collapsed:: true
	- 'Big' things are obtained by {{cloze capitalizing the first letter}}.
		- $\Rightarrow$ = `\Rightarrow`
	- $\subset$ and $\subseteq$ #card
	  card-last-interval:: 297.18
	  card-repeats:: 4
	  card-ease-factor:: 2.66
	  card-next-schedule:: 2024-06-19T17:49:56.308Z
	  card-last-reviewed:: 2023-08-27T13:49:56.309Z
	  card-last-score:: 3
		- `\sub` and `\subseteq`
	- $\hookrightarrow$ #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-11-18T06:38:04.191Z
	  card-last-reviewed:: 2023-10-18T00:38:04.191Z
	  card-last-score:: 5
		- `\hookrightarrow`
	-
- # Fonts
  collapsed:: true
	- mathsf vs mathbf
		- $\mathsf A, \mathsf B, \mathsf C$
		- $\mathbf A,\mathbf B,\mathbf C$
		-
	- mathcal vs mathscr
		- $\mathcal A, \mathcal B, \mathcal C$
		- $\mathscr A,\mathscr B,\mathscr C$
	-
		-
- # Matrix and Array
  collapsed:: true
	- $$\rho =\left [\begin{array}{ c c|c c }
	  1 & 0 & 0 & 1\\
	  0 & 0 & 0 & 0\\
	  \hline
	  0 & 0 & 0 & 0\\
	  1 & 0 & 0 & 1
	  \end{array} \right ]$$
		- `c c | c c` for the vertical line, `hline` for the horizontal line
		- The brackets encircles the whole array by `\left` and `\right`
			- In Mathcha, just input them at the left and right of the array.
- # Formatting
  collapsed:: true
	- Paragraph Formatting
		- Indentation
			- ```
			  \setlength{\parindent}{20pt}
			  ```
			- Avoid indentation by setting to 0pt or use `\noindent` at the beginning of each paragraph.
			- `\indent` forces indentation.
		- New lines after each paragraph
			- Just add `\usepackage{parskip}`
			-
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
	  collapsed:: true
		- `\package{multicols}{n}`
		-
- # Citation and Bib
  collapsed:: true
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
  collapsed:: true
	- #+BEGIN_CAUTION
	  Latex is quite old and decentralized, so there are many strange bugs. 
	  #+END_CAUTION
	- Don't use `$$$$` to create multi-line formulae. Use `\begin{equation}` to avoid potential problems.
	- Avoid using `Shift+Enter` to create a new line in formulae. Use `\begin{aligned}`.
	-
- Color
	- ```
	  \textcolor{red}{Some text to be colored}
	  ```
-