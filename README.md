# Inventario armadio

Pagina statica per GitHub Pages. Nessun backend.

## Accesso
`index.html` contiene solo un campo password. Il percorso dell'app è cifrato (AES-GCM, chiave derivata dalla password con PBKDF2-SHA256, 250.000 iterazioni): senza password il file contiene solo dati illeggibili. Password errata → nessun redirect.

L'app vive in una cartella con nome casuale (`36fabb1bcddf6d49408ab190/`). Non linkarla da nessuna parte e non citarla in README pubblici.

⚠ È una protezione per oscuramento: chi vede la repository vede anche il nome della cartella. Per una protezione reale usa una **repository privata** (GitHub Pages da repo privata richiede un piano a pagamento) oppure non condividere il link della repo.

## Pubblicazione
1. Carica **tutto il contenuto** di questa cartella nella root della repository, incluso il file nascosto `.nojekyll` (serve perché la cartella `_ds/` venga pubblicata).
2. Settings → Pages → Source: `Deploy from a branch`, branch `main`, cartella `/ (root)`.
3. Apri `https://<utente>.github.io/<repo>/` e inserisci la password.

## Aggiornare i dati
1. Modifica gli oggetti dalla pagina (le modifiche restano sul dispositivo).
2. Premi **Esporta**: scarica `inventario.json`.
3. Rinominalo in `inventario.json` se il browser ha aggiunto "(1)".
4. Nella repository: cartella `36fabb1bcddf6d49408ab190/` → Upload → sostituisci `inventario.json` → Commit.
5. GitHub Pages può impiegare qualche minuto a mostrare la nuova versione.

Aggiornare da una sola persona/dispositivo alla volta: l'ultimo export sovrascrive il file.
