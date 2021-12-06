**Concetti base di HTML, CSS e Javascript per chi vuole diventare sviluppatore**

## 1 Come funziona il WEB?

[vedi immagine del funzionamento del web](https://daniepa.github.io/TDPC/web.jpg)

I **client** sono tutti quei dispositivi che dispongono di un browser di una connessione ad internet.

I **server** sono dei computer sparsi per il mondo, molto performanti e costantementi collegati alla rete sui quali sono presenti i vari siti internet. 

Il **web** (o internet) sta in mezzo a questi due elementi.

**"Come avviene la magia che ogni giorno ci permette di visualizzare i siti internet sui nostri clients?"**

Quando sul nostro client apriamo il browser e digitiamo un indirizzo, ad esempio:
```markdown
    https://www.google.com
```
stiamo inviando una **request** (o richiesta) nella quale:
- chiediamo ad internet di trovare il server che ospita quel sito (dominio);
- passiamo un metodo di tipo GET (vogliamo che ci tornino indietro delle risorse);

Il compito del server è quello di gestire tutte le request che gli arrivano.
Una volta che prende in carico la nostra richiesta invia al nostro client una **response** (o risposta) contenente:
- un **codice di stato** (ad esempio 200 significa "OK" oppure 404 "Not found");
- un pacchetto contenente le **risorse** che abbiamo richiesto contenente che tipicamente sono file di tipo:
  - HTML;
  - CSS;
  - JavaScript;

Ed eccoci alla magia:
Il browser installato sul nostro client è un programma che al suo interno ha un **interprete**. I suoi compiti sono:
- prendere in pasto i file con estensione .html, .css e .js;
- interpretarli fornendo all'utente finale una **visualizzazione del contenuto** a lui comprensibile.

## 2.1 HTML

HTML significa **H**yper**T**ext **M**arkup **L**anguage ovvero Linguaggio di markup per ipertesti.
Dalla nascita di internet e dell'HTML, la vera innovazione era proproi quella di poter navigare fra le pagine attraverso delle scritte clickabili (**collegamenti ipertestuali**).
Linguaggio di markup significa che l'HTML non è un linguaggio di programmazione, ma basato su markup ovvero dei marcatori (o etichette, o tag).
Dal browser Chrome su qualsiasi pagina web, digitando CTRL+U (o visualizza sorgente pagina) è possibile visualizzare il codice HTML di quella pagina.
Ad un primo sguardo può sembrare un codice incomprensibile.
Noteremo come il codice sarà pieno di simboli maggiore e minore (< e >).
I **tag o marcatori** sono proprio delle parole chiave contenute fra questi simboli, dette anche parentesi angolari.

## 2.2 I tag HTML

I tag sono parole chiave.
La maggior parte dei tag, è composto da:
- tag di apertura: <tag>
- contenuto del tag (testo o altri tag);
- tag di chiusura: </tag>

Risultato:
```markdown
    <nomeDelTag> Contenuto del tag </nomeDelTag>
```

Dobbiamo immaginare tutti gli elementi che vediamo in una pagina web come dei blocchi.
Immaginate ad esempio un post di Instagram:
- la pagina intera è il blocco principale;
        - all'interno partendo dall'alto è presente un primo blocco orizzontale contenente:
            - l'immagine circolare dell'utente che ha pubblicato il post;
            - alla sua destra il nome;
            - sulla destra i tre puntini che permettono di aprire il menù;
        - il secondo blocca occupa gran parte dell'immagine e contiene la foto;
        - il terzo blocco contiene gli elemnti:
            - sulla sinistra le icone 'cuore', 'commenta' e 'invia';
            - sulla destra l'icona 'salva nella raccolta'
e così via...

E' una struttura ad albero o a scatola cinese con un elemento contenuto nel successivo che a sua volta contiene elementi.
La struttura dei file HTML è proprio così: tag che contengono altri tag che contengono altri tag...

Esempio:
```markdown
    <tag1>
        <tag2></tag2>
        <tag3>
            <tag4></tag4>
            <tag5></tag5>
        </tag3>
    </tag1>
```
**NB: è importante mantenere i tag "indentati" correttamente ovvero spaziare con un rientro i tag contenuti in altri tag.
In questo modo si vede visivamente dove si apre un tag e dove viene ghiuso diverse righe più giù.**

**Casi particolari**

Esistono alcuni tag che che non necessitano del tag di chiusura e possono scriversi in 2 diversi metodi:
Esempio:
```markdown
    <tagSenzaChiusura1>
    ...
    <tagSenzaChiusura2 />    
```

## 2.3 La struttura base della pagina HTML
**<!DOCTYPE html>**
Questo è un tag particolare che deve essere messo ad inizio documento. Dice all'interprete che il documento che si appresta a leggere è di tipo HTML.

**<html>...</html>**
E' il tag che contiene tutta la pagina web. Dopo questo tag non ci dovrebbe più essere nulla.

All'interno di questo tag sono presenti due tag distinti
**<head>...</head>**
Contiene tutto ciò che non è visibile all'utente nella pagina. Contiene altri tagche servono a fare caricare correttamnete delle risorse aggiuntive.

**<body>...</body>**
Contiene tutto il contenuto visibile all'utente della pagina web.
```markdown
    <html>
        <head>
            ...
        </head>
        <body>
            ...
        </body>
    </html>
```


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
