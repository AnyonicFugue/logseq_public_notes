- Basic signs
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
	- Paragraph Formatting
	  collapsed:: true
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
	- Page size and margins
		-
	- Size
		- resizebox
		  collapsed:: true
			- ```
			  \resizebox{10cm}{!}
			  {
			  \begin{tabular}{ccccccccccccc}
			  \hline
			      This & is & a & very & large & table & that & exceeds & the & size & of & the & frame\\
			  \hline
			      a & b & c & d & e & f & g & h & i & j & k & l & m\\
			  \hline
			  \end{tabular}
			  }
			  ```
			- Note that to insert equations, I must use `$` to enter math mode.
				- ```
				  \resizebox{10cm}{!}
				  {
				  $\hat{\sigma}_2=\left(\begin{array}{ccc}
				  e^{3 \pi i / 5} & & \\
				  & \phi^{-1} e^{4 \pi i / 5} & \phi^{-1 / 2} e^{-3 \pi i / 5} \\
				  & \phi^{-1 / 2} e^{-3 \pi i / 5} & -\phi^{-1}
				  \end{array}\right)$
				  }
				  ```
- # Citation and Bib
	- Summary
		- First, create a `.bib` file
		- Add items to the file
			- They can be exported in arXiv
		- Use `\bibliography{file}` to include it
			- Add `\bibliographystyle{unsrt}` for a blank project
		-
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
- # Beamer
  id:: 65541d7c-bacd-45f3-82c1-3dfd0939e173
  collapsed:: true
	- [Beamer - Overleaf, Online LaTeX Editor](https://www.overleaf.com/learn/latex/Beamer%23Creating_a_table_of_contents)
	- Use `\begin{frame}` and `\end{frame}` to create a new page.
	-
	- ## Title Page
	  collapsed:: true
		- ```
		  \title[About Beamer] %optional
		  {About the Beamer class in presentation making}
		  
		  \subtitle{A short story}
		  
		  \author[Arthur, Doe] % (optional, for multiple authors)
		  {A.~B.~Arthur\inst{1} \and J.~Doe\inst{2}}
		  
		  \institute[VFU] % (optional)
		  {
		  \inst{1}%
		  Faculty of Physics\\
		  Very Famous University
		  \and
		  \inst{2}%
		  Faculty of Chemistry\\
		  Very Famous University
		  }
		  
		  \date[VLC 2021] % (optional)
		  {Very Large Conference, April 2021}
		  
		  \logo{\includegraphics[height=1cm]{overleaf-logo}}
		  ```
		- ![Beamer-titlepageUpdated.png](https://sharelatex-wiki-cdn-671420.c.cdn77.org/learn-scripts/images/1/1b/Beamer-titlepageUpdated.png)
		-
	- ## Table of Contents
	  collapsed:: true
		- ```
		  \begin{frame}
		  \frametitle{Table of Contents}
		  \tableofcontents
		  \end{frame}
		  ```
		- Also we can add TOC at the beginning of each section:
		  ```
		  \AtBeginSection[]
		  {
		    \begin{frame}
		      \frametitle{Table of Contents}
		      \tableofcontents[currentsection]
		    \end{frame}
		  }
		  ```
		-
	- ## Figures
		- ```
		  \begin{figure}
		  \centering
		      \includegraphics[width=0.25\textwidth]{filename}
		      \caption{Caption of the figure}
		      \label{fig:question}
		  \end{figure}
		  
		  Observe Figure \ref{fig:question}: it is the
		  first figure I have inserted in beamer.
		  ```
		- In this way the figure both has a caption and we have a way to cite this figure.
		- We could also use ((65541fa8-214d-427e-bb71-aedc97393d99)) to put figures in one column and texts in another.
		-
	- ## Highlight
		- ```
		  \begin{frame}
		  \frametitle{Sample frame title}
		  
		  In this slide, some important text will be
		  \alert{highlighted} because it's important.
		  Please, don't abuse it.
		  
		  \begin{block}{Remark}
		  Sample text
		  \end{block}
		  
		  \begin{alertblock}{Important theorem}
		  Sample text in red box
		  \end{alertblock}
		  
		  \begin{examples}
		  Sample text in green box. The title of the block is ``Examples".
		  \end{examples}
		  
		  \end{frame}
		  ```
		-
	- ## Multi-Column
	  id:: 65541fa8-214d-427e-bb71-aedc97393d99
		- Use `\begin{columns}`
		- ```
		  \begin{frame}
		  \frametitle{Two-column slide}
		  
		  \begin{columns}
		  
		  \column{0.5\textwidth}
		  This is a text in first column.
		  $$E=mc^2$$
		  \begin{itemize}
		  \item First item
		  \item Second item
		  \end{itemize}
		  
		  \column{0.5\textwidth}
		  This text will be in the second column
		  and on a second thoughts, this is a nice looking
		  layout in some cases.
		  
		  \end{columns}
		  
		  \end{frame}
		  ```
		-
- Color
	- ```
	  \textcolor{red}{Some text to be colored}
	  ```
-