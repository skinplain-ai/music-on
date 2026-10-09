# ChordCapo

Accordi che scorrono insieme al brano, con capotasto, trasposizione, diagrammi per chitarra e librerie.

## Come si usa

- **YouTube**: cerca un brano o incolla un link. Il video si vede nell'app. Premi **Rileva ascoltando**, fai partire il video con gli altoparlanti accesi e l'app scrive gli accordi sulla linea del tempo ascoltando dal microfono. Dalla volta successiva gli accordi scorrono da soli, sincronizzati con il video.
- **File audio tuo** (mp3, m4a, wav): accordi, tempo (BPM) e battute vengono rilevati in automatico sul dispositivo.
- **Accordi**: maggiori, minori e settime (7, maj7, m7). Il riconoscimento usa il basso per trovare la fondamentale, dà meno peso alla voce, si adatta a registrazioni non accordate sul La 440 e decide gli accordi sull'intero tratto ascoltato, non su un istante alla volta.
- **Sincronia**: se gli accordi arrivano un po' prima o dopo la musica, puoi anticiparli o ritardarli di 0,1 s alla volta.
- **Griglia battute** come in Chordify, con l'accordo per ogni battito. Il tempo si può anche dare con *Tap tempo*, e il pulsante *Allinea alle battute* sistema i cambi di accordo.
- **Capotasto consigliato**: l'app calcola il capo che ti fa suonare più accordi aperti, e con un file lo imposta da sola.
- **Tonalità stimata** del brano e delle forme che suoni con il capo.
- **Velocità** dal 50% al 150% senza cambiare l'intonazione, e **loop A–B** per ripetere i passaggi difficili.
- **Diagrammi** per chitarra (anche per mancini) o pianoforte, notazione **Do Re Mi** oppure **C D E**, e opzione **accordi semplificati**.
- **Accordatore** per chitarra con il microfono.
- **Schermo intero** con accordi giganti, da usare sul leggio.
- **Librerie** con filtro, **esportazione e importazione** (backup o passaggio a un altro dispositivo) e **Copia accordi** per condividerli.
- **Scorciatoie**: Spazio per play/pausa, ← → per 5 secondi, A/B per i punti del loop, L per attivare o togliere il loop.

La ricerca dentro l'app è facoltativa e richiede una chiave gratuita di YouTube Data API v3, da inserire nelle impostazioni. Senza chiave, la ricerca apre YouTube in una nuova scheda.

## Interfaccia

- **Quattro sezioni**: Libreria, Suona, Accordatore e Impostazioni. Su telefono sono in una barra in basso, come in un'app.
- **Una sola barra di ricerca**: scrivi un titolo oppure incolla un link YouTube, che si apre subito.
- **Libreria a schede** con copertina del video, capo e BPM. Puoi filtrarla per libreria o per titolo, ordinarla e, dal menu ⋯ di ogni brano, spostarlo, rinominarlo o eliminarlo (con *Annulla*).
- **Comandi sempre a portata**: play, ±5 s, Capo, Tono, Velocità e Loop sono in una barra fissa e si regolano da pannelli che salgono dal basso.
- **Mini-player**: quando esci dal brano, l'accordo attuale resta visibile e puoi mettere in pausa.
- **Tema** chiaro, scuro o automatico.
- **Installabile**: dal browser si aggiunge alla schermata Home e si apre a schermo pieno, anche offline.

## Pubblicarla

L'app è fatta di `index.html` più tre piccoli file per l'installazione: `manifest.webmanifest`, `sw.js` e `icon.svg`. Pubblica la cartella intera (funziona anche solo `index.html`, ma senza l'installazione come app). Il sito deve essere servito in https perché il player YouTube e il microfono funzionino:

- **GitHub Pages**: Settings → Pages → Deploy from a branch → scegli il branch e la cartella `/ (root)`.
- **Netlify Drop**: trascina la cartella con i quattro file su app.netlify.com/drop.
- **In locale**: `python3 -m http.server`, poi apri `http://localhost:8000`.

L'audio dei video YouTube non viene scaricato né estratto: il rilevamento ascolta la musica dal microfono, come un'app di riconoscimento musicale.
