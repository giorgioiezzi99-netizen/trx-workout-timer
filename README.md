# SetTempo

Sito ufficiale e timer web di SetTempo, progettati con lo stesso linguaggio visivo dell’app iPhone.

## Struttura

- `/` — landing page del prodotto
- `/app/` — timer completo utilizzabile nel browser
- `/privacy/` — informativa privacy
- `/manifest.webmanifest` — installazione del timer web come PWA
- `/assets/` — logo, stili, script e avvisi vocali

Il progetto è statico e non richiede una fase di build.

## Allenamento predefinito

- Nome: `Allenamento Base`
- 10 serie
- 6 ripetizioni per serie
- 24 secondi di esercizio
- 10 secondi di recupero tra ripetizioni
- 15 secondi di recupero tra serie
- Durata totale: `34:35`

## Timer web

- Avvia, pausa e azzera
- Fasi di esercizio, recupero e recupero tra serie
- Timer personalizzati salvati nel browser
- Avvisi sonori e voce italiana
- 20 stazioni radio italiane con cambio automatico in caso di errore
- Controlli pensati per desktop, iPhone e installazione dalla schermata Home

## Pubblicazione

Il repository è collegato al progetto Vercel `trx-workout-timer`. La landing page può essere pubblicata direttamente senza configurare comandi di build o cartelle di output.

Il pulsante App Store resta nello stato `Presto su App Store` finché non è disponibile l’URL pubblico definitivo dell’app.
