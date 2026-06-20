# Sistema operativo neuro-adattivo per l'efficienza energetica

**Autore:** Giacomo Giovetti

Paper concettuale su un'architettura di sistema operativo che usa modelli neurali per ridurre il consumo energetico lungo l'intera catena di esecuzione, dal livello macchina fino al controllo di un braccio robotico.

## Idea centrale

La proposta parte da un principio semplice: un sistema operativo non dovrebbe mantenere attivo un insieme ampio e generico di moduli quando il task corrente ne richiede solo una parte.
L'architettura descritta nel paper introduce un controllore neurale che osserva il contesto, prevede il `working set funzionale` necessario e suggerisce al kernel quali componenti tenere attivi, pre-caricare o sospendere.

## Stato del lavoro

Questo repository contiene una proposta architetturale formalizzata.
Il testo è pensato come base di ricerca e di discussione tecnica, non come dimostrazione empirica già conclusa.

Al momento il repository contiene soprattutto documentazione e paper, non ancora una base codice eseguibile del sistema operativo.

## Licenza

Questo progetto adotta una struttura a doppia licenza, orientata a mantenere il lavoro aperto in modo permanente:

- `LICENSE-CODE`: `AGPL-3.0-or-later` per il codice sorgente presente o futuro
- `LICENSE-DOCS`: `CC BY-SA 4.0` per paper, documentazione e materiali testuali
- `LICENSE`: panoramica breve della politica di licenza del repository
