**Concetti base di HTML, CSS e Javascript per chi vuole diventare sviluppatore**

## 1 Come funziona il WEB?

I **client** sono tutti quei dispositivi che dispongono di un browser di una connessione ad internet.

I **server** sono dei computer sparsi per il mondo, molto performanti e costantementi collegati alla rete sui quali sono presenti i vari siti internet. 

Il **web** (o internet) sta in mezzo a questi due elementi.

**"Come avviene la magia?"**
![web](https://user-images.githubusercontent.com/29860929/144933977-ec9fae88-ccc9-40f5-a067-ef1ddcbb65f1.jpg)
Sul nostro client apriamo il browser e digitiamo un indirizzo:
```markdown
    https://www.google.com
```
Stiamo inviando una **request** (o richiesta) che attraverso internet arriva al server.
La richiesta contiene:
- **dominio** google.com;
- **method o action** di tipo GET se vogliamo che il server ci invii delle risorse;

Il server **gestisce tutte le request** che gli arrivano.
Prende in carico la nostra richiesta e invia al nostro client una **response** (o risposta)
La risposta contiene:
- un **codice di stato** (ad esempio 200 significa "OK" oppure 404 "Not found");
- un pacchetto contenente le **risorse** che abbiamo richiesto. Tipicamente sono file:
  - HTML;
  - CSS;
  - JavaScript;

La magia:
Il browser sul nostro client ha un **interprete**:
- prende in pasto i file .html, .css e .js inviati dal server;
- li interpreta: fornendo all'utente finale una **visualizzazione del contenuto** a lui comprensibile.

## 2.1 HTML

**H**yper**T**ext **M**arkup **L**anguage = Linguaggio di markup per ipertesti.
Anni 90: innovazione di internet e HTML: poter navigare fra le pagine (risorse) attraverso i **collegamenti ipertestuali**.
Linguaggio di markup: basato su markup (o marcatori, o etichette, o tag).
I **tag o marcatori** sono parole chiave racchiuse da parentesi angolari: <nomeTagEsempio>

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

Tutto ciò che vediamo in una pagina web è un elemento.
Spesso un elemento contiene altri elemti.
Si tratta di una struttura annidata (come le scatole cinesi).
Esempio: un menù di navigazione che al suo interno contiene un immagine e un elenco di voci.
Esempio2: una pagina con tre colonne; nella prima e terza sono presenti articoli; la centrale è ulteriormente divisa in due sezioni;
    la prima contiene un titolo; la seconda un'immagine.

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
**NB: Per non "perdersi nei meandri del codice", bisogna tenere "indentati" i tag.
Significa spaziare con un rientro i tag contenuti in altri tag.
Così vediamo a prima vista dove si apre un tag e dove viene chiuso diverse righe più giù.**

**Casi particolari**

Alcuni tag nonhanno il tag di chiusura. Possono essere scritti:
```markdown
    <tagSenzaChiusura1>   
```
Oppure:
```markdown
    <tagSenzaChiusura2 />    
```

## 2.3 La struttura base della pagina HTML
**<!DOCTYPE html>**
Questo è un tag particolare che deve essere messo ad inizio documento.
Dice all'interprete che il documento che si appresta a leggere è di tipo HTML.

**<html>...</html>**
E' il tag che contiene tutta la pagina web. Dopo questo tag non ci dovrebbe più essere nulla.
All'interno di questo tag sono presenti due tag: **head** e **body**
        
**<head>...</head>**
I tag che contoiene non sono visibili all'utente. Servono a fare caricare correttamnete delle risorse aggiuntive.

**<title>...</title>**
Posizionare questo tag dentro il tag head. Il testo che inseriremo sarà visualizzato nella tab del browser.
        
**<body>...</body>**
Contiene tutto il contenuto visibile all'utente della pagina web.
```markdown
    <!DOCTYPE html>
        <html>
            <head>
                <title>La mia pagina web</title>
                ...
            </head>
            <body>
                ...
            </body>
        </html>
```


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
