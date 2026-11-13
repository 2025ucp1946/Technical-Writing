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


## Example and expected output

For the basic file above, compile `main.tex` in Overleaf or another LaTeX editor.

The generated PDF will look approximately like this:

\`\`\`text
             My First Document
                Student Name
             [Current date]

1  Introduction
This is my first LaTeX document.

2  Conclusion
LaTeX makes documents neat and organized.
\`\`\`

The exact spacing and date depend on the compiler and when you compile it.

### Example: formatting text

Code:

\`\`\`latex
Normal text, \textbf{bold text}, and \textit{italic text}.
\`\`\`

Expected PDF text:

\`\`\`text
Normal text, bold text, and italic text.
\`\`\`

The words marked with \textbf are bold, and the words marked with \textit are italic.

### Example: list output

The itemize example produces a bulleted list:

- First point
- Second point

The enumerate example produces a numbered list:

1. First step
2. Second step

### Example: equation output

The code \`\\[a^2 + b^2 = c^2\\]\` displays a centered equation:

\[
a^2 + b^2 = c^2
\]

### Example: table output

The table code produces a two-column table:

| Name | Marks |
|---|---:|
| Asha | 90 |
| Ravi | 85 |

These are examples of the PDF result; LaTeX source code itself is not the final formatted document.
