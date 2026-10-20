# PICUS - Programma Integrativo Contro Urgenze Sociali

Progetto universitario: analisi e sviluppo incrementale, con Scrum, di un sistema per coordinare Banco Alimentare, OPT ed erogatori.

## Stato

Iterazione 1 - Preparazione (15 ottobre - 5 novembre 2026): analisi, backlog e proposta di MVP. Nessuna implementazione.

## Gruppo

| Nome | Ruolo |
| --- | --- |
| Matteo | [da assegnare] |
| Marco [cognome] | [da assegnare] |
| Ciro Circolo | [da assegnare] |
| Peppe Boccia | [da assegnare] |
| Biagio Landi | [da assegnare] |
| Gagandeep Suman | [da assegnare] |
| Mattia Tartaglia | [da assegnare] |

I ruoli Scrum (Product Owner, Scrum Master) sono definiti in [docs/organizzazione-progetto.md](docs/organizzazione-progetto.md).

## Documentazione

- [Organizzazione del progetto](docs/organizzazione-progetto.md)
- Artefatti di analisi: cartella `docs/`

## Come collaborare

### Branch e Pull Request

- `main` è protetto: nessuno scrive direttamente, si integra solo tramite Pull Request.
- Ogni attività si svolge su un branch dedicato, con nome `<type>/<task-slug>` (per esempio `docs/context-diagram`).
- Una Pull Request richiede almeno **1 approvazione** di un altro membro prima del merge; chi l'ha aperta non approva la propria.
- Collega la Pull Request all'issue corrispondente (`Closes #<numero>`), così l'issue si chiude al merge.
- Commit secondo Conventional Commits (`docs:`, `feat:`, `fix:`, `chore:`), con messaggi brevi e chiari.
- Nei commit e nelle Pull Request non vanno firme o riferimenti automatici di strumenti esterni.

### Label

| Label | Uso |
| --- | --- |
| `epic` | Area funzionale ampia che raggruppa più storie |
| `story` | User Story, dal punto di vista dell'utente |
| `task` | Attività di analisi, documentazione o sviluppo |
| `question` | Domanda da fare al committente |
| `blocked` | Lavoro fermo per un impedimento, da spiegare nell'issue |

Ogni issue ha un solo tipo tra `epic`, `story`, `task` e `question`; `blocked` si aggiunge quando serve e si toglie a impedimento risolto.

### GitHub Project

Il Project è la nostra lavagna Scrum e raccoglie tutte le issue.

- **Stati:** Backlog → Ready → In progress → In review → Done.
- **Campi:** Priority (P1 alta, P2 media, P3 bassa), Ordine (10, 20, 30…), Iteration, Assignees, Milestone.
- **Viste:** Product Backlog (solo `story`, per Ordine), Iterazione corrente (board per stato), Domande al committente (solo `question`).
- Il Product Owner decide l'ordine del backlog; lo Scrum Master cura le iterazioni e gli impedimenti.

### Regole generali

- Le attività si svolgono tutti insieme in sessioni comuni; per ognuna c'è un responsabile che coordina e un revisore che verifica.
- Niente credenziali o dati personali reali in file, issue e commenti: i dati dimostrativi sono fittizi.
- Il dettaglio del lavoro è in [docs/organizzazione-progetto.md](docs/organizzazione-progetto.md).
