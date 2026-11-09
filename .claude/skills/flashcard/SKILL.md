---
name: flashcard
description: Estrae flashcard (definizioni, articoli di legge, termini, sentenze, differenze tra istituti) dagli schemi della repo e le salva in un file importabile in Anki. Usala quando l'utente chiede flashcard, carte per Anki o materiale da ripassare dal telefono.
argument-hint: "[capitolo/tema | tutto]"
---

# Flashcard

Scrivi in italiano.

## 1. Scegli gli schemi

- Da `$ARGUMENTS`: un capitolo o tema (es. `cap-19`, `accesso`), oppure `tutto`/vuoto = tutti gli schemi completi in `parte-base/` e `parte-avanzata/` (salta quelli con stato "da fare").
- Un file di output per schema: `flashcard/<nome-schema>.txt` (es. `flashcard/cap-15-procedimento.txt`). Se il file esiste, rigeneralo da capo (l'import in Anki aggiorna le carte con lo stesso fronte).

## 2. Scegli le carte

Solo contenuti presenti nello schema, niente aggiunte. Da 15 a 30 carte per schema, a seconda della lunghezza. Tipi:

| Tipo | Fronte | Retro |
| --- | --- | --- |
| Definizione | Che cos'è l'interesse legittimo? | Definizione in 1-2 righe |
| Norma | Dove è disciplinato l'annullamento d'ufficio? | Art. 21-nonies L. 241/1990 + contenuto essenziale |
| Numero | Entro quanto si può annullare d'ufficio un provvedimento autorizzatorio? | 6 mesi (L. 182/2025; prima 12) |
| Sentenza | Granital (Corte cost. 170/1984) | Cosa ha stabilito, in una riga |
| Differenza | SCIA vs silenzio assenso | Differenza chiave in 2 righe |

Regole:
- Una sola informazione per carta. Retro di **massimo 3 righe**.
- Domande formulate in modo che la risposta sia univoca.
- Segnala le novità successive al libro (es. "novità L. 1/2026") così l'utente sa che non le troverà su Mattarella.
- Niente carte su contenuti segnati "Verifica sul libro" se non sono confermati.

## 3. Formato Anki

File di testo UTF-8, separato da tabulazioni, con le intestazioni che Anki (2.1.55 o successivo) legge in automatico:

```
#separator:tab
#html:true
#tags column:3
Fronte	Retro	cap-15 procedimento
```

- Colonna 1 fronte, colonna 2 retro, colonna 3 tag separati da spazio: nome breve dello schema + tipo (`definizione`, `norma`, `numero`, `sentenza`, `differenza`).
- Niente tabulazioni o a capo dentro i campi: per andare a capo usa `<br>`; il grassetto con `<b>...</b>`.
- Controlla che ogni riga abbia esattamente 3 campi.

## 4. Chiudi

- Se manca, crea `flashcard/README.md` con le istruzioni di import: Anki → File → Importa → scegli il file → tipo di nota "Base", mazzo "Diritto amministrativo" → Importa. Su telefono: importa da desktop e sincronizza con AnkiWeb (AnkiDroid importa anche direttamente).
- In chat: file creati, numero di carte per file, eventuali parti dello schema escluse e perché.
