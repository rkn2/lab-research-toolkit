# LaTeX and Overleaf

All papers and grants written by this lab are written in LaTeX. If you have not used LaTeX before, this guide will get you started. If you have used it before, the sections on Overleaf and Penn State templates are still worth reading.

**Jump to:**
- [What is LaTeX?](#what-is-latex)
- [Overleaf](#overleaf)
- [Penn State Dissertation Template](#penn-state-dissertation-template)
- [Journal and Conference Templates](#journal-and-conference-templates)
- [Essential LaTeX to Know](#essential-latex-to-know)
- [Managing References with BibTeX](#managing-references-with-bibtex)
- [When You Get Stuck](#when-you-get-stuck)

---

## What is LaTeX?

LaTeX is a document preparation system used throughout engineering, math, and science. Instead of formatting text visually like in Word, you write plain text with markup commands and LaTeX handles the typesetting. This means:

- Equations, figures, and references are handled automatically and consistently
- You focus on content, not on manually adjusting spacing or numbering
- The output looks professional and meets journal/conference formatting standards without manual work

The learning curve is real but short. After a few days of use, the basics become second nature.

---

## Overleaf

**overleaf.com**

Overleaf is a browser-based LaTeX editor — no installation required. It compiles your document in real time so you can see the output as you write. This is where all lab writing happens.

**Getting started:**
1. Create a free account at overleaf.com
2. Use your Penn State email — Penn State has an institutional Overleaf license that gives you access to premium features including real-time collaboration
3. When Rebecca shares a project with you, you will get an email invitation — accept it and the project will appear in your Overleaf dashboard

**Key features to know:**
- **Track changes** — like Word's track changes, useful during revision rounds
- **Comments** — leave inline comments for collaborators
- **History** — every compile is saved; you can roll back to any previous version
- **Git sync** — Overleaf projects can be linked to a GitHub repository (premium feature)

---

## Penn State Dissertation Template

Penn State has an official LaTeX template for dissertations that meets the Graduate School formatting requirements. This is what you will use when writing your dissertation.

The template is maintained by the Penn State Graduate School and is available on Overleaf:
- Search "Penn State Thesis" in the Overleaf template gallery
- Or ask Rebecca for the lab's current working copy

Do not attempt to format your dissertation manually — use the template from the start. Reformatting a 200-page document at the end is not a good use of your time.

---

## Journal and Conference Templates

Most journals and conferences provide LaTeX templates. When you are ready to submit a paper:

1. Find the author guidelines on the journal or conference website
2. Download their LaTeX template (usually a `.zip` file containing a `.cls` or `.sty` file and a sample `.tex` file)
3. Upload the template files to Overleaf and start writing in the sample `.tex` file

Common templates the lab uses:
- **ASCE journals** — American Society of Civil Engineers format
- **Elsevier journals** — used for journals like *Engineering Structures*, *Construction and Building Materials*
- **ISPRS** — for photogrammetry and remote sensing conferences

---

## Essential LaTeX to Know

You do not need to memorize LaTeX syntax — you will look things up constantly and that is normal. But a few things are worth learning early:

**Sections:**
```latex
\section{Introduction}
\subsection{Background}
```

**Figures:**
```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.8\textwidth]{figures/myimage.png}
    \caption{A descriptive caption.}
    \label{fig:myimage}
\end{figure}
```

**Cross-references** (always use these instead of typing "Figure 3"):
```latex
As shown in Figure~\ref{fig:myimage}...
```

**Citations** (using BibTeX):
```latex
This has been shown in previous work~\cite{napolitano2020}.
```

**Equations:**
```latex
\begin{equation}
    E = mc^2
    \label{eq:energy}
\end{equation}
```

---

## Managing References with BibTeX

LaTeX handles citations through `.bib` files containing reference entries. Zotero can export your library directly to `.bib` format — this is the recommended workflow:

1. Organize your references in Zotero
2. Export your Zotero collection as a BibTeX `.bib` file
3. Upload the `.bib` file to your Overleaf project
4. Cite using `\cite{key}` where `key` matches the identifier in your `.bib` file

Better yet: Zotero has an Overleaf integration that keeps your `.bib` file automatically synced.

---

## When You Get Stuck

- **Overleaf documentation** — overleaf.com/learn is comprehensive and well-written
- **TeX Stack Exchange** — tex.stackexchange.com answers almost every LaTeX question ever asked
- **Your labmates** — someone has almost certainly solved whatever you are stuck on
