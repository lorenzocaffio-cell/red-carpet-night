# Red Carpet Night

Web app per la festa di Mattia: coppie, carte giocatore, voti, pronostici, foto e cerimonia in stile Oscar.
Un solo file: `index.html`. Admin: codice iniziale `1221` (icona chiave).

## 1. Database condiviso (Firebase, gratis, 3 minuti)
1. Vai su https://console.firebase.google.com → **Aggiungi progetto** (nome a piacere, Analytics disattivato).
2. Menu **Build → Realtime Database → Crea database**. Scegli la regione e **modalità test**.
3. Scheda **Regole**: incolla e pubblica
   ```
   { "rules": { ".read": true, ".write": true } }
   ```
4. Copia l'indirizzo in cima alla scheda **Dati**, tipo `https://NOME-default-rtdb.europe-west1.firebasedatabase.app`.
5. Apri `index.html`, cerca `const FIREBASE_URL=''` e metti l'indirizzo tra gli apici (senza `/` finale).

## 2. Pubblicare su GitHub Pages
1. Nuovo repository pubblico, carica `index.html`, `.nojekyll`, `README.md`.
2. Settings → Pages → Deploy from a branch → `main` / `(root)`.
3. Il link è `https://<utente>.github.io/<repository>/`: condividilo con gli ospiti.

## Note
- Le regole aperte vanno bene per una serata: dopo la festa elimina il progetto Firebase.
- La musica (Firework) si carica dalla Regia e resta salvata nel browser del dispositivo che la riproduce; non è nel repository.
- Se `FIREBASE_URL` è vuoto, l'app funziona ma ogni telefono vede solo i propri dati.
