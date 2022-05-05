---
title: "Markdown - HOWTO"
---

# FORMATTAZIONE
## Tab

```
## section 1 {.tabset .tabset-fade}
content above tabbed region.

### tab 1 

tab content 1

### tab 2

tab content 2

## section 2 {.tabset .tabset-fade}

### tab 1 

tab content 1

### tab 2

tab content 2

### tab 3

tab content 3

#
content below tabbed region

```


## note a piè di pagina
Nel corpo del testo [^1] inserire [^2] note a piè di pagina.

<br>

[^1]: qui c’è il testo delle note a piè di pagina.
[^2]: Anche le **note a piè di pagina** possono essere *formattate*.
E queste includono anche diverse linee.



## pulsanti
### Inserire un pulsante personalizzato usando il codice HTML
<form 
method="get" action="http://www.puntoinformaticofree.it">
<input type="submit" value="Scopri di più" 
style="background-color: #ce401c; 
width: 15em;
padding: .5em;
color: #ffffff;
text-shadow: 1px 1px 1px #000;
font: 16px Arial, Helvetica, sans-serif;
border: solid thin #882d13;
-webkit-border-radius: .7em;
-moz-border-radius: .7em;
border-radius: .7em;
background-image: -webkit-gradient(linear, left top, left bottom,
from(#e9ede8), to(#ce401c),color-stop(0.4, #8c1b0b));">
</form>
### Inserire un pulsante semplice usando il codice HTML


Per inserire un pulsante semplice all'interno della nostra pagina web che ci colleghi selezionandolo ad un indirizzo internet posizionarsi dove vogliamo inserirlo e digitiamo il seguente codice HTML:

<form method="get" action="INDIRIZZO_URL"><button type="submit">TESTO_PULSANTE</button></form>

Nel nostro caso dovremo digitare il seguente codice HTML:

<form method="get" action="http://www.puntoinformaticofree.it/"><button type="submit">Scopri di più</button></form>

Produrremo:


Se invece vogliamo che il testo del pulsante sia in grassetto dovremo digitare il seguente codice:

<form method="get" action="http://www.puntoinformaticofree.it/"><button type="submit"> <strong>Scopri di più</strong></button></form>

Produrremo: 

### Gli stili del pulsante


Spieghiamo ora le righe del codice HTML dell'esempio sopra che conpongono lo stile del pulsante. Comprendendo come viene creato lo stile del pulsante sappiamo come modificarlo per creare un eventuale pulsante diverso che ci piaccia di più.


Apertura form:


Digitiamo il codice dell'apertura del contenitore in cui inseriamo il pulsante HTML:

<form


Link Web e testo pulsante:


Digitiamo il codice dell'apertura del contenitore in cui inseriamo il pulsante HTML:

method="get" action="http://www.puntoinformaticofree.it">
<input type="submit" value="Scopri di più"


Colore di sfondo del pulsante:


Digitiamo il codice del colore di sfondo del pulsante HTML:

style="background-color: #ce401c;


Padding e larghezza


Digitiamo il codice del padding (il padding è la distanza tra il testo ed il bordo di un contenitore) e della larghezza del pulsante:

width: 15em;
padding: .5em;


Colore del testo, ombreggiatura e font:


Digitiamo il codice del colore del testo, ombreggiatura e font:

color: #ffffff;
text-shadow: 1px 1px 1px #000;
font: 16px Arial, Helvetica, sans-serif;


Arrotondare gli angoli del pulsante:


Digitiamo il codice per arrotondare gli angoli del pulsante:

border: solid thin #882d13;
-webkit-border-radius: .7em;
-moz-border-radius: .7em;
border-radius: .7em;


Sfondo con gradiente:


Digitiamo il codice per applicare lo sfondo con gradiente:

background-image: -webkit-gradient(linear, left top, left bottom,
from(#e9ede8), to(#ce401c),color-stop(0.4, #8c1b0b));">

Potrebbe sembrare complicata, ma non lo è.

Il nome della funzione è gradient (poiché è sperimentale usiamo il prefisso -webkit-).

Poi specifichiamo il tipo di gradiente. Vogliamo un gradiente lineare.

Dopo specifichiamo i punti di inizio e finale del gradiente: nel nostro caso la parte superiore (top) e inferiore (bottom) dell’elemento, su una linea verticale.

Specifichiamo poi i colori iniziali e finali, e infine un colore di stop situato al 40% verso la parte inferiore dell’elemento. Insieme, questo crea un gradiente con una transizione morbida dal colore iniziale nella parte alta, verticalmente fino al colore di stop, con un’altra transizione morbida verso il colore finale.


Chiusura form:


Digitiamo il codice della chiusura del contenitore in cui inseriamo il pulsante HTML:

</form>



Risultato finale:


Quindi il coidice finale sarà il seguente:

<form 
method="get" action="http://www.puntoinformaticofree.it">
<input type="submit" value="Scopri di più" 
style="background-color: #ce401c; 
width: 15em;
padding: .5em;
color: #ffffff;
text-shadow: 1px 1px 1px #000;
font: 16px Arial, Helvetica, sans-serif;
border: solid thin #882d13;
-webkit-border-radius: .7em;
-moz-border-radius: .7em;
border-radius: .7em;
background-image: -webkit-gradient(linear, left top, left bottom,
from(#e9ede8), to(#ce401c),color-stop(0.4, #8c1b0b));">
</form>

E produrrà:


Elementi di campata
Link

Markdown supporta due stili di link: inline e reference .

In entrambi gli stili, il testo del collegamento è delimitato da [parentesi quadre].

Per creare un collegamento in linea, usa immediatamente una serie di parentesi regolari dopo la parentesi quadra di chiusura del testo del collegamento. All'interno delle parentesi, metti l'URL dove vuoi che punti il ​​link, insieme a un facoltativo titolo del collegamento, racchiuso tra virgolette. Per esempio:

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

Produrrà:

<p>This is <a href="http://example.com/" title="Title">
an example</a> inline link.</p>

<p><a href="http://example.net/">This link</a> has no
title attribute.</p>

Se ti riferisci a una risorsa locale sullo stesso server, puoi usa percorsi relativi:

See my [About](/about/) page for details.   

I collegamenti in stile riferimento utilizzano una seconda serie di parentesi quadre, all'interno cui apporre un'etichetta a scelta per identificare il collegamento:

This is [an example][id] reference-style link.

Puoi facoltativamente utilizzare uno spazio per separare i gruppi di parentesi:

This is [an example] [id] reference-style link.

Quindi, in qualsiasi punto del documento, definisci l'etichetta del tuo collegamento in questo modo, su una riga da solo:

[id]: http://example.com/  "Optional Title Here"

Questo è:

    Parentesi quadre contenenti l'identificatore del collegamento (facoltativamente rientrato dal margine sinistro utilizzando fino a tre spazi);
    seguito da due punti;
    seguito da uno o più spazi (o tab);
    seguito dall'URL del collegamento;
    facoltativamente seguito da un attributo title per il collegamento, racchiuso tra virgolette doppie, singole o racchiuse tra parentesi.

Le seguenti tre definizioni di collegamento sono equivalenti:

[foo]: http://example.com/  "Optional Title Here"
[foo]: http://example.com/  'Optional Title Here'
[foo]: http://example.com/  (Optional Title Here)

Nota: esiste un bug noto in Markdown.pl 1.0.1 che impedisce virgolette singole dall'essere utilizzate per delimitare i titoli dei collegamenti.

L'URL del collegamento può, facoltativamente, essere racchiuso tra parentesi angolari:

[id]: <http://example.com/>  "Optional Title Here"

Puoi inserire l'attributo del titolo nella riga successiva e utilizzare spazi extra o schede per il riempimento, che tende ad avere un aspetto migliore con URL più lunghi:

[]: http://example.com/longish/path/to/resource/here
    "Optional Title Here"

Le definizioni dei collegamenti vengono utilizzate solo per creare collegamenti durante il Markdown elaborazione e vengono rimossi dal documento nell'output HTML.

I nomi delle definizioni dei collegamenti possono essere costituiti da lettere, numeri, spazi e punteggiatura - ma sono senza maiuscole e minuscole. Es. questi due link:

[link text][a]
[link text][A]

sono equivalenti.

La implicita del nome del scorciatoia collegamento ti consente di omettere il nome del collegamento, nel qual caso il testo del collegamento stesso viene utilizzato come nome. Basta usare un insieme vuoto di parentesi quadre, ad esempio per collegare la parola “Google” al sito web google.com, potresti semplicemente scrivere:

[Google][]

E poi definire il collegamento:

[Google]: http://google.com/

Poiché i nomi dei collegamenti possono contenere spazi, questa scorciatoia funziona anche per più parole nel testo del collegamento:

Visit [Daring Fireball][] for more information.

E poi definire il collegamento:

[Daring Fireball]: http://daringfireball.net/

Le definizioni dei collegamenti possono essere posizionate ovunque nel documento Markdown. io tendono a metterli subito dopo ogni paragrafo in cui si trovano usati, ma se vuoi puoi metterli tutti alla fine del tuo documento, una sorta di note a piè di pagina.

Ecco un esempio di link di riferimento in azione:

I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

Utilizzando la scorciatoia implicita del nome del collegamento, potresti invece scrivere:

I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [Google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"

Entrambi gli esempi precedenti produrranno il seguente output HTML:

<p>I get 10 times more traffic from <a href="http://google.com/"
title="Google">Google</a> than from
<a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

Per confronto, ecco lo stesso paragrafo scritto usando Lo stile di collegamento in linea di Markdown:

I get 10 times more traffic from [Google](http://google.com/ "Google")
than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
[MSN](http://search.msn.com/ "MSN Search").

Il punto di riferimento dei collegamenti in stile non è che sono più facili da Scrivi. Il punto è che con i collegamenti in stile riferimento, il tuo documento la fonte è molto più leggibile. Confronta gli esempi precedenti: using link in stile riferimento, il paragrafo stesso è di soli 81 caratteri lungo; con collegamenti in linea, sono 176 caratteri; e come HTML grezzo, sono 234 caratteri. Nell'HTML grezzo, c'è più markup di quello che c'è è testo.

Con i collegamenti in stile riferimento di Markdown, un documento sorgente molto di più assomiglia molto all'output finale, come reso in un browser. Di permettendoti di spostare i metadati relativi al markup fuori dal paragrafo, puoi aggiungere link senza interrompere il flusso narrativo del tuo prosa.
enfasi

Markdown tratta gli asterischi ( *) e trattini bassi ( _) come indicatori di enfasi. Testo avvolto con uno *o _sarà avvolto con un HTML <em>etichetta; Doppio *'s o _saranno racchiusi in un HTML <strong>etichetta. Ad esempio, questo ingresso:

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

produrrà:

<em>single asterisks</em>

<em>single underscores</em>

<strong>double asterisks</strong>

<strong>double underscores</strong>

Puoi usare lo stile che preferisci; l'unica restrizione è che lo stesso carattere deve essere utilizzato per aprire e chiudere un intervallo di enfasi.

L'enfasi può essere usata nel mezzo di una parola:

un*frigging*believable

Ma se circondi un *o _con gli spazi, sarà trattato come a letterale asterisco o underscore.

Per produrre un asterisco o un carattere di sottolineatura letterale in una posizione in cui è altrimenti verrebbe usato come delimitatore di enfasi, puoi usare il backslash fuggilo:

\*this text is surrounded by literal asterisks\*

Codice

Per indicare un intervallo di codice, avvolgilo tra virgolette inverse ( `). A differenza di un blocco di codice preformattato, un intervallo di codice indica il codice all'interno di a paragrafo normale. Per esempio:

Use the `printf()` function.

produrrà:

<p>Use the <code>printf()</code> function.</p>

Per includere un carattere di apice inverso letterale all'interno di un intervallo di codice, puoi usare più apici inversi come delimitatori di apertura e chiusura:

``There is a literal backtick (`) here.``

che produrrà questo:

<p><code>There is a literal backtick (`) here.</code></p>

I delimitatori di backtick che circondano un intervallo di codice possono includere spazi, uno dopo l'apertura, uno prima della chiusura. Questo ti permette di posizionare caratteri di backtick letterali all'inizio o alla fine di un intervallo di codice:

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``

produrrà:

<p>A single backtick in a code span: <code>`</code></p>

<p>A backtick-delimited string in a code span: <code>`foo`</code></p>

Con un intervallo di codice, le e commerciali e le parentesi angolari sono codificate come HTML entità automaticamente, il che semplifica l'inclusione di HTML di esempio tag. Markdown trasformerà questo:

Please don't use any `<blink>` tags.

in:

<p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

Puoi scrivere questo:

`&#8212;` is the decimal-encoded equivalent of `&mdash;`.

produrre:

<p><code>&amp;#8212;</code> is the decimal-encoded
equivalent of <code>&amp;mdash;</code>.</p>

immagini

Certo, è abbastanza difficile escogitare una sintassi "naturale" per inserire le immagini in un formato di documento di testo normale.

Markdown utilizza una sintassi dell'immagine che ha lo scopo di assomigliare alla sintassi per i collegamenti, consentendo due stili: inline e riferimento .

La sintassi dell'immagine in linea è simile alla seguente:

![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Questo è:

    Un punto esclamativo: !;
    seguito da un insieme di parentesi quadre, contenente il alt testo dell'attributo per l'immagine;
    seguito da una serie di parentesi, contenente l'URL o il percorso per l'immagine e un optional titleattributo racchiuso tra double o virgolette singole.

La sintassi dell'immagine in stile riferimento è simile alla seguente:

![Alt text][id]

Dove "id" è il nome di un riferimento immagine definito. Riferimenti immagine sono definiti utilizzando una sintassi identica ai riferimenti di collegamento:

[]: url/to/image  "Optional title attribute"

Al momento della stesura di questo articolo, Markdown non ha una sintassi per specificare il dimensioni di un'immagine; se questo è importante per te, puoi semplicemente usa il normale HTML <img>tag.
Varie
Collegamenti automatici

Markdown supporta uno stile di collegamento per la creazione di collegamenti "automatici" per URL e indirizzi e-mail: è sufficiente racchiudere l'URL o l'indirizzo e-mail tra parentesi angolari. Ciò significa che se vuoi mostrare il testo effettivo di un URL o di un indirizzo e-mail e anche che sia un link cliccabile, puoi farlo:

<http://example.com/>

Markdown lo trasformerà in:

<a href="http://example.com/">http://example.com/</a>

I collegamenti automatici per gli indirizzi e-mail funzionano in modo simile, tranne che Markdown eseguirà anche un po 'di decimale ed esadecimale randomizzati codifica dell'entità per aiutare a nascondere il tuo indirizzo dalla raccolta di indirizzi spambot. Ad esempio, Markdown trasformerà questo:

<address@example.com>

in qualcosa del genere:

<a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
&#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

che verrà visualizzato in un browser come collegamento cliccabile a " address@example.com ".

(Questo tipo di trucco di codifica delle entità ingannerà davvero molti, se non lo farà la maggior parte dei robot per la raccolta degli indirizzi, ma sicuramente non ingannerà tutti loro. È meglio di niente, ma un indirizzo pubblicato in questo modo probabilmente inizierà a ricevere spam.)
Fughe con barra rovesciata

Markdown ti consente di utilizzare gli escape backslash per generare letterali caratteri che altrimenti avrebbero un significato speciale in Markdown's sintassi di formattazione. Ad esempio, se volessi racchiudere una parola con asterischi letterali (invece di un HTML <em>tag), puoi usare barre rovesciate prima degli asterischi, in questo modo:

\*literal asterisks\*

Markdown fornisce escape backslash per i seguenti caratteri:

\   backslash
`   backtick
*   asterisk
_   underscore
{}  curly braces
[]  square brackets
()  parentheses
#   hash mark
+   plus sign
-   minus sign (hyphen)
.   dot
!   exclamation mark








pandoc B2B.md -o myslides.pptx --reference-doc template-red4.pptx



###### tags: `Tag(change me!)`

> This note is yours, feel free to play around.  :video_game: 
> Type on the left :arrow_left: and see the rendered result on the right. :arrow_right: 


## paragrafi


# LINK


aprire una nuova pagina da un link {:target="_blank"}

# IMMAGINI
## inserire un'immagine

![Explanatory Text](./immagini/01.PNG)

<img src="D:/dir/immagini/0.jpg"></img>

![Explanatory Text](./immagini/0.jpg)

<img src=./immagini/0.jpg></img>




# COME INIZIARE
### Step 1: Change the title and add a tag

- [x] Create my first HackMD note (this one!)
- [ ] Change its title
- [ ] Add a tag

:rocket: 

### Step 2: Write something in Markdown

Let's try it out!
Apply different styling to this paragraph:
**HackMD gets everyone on the same page with Markdown.** ==Real-time collaborate on any documentation in markdown.== Capture fleeting ideas and formalize tribal knowledge.

- [x] **Bold**
- [ ] *Italic*
- [ ] Super^script^
- [ ] Sub~script~
- [ ] ~~Crossed~~
- [x] ==Highlight==

:::info
:bulb: **Hint:** You can also apply styling from the toolbar at the top :arrow_upper_left: of the editing area.

![](https://i.imgur.com/Cnle9f9.png)
:::

> Drag-n-drop image from your file system to the editor to paste it!

### Step 3: Invite your team to collaborate!

Click on the <i class="fa fa-share-alt"></i> **Sharing** menu :arrow_upper_right: and invite your team to collaborate on this note!

![permalink setting demo](https://i.imgur.com/PjUhQBB.gif)

- [ ] Register and sign-in to HackMD (to use advanced features :tada: ) 
- [ ] Set Permalink for this note
- [ ] Copy and share the link with your team

:::info
:pushpin: Want to learn more? ➜ [HackMD Tutorials](https://hackmd.io/c/tutorials) 
:::
## BONUS: More cool ways to HackMD!

- Table

| Features          | Tutorials               |
| ----------------- |:----------------------- |
| GitHub Sync       | [:link:][GitHub-Sync]   |
| Browser Extension | [:link:][HackMD-it]     |
| Book Mode         | [:link:][Book-mode]     |
| Slide Mode        | [:link:][Slide-mode]    | 
| Share & Publish   | [:link:][Share-Publish] |

[GitHub-Sync]: https://hackmd.io/c/tutorials/%2Fs%2Flink-with-github
[HackMD-it]: https://hackmd.io/c/tutorials/%2Fs%2Fhackmd-it
[Book-mode]: https://hackmd.io/c/tutorials/%2Fs%2Fhow-to-create-book
[Slide-mode]: https://hackmd.io/c/tutorials/%2Fs%2Fhow-to-create-slide-deck
[Share-Publish]: https://hackmd.io/c/tutorials/%2Fs%2Fhow-to-publish-note

- LaTeX for formulas

$$
x = {-b \pm \sqrt{b^2-4ac} \over 2a}
$$

- Code block with color and line numbers：
```javascript=16
var s = "JavaScript syntax highlighting";
alert(s);
```

- UML diagrams
```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
Note left of Alice: Alice responds
Alice->Bob: Where have you been?
```
- Auto-generated Table of Content
[ToC]

> Leave in-line comments! [color=#3b75c6]

- Embed YouTube Videos

{%youtube PJuNmlE74BQ %}

> Put your cursor right behind an empty bracket {} :arrow_left: and see all your choices.

- And MORE ➜ [HackMD Tutorials](https://hackmd.io/c/tutorials)



* <small>testo piccolo</small>
* <big>testo grande </big> 
-------------------------------------




# Table of contents
1. [Introduction](#introduction)
2. [Some paragraph](#paragraph1)
    1. [Sub paragraph](#subparagraph1)
3. [Another paragraph](#paragraph2)

## This is the introduction <a name="introduction"></a>
Some introduction text, formatted in heading 2 style

## Some paragraph <a name="paragraph1"></a>
The first paragraph text

### Sub paragraph <a name="subparagraph1"></a>
This is a sub paragraph, formatted in heading 3 style

## Another paragraph <a name="paragraph2"></a>
The second paragraph text



# Table of Contents
1. [Example](#example)
2. [Example2](#example2)
3. [Third Example](#third-example)

## Example [](#){name=example}
## Example2 [](#){name=example2}
## [Third Example](#){name=third-example}

-------------------------------

# My Table of content
- [Section 1](#id-section1)
- [Section 2](#id-section2)

<div id='id-section1'/>
## Section 1
<div id='id-section2'/>
## Section 2

[my link](file:///C:/Users/PVolterr/Downloads/20210906_224.pdf)


% Scrivere e pubblicare in CommonMark alla buona
% Daniele Salvini
% 16 marzo 2016

\newpage



# ALTRE ISTRUZIONI

## Marcare il testo

Un marcatore Ã¨ un segno convenzionale per indicare la formattazione.

I linguaggi di marcatura *leggeri* usano espressioni codificate abbastanza
semplici da essere utilizzabili durante la fase creativa di scrittura.

In altre parole sono un linguaggio con regole semplici per descrivere la
rappresentazione del testo da cui creare documenti strutturati che saranno
utilizzabili su piÃ¹ supporti.

## Esempio di scrittura con marcatori

    # Capitolo primo
      bla bla bla
    
    # Capitolo secondo 
      bla bla *bla in grassetto*

Una caratteristica importante Ã¨ che la lettura del testo crudo non presenta
difficoltÃ .

## Markdown e CommonMark

Markdown Ã¨ il linguaggio di marcatura inventato da Aaron Swartz e John Gruber.
Nato per pubblicare in HTML, presenta delle limitazioni per altri formati di
pubblicazione. CommonMark Ã¨ il dialetto che si propone di superare queste
limitazioni e di uniformare le convenzioni. Alla buona: Markdown Ã¨ il formato
stretto creato nel 2004, CommonMark Ã¨ il Markdown esteso grazie alla conversione
con Pandoc. Un testo scritto in CommonMark puÃ² essere convertito in un formato
di pubblicazione come HTML, PDF, EPUB o LaTeX.

Questo testo Ã¨ stato scritto in Markdown esteso e convertito con Pandoc.
Per la sua eventuale utilitÃ  se ne consiglia la lettura nel formato
[crudo in CommonMark][] e il confronto con la pagina [convertita in HTML][]
[o in PDF][].

## Usare un editore di testo

Per scrivere e inserire i marcatori liberamente Ã¨ necessario usare un editore di
testo che sappia scrivere, salvare, riscrivere e stampare e che non conosca la
formattazione[^nonsa], di quella si occupa lo scrittore usando i marcatori.

Qualunque editore di testo va bene a patto che scriva e salvi in formato puro
testo (TXT). Ad esempio [Gedit][], il quale Ã¨ anche in grado di visualizzare la
struttura logica del testo evidenziando i marcatori.

Quando viene data al documento una desinenza che dichiara il formato, l'editore
potrÃ  riconoscerlo automagicamente: la desinenza .md significa Markdown.

Esempio: questo documento si chiama: commonmark-buona.md

[^nonsa]: I documenti scritti in un linguaggio di marcatura come HTML vengono
        solitamente fruiti con la formattazione che gli viene restituita da un
        navigatore, ma restano documenti in semplice testo.



# Sintassi
## Capitoli

Un Capitolo Ã¨ rappresentato da una riga preceduta da un cancelletto.

Se ne possono usare fino a sei: #, ##, ###, eccetera[^h].

    Esempio:
    
    # Titolo
    ## Capitolo
    ### Sottocapitolo

[^h]: Ci sono anche altri metodi per creare gli headers, si possono usare quelli
    che si preferiscono, solo non Ã¨ il caso di mischiarli tra loro.


## Paragrafi

Per andare a capo (punto e a capo), mettere due spazi a fine riga.

Ecco come funzionano le pillole:  
gialla e rossa, nella fossa.  
Bianca e viola, qui si vola.

Per rappresentare un paragrafo, lasciare una linea vuota.

## Attributi del testo

Per creare attributi al testo si usa spesso l'asterisco.

### Italico

Una parola tra asterischi Ã¨ in *italico*

`*italico*`

### Grassetto

Una parola (o frase) tra due asterischi Ã¨ **grassetto**

`**grassetto**`

### Barrato

Una parola tra quattro tilde Ã¨ ~~barrata~~ [^al]

`~~barrata~~`

[^al]: Esistono altri tipi di attributi, come superscript, tag e spoiler, oltre
    le tabelle e anche le funzioni matematiche, che non verranno descritti qui.

## Links

Vengono considerati quattro tipi di link: automatico, allineato, di riferimento
e interno alla pagina.

### Link automatico

Un indirizzo web (URL) tra parentesi acute verrÃ  automaticamente visualizzato.

`<URL>`

<https://stackoverflow.com/editing-help>

### Link allineato

La sintassi del link allineato Ã¨: nome tra parentesi quadre e URL tra
parentesi tonde.

`[nome](url)`

Esempio: [markdown announce page](http://www.aaronsw.com/weblog/001189)

### Link di riferimento

Il link di riferimento Ã¨ composto da due parti dove l'una rimanda all'altra.

#### Link di riferimento esplicito

Il link di riferimento esplicito usa solo parentesi quadre, si riferisce a un
nome che viene espresso piÃ¹ avanti, ad esempio a fine pagina.

`[riferimento][nome]`

e

`[nome]:url`

Esempio: [12121][markdown page] la pagina del markdown

[markdown page]: https://daringfireball.net/projects/markdown/ "markdown page"

#### Link di riferimento implicito

Il link di riferimento implicito omette il nome.

`[riferimento][]`

e 

`[riferimento]:url`

### Link interno alla pagina

Per rappresentare un link a una sezione del documento, lo si puÃ² puntare a un
capitolo.

`vai alla sezione [Sintassi](#sintassi)`

vai alla sezione [Sintassi](#sintassi)

### Link a un'immagine

L'inserimento delle immagini usa la stessa sintassi dei link, ma preceduta da un
punto esclamativo.

`![nome](immagine.png)`

### Utilizzo dei link

Per accompagnare il link a una descrizione metterla tra virgolette dopo l'URL.

`[nome](url "descrizione")`

Il link allineato Ã¨ piÃ¹ veloce da inserire scrivendo, ma rende la lettura del
testo crudo piÃ¹ faticosa, mentre il link di riferimento scorre meglio.

Questo esempio mostra un link allineato con descrizione che punta alla
[parola Markdown](https://it.wikipedia.org/wiki/Markdown "Markdown Ã¨ un
linguaggio di markup con una sintassi del testo semplice") sull'enciclopedia
libera. Va benissimo per la pubblicazione sul web, ma leggere il testo crudo non
Ã¨ comodo, soprattutto se i link fossero molti.

Questo link di riferimento implicito con descrizione invece scorre benissimo:
punta [alla parola Markdown][] sull'enciclopedia libera. La leggibilitÃ  Ã¨ ottima
in quanto il riferimento compare a fine pagina o paragrafo e non ostacola la
lettura.

[alla parola Markdown]: https://it.wikipedia.org/wiki/Markdown "Markdown Ã¨ un linguaggio di markup con una sintassi del testo semplice"

## Rappresentare il Codice

Per rappresentare del codice Ã¨ possibile usare un blocco di testo con quattro
spazi (o una Tab) a inizio riga.

    blocco di testo
    rappresentato come codice

Ãˆ possibile anche mettere la parola o frase tra accenti a sinistra (backtick).

`` ` ``codice`` ` ``

Esempio: `questa frase viene rappresentata come codice`.

## Blockquotes

Per rappresentare un blocco di testo che risulti separato dal resto usare
una parentesi acuta `>` a inizio riga.

Esempio:

`> blocco di testo separato dal resto`

Risulta:

> blocco di testo separato dal resto

## Elenchi

Per rappresentare una lista non numerata usare un asterisco a inizio riga.

Esempio:

    * latte
    * caffÃ©
    * miele

Risulta: 

* latte
* caffÃ©
* miele

Lasciando delle righe in mezzo si creano paragrafi multipli.

Per rappresentare una lista numerata usare i numeri:

1. cartine
3. tabacco
2. filtri

Non Ã¨ necessario che la numerazione sia progressiva, ma Ã¨ consigliabile.

## Note a piÃ© pagina

Le note a piede pagina sono in due parti, si rappresentano usando un accento
circonflesso `^` tra parentesi quadre.

`[^nota]`

e

`[^nota]: riferimento`

Questa Ã¨ una nota [^nota]

[^nota]: Il riferimento puÃ² essere messo essere posto ovunque e comparirÃ  al piede della
pagina.

    Il riferimento alla nota puÃ² anche continuare in un blocco di testo.

# Pubblicazione

## Impaginazione

### Informazioni bibliografiche

Titolo autore e data possono essere rappresentati con questa sintassi all'inizio
del testo

    % Titolo
    % Autore
    % Data

### Interruzione di pagina

Per rappresentare un'interruzione di pagina[^ip] si puÃ² utilizzare:

`\newpage`

[^ip]: l'interruzione di pagina non viene resa in HTML

## Conversione

Una volta scritto il documento, Ã¨ possibile convertirlo in un formato di
pubblicazione. In questo contesto viene usato il convertitore di documenti
libero e a sorgente aperta Pandoc, alcuni esempi:[^deb]

[^deb]: Ãˆ stata utilizzata BunsenLabs, distribuzione Linux basata su Debian 8.

Installare Pandoc e Citeproc:

    apt-get install pandoc pandoc-citeproc

Convertire da Markdown in HTML:

    pandoc -s articolo.md -o articolo.html

Convertire da Markdown in PDF:

    pandoc tesina.md -o tesina.pdf

Convertire da Markdown a EPUB:

    pandoc -f markdown libro.md -t epub -o libro.epub

Convertire da Markdown in LaTeX:

    pandoc -f markdown saggio.md -t latex -o saggio.tex

## Citazioni

### Inserire una citazione

> Ãˆ sempre una buona idea scrivere da qualche parte, a grandi caratteri che
> ispirano fiducia, le parole: NON FATEVI PRENDERE DAL PANICO [vedi @dougadams:ggpa, pp. 5].

La sintassi per inserire una citazione estraendola da un file bibliografico:
(id)entificativo del file bibliografico preceduto da una chiocciola tra
parentesi quadre, separate (se le citazioni sono piÃ¹ d'una) da punto e virgola.

Esempio:

`[@id]`

Esempio citazione:

`[vedi @dougadams, pp. 21-22]`

Esempio doppia citazione:

`[considera @dougadams79, pp. 21-22 ; ma anche @tumembete85, pp. 42]`

Si possono usare anche le citazioni allineate:

`@manzoni ha scritto che`

### Creare un documento in LaTeX o PDF con bibliografia

Una volta aggiunte al testo le citazioni, si potrÃ  convertire il file da
Markdown nel formato desiderato usando Pandoc e l'estensione pandoc-citeproc.

Esempio: il file in formato BibTeX `biblio.bib` contiene le seguenti righe:

    @book{dougadams:ggpa,
        author = {Douglas, Adams},
        title = {Guida galattica per gli autostoppisti},
        series = {Urania},
        volume = {1},
        publisher = {Mondadori},
        address = {Milano},
        year = {1980}
        }

Convertire un testo da Markdown a LaTeX specificando il file bibliografico
esterno:

`pandoc --bibliography=biblio.bib saggio.md -o saggio.tex`

Convertire un testo da Markdown a PDF con indice:

`pandoc --bibliography=biblio.bib --toc -s saggio.md -o saggio.pdf`

Lo stesso comando con estensione .epub produrrÃ  l'effetto desiderato. (generare
un EPUB). 

L'opzione standalone `-s` produce un documento indipendente;  
L'opzione `--toc` genera l'indice dei contenuti;  
L'opzione `-N` numera i capitoli;  
L'opzione `-H`, ad esempio: `-H head.css`, puÃ² essere usata per
inserire un link a un file css nel header HTML.

Quando non si specifica lo stile di citazione con l'opzione `--csl` Pandoc usa
il Chicago Manual of Style.

Pandoc usa unicode UTF-8. Consultare il manuale di [Pandoc][] per altre opzioni.

Le citazioni vengono riportate automaticamente alla fine del documento, dunque
l'ultimo capitolo farÃ  bene a chiamarsi: Bibliografia.

`# Bibliografia`

\newpage


