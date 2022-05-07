Per avere intestazioni e piè di pagina piacevoli, devi fornire metadati al tuo documento. Puoi farlo con un blocco di metadati YAML nella parte superiore del tuo documento markdown (vedi il file markdown di esempio ). Il tuo documento markdown potrebbe essere simile al seguente:

```YAML
titolo : " Il titolo del documento " 
autore : [Esempio autore, Altro autore] 
data : " 2017-02-20 " 
parole chiave : [Rivalutazione, Esempio] 
```



# YAML usato per il PDF "Superbonus"

```yaml
---
title: \vspace{2.5in}**Superbonus 110\%**
author: Paolo Volterra
header-includes: |
  \usepackage{tikz,pgfplots}
  \usepackage{fancyhdr}
  \usepackage[italian]{babel}
  \pagestyle{fancy}
  \fancyhead[CO,CE]{}
  \fancyfoot[CO,CE]{Superbonus 110\%}
  \fancyfoot[LE,RO]{\thepage}
  \graphicspath{{immagini/}}
  \usepackage{pdfpages}
  \usepackage{imakeidx}
  \makeindex
  
output: pdf_document
fontsize: 13pt
keywords: [superbonus, cessione del credito, PMI, imprese]
abstract: Superbonus 110\% è un’agevolazione prevista dal Decreto Rilancio del 2020 che eleva al 110\% l’aliquota di detrazione delle spese per interventi di efficienza energetica e riduzione del rischio sismico sostenute da persone fisiche e altri soggetti da luglio 2020 a giugno 2022.  Considerato che l'orizzonte temporale rappresenta uno dei punti chiave per la buona riuscita della misura fiscale, da più parti è arrivata la richiesta di uniformare la data di scadenza e posticiparla almeno al 2023.  Nel business agiscono non solo le banche ma anche Poste Italiane, alcuni gruppi assicurativi e utilities che hanno stretto collaborazioni con  advisor internazionali per il supporto tecnico. Il costo di cessione in media equivale a circa il 10\% per cento del bonus e un costo medio dell'8\%.Il mercato è abbastanza allineato nell’Offerta. Oltre metà degli italiani approva nei fatti il Superbonus.
---

\newpage
\tableofcontents
\listoffigures
\listoftables
\newpage

# Introduzione 

![logo agevolazione](./immagini/ANIT_110.jpg){ width=30% height=30% }

```
