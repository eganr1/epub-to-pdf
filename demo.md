---
title: Demo Book
creator:
- role: author
  text: Regina Egan
cover-image: cover.jpg
---

# How to Convert Files to PDFs Using Pandoc

## 1. Markdown to PDF

### 1. Initial Set Up

Navigate to the desired folder or path and ensure that there is a demo.md file there with content.

Ensure that the following are installed:

#### `xelatex`
`brew tap homebrew/cask`
`brew install basictex`
`eval "$(/usr/libexec/path_helper)"`
`sudo tlmgr update --self`
`sudo tlmgr install texliveonfly`
`sudo tlmgr install xelatex`
`sudo tlmgr install adjustbox`
`sudo tlmgr install tcolorbox`
`sudo tlmgr install collectbox`
`sudo tlmgr install ucs`
`sudo tlmgr install environ`
`sudo tlmgr install trimspaces`
`sudo tlmgr install titling`
`sudo tlmgr install enumitem`
`sudo tlmgr install rsfs`

#### `pandoc`
`brew install pandoc`

### 2. Formatting the Markdown file

Add the following text to the top of the file:

`---
title: Demo Book
creator:
- role: author
  text: Regina Egan
cover-image: cover.jpg
---`

### 3. Converting to PDF

Run the following command:

`pandoc demo.md --pdf-engine=xelatex -o demo.pdf`

## EPUB to PDF

### 1. Initial Set Up

This example uses the `I.xhtml` file located in this folder (./Hamlet.epub/OEBPS/Text/I.xhtml)

### 2. Converting to PDF

Run the following command to convert the first act to a PDF:

`pandoc ./Hamlet.epub/OEBPS/Text/I.xhtml --pdf-engine=xelatex -o hamlet1.pdf`

For another example, create a pdf of the second act:

`pandoc ./Hamlet.epub/OEBPS/Text/II.xhtml --pdf-engine=xelatex -o hamlet2.pdf`

For the third act:

`pandoc ./Hamlet.epub/OEBPS/Text/III.xhtml --pdf-engine=xelatex -o hamlet3.pdf`

For the fourth act:

`pandoc ./Hamlet.epub/OEBPS/Text/IV.xhtml --pdf-engine=xelatex -o hamlet4.pdf`

### 3. Combining PDFs