# Sistema operativo neuro-adattivo per l'efficienza energetica

**Autore:** Giacomo Giovetti

Paper concettuale su un'architettura di sistema operativo che usa modelli neurali per ridurre il consumo energetico lungo l'intera catena di esecuzione, dal livello macchina fino al controllo di un braccio robotico.

## Contenuto

- `index.html`: versione principale del paper, adatta anche come pagina iniziale del repository
- `paper-os-neurale.html`: copia del paper con il nome originale
- `prototype/`: primo prototipo eseguibile in `Python`
- `LICENSE`, `LICENSE-CODE`, `LICENSE-DOCS`: struttura di licenza per apertura permanente
- `CITATION.cff`: metadati di citazione del progetto

## Idea centrale

La proposta parte da un principio semplice: un sistema operativo non dovrebbe mantenere attivo un insieme ampio e generico di moduli quando il task corrente ne richiede solo una parte.  
L'architettura descritta nel paper introduce un controllore neurale che osserva il contesto, prevede il `working set funzionale` necessario e suggerisce al kernel quali componenti tenere attivi, pre-caricare o sospendere. Lo stesso metodo viene esteso a un livello di sicurezza complementare, che attesta il percorso esecutivo del task con descrizioni canoniche e `path token` verificabili.

## Stato del lavoro

Questo repository contiene una **proposta architetturale formalizzata**.  
Il testo è pensato come base di ricerca e di discussione tecnica, non come dimostrazione empirica già conclusa.

Al momento il repository contiene soprattutto **documentazione e paper**, ma ora include anche un **primo prototipo eseguibile** che simula il confronto tra una baseline statica e una policy neuro-adattiva.

## Corroborazione attuale

I benchmark interni eseguiti finora portano a una conclusione sobria ma importante: la semplicità architetturale conta più dell'aumento continuo di complessità.

In sintesi:

- `v1` ha mostrato che l'idea è simulabile
- `v2` è emersa come versione più robusta nel compromesso complessivo
- `v3` ha introdotto un apprendimento utile, ma non sempre stabile fuori dai casi favorevoli
- `v4` ha dato un miglioramento solo marginale
- `v5`-`v8` non hanno prodotto vantaggi netti nel benchmark neutrale
- nel benchmark ostile, molte versioni più sofisticate hanno peggiorato energia, latenza e affidabilità

La conclusione provvisoria del progetto è quindi questa: **oltre un certo punto, migliorare il codice aggiungendo solo sofisticazione del modello non produce un avanzamento reale; può invece aumentare fragilità e costo operativo**.

In particolare, il paper:

- definisce il problema energetico in termini di mismatch tra sistema attivo e task reale
- propone un'architettura a strati dal livello macchina al controllo robotico
- colloca l'idea rispetto a `Energy Aware Scheduling`, `seL4`, `Unikraft`, `ROS 2` e controllori ML per l'efficienza energetica
- specifica un protocollo di backtest e validazione sperimentale

## Come leggerlo

Apri direttamente `index.html` in un browser.

Se vuoi servirlo in locale:

```bash
python3 -m http.server 8000
```

Poi visita `http://localhost:8000/`.

## Come provarlo

Per eseguire il primo prototipo:

```bash
python3 prototype/simulate.py
```

Per una simulazione esplicita con export JSON:

```bash
python3 prototype/simulate.py \
  --scenario prototype/scenarios/default_workload.json \
  --repeat 10 \
  --seed 42 \
  --export-json prototype/results.json
```

## Pubblicazione su GitHub

Questa cartella è già organizzata in modo compatibile con un repository Git.

Passi consigliati:

1. crea un nuovo repository su GitHub
2. carica il contenuto di questa cartella
3. imposta `index.html` come pagina iniziale del progetto
4. se vuoi una preview web pubblica, abilita GitHub Pages dalla root del branch principale

## Nota editoriale

Il documento usa un taglio da whitepaper tecnico.  
Se vuoi convertirlo in una forma più accademica, il passo successivo naturale è aggiungere:

- `Introduction`
- `Research questions`
- `Methodology`
- `Experimental setup`
- `Threats to validity`
- `References` in stile accademico coerente

## Licenza

Questo progetto adotta una struttura a doppia licenza, orientata a mantenere il lavoro aperto in modo permanente:

- `LICENSE-CODE`: `AGPL-3.0-or-later` per il codice sorgente presente o futuro
- `LICENSE-DOCS`: `CC BY-SA 4.0` per paper, documentazione e materiali testuali
- `LICENSE`: panoramica breve della politica di licenza del repository

In pratica:

- chi modifica il codice e lo redistribuisce, o lo usa come servizio di rete, deve condividere le modifiche sotto la stessa famiglia di licenza
- chi adatta il paper o la documentazione deve mantenerli condivisibili allo stesso modo
