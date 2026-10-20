# PICUS - Organizzazione del progetto e scelte del gruppo

Aggiornato al **19 ottobre 2026**. Documento di lavoro del nostro gruppo: raccoglie dominio, organizzazione su GitHub, ruoli e calendario. Le parti da decidere sono segnate esplicitamente. Nessuna scelta tecnologica è stata fatta: l'analisi precede lo stack.

## 1. Dominio e attori

**PICUS (Programma Integrativo Contro Urgenze Sociali)** supporta il Banco Alimentare nel coordinamento delle Organizzazioni Partner Territoriali (OPT), delle misure di accompagnamento e degli erogatori.

- **Banco:** gestisce il centro operativo regionale, riceve le richieste delle OPT, individua un possibile erogatore, ne verifica la disponibilità e coordina l'appuntamento.
- **OPT:** circa 200, distribuite in circa 200 comuni; richiedono servizi e possono offrire misure. Mantengono i contatti con la persona o il nucleo assistito.
- **Operatori / erogatori:** operatori interni al Centro PICUS, professionisti esterni sul territorio oppure operatori o volontari delle OPT che svolgono direttamente alcune attività.
- **Persone assistite:** stakeholder del dominio; i contatti con loro sono in capo all'OPT richiedente.

Il sistema oggi si regge su strumenti e comunicazioni non integrati. Obiettivo della preparazione: comprendere il dominio, ricostruire il processo attuale e trasformare i desiderata informali del committente in un primo Product Backlog ragionato, verificabile e prioritizzato.

Aree funzionali da considerare (non ancora una decomposizione definitiva): account e ruoli, catalogo delle misure, disponibilità degli erogatori, richieste di servizio, appuntamenti, comunicazioni, monitoraggio trimestrale, amministrazione e reporting.

## 2. Architettura software

**Da definire.** Come previsto dalla traccia, stile architetturale, decomposizione in moduli, persistenza, comunicazione, viste architetturali e ADR appartengono alla prima iterazione di costruzione, non alla fase di analisi. Fino ad allora:

- nessuno stack, framework o database è stato scelto;
- gli scenari di qualità, i vincoli e le domande al committente alimenteranno la scelta;
- le decisioni significative verranno motivate tramite ADR.

## 3. Repository e collaborazione

- Repository: **[nome-repo]** sul profilo GitHub di **[username]** (da creare). Link: _da inserire_.
- Branch `main` protetto; lavoro su branch dedicati `<type>/<task-slug>` e integrazione tramite Pull Request con almeno una review di un altro membro.
- Conventional Commits.
- Nessuna credenziale o dato personale reale in file, issue o allegati; eventuali dati dimostrativi sono fittizi.
- Gli artefatti di analisi stanno in `docs/`.

## 4. GitHub Project

Project: **[nome-project]** (link da inserire).

### Label

| Label | Uso |
| --- | --- |
| `epic` | Area funzionale ampia |
| `story` | Funzionalità dal punto di vista dell'utente |
| `task` | Attività di analisi, documentazione o sviluppo |
| `question` | Domanda al committente |
| `blocked` | Impedimento esplicitato nell'issue |

### Campi e stati

- **Status:** Backlog → Ready → In progress → In review → Done.
- **Priority:** P1 - Alta, P2 - Media, P3 - Bassa.
- **Ordine:** numero crescente (10, 20, 30) per ordinare il Product Backlog e consentire inserimenti.
- **Iteration**, **Assignees** e **Milestone** completano la pianificazione.

Gli stati del Project descrivono il lavoro del team; il ciclo di vita delle richieste PICUS è un modello distinto, da definire nell'analisi.

### Viste

| Vista | Layout | Filtro |
| --- | --- | --- |
| Product Backlog | Table | `label:story`, per Ordine crescente |
| Iterazione corrente | Board | iterazione attiva, colonne per Status |
| Domande al committente | Table | `label:question`, priorità alta per prima |

Le viste mostrano gli stessi elementi filtrati: non si duplicano le issue.

## 5. Ruoli del gruppo

| Ruolo | Responsabilità | Chi |
| --- | --- | --- |
| Product Owner | Chiarisce obiettivi e valore, mantiene il backlog e ne definisce l'ordine, risponde alle domande del committente | [da assegnare: Matteo o altro] |
| Scrum Master | Facilita planning ed eventi, fa emergere e rimuove gli impedimenti (può ruotare a ogni iterazione) | [da assegnare] |
| Team | Concorda il lavoro sostenibile, si organizza, produce e revisiona gli output (PO e SM inclusi) | Tutti e 7 i membri |

Membri del gruppo (7): Matteo, Marco Galasso, Ciro Circolo, Peppe Boccia, Biagio Landi, Gagandeep Suman, Mattia Tartaglia.

Le attività si svolgono **tutti insieme** in sessioni di lavoro comuni. Per ogni attività c'è un **responsabile** che coordina e consolida il documento e un **revisore** diverso che lo verifica prima della chiusura.

## 6. Iterazione 1 - Preparazione

Periodo: **15 ottobre - 5 novembre 2026**, con Sprint Review in aula il 5 novembre (10 minuti per gruppo). **Non è richiesta implementazione.**

Milestone: **Iterazione 1 - Preparazione PICUS**, scadenza 5 novembre 2026.

| Codice | Attività | Risultato atteso | Responsabile | Revisore |
| --- | --- | --- | --- | --- |
| P1-01 | Contesto | Stakeholder, obiettivi, confini e Context Diagram | Ciro | Marco |
| P1-02 | Processo as-is | Passaggi di Banco, OPT e operatori; criticità | Mattia | Biagio |
| P1-03 | Processo to-be | Ruoli, responsabilità, stati; miglioramenti motivati | Biagio | Mattia |
| P1-04 | Epic | Aree funzionali coerenti (5-8) | Marco | Peppe |
| P1-05 | User Story | Storie con ruolo, obiettivo, beneficio, Epic, priorità, ipotesi (15-25) | Peppe | Gagandeep |
| P1-06 | Verifica INVEST | Storie suddivise o segnate "da approfondire"; criteri di accettazione dettagliati per almeno 8 | Gagandeep | Matteo |
| P1-07 | Scenari di qualità | 6-10 scenari misurabili (sorgente, stimolo, ambiente, artefatto, risposta, misura) | Ciro | Biagio |
| P1-08 | Open Questions Log | 5-10 domande con motivazione, storie coinvolte e ipotesi provvisoria | Mattia | Peppe |
| P1-09 | Proposta di MVP | 4-7 storie per un flusso end-to-end, motivate | Matteo | Ciro |
| P1-10 | Coerenza e review | Tracciabilità tra artefatti e presentazione da 10 minuti | Matteo | Gagandeep |

I codici P1-xx sono identificativi interni, non i numeri GitHub. Le singole domande dell'Open Questions Log diventano issue con label `question`.

Le iterazioni successive (costruzione) verranno configurate nel Project dopo la review: ogni iterazione parte nella data della review precedente.

## 7. Criteri comuni e fonti

Ogni attività collega il proprio output ai desiderata, cita le fonti, distingue fatti, proposte e ipotesi, mantiene coerenza con gli altri artefatti e prevede una revisione. Le User Story indicano ruolo, obiettivo, beneficio, Epic, criteri di accettazione e dipendenze. Le quantità sono indicazioni della traccia, non quote rigide; il numero di funzionalità da solo non indica qualità.

Fonti: `PICUS.pdf` (traccia del progetto e attività 1-9) e le richieste informali del committente.
