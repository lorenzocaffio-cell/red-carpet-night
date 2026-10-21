# Red Carpet Night

Web app per la festa di compleanno di Mattia: festa a tema a coppie con premiazione in stile Oscar.
Iscrizione delle coppie, carte giocatore, votazioni Likert, pronostici, foto della serata e cerimonia finale sincronizzata.

È un unico file: `index.html`. Nessuna build.

## Pubblicarlo su GitHub Pages
1. Crea un repository (es. `red-carpet-night`) e carica `index.html` e `.nojekyll`.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.
3. Dopo un minuto il sito è su `https://<tuo-utente>.github.io/red-carpet-night/`.

## Attenzione: dati condivisi
Sulla piattaforma Claude (dove è nato) i dati sono condivisi in tempo reale tra tutti i telefoni.
Fuori da lì (GitHub Pages incluso) l'app usa il **localStorage**: ogni telefono vede **solo i propri dati**,
quindi iscrizioni, voti e cerimonia NON si sincronizzano tra gli ospiti.
Per usare GitHub Pages serve un database condiviso (es. Firebase Firestore o Supabase): va scritto un adattatore
al posto di `localBackend()` nel codice (stessa interfaccia: `sub`, `set`, `del`, `clear`).

## Admin
Codice iniziale: `1221` (cambiabile dalla Regia, icona chiave).

## Musica
Dalla Regia si carica il file audio di Firework: resta salvato nel browser del dispositivo e suona solo lì.
Il file non è incluso nel repository (copyright).
