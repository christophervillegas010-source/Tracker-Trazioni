# WeightTrack — guida rapida

Questa è una prima versione di una Progressive Web App (PWA) per Android. Usa HTML, CSS e JavaScript; i dati sono salvati nel `localStorage` del browser e non vengono inviati a un server.

## Funzioni
- Inserimento, modifica ed eliminazione del peso per data
- Grafico SVG con finestre da 7 giorni, 30 giorni o tutto lo storico
- Esportazione e importazione di backup CSV
- Interfaccia adattabile a telefoni e modalità chiara/scura
- Service worker per aprire l'app anche offline dopo il primo caricamento riuscito

## Come usarla su Android
Per installarla come PWA, i file devono essere pubblicati su un sito HTTPS. Aprire `index.html` come file locale non consente normalmente di installare la PWA e non abilita il service worker.

### Pubblicazione gratuita con GitHub Pages
1. Da Chrome sul telefono, accedi o crea un account GitHub.
2. Crea un nuovo repository pubblico, ad esempio `weighttrack`.
3. Carica tutti i file contenuti in questa cartella nella radice del repository.
4. Nel repository apri **Settings → Pages**.
5. In **Build and deployment**, scegli **Deploy from a branch**, seleziona `main` e `/ (root)`, poi salva.
6. Attendi la pubblicazione. Apri l'indirizzo HTTPS indicato da GitHub Pages.
7. In Chrome, menu `⋮` → **Aggiungi a schermata Home** o **Installa app** (la dicitura può variare).

## Importante: conservazione dei dati
- Le misurazioni restano nel browser e nell'origine web di questa app. Non sincronizzano automaticamente con altri browser o telefoni.
- Non cancellare i dati del sito/browser senza aver prima esportato un backup CSV.
- Esporta periodicamente il backup; prova l'importazione con un file di backup se vuoi verificare il ripristino.
- Questa è una versione iniziale: non è un dispositivo medico e non interpreta variazioni di peso come diagnosi.

## Modifiche
- `index.html`: interfaccia, grafico e logica dei dati.
- `manifest.webmanifest`: nome, icone e comportamento d'installazione.
- `sw.js`: cache offline dell'app.
