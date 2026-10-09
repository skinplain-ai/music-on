# ChordCapo

Accordi che scorrono insieme al brano, con capotasto, trasposizione, diagrammi per chitarra e librerie.

## Come si usa

- **YouTube**: cerca un brano o incolla un link. Il video si vede nell'app. Premi **Rileva ascoltando**, fai partire il video con gli altoparlanti accesi e l'app scrive gli accordi sulla linea del tempo ascoltando dal microfono. Dalla volta successiva gli accordi scorrono da soli, sincronizzati con il video.
- **File audio tuo** (mp3, m4a, wav): il rilevamento è automatico e avviene sul dispositivo.
- **Capotasto e trasposizione**: gli accordi diventano le forme da suonare. Viene indicato anche l'accordo reale.
- **Correzioni**: puoi sostituire, inserire o togliere un cambio di accordo nel punto in cui ti trovi.
- **Librerie**: i brani salvati restano nel browser del dispositivo.

La ricerca dentro l'app è facoltativa e richiede una chiave gratuita di YouTube Data API v3. Senza chiave, la ricerca apre YouTube in una nuova scheda.

## Pubblicarla

È un'unica pagina, `index.html`, senza bisogno di build. Deve essere servita in https perché il player YouTube e il microfono funzionino:

- **GitHub Pages**: Settings → Pages → Deploy from a branch → scegli il branch e la cartella `/ (root)`.
- **In locale**: `python3 -m http.server`, poi apri `http://localhost:8000`.

L'audio dei video YouTube non viene scaricato né estratto: il rilevamento ascolta la musica dal microfono, come un'app di riconoscimento musicale.
