# Beamer

## What is Beamer?

Beamer is a LaTeX document class used to create presentations. A Beamer presentation is written as LaTeX code and compiled into slides in PDF format.

## Basic Beamer presentation

Save the following as `presentation.tex`.

```latex
\documentclass{beamer}

\title{My First Presentation}
\author{Student Name}
\date{\today}

\begin{document}

\begin{frame}
  \titlepage
\end{frame}

\begin{frame}{Introduction}
  This is my first slide.
\end{frame}

\begin{frame}{Topics}
  \begin{itemize}
    \item First topic
    \item Second topic
    \item Third topic
  \end{itemize}
\end{frame}

\end{document}
```

## Important commands

- `\documentclass{beamer}`: creates a presentation.
- `\begin{frame}...`: starts a slide.
- `\end{frame}`: ends a slide.
- `\title{}`, `\author{}`, `\date{}`: set presentation details.
- `\titlepage`: displays the title slide.
- `\frametitle{}`: sets a slide title.
- `\section{}`: groups slides into sections.
- `\pause`: reveals content step by step.

## Adding an image

```latex
\begin{frame}{My Image}
  \includegraphics[width=0.6\textwidth]{image.png}
\end{frame}
```

For images, load the graphics package in the preamble:

```latex
\usepackage{graphicx}
```

## Themes

A theme changes the appearance of the slides. Example:

```latex
\usetheme{Madrid}
```

Place the theme command before `\begin{document}`.

## How to create a presentation

1. Create a `.tex` file.
2. Add the Beamer document class.
3. Write each slide inside a frame.
4. Compile the file using Overleaf or a LaTeX installation.
5. Check the generated PDF presentation.

## What I learned

I learned how to make slides using LaTeX, add titles and bullet points, insert images, and apply themes.


## Example and expected slide output

Compile \`presentation.tex\`. The result is a PDF presentation with three slides.

**Slide 1 – Title slide**

\`\`\`text
My First Presentation

Student Name
[Current date]
\`\`\`

**Slide 2 – Introduction**

\`\`\`text
Introduction

This is my first slide.
\`\`\`

**Slide 3 – Topics**

\`\`\`text
Topics

• First topic
• Second topic
• Third topic
\`\`\`

The actual appearance depends on the selected Beamer theme.

### Example: reveal content step by step

Code:

\`\`\`latex
\begin{frame}{Steps}
  First point
  \pause
  Second point
\end{frame}
\`\`\`

Expected result: the first point appears first. The second point appears on the next presentation step.

### Example: use a theme

Add this before \`\\begin{document}\`:

\`\`\`latex
\usetheme{Madrid}
\`\`\`

Expected result: the slides use the Madrid theme's colors and layout.

### Example: add an image

If \`image.png\` is in the same folder as the LaTeX file, the image is displayed on the slide. If the file is missing or the name is incorrect, compilation may report an error.
