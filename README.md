# Make It Simple

Una skill per Codex per portare a termine modifiche circoscritte. Invita l’agente a riutilizzare ciò che funziona, intervenire sui punti che servono e verificare il risultato. I controlli di sicurezza e il livello di approfondimento richiesto fanno parte del lavoro. [Leggi le istruzioni della skill](make-it-simple/SKILL.md).

## Esempi

- **Duplicare uno Zap per una nuova campagna.** copia il flusso esistente, aggiorna i campi della campagna e verifica la copia, senza ridisegnare l'automazione.
- **Correggere un errore nelle date.** individua la causa, applica una correzione mirata ed esegui le verifiche pertinenti.

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

Apri una nuova conversazione Codex nel progetto in cui vuoi usarla.

## Utilizzo

Puoi richiamarla direttamente nella richiesta.

```text
$make-it-simple Correggi questo errore mantenendo la modifica circoscritta.
```
