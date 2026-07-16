# Timer Allenamento TRX

Timer browser in un singolo file per un allenamento TRX / Tabata. Il progetto è stato spostato dal thread Codex `019f1cf3-03ce-75a0-b3a9-64d4ee1d910a`.

## File

- File principale: `index.html`
- Logo: `assets/trx-timer-logo.png`
- File sorgente originale copiato da: `/Users/giorgioiezzi/Documents/Codex/2026-07-01/okay-so-i-need-you-to/outputs/trx-tabata-timer.html`
- Non serve installare l'app o fare una build. La pagina è pensata per aprirsi direttamente nel browser.

## Allenamento predefinito

- Nome timer: `Allenamento TRX`
- Serie: `10`
- Ripetizioni per serie: `6`
- Durata ripetizione: `24` secondi
- Recupero tra ripetizioni: `10` secondi
- Recupero tra serie: `15` secondi
- Dopo la ripetizione 6, il recupero serie da 15 secondi sostituisce il normale recupero da 10 secondi.
- Durata totale predefinita: `34:35`

Calcolo totale:

- Esercizio: `10 * 6 * 24s = 24:00`
- Recuperi tra ripetizioni: `10 serie * 5 recuperi * 10s = 8:20`
- Recuperi tra serie: `9 recuperi * 15s = 2:15`
- Totale: `34:35`

## Funzioni attuali

- Controlli Avvia, Pausa e Azzera.
- Tracciamento automatico delle fasi: Esercizio, Recupero, Recupero serie e Completato.
- Timer personalizzati salvati con `localStorage` del browser.
- Flussi Nuovo, Copia, Elimina, Salva e Annulla.
- Nome timer, serie, ripetizioni per serie, secondi ripetizione, recupero tra ripetizioni e recupero tra serie modificabili.
- Segnali sonori e voce italiana preregistrata per le transizioni.
- Layout responsive desktop e mobile.
- Logo generato usato nell'intestazione e come favicon.
- Editor timer nascosto dopo il salvataggio o la selezione di un timer salvato.
- Il pulsante Modifica riapre l'editor; Nascondi lo richiude.
- Il controllo Salta è stato rimosso.
- I miei timer è chiuso di default e appare sopra il timer, così i timer salvati sono facili da raggiungere senza occupare il layout mobile.
- Musica è chiusa di default e offre Senza musica o Radio italiane.
- Radio italiane include 20 stazioni italiane principali con controlli Radio precedente e Radio successiva.
- Avviare l'allenamento avvia la radio selezionata; pausa/azzera mettono in pausa o fermano la radio.
- Volume musica e Volume avvisi hanno slider grandi e visibili.
- Segnali e voce sono riprodotti come un unico file audio multimediale, così seguono la stessa uscita Bluetooth della musica.
- Il volume avvisi viene applicato direttamente ai campioni di segnali e voce, anche sui dispositivi che ignorano il volume degli elementi audio.
- Su iPhone, quando Safari non permette di regolare il volume della radio dalla pagina, l'interfaccia indica di usare i tasti fisici del telefono.
- I segnali e i countdown vocali abbassano temporaneamente il volume della musica per la durata reale dell'avviso, poi lo ripristinano esattamente.
- Su iPhone, dove Safari impedisce l'attenuazione graduale, viene silenziata soltanto la radio durante l'avviso e riattivata automaticamente subito dopo.
- Durante il timer, l'app richiede il blocco schermo attivo dove supportato dal browser.

## Fonti audio

- Senza musica: avvia il timer senza caricare stream audio. Voce e segnali sonori restano attivi.
- Radio italiane: 20 stazioni principali, con stream audio diretti o HLS verificati come media riproducibili dal browser.
  - RTL 102.5, Radio Italia, RDS, Radio Deejay, Radio 105, Radio Kiss Kiss
  - Rai Radio 1, Virgin Radio, Radio 24, Rai Radio 2, R101, Radio Monte Carlo
  - Radio Capital, m2o, Radiofreccia, Radio Zeta, Radio Bruno, Radio Subasio
  - Radio Norba, Radio Parsifal

## Note dal vecchio thread

La richiesta originale era creare un sito o un file HTML semplice perché la mamma dell'utente potesse usarlo senza scaricare un'app.

La prima versione completata era stata verificata nel vecchio thread con Playwright su desktop `1440x920` e mobile `390x844`. Quel controllo includeva avvio, pausa, azzera, transizione dalla ripetizione 6 al recupero serie da 15 secondi, salvataggio timer personalizzato, persistenza dopo reload, conferma eliminazione, layout responsive e console pulita dopo la correzione della favicon.

L'ultima modifica nel vecchio thread era stata interrotta dopo l'applicazione delle patch. Queste patch sono presenti in questa copia del progetto: l'editor parte chiuso con toggle Modifica/Nascondi e il pulsante Salta è stato rimosso.
