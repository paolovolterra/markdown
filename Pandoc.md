## Pandoc


Creare un documento in LaTeX o PDF con bibliografia

Una volta aggiunte al testo le citazioni, si potrà convertire il file da Markdown nel formato desiderato usando Pandoc e l'estensione pandoc-citeproc.

Esempio: il file in formato BibTeX biblio.bib contiene le seguenti righe:

@book{dougadams:ggpa,
    author = {Douglas, Adams},
    title = {Guida galattica per gli autostoppisti},
    series = {Urania},
    volume = {1},
    publisher = {Mondadori},
    address = {Milano},
    year = {1980}
    }

Convertire un testo da Markdown a LaTeX specificando il file bibliografico esterno:

pandoc --bibliography=biblio.bib saggio.md -o saggio.tex

Convertire un testo da Markdown a PDF con indice:

pandoc --bibliography=biblio.bib --toc -s saggio.md -o saggio.pdf

Lo stesso comando con estensione .epub produrrà l'effetto desiderato. (generare un EPUB).

L'opzione standalone -s produce un documento indipendente;
L'opzione --toc genera l'indice dei contenuti;
L'opzione -N numera i capitoli;
L'opzione -H, ad esempio: -H head.css, può essere usata per inserire un link a un file css nel header HTML.

Quando non si specifica lo stile di citazione con l'opzione --csl Pandoc usa il Chicago Manual of Style.

Pandoc usa unicode UTF-8. Consultare il manuale di Pandoc per altre opzioni.

Le citazioni vengono riportate automaticamente alla fine del documento, dunque l'ultimo capitolo farà bene a chiamarsi: Bibliografia.

# Bibliografia


vedi [pagina apposita](https://github.com/paolovolterra/markdown/blob/main/Pandoc.md#converting-markdown-to-pdf-or-docx-with-pandoc)


  
# [Converting Markdown to PDF or DOCX with Pandoc](https://www.mscharhag.com/software-development/pandoc-markdown-to-pdf)

Markdown is a popular text formatting syntax among developers these days. Popular Sites like Github or Bitbucket use Markdown for project documentation and various other types of user generated content. These sites automatically convert markdown syntax to HTML, so it can be displayed in a browser.

## Windows
However, maybe you want to use Markdown as document format without using a platform that does the conversion for you. Or you are in need of an output format other than HTML. In this case you need a tool that can convert markdown to the desired target format. Pandoc is is a document conversion tool that can be used for exactly this (and a lot of other things). With Pandoc you can convert Markdown documents to PDF, HTML, Words DOCX or many other formats.

After installing Pandoc, you can simply run it from command line.

Note: By default, Pandoc uses LaTeX to generate PDF documents. So, if you want to generate PDF documents, you need to install a LaTex processor first (list of required LaTeX packages).

To convert a doc.md Markdown file into a PDF document, the following command can be used:

>  pandoc -s -o doc.pdf doc.md

Pandoc is able to merge multiple Markdown files into a single PDF document. To generate a single PDF document out of two Markdown files you can use:

>  pandoc -s -o doc.pdf part01.md part02.md

By default the page margins in the resulting PDF document are quite large. You can change this by passing a margin parameter:

>  pandoc -s -V geometry:margin=1in -o documentation.pdf part01.md part02.md

To create HTML or DOCX documents you simply have to change the file extension of the target file:

>  pandoc -s -o doc.html part01.md part02.md
>  pandoc -s -o doc.docx part01.md part02.md

The resulting documents are well formatted. 

## Linux

> sudo apt-get install pandoc pandoc-citeproc texlive


## sitografia

### generici
https://opensource.com/article/18/9/intro-pandoc

### linux
https://waylonwalker.com/til/convert-markdown-pdf-linux/

## video
https://www.youtube.com/watch?v=nr5HA32GMFA
