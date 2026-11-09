---
name: quiz
description: Genera un quiz (risposta multipla, vero/falso, "quale norma?", completamento) sugli schemi della repo, lo corregge e registra gli errori in verifiche/errori.md, così i quiz successivi ripartono dai punti deboli. Usala quando l'utente chiede un quiz, un test o domande di ripasso veloci.
argument-hint: "[capitolo/tema | tutto | errori] [n. domande]"
---

# Quiz

Scrivi in italiano.

## Preparazione

1. Argomento da `$ARGUMENTS`:
   - un capitolo o tema (es. `cap-16`, `accesso`, `servizi pubblici`);
   - `tutto` o vuoto: tutto il programma studiato;
   - `errori`: solo argomenti presenti in `verifiche/errori.md` non ancora segnati come recuperati.
   Numero di domande: quello indicato, altrimenti 10.
2. Leggi gli schemi pertinenti (`parte-base/`, `parte-avanzata/`) e `verifiche/errori.md` se esiste. Anche senza `errori`, circa un terzo delle domande deve riguardare argomenti sbagliati di recente.
3. Costruisci le domande **solo** da contenuti presenti negli schemi. Mescola i tipi:
   - **risposta multipla** (4 opzioni, una giusta, distrattori plausibili: termini vicini, articoli vicini, istituti simili);
   - **vero/falso** con motivazione richiesta;
   - **quale norma?** (es. "Dove è previsto il preavviso di rigetto?" → art. 10-bis L. 241/1990);
   - **completamento** di termini e numeri (giorni, mesi, anni).
   Dai priorità a ciò che all'esame si sbaglia facilmente: termini, articoli, differenze tra istituti, novità successive al libro.

## Svolgimento

- Mostra **tutte le domande insieme**, numerate, senza soluzioni. Chiedi all'utente di rispondere in un messaggio unico (es. `1b 2V 3 art. 21-octies ...`).
- Fermati e aspetta le risposte.

## Correzione

- Tabella: n. · risposta data · risposta giusta · ✅/❌ · spiegazione in una riga con il riferimento allo schema (`file#sezione`).
- Punteggio (es. 7/10) e gli argomenti da rileggere.

## Registro errori

Aggiorna `verifiche/errori.md` (crealo se non c'è, con questa intestazione):

```markdown
# Registro errori

Errori di quiz e interrogazioni. Le skill `quiz` e `interrogazione` ripartono da qui.

| Data | Fonte | Argomento | Errore | Da rileggere |
| --- | --- | --- | --- | --- |
```

- Aggiungi una riga per ogni risposta sbagliata (`Fonte` = `quiz`).
- Se in un quiz `errori` l'utente risponde bene su un argomento già nel registro, aggiungi ✔️ recuperato (data) nella colonna `Errore` della riga vecchia invece di cancellarla.

Ricorda che le domande vengono dagli schemi: dove lo schema dice "Verifica sul libro", la risposta va controllata su Mattarella.
