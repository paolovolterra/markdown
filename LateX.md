---
LateX
---

![](https://meccanicaweb.it/wp-content/uploads/2017/09/LaTeX_logo.png)

LaTeX è un sistema per la creazione di documenti di alta qualità. È comunemente usato da scienziati, ingegneri, sviluppatori di software, matematici e altri professionisti per produrre documenti lunghi e tecnici, ma la sua utilità non è limitata a quello spazio. A differenza di un tipico word processor "ciò che vedi è ciò che ottieni" come Microsoft Word, LaTeX utilizza un linguaggio di markup di testo semplice (simile a HTML e CSS) che viene compilato in un documento PDF utilizzando regole tipografiche ottimali. Ciò si traduce in documenti dall'aspetto professionale che sono di una classe diversa rispetto all'output di un elaboratore di testi. Le numerose opzioni di personalizzazione in LaTeX consentono la creazione di una varietà di tipi di documenti con un controllo preciso su layout e formattazione. LaTeX si presta bene alla creazione di modelli che non richiedono una conoscenza avanzata di LaTeX da utilizzare e manipolare, consentendo a un utente inesperto di LaTeX di creare bellissimi documenti e imparare LaTeX mentre procede. 

LaTeX utilizza un sistema di pacchetti per estenderne funzionalità e caratteristiche. Esistono numerosi pacchetti per creare praticamente qualsiasi elemento del documento e i pacchetti vengono scritti e aggiornati frequentemente

Con LaTeX, il documento viene scritto in un editor di testo semplice (semplice come Blocco note o TextEdit) e fornito al compilatore LaTeX che interpreta i comandi LaTeX insieme al testo per produrre un output PDF. Ciò significa che le impostazioni importanti del documento come i caratteri, i margini e gli stili di intestazione sono definite in una sezione nella parte superiore del documento e qualsiasi formattazione locale (come il testo in grassetto) viene eseguita tramite l'uso di comandi nel testo. 

**prima** <img src="https://www.latextemplates.com/images/freeman-cv_code.png" width="300" height="300"> **dopo** <img src="https://www.latextemplates.com/images/freeman-cv.jpg" width="300" height="300">


# siti interessanti

https://avvocati-e-mac.squarespace.com/blog/2019/4/9/compilare-un-atto-telematico-in-markdown-con-pandoc

https://avvocati-e-mac.squarespace.com/blog/2019/4/7/aggiungere-il-dialetto-di-latex-ad-un-atto-telematico

https://avvocati-e-mac.squarespace.com/blog/2019/4/5/come-scrivere-un-atto-telematico-avanzato-in-markdown

https://avvocati-e-mac.squarespace.com/blog/2021/8/23/scrivere-atti-telematici-avanzati-in-latex-parte-i

https://avvocati-e-mac.squarespace.com/blog/2021/8/30/scrivere-atti-telematici-avanzati-in-latex-parte-ii-convertire-lintestazione-yaml

https://avvocati-e-mac.squarespace.com/blog/2021/9/5/atti-telematici-avanzati-in-latex-p3-le-regole-base-della-formattazione

https://avvocati-e-mac.squarespace.com/blog/2021/11/2/crivere-atti-telematici-avanzati-in-latex-parte-iv-link-interni-a-documenti-ed-al-web-ed-immagini


# ruotare un testo (Latex)

\usepackage{landscape}

\begin{landscape}

\end{landscape}

 
<br>

# tabelle

## [tabella](https://www.youtube.com/watch?v=1cEdqTMtHZQ)

![tabella](./immagini/2021070901.PNG)

![tabella](./immagini/2021070902.PNG)

<br>


## [Excel2LaTeX – Convert Excel spreadsheets to LaTeX tables](https://www.ctan.org/pkg/excel2latex?lang=en)

![tabella](./immagini/2021070905.PNG)
![tabella](./immagini/2021070906.PNG)

 
<br>



## [Creating Flowcharts with TikZ (LaTeX)](https://www.youtube.com/watch?v=LoBC8zIB-3k)
![tabella](./immagini/2021070907.PNG)
 
<br>


## [Excel to Latex - import data table directly from csv file with csvsimple](https://www.youtube.com/watch?v=FYFZS48sLfk)
![tabella](./immagini/2021070908.PNG)
 
<br>


## PDF/A

* [Creating high-quality PDF/A documents using LaTeX](https://www.mathstat.dal.ca/~selinger/pdfa/)

## Inserimento di un file PDF

Usa il pacchetto pdfpages \usepackage{pdfpages}

Per includere tutte le pagine nel file PDF: 

* \includepdf[pages=-]{myfile.pdf} oppure

* \ includepdf {myfile.pdf} 

Per includere solo la prima pagina di un PDF: \includepdf[pages={1}]{myfile.pdf}

Esegui texdoc pdfpagesin una shell per vedere il manuale completo di pdfpages

 
## Layout verticale e orizzontale in un unico PDF

* [Rstudio rmarkdown: layout verticale e orizzontale in un unico PDF](https://www.it-swarm.it/it/r/rstudio-rmarkdown-layout-verticale-e-orizzontale-un-unico-pdf/1049572054/)

Per i casi più comuni.

Ci sono 3 condizioni.

*    Tutto in modalità verticale.

*    Tutto in modalità orizzontale.

*    Miscela di modalità verticale e orizzontale.

Restringiamo ogni singola condizione.

    Il primo, diciamo che abbiamo un documento markdown che inizia con il codice qui sotto. E questa è l'impostazione predefinita in Rstudio quando si crea un file rmd. Quando lo lavori a maglia. Supporrà automaticamente che sia una modalità ritratto senza dubbio.

    title: "Landscape and Portrait"
        author: "Jung-Han Wang"
        date: "Thursday, March 19, 2015"
        output: pdf_document

    Quando vuoi unire il PDF in modalità orizzontale, l'unica cosa che devi aggiungere è classoption: landscape

        title: "Landscape and Portrait"
        author: "Jung-Han Wang"
        date: "Thursday, March 19, 2015"
        output: pdf_document
        classoption: landscape

    Se vuoi una combinazione di entrambi, dovrai aggiungere il file .tex in YAML. Facendo riferimento al link che ho menzionato sopra. Puoi scaricare il codice .tex qui. http://goo.gl/cptOqg O semplicemente copia il codice e salvalo come header.tex Quindi, per semplificare la vita, metti questo file .tex insieme al file rmd da lavorare a maglia. Assicurati di aver fatto queste due cose: copia il file tex e spostalo insieme al file rmd. Cambia l'inizio di rmd in:

     title: "Landscape and Portrait"
        author: "Jung-Han Wang"
        date: "Thursday, March 19, 2015"
        output:
          pdf_document:
            includes:
              in_header: header.tex
              
              
---


# LaTeX Beamer - Federico Tartarini

1 [Creare una presentazione in LaTeX](https://www.youtube.com/watch?v=hCiiS0IRyhc)

2 [Cambiare tema, dimensione slides e usare un template](https://www.youtube.com/watch?v=cbbq6vE9EXs)

3 [Figure, Tabelle, Colonne, Liste e Immagini](https://www.youtube.com/watch?v=tLV4LM9GKHw&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=3)

4 [Bibliografia, citazioni e note](https://www.youtube.com/watch?v=f7G0wtqIpv4&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=4)

5 [Aggiungere video alla presentazione](https://www.youtube.com/watch?v=fw0BJYwGS1s&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=5)

6 [Working Offline in Overleaf -- GitHub and Dropbox integration Overleaf](https://www.youtube.com/watch?v=gxA4FmAWFA0&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=6)

# ruotare un testo (Latex)

\usepackage{landscape}

\begin{landscape}

\end{landscape}

 
<br>

# tabelle

## [tabella](https://www.youtube.com/watch?v=1cEdqTMtHZQ)

![tabella](./immagini/2021070901.PNG)

![tabella](./immagini/2021070902.PNG)

<br>


## [Excel2LaTeX – Convert Excel spreadsheets to LaTeX tables](https://www.ctan.org/pkg/excel2latex?lang=en)

![tabella](./immagini/2021070905.PNG)
![tabella](./immagini/2021070906.PNG)

 
<br>



## [Creating Flowcharts with TikZ (LaTeX)](https://www.youtube.com/watch?v=LoBC8zIB-3k)
![tabella](./immagini/2021070907.PNG)
 
<br>


## [Excel to Latex - import data table directly from csv file with csvsimple](https://www.youtube.com/watch?v=FYFZS48sLfk)
![tabella](./immagini/2021070908.PNG)
 
<br>


## PDF/A

* [Creating high-quality PDF/A documents using LaTeX](https://www.mathstat.dal.ca/~selinger/pdfa/)

## Inserimento di un file PDF

Usa il pacchetto pdfpages \usepackage{pdfpages}

Per includere tutte le pagine nel file PDF: 

* \includepdf[pages=-]{myfile.pdf} oppure

* \ includepdf {myfile.pdf} 

Per includere solo la prima pagina di un PDF: \includepdf[pages={1}]{myfile.pdf}

Esegui texdoc pdfpagesin una shell per vedere il manuale completo di pdfpages

 
## Layout verticale e orizzontale in un unico PDF

* [Rstudio rmarkdown: layout verticale e orizzontale in un unico PDF](https://www.it-swarm.it/it/r/rstudio-rmarkdown-layout-verticale-e-orizzontale-un-unico-pdf/1049572054/)

Per i casi più comuni.

Ci sono 3 condizioni.

*    Tutto in modalità verticale.

*    Tutto in modalità orizzontale.

*    Miscela di modalità verticale e orizzontale.

Restringiamo ogni singola condizione.

    Il primo, diciamo che abbiamo un documento markdown che inizia con il codice qui sotto. E questa è l'impostazione predefinita in Rstudio quando si crea un file rmd. Quando lo lavori a maglia. Supporrà automaticamente che sia una modalità ritratto senza dubbio.

    title: "Landscape and Portrait"
        author: "Jung-Han Wang"
        date: "Thursday, March 19, 2015"
        output: pdf_document

    Quando vuoi unire il PDF in modalità orizzontale, l'unica cosa che devi aggiungere è classoption: landscape

        title: "Landscape and Portrait"
        author: "Jung-Han Wang"
        date: "Thursday, March 19, 2015"
        output: pdf_document
        classoption: landscape

    Se vuoi una combinazione di entrambi, dovrai aggiungere il file .tex in YAML. Facendo riferimento al link che ho menzionato sopra. Puoi scaricare il codice .tex qui. http://goo.gl/cptOqg O semplicemente copia il codice e salvalo come header.tex Quindi, per semplificare la vita, metti questo file .tex insieme al file rmd da lavorare a maglia. Assicurati di aver fatto queste due cose: copia il file tex e spostalo insieme al file rmd. Cambia l'inizio di rmd in:

     title: "Landscape and Portrait"
        author: "Jung-Han Wang"
        date: "Thursday, March 19, 2015"
        output:
          pdf_document:
            includes:
              in_header: header.tex
              
              
---


# LaTeX Beamer - Federico Tartarini

1 [Creare una presentazione in LaTeX](https://www.youtube.com/watch?v=hCiiS0IRyhc)

2 [Cambiare tema, dimensione slides e usare un template](https://www.youtube.com/watch?v=cbbq6vE9EXs)

3 [Figure, Tabelle, Colonne, Liste e Immagini](https://www.youtube.com/watch?v=tLV4LM9GKHw&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=3)

4 [Bibliografia, citazioni e note](https://www.youtube.com/watch?v=f7G0wtqIpv4&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=4)

5 [Aggiungere video alla presentazione](https://www.youtube.com/watch?v=fw0BJYwGS1s&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=5)

6 [Working Offline in Overleaf -- GitHub and Dropbox integration Overleaf](https://www.youtube.com/watch?v=gxA4FmAWFA0&list=PLY91jl6VVD7yNinlE2KLYgd5TL83jsRoW&index=6)
