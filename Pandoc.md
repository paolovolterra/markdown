## Pandoc

vedi [pagina apposita](https://github.com/paolovolterra/markdown/blob/main/Pandoc.md#converting-markdown-to-pdf-or-docx-with-pandoc)



## Kramdown

Kramdown è un convertitore Markdown gratuito e open source scritto nel linguaggio di programmazione Ruby. 
È progettato principalmente per convertire i file Markdown in file HTML. 
Tuttavia, puoi usarlo per convertire i file Markdown anche nei formati di file kramdown, LaTeX e PDF.

Puoi installare Kramdown in Ubuntu usando il comando specificato di seguito: **$ sudo apt install kramdown**

Puoi installare Kramdown in altre distribuzioni Linux dal gestore pacchetti. 
Ulteriori istruzioni per l'installazione sono disponibili qui .

Per convertire un file ".md" in un file ".html" utilizzando Kramdown, esegui un comando nel seguente formato: **$ kramdown file.md -i markdown -o html > file.html**

Sostituisci "file.md" per cambiare il nome del file di input. 
L'opzione "-i" prende un nome per il formato del file di input mentre l'opzione "-o" può essere utilizzata per specificare il formato per l'output convertito. Sostituisci "file.html" con il nome desiderato per il file di output.

Per ulteriori informazioni su Kramdown, eseguire i seguenti due comandi:
$ kramdown --aiuto
$ uomo Kramdown

## Cmark

Cmark o CommonMark è un parser e convertitore Markdown gratuito e open source scritto nel linguaggio di programmazione C. 
Afferma di essere molto più veloce di altre app di analisi Markdown disponibili sul Web. 
Fornisce inoltre una versione modificata della sintassi di Markdown, con l'obiettivo di semplificare la scrittura di contenuti RTF.

Puoi installare Cmark in Ubuntu usando il comando specificato di seguito:	**$ sudo apt install cmark**

Puoi installare Cmark in altre distribuzioni Linux dal gestore pacchetti. 
Ulteriori istruzioni per l'installazione sono disponibili qui .

Per convertire un file ".md" in un file ".html" utilizzando Cmark, eseguire un comando nel seguente formato:	**$ cmark file.md -t html > file.html**

Sostituisci "file.md" per cambiare il nome del file di input. 
L'opzione "-t" viene utilizzata per specificare il formato del file di output. 
Sostituisci "file.html" con il nome desiderato per il file di output. 
Puoi convertire i file ".md" nei formati xml, html, commonmark, latex e man (manpage) usando Cmark.

Per ulteriori informazioni su Cmark, eseguire i due comandi seguenti:
	$ uomo cmark
	$ cmark --help

## Grip

Grip è un renderer e un visualizzatore di file Markdown gratuito e open source scritto in Python. 
È progettato principalmente per visualizzare in anteprima i file "README.md" compatibili con GitHub. Ma puoi usarlo anche per convertire altri file Markdown in formato file HTML.

Puoi installare Grip in Ubuntu usando il comando specificato di seguito:	**$ sudo apt install grip**

Puoi installare Grip in altre distribuzioni Linux dal gestore pacchetti. 
Ulteriori istruzioni per l'installazione sono disponibili qui .

Per convertire un file ".md" in un file ".html" utilizzando Grip, esegui un comando nel seguente formato:	**$ grip file.md --export file.html**

Sostituisci "file.md" per cambiare il nome del file di input. 
Sostituisci "file.html" con il nome desiderato per il file di output. 
Assicurati che il nome del file di output termini con l'estensione ".html" per convertire il file correttamente senza errori.

Per ulteriori informazioni su Grip, eseguire i due comandi seguenti:
	$ grip --aiuto
	$ dell'uomo presa
  
  
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
