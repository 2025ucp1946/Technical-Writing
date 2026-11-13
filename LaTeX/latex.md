# LaTeX

## What is LaTeX?

LaTeX is a document preparation system used to create well-formatted documents. It is especially useful for reports, assignments, research papers, books, and documents containing mathematical equations.

## Basic LaTeX file

Save this code in a file named `main.tex`.

```latex
\documentclass{article}

\title{My First Document}
\author{Student Name}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}
This is my first LaTeX document.

\section{Conclusion}
LaTeX makes documents neat and organized.

\end{document}
```

## Important commands

- `\documentclass{article}`: selects the document type.
- `\begin{document}` and `\end{document}`: mark the document body.
- `\title{}`, `\author{}`, `\date{}`: set document details.
- `\maketitle`: displays the title.
- `\section{}`: creates a section.
- `\subsection{}`: creates a subsection.
- `\textbf{}`: makes text bold.
- `\textit{}`: makes text italic.
- `\underline{}`: underlines text.

## Lists

Bulleted list:

```latex
\begin{itemize}
  \item First point
  \item Second point
\end{itemize}
```

Numbered list:

```latex
\begin{enumerate}
  \item First step
  \item Second step
\end{enumerate}
```

## Mathematical equations

Inline equation: `$a^2 + b^2 = c^2$`

Displayed equation:

```latex
\[
a^2 + b^2 = c^2
\]
```

## Tables

```latex
\begin{tabular}{|c|c|}
\hline
Name & Marks \\
\hline
Asha & 90 \\
Ravi & 85 \\
\hline
\end{tabular}
```

## How to compile

1. Write the code in a `.tex` file.
2. Open it in a LaTeX editor such as Overleaf or a local LaTeX installation.
3. Compile the file to generate a PDF.
4. Check the PDF and correct any errors.

## What I learned

I learned how to create a document, add headings and lists, format text, write equations, and make tables using LaTeX.
