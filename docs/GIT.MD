# GIT

## Introduzione

**Git** è un sistema di _controllo di versione distribuito, o "versioning"_, che consente agli sviluppatori di tenere traccia delle modifiche apportate al codice sorgente nel tempo. Git è progettato per gestire progetti di sviluppo software in modo efficiente, permettendo a più persone di lavorare contemporaneamente senza conflitti. La sua principale funzione è quella di **registrare ogni modifica al codice**, consentendo di **tornare "indietro nel tempo", ovvero a versioni precedenti** se necessario e facilitando la collaborazione tra team.

## Caratteristiche e Utilizzo di Git

- **Versionamento**: Git tiene una cronologia dettagliata delle modifiche, permettendo agli sviluppatori di sapere chi ha fatto cosa e quando. Questo è fondamentale per gestire progetti complessi dove più sviluppatori possono apportare modifiche simultaneamente.
- **Collaborazione**: Grazie a Git, diversi membri di un team possono lavorare su rami separati del progetto (chiamati branch) e successivamente unire le loro modifiche nel codice principale. Questo processo aiuta a evitare conflitti e a mantenere il codice organizzato.
- **Backup e Ripristino**: Ogni copia di un repository Git è un backup completo, il che significa che in caso di problemi, gli sviluppatori possono facilmente ripristinare versioni precedenti del codice.
- **Strumenti Avanzati**: Git offre funzionalità come il branching e il merging, che permettono di testare nuove idee senza influenzare il codice stabile. Le modifiche vengono registrate attraverso operazioni chiamate commit, ognuna delle quali rappresenta uno stato specifico del progetto.

## Guida al primo utilizzo di Git

### Download software Git

La prima cosa da fare è scaricare ed installare Git dal sito originale: [https://git-scm.com/downloads](https://git-scm.com/downloads)

### Creazione di una Repository Locale

Per iniziare a utilizzare Git in un progetto, il primo passo è **creare una repository locale**. Questo processo è semplice e può essere realizzato seguendo questi passaggi:

1. **Creare una Nuova Cartella**: Crea una nuova directory per il tuo progetto.
2. **Accedere alla Cartella**: Apri il terminale e naviga nella directory appena creata.
3. **Inizializzare la Repository**: Esegui il comando:
   ```bash
   git init
   ```
   Questo comando crea una sottodirectory `.git`, che contiene tutti i file necessari per la gestione della repository.
4. **Aggiungere File**: Aggiungi i file al tuo progetto utilizzando:
   ```bash
   git add <nome_file>
   ```
5. **Commettere le Modifiche**: Effettua il primo commit con:
   ```bash
   git commit -m "Primo commit"
   ```

Se stai lavorando su un progetto esistente, puoi semplicemente navigare nella cartella del progetto e ripetere i passaggi 3-5.

### Creazione di una Repository Online su GitHub

Dopo aver creato una repository locale, puoi anche **pubblicarla online su GitHub** per condividerla e collaborare con altri. Ecco come fare:

1. **Accedi a GitHub**: Vai su GitHub e accedi al tuo account.
2. **Creare una Nuova Repository**: Clicca sul pulsante "New" in alto a destra.
3. **Compilare i Dettagli della Repository**:
   - Assegna un nome alla tua repository.
   - Aggiungi una descrizione (opzionale).
   - Scegli la visibilità (pubblica o privata).
   - Poi puoi anche decidere di inizializzarla con un file README o un file `.gitignore`.
4. **Creare la Repository**: Clicca su "Create repository".

### Collegamento della Repository Locale a GitHub

Una volta creata la repository online, puoi collegarla alla tua repository locale:

1. **Imposta l'URL Remoto**:
   ```bash
   git remote add origin https://github.com/username/nome_repository.git
   ```
2. **Pubblica le Modifiche**:
   ```bash
   git push -u origin master
   ```

Questi passaggi ti permetteranno di avere una repository locale sincronizzata con quella online, facilitando la collaborazione e la gestione del codice sorgente.

## Comandi Git

### Merge Commit

**Definizione**: Un _merge commit_ è un tipo di commit che viene creato quando si uniscono due branch. Esso include i commit precedenti all'apice della cronologia e aggiunge un ulteriore commit che rappresenta l'unione.

### Squash Commit

**Definizione**: Con il _squash commit_, i commit vengono uniti, ma non viene creato un ulteriore commit come nel caso del merge. Questo metodo è utile per mantenere una cronologia più pulita.

### Git Rebase

**Funzione**: Il comando `git rebase` concatena i nuovi commit e li inserisce sempre alla cima della cronologia. A differenza del merge, il rebase cambia la storia dei commit, rendendo la cronologia lineare.

### Comandi Fondamentali

- **Switching Branch**:
  - `git switch main`: Torna al branch principale.
  - `git merge nomebranch`: Unisce il branch specificato nel branch principale.
- **Visualizzazione Differenze**:
  - `git diff nomefile`: Mostra le modifiche apportate a un file.
  - `git diff <ascii_commit>`: Mostra le differenze rispetto a un commit specifico.

### Rebase Interattivo

**Comando**:

```bash
git rebase -i <commit_ascii>
```

Avvia una sessione di rebase interattivo, dove si possono modificare i commit.

**Comandi Utilizzabili**:

- `pick`: Mantiene il commit.
- `squash`: Unisce il commit con quello precedente.
- `fixup`: Simile a squash, ma non permette di modificare il messaggio del commit.
- `reword`: Cambia il messaggio del commit.

### Modifica dell'Ultimo Commit

**Comando**:

```bash
git commit --amend
```

Aggiunge il commit più recente al precedente, permettendo di cambiare il messaggio.

```bash
—no-edit—
```

Mantiene il titolo del commit senza modificarlo.

### Cherry-pick

**Funzione**: Utilizzato per prendere un commit specifico da un branch e spostarlo in un altro (ad esempio nel main) con il comando:

```bash
git cherry-pick <ascii_commit>
```

### Stashing delle Modifiche

**Comandi**:

- `git stash`: Mettere da parte le modifiche correnti.
- `git stash apply`: Riapplica le modifiche stashed.
- `git stash push -m <nome>`: Rinomina uno stash.
- `git stash list`: Mostra la lista degli stash.

```

```
