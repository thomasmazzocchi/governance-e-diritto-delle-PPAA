---
name: glossario
description: Aggiorna glossario.md con sigle e termini tecnici presenti negli schemi della repo (parte base e parte avanzata) che non sono ancora nel glossario. Usala quando l'utente chiede di aggiornare o completare il glossario, o dopo aver scritto uno schema nuovo.
argument-hint: "[schema | tutto]"
---

# Glossario

Scrivi in italiano.

## 1. Raccogli

1. Leggi `glossario.md`: formato `- **Termine** – spiegazione breve (norma, se c'è)`.
2. Schemi da esaminare (`$ARGUMENTS`): uno schema o tema, oppure `tutto`/vuoto = tutti i file in `parte-base/` e `parte-avanzata/`.
3. Estrai:
   - **sigle** (SCIA, TAR, CdS, PNRR, ...), con la forma estesa e la norma;
   - **termini tecnici** che all'orale vanno definiti con precisione (es. autotutela, silenzio assenso, interesse legittimo, in house, eccesso di potere), con una definizione di massimo 2 righe presa dallo schema.
   Salta i termini già presenti, anche se scritti in modo diverso (es. "D.Lgs." e "d.lgs.").

## 2. Scrivi

- Usa solo contenuti degli schemi (o il testo vigente della norma, se serve la sigla estesa). Non inventare.
- Ogni voce rimanda allo schema: `- **SCIA** – Segnalazione certificata di inizio attività (art. 19 L. 241/1990). → [cap-15](parte-base/cap-15-procedimento.md)`.
- Mantieni il formato e l'ordine del file. Se le voci diventano molte (oltre ~30), dividi in `## Sigle` e `## Termini`, ciascuna in ordine alfabetico, senza perdere voci esistenti.
- Uniforma lo stile delle sigle normative a quello degli schemi (`d.lgs.`, `L.`, `D.L.`).

## 3. Chiudi

In chat: quante voci aggiunte, divise per schema, e quali termini hai lasciato fuori perché lo schema non li definisce abbastanza (da completare sul libro).
