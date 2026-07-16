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
- Radio italiane include 20 stazioni italiane principali, tutte su stream HTTPS, con controlli Radio precedente e Radio successiva.
- Se una radio perde la connessione, l'app tenta il ripristino e, se non risponde, passa automaticamente alla stazione successiva.
- Avviare l'allenamento avvia la radio selezionata; pausa/azzera mettono in pausa o fermano la radio.
- Musica, segnali e voce usano un rapporto fisso e vengono regolati insieme con i tasti fisici del telefono; gli slider interni sono stati rimossi.
- La voce usa normalizzazione e compressione dedicate per risultare più forte e intelligibile della musica senza clipping.
- Segnali e voce sono riprodotti come un unico file audio multimediale, così seguono la stessa uscita Bluetooth della musica.
- Su iPhone la radio non viene più silenziata o interrotta durante gli avvisi: musica e voce restano sovrapposte e continue.
- Sui browser che supportano davvero il controllo del volume multimediale resta disponibile un'attenuazione graduale automatica della radio.
- Per il blocco schermo, l'app prepara una singola traccia PCM 16-bit / 12 kHz con tutti gli avvisi già posizionati nel tempo. Su iPhone va avviata da Safari prima di bloccare il telefono; i browser interni di WhatsApp e altre app possono comunque interrompere l'audio in background.
- Durante il timer, l'app richiede il blocco schermo attivo dove supportato dal browser.

## Fonti audio

- Senza musica: avvia il timer senza caricare stream audio. Voce e segnali sonori restano attivi.
- Radio italiane: 20 stazioni principali, con stream audio diretti o HLS verificati come media riproducibili dal browser.
  - RTL 102.5, Radio Italia, RDS, Radio Deejay, Radio 105, Radio Kiss Kiss
  - Rai Radio 1, Virgin Radio, Rai Radio 3, Rai Radio 2, R101, Radio Monte Carlo
  - Radio Capital, m2o, Radiofreccia, Radio Zeta, Radio Bruno, Radio Subasio
  - Radio Norba, Radio Parsifal

## Note dal vecchio thread

La richiesta originale era creare un sito o un file HTML semplice perché la mamma dell'utente potesse usarlo senza scaricare un'app.

La prima versione completata era stata verificata nel vecchio thread con Playwright su desktop `1440x920` e mobile `390x844`. Quel controllo includeva avvio, pausa, azzera, transizione dalla ripetizione 6 al recupero serie da 15 secondi, salvataggio timer personalizzato, persistenza dopo reload, conferma eliminazione, layout responsive e console pulita dopo la correzione della favicon.

L'ultima modifica nel vecchio thread era stata interrotta dopo l'applicazione delle patch. Queste patch sono presenti in questa copia del progetto: l'editor parte chiuso con toggle Modifica/Nascondi e il pulsante Salta è stato rimosso.
