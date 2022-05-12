# MARKDOWN
![](https://lh3.googleusercontent.com/eMHydm0FuqFGOttVptB2M9HIrGEnLIZxkoHwlBGlrtq8yijnWNy0459ncJl71OtWAO69E4pVSFsdzYIhkV8NbuEchDs=w128-h128-e365-rj-sc0x00ffffff)

L'idea di Markdown è quella di utilizzare un file di testo (.TXT) utilizzando dei "segni" (in linguaggio tecnico markup) per attribuire alle parole una formattazione convenzionale.

* se metto ad es 2 asterischi  - * - sia prima che dopo una parola, markdown capisce che quella parola deve essere scritta in **grassetto**

* se uso la sequenza [ ] ( ) e dentro metto nella prima parte del testo e nella seconda un link, capisce che devo scrivere il testo con un hyperlink [prova]()

Qui c'è il resto della sintassi per dire all'editor che il testo deve essere trattato in modi particolari [link](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)


## gestire un'immagine
linkandola direttamente o prevedere riferimenti

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"


## comando MD
Markdown è anche un'applicazione a riga di comando gratuita e open source in grado di convertire file scritti con un qualsiasi editor (notepad, vim, ecc) in file HTML, PDF, docx

## installare md su Ubuntu:

```linux
$ sudo apt install markdown
```

## usare il comando md

Per convertire un file “.md” in un file “.html”, eseguire un comando nel seguente formato:	$ **markdown file.md > file.html**




## [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

# [Table to Markdown](https://github.com/kbravh/table-to-markdown/blob/master/README.md)
![](https://github.com/kbravh/table-to-markdown/raw/master/images/logo_128.png)


<img src="icon.png" align="right" height="110"/>

# [Eisvogel](https://github.com/pianomanfrazier/pandoc-latex-template#readme)

[![Build Status](https://travis-ci.org/Wandmalfarbe/pandoc-latex-template.svg?branch=master)](https://travis-ci.org/Wandmalfarbe/pandoc-latex-template)

A clean **pandoc LaTeX template** to convert your markdown files to PDF or LaTeX. It is designed for lecture notes and exercises with a focus on computer science. The template is compatible with pandoc 2.



## Preview

[![manuale Pandoc](PandocManual_1.png)](PandocManual.pdf)



graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
    
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!

gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2              :         des4, after des3, 5d


[torna su](#MARKDOWN)
