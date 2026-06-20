# Benchmark neutrale

## Setup

- Scenario condiviso: `neutral_common.json`
- Repeat: `12`
- Tamper rate: `0.02`
- Seed multipli fissi per tutte le versioni
- Profilo v2 fissato a `balanced`
- v3 valutata con training/evaluation separati
- v4-v8 valutate con motore comune avanzato e parametri specifici per versione

## Risultati medi

| Versione | Energy saving % | Delta latenza ms | Success rate | Avg active modules | Integrity failures | Blocked actions | Precision | Recall |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| `v1` | 12.4888 | 0.7410 | 1.0000 | 4.9440 | 1.4000 | 0.0000 | 0.0000 | 0.0000 |
| `v2` | 13.5257 | 0.3746 | 0.9972 | 6.4420 | 1.4000 | 0.2000 | 0.0000 | 0.0000 |
| `v3` | 15.0754 | 0.2769 | 0.9923 | 6.2220 | 0.4000 | 0.2000 | 0.9395 | 1.0000 |
| `v4` | 15.1852 | 0.2769 | 0.9923 | 6.1900 | 0.4000 | 0.2000 | 0.9441 | 1.0000 |
| `v5` | 15.1852 | 0.2769 | 0.9923 | 6.1900 | 0.4000 | 0.2000 | 0.9441 | 1.0000 |
| `v6` | 15.1852 | 0.2769 | 0.9923 | 6.1900 | 0.4000 | 0.2000 | 0.9441 | 1.0000 |
| `v7` | 15.1852 | 0.2769 | 0.9923 | 6.1900 | 0.4000 | 0.2000 | 0.9441 | 1.0000 |
| `v8` | 15.1852 | 0.2769 | 0.9923 | 6.1900 | 0.4000 | 0.2000 | 0.9441 | 1.0000 |

## Nota

Questo benchmark è più neutrale dei singoli run, ma non è ancora una validazione su hardware reale. Le versioni condividono ancora ipotesi di simulazione comuni e quindi il confronto resta corretto come benchmark interno, non come prova finale di ricerca sperimentale.
