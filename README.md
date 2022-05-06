# MARKDOWN and beyond

![](https://miro.medium.com/max/1400/1*zv16_HpmtjBQ3QfObwGkiA.jpeg)

Markdown è un'applicazione a riga di comando gratuita e open source in grado di convertire i file Markdown in file HTML. È un'utilità della riga di comando sviluppata dai creatori della sintassi Markdown stessa. Per installarlo in Ubuntu, usa il comando seguente:
	$ sudo apt install markdown

Puoi installare lo strumento da riga di comando Markdown in altre distribuzioni Linux dal gestore pacchetti. Puoi anche compilarlo dal suo codice sorgente disponibile qui .

Per convertire un file “.md” in un file “.html”, eseguire un comando nel seguente formato:	$ **markdown file.md > file.html**


## gestire un'immagine
linkandola direttamente o prevedere riferimenti

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"



## Pandoc

vedi pagina apposita



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


# [Table to Markdown](https://github.com/kbravh/table-to-markdown/blob/master/README.md)
![](https://github.com/kbravh/table-to-markdown/raw/master/images/logo_128.png)

