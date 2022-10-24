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
**`<!DOCTYPE html>`**
Questo è un tag particolare che deve essere messo ad inizio documento.
Dice all'interprete che il documento che si appresta a leggere è di tipo HTML.

**`<html>...</html>`**
E' il tag che contiene tutta la pagina web. Dopo questo tag non ci dovrebbe più essere nulla.
All'interno di questo tag sono presenti due tag: **head** e **body**
        
**`<head>...</head>`**
I tag che contiene non sono visibili all'utente. Servono a fare caricare correttamnete delle risorse aggiuntive.

**`<title>...</title>`**
Posizionare questo tag dentro il tag head. Il testo che inseriremo sarà visualizzato nella tab del browser.
        
**`<body>...</body>`**
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

## 2.4 Nel body...header, paragraph, comments
**`<h1>...</h1>`**  
Titolo di primo livello. Esistono i tag di header (intestazioni) da h1 ad h6 (dal più grande al più piccolo).
        
**`<p>...</p>`**
Paragrafi. Il testo verrà formattato come paragrafi.
Se nel codice andiamo a capo una o più volte, la modifica non si riflettarà nella pagina:
questo perché **il computer non considera gli a capo** scritti nel nostro codice.
Aggiungendo un altro paragrafo però si noterà che fra i due paragrafi ci saràuna linea vuota.
Il tag p (come il tag h) è un elemento di blocco: prima e dopo di esso verrà generata una linea vuota.
        
**`<!-- -->`**
Il testo racchiuso in questi tag verrà ignorato dall'interprete del browser.
Viene usato per inserire commenti utili nel codice.
        
## 2.5 break e horizontal rule.
**`<br />`**
Dato che a codice non esiste "a capo", il tag break serve proprio a forzare **"un a capo"**.
Ad esempio, usato dentro un paragrafo, il testo andrà a capo:
```markdown
    <p>
        Prima riga del primo paragrafo.
        Questa seconda riga NON verrà scritta a capo.
    </p>
    <p>
        Prima riga del secondo paragrafo
        <br />
        Questa seconda riga verrà scritta a capo! :)
    </p>
```

**`<hr />`**
Questo tag genera una linea orizzontale utile a dividere i contenuti della pagina web.    

## 2.6 tag per la formattazione.
I due principali tag per la formattazione del testo sono:
**`<strong>...<strong/>`**
Trasforma contenuto in testo in graseetto.
**`<em>...</em>`**
Trasforma contenuto in testo in corsivo.
```markdown
    <p>
        Sono <strong>Danilo</strong> e sono un <em>web developer</em>.
    </p>
```

## 2.7 tag div e span: contenitori generici.
Il tag div ed il tag span sono dei contenitore generici.
La differenza fra i due è che div è un tag di blocco mentre span è un tag inline
**`<div>...<div/>`**
**`<span>...<span/>`**
Anche lui al suo interno può contenere altri tag
```markdown
    <div>
        <p>ciao, sono un <span>paragrafo</span> contenuto in un div.</p>
    </div>
```

        
### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
