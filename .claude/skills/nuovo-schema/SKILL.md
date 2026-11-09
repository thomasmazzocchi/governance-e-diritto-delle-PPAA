---
name: nuovo-schema
description: Scrive un nuovo schema di studio (capitolo o paragrafo del Mattarella, oppure materiale della parte avanzata) nel formato obbligatorio della repo e aggiorna il README. Usala quando l'utente chiede di schematizzare un capitolo, un paragrafo o un tema (es. "fai lo schema del cap. VII sui servizi pubblici").
argument-hint: "<capitolo/paragrafo o tema> [fonte]"
---

# Nuovo schema

Scrivi in italiano. Obiettivo: uno schema identico per stile ai cap. 1, 2 e 4 (`parte-base/cap-01-*.md`, `cap-02-*.md`, `cap-04-*.md`).

## 1. Prepara

1. Leggi `CLAUDE.md` (programma, mappa capitoli, novità già integrate) e `templates/schema-capitolo.md`.
2. Leggi uno schema di riferimento (`parte-base/cap-04-fonti.md`) per tono e lunghezza.
3. Individua il contenuto richiesto (`$ARGUMENTS`):
   - **Mattarella**: titoli dei paragrafi da `risorse/indice-mattarella-1a-ed.md`, pagine dalla mappa in `CLAUDE.md`. Se il tema non è nel programma, dillo e chiedi conferma prima di scrivere.
   - **Parte avanzata**: controlla in `parte-avanzata/` il file del tema e le note su autore/edizione da chiarire. Se l'indice del libro non è disponibile, chiedi all'utente l'indice o le pagine invece di inventare i titoli.
4. Se lo schema esiste già, non sovrascriverlo: proponi di integrarlo.

## 2. Ricerca

- Testo del libro online: solo l'estratto Giappichelli (cap. 1). Per il resto usa fonti affidabili: Normattiva (testo vigente), Corte costituzionale, EUR-Lex, giustizia-amministrativa.it, materiali universitari.
- Controlla sempre il **testo vigente** delle norme: dopo il libro ci sono state riforme (vedi `CLAUDE.md`, "Novità successive"). Se trovi altre novità, segnalale nello schema e all'utente.
- Non inventare sentenze, numeri di articolo o pagine. Se non sei sicuro, scrivi "Verifica sul libro...".

## 3. Scrivi

File:
- Mattarella: `parte-base/cap-NN-titolo.md` o `parte-base/par-NN.N-titolo.md` (minuscole, trattini).
- Parte avanzata: aggiorna o crea il file in `parte-avanzata/` (es. `servizi-pubblici.md`), conservando le righe iniziali su fonti, priorità e periodo, e aggiornando la riga **Stato**.

Struttura obbligatoria:

1. Titolo `# Cap. N – Titolo (Mattarella)` (parte avanzata: `# Tema – Titolo (Autore, cap. X)`).
2. Paragrafo introduttivo che dichiara **da dove viene il contenuto**: testo dell'autore o fonti esterne da confrontare con il libro, con le pagine.
3. Una sezione `## N.x Titolo` per ogni paragrafo del libro, con i titoli del libro. Ognuna:
   - si apre con **una frase che dice la tesi**;
   - prosegue con un elenco puntato `- **Concetto.** spiegazione in 1-2 frasi, con la norma (es. art. 21-nonies L. 241/1990).`;
   - tabelle per i confronti;
   - un riquadro `> **Nel mondo reale.** ...` con un esempio concreto e verificabile (non dal libro);
   - nota `Verifica sul libro ...` dove il contenuto non viene dal testo.
4. `## Domande di verifica`: 3-5 domande numerate, del tipo che potrebbe fare il professore all'orale.
5. Checkbox: `- [ ] Leggere il cap. N sul libro (pp. ___-___) e confrontarlo con questo schema`.
6. `## Fonti`: link affidabili, uno per riga.

## 4. Chiudi

- Aggiorna la tabella del `README.md` (riga del tema, link allo schema, stato ✅ con eventuali note).
- Aggiungi a `glossario.md` sigle e termini nuovi, in ordine come gli altri.
- Se lo schema introduce novità normative successive al libro, aggiornale anche nella sezione "Stato dei lavori" di `CLAUDE.md`.
- Suggerisci all'utente di far girare il fact-check sullo schema nuovo.
- Riassumi in chat: file creato, paragrafi coperti, punti da verificare sul libro.
