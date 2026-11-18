# Make It Simple

**Versione 1.1.0.** Una skill per Codex che chiede all’agente di arrivare al risultato per la via affidabile più breve. Se il file è indicato, si parte da quel file. Se basta eseguire il programma per confermare che il risultato è già corretto, il lavoro finisce lì. Un controllo ulteriore serve quando risponde a una domanda ancora aperta, è obbligatorio oppure è stato richiesto. [Leggi le istruzioni della skill](make-it-simple/SKILL.md).

La stessa regola vale per ciò che si consegna. Il lettore trova subito il risultato e le eventuali decisioni da prendere. Se si tratta di una simulazione, lo capisce dalla prima descrizione del risultato. Log e identificativi utili all’assistenza possono stare in una breve nota tecnica in fondo. Quando il destinatario chiede codice o dati in un formato preciso, la skill rispetta quel formato.

## Esempi

- **Spostare un promemoria.** Cambiare l’anticipo delle quote soci e verificare che il valore delle fatture fornitori sia rimasto identico.
- **Duplicare un flusso.** Riutilizzare il flusso esistente, aggiornare identità e riferimenti, lasciare la copia nello stato richiesto.
- **Controllare un calcolo.** Se viene chiesto il prezzo finale di un singolo articolo, eseguire quel caso. Se vengono richiesti tre importi, verificare tutti e tre.

## Installazione

Per installarla a livello personale, clona il repository e copia la cartella della skill.

```sh
git clone https://github.com/michele-miglio/make-it-simple.git
cd make-it-simple
skills_dir="${CODEX_HOME:-$HOME/.codex}/skills"
mkdir -p "$skills_dir"
if [ -e "$skills_dir/make-it-simple" ] || [ -L "$skills_dir/make-it-simple" ]; then
  echo "La skill esiste già: installazione interrotta."
else
  cp -R -n make-it-simple "$skills_dir/"
fi
```

Apri una nuova conversazione Codex nel progetto in cui vuoi usarla. Per aggiornare un’installazione precedente, esegui `git pull --ff-only` nel clone e confronta il suo `make-it-simple/SKILL.md` con la copia personale. Per passare dalla 1.0.0 alla 1.1.0 basta aggiornare quel file, conservando prima le eventuali personalizzazioni.

## Utilizzo

Puoi descrivere normalmente la modifica oppure scegliere la skill in modo esplicito.

```text
$make-it-simple Correggi questo errore mantenendo la modifica circoscritta.
```
