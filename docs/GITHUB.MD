# GITHUB

## GitHub: Funzionalità e Gestione dei Progetti

**GitHub** è una piattaforma di hosting per repository Git che supporta la collaborazione tra sviluppatori. Fornisce strumenti utili per lavorare su progetti, tracciarne le versioni e organizzare il lavoro in team.

## Repository e Organizzazione dei File

- **Repository**: Contenitore del progetto dove vengono salvati i file e le cronologie delle modifiche.
- **Branch**: I branch permettono di sviluppare nuove funzionalità senza interferire con il codice principale (tipicamente il branch `main` o `master`).
- **README.md**: File Markdown di descrizione del progetto visualizzato nella pagina principale del repository; ottimo per includere una panoramica, istruzioni e documentazione di base.
- **LICENSE**: File che specifica le condizioni di licenza del codice.
- **.gitignore**: File che definisce quali file o cartelle escludere dal repository (ad es., dati sensibili o file di sistema).

## Strumenti per la Collaborazione

- **Fork**: Copia di un repository nel proprio account GitHub, usata spesso per contribuire a progetti open source. È possibile fare modifiche nel fork e poi proporre l’integrazione nel repository originale tramite una pull request.
- **Pull Request**: Richiesta per unire il codice da un branch a un altro (spesso da una copia fork al repository originale). Le pull request consentono di discutere le modifiche, ottenere feedback e fare revisioni prima dell’integrazione.
- **Actions**: Strumento per configurare e automatizzare workflow come Continuous Integration (CI) e Continuous Deployment (CD). Con le Actions, è possibile automatizzare test, build e distribuzione del codice.

## Gestione delle Attività con Issues e Projects

- **Issues**: Segnalazioni usate per tracciare bug, miglioramenti e nuove funzionalità. Ogni issue può avere una descrizione, assegnatari, label e milestone per organizzarla al meglio.
- **Labels**: Etichette che categorizzano le issues (ad esempio, `bug`, `enhancement`, `help wanted`) per migliorarne la visibilità e priorità.
- **Milestones**: Obiettivi con una scadenza per un gruppo di issues; molto utili per pianificare rilasci.
- **Projects**: Strumenti di gestione visiva delle task che funzionano come un kanban board (con colonne `Backlog`, `To Do`, `In Progress`, ecc.). Utili per coordinare il lavoro di team e tenere traccia dello stato di avanzamento.

## Gestione del Codice e Revisione

- **Code Review**: Strumento di GitHub per controllare il codice proposto nelle pull request. È possibile lasciare commenti, richiedere modifiche o approvare le modifiche proposte da altri collaboratori.
- **Protezione dei Branch**: Impostazione che richiede il completamento di determinate condizioni prima che un branch possa essere modificato (ad es., approvazione delle pull request, superamento dei test automatizzati).
- **Template per Issues e Pull Requests**: Modelli preimpostati per creare issues e pull request, aiutano a mantenere un formato uniforme e una comunicazione chiara. Si creano file `.md` in una cartella chiamata `.github`.

### Versionamento e Rilasci

- **Tagging e Releases** - I tag permettono di “bloccare” un particolare commit con un nome specifico (ad es., `v1.0.0`). Con i tag, si possono creare “releases” per segnare versioni stabili del progetto, con allegati (es. binari, pacchetti) e note di rilascio.
- **Semantic Versioning (SemVer)** - Standard di versionamento usato per indicare il tipo di cambiamento in una versione (`major.minor.patch`).

### Comunicazione e Documentazione

- **Wiki** - Ogni repository ha una sezione Wiki per creare una documentazione più estesa e strutturata rispetto al README.
- **GitHub Discussions** - Strumento per gestire conversazioni e discussioni più informali all'interno del repository, spesso utilizzato per richieste di funzionalità, domande generali o brainstorming.
- **GitHub Pages** - Servizio di hosting per pubblicare pagine web direttamente da un repository GitHub. Utile per creare documentazione o siti web per progetti open source.

### GitHub e le Piattaforme Cloud

GitHub è spesso utilizzato in combinazione con piattaforme cloud come:

- **GitHub Actions** - Permette di automatizzare il deploy su cloud come **AWS**, **Azure** e **Google Cloud**.
- **Integrazione CI/CD** - Con GitHub Actions, puoi configurare flussi di lavoro per test e deploy automatici, collegando GitHub al cloud provider che preferisci.

### Best Practices per GitHub

1. **Usa i Branch per lo Sviluppo**: Crea branch separati per le nuove funzionalità e per risolvere i bug.
2. **Scrivi Commit e Pull Request Chiari**: Usa messaggi chiari e dettagliati per spiegare le modifiche.
3. **Crea Issues per Ogni Task**: Traccia ogni lavoro come issue e aggiorna il loro stato per favorire la trasparenza.
4. **Configura le Pull Request con Revisioni e Approvi**: Usa le review per controllare la qualità del codice.
5. **Usa le GitHub Actions per Automatizzare i Test**: Automatizza i test per rilevare rapidamente problemi nel codice.
6. **Aggiorna la Documentazione**: Mantieni README, Wiki e altre documentazioni allineate allo stato del progetto.

---

GitHub fornisce strumenti potenti per gestire il ciclo di vita del progetto, automatizzare workflow e collaborare efficacemente in team. Utilizzare questi strumenti consente una gestione del codice più ordinata, una comunicazione fluida e un’integrazione continua.

---

### 1. Repository e Gestione dei File su GitHub

#### Creazione e Struttura di un Repository

- **Repository pubblico vs. privato**: Puoi creare repository pubblici (visibili a tutti) o privati (accessibili solo a te e agli utenti autorizzati). I repository privati sono utili per progetti interni o in fase di sviluppo.
- **Template repository**: Puoi usare un repository come modello per crearne altri con la stessa struttura, molto utile per progetti che richiedono configurazioni simili.

#### .gitignore

- **File .gitignore**: File che indica a Git quali file o cartelle ignorare. È particolarmente utile per escludere file di sistema, dati sensibili o file di configurazione locale.

#### Branches e Workflows

- **Branches per Ambienti di Lavoro**: Oltre ai branch di sviluppo (`develop`) e al branch principale (`main` o `master`), è possibile creare branch per ambienti specifici come `staging` e `production`, per differenziare il codice in base al livello di maturità.
- **Branch Protection Rules**: Le regole di protezione dei branch ti permettono di configurare restrizioni (es. approvazioni multiple, check CI superati) per garantire che solo il codice di qualità venga unito al branch protetto (di solito `main` o `master`).

### 2. Strumenti di Collaborazione GitHub

#### Forking e Contributi

- **Fork**: Una copia di un repository che puoi modificare liberamente. Utilizzata per contribuire a progetti open source, specialmente quando non si ha accesso in scrittura al repository originale.
- **Contributing Guidelines**: Puoi aggiungere un file `CONTRIBUTING.md` nel repository, con le linee guida per chi desidera contribuire. Questo file aiuta a standardizzare il processo di contribuzione, spiegando come fare le pull request e segnalare i problemi.

#### Code Owners

- **CODEOWNERS**: Un file speciale che assegna automaticamente revisori a determinate parti del codice. Ad esempio, i membri responsabili di una specifica area del progetto (come il frontend o il backend) vengono notificati automaticamente quando vengono proposte modifiche a quella parte di codice.

#### GitHub Discussions e Community Engagement

- **Discussions**: Uno spazio per comunicazioni informali all'interno del repository. È ideale per domande aperte, brainstorming e interazioni non legate a problemi specifici.
- **Sponsor e Donazioni**: Con GitHub Sponsors, sviluppatori e team open source possono ricevere donazioni per sostenere i loro progetti, creando una fonte di finanziamento per il lavoro di sviluppo gratuito.

### 3. Issues, Labels e Milestone: Gestione delle Attività

#### Issues

- **Creazione e Organizzazione**: Le issues sono segnalazioni utilizzate per registrare problemi, richieste di miglioramento o attività specifiche. Ogni issue ha un titolo, una descrizione, assegnatari e può avere delle **label**.
- **Link alle Pull Request**: È possibile collegare un issue a una pull request specifica. Una volta che la pull request è chiusa, l’issue viene automaticamente chiusa se viene usato un termine come "Fixes #numero_issue".

#### Labels

- **Tipologie di Labels**: GitHub fornisce alcune etichette di base (`bug
