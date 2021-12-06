## 1. Come funziona il WEB?

[Il web](url)

I **client** sono tutti quei dispositivi che dispongono di un browser di una connessione ad internet.

I **server** sono dei computer sparsi per il mondo, molto performanti e costantementi collegati alla rete sui quali sono presenti i vari siti internet. 

Il **web** (o internet) sta in mezzo a questi due elemnti.

**"Come avviene la magia che ogni giorno ci permette di visualizzare i siti internet sui nostri clients?"**

Quando sul nostro client apriamo il browser e digitiamo un indirizzo, ad esempio:
```markdown
    https://www.google.com
```
stiamo inviando una **request** (o richiesta) nella quale:
- chiediamo ad internet di trovare il server che ospita quel sito (dominio);
- passiamo un metodo di tipo GET (vogliamo che ci tornino indietro delle risorse);

Il compito del server è quello di tutte le request che gli arrivano.
Una volta che prende in carico la nostra richiesta invia al nostro client una **response** (o risposta) contenente:
- un codice di stato (ad esempio 200 significa "OK" oppure 404 "Not found");
- un pacchetto contenente le risorse che abbiamo richiesto contenente che tipicamente sono file di tipo:
  - HTML;
  - CSS;
  - JavaScript;


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
