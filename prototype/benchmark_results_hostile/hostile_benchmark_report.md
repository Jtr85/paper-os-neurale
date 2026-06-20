# Benchmark ostile

## Setup

- Scenario ostile: `hostile_common.json`
- Repeat: `1`
- Tamper rate: `0.08`
- Seed multipli fissi per tutte le versioni
- Scenario con phase shift tra training ed evaluation
- Deadline più strette, pattern meno stabili e richieste più rumorose

## Risultati medi

| Versione | Energy saving % | Delta latenza ms | Success rate | Avg active modules | Integrity failures | Blocked actions | Precision | Recall |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| `v1` | -14.5185 | 5.7575 | 0.7800 | 6.0600 | 1.0000 | 0.0000 | 0.0000 | 0.0000 |
| `v2` | 10.4362 | 1.8300 | 0.9500 | 6.9100 | 2.0000 | 0.8000 | 0.0000 | 0.0000 |
| `v3` | -16.1095 | 5.9537 | 0.7428 | 7.3720 | 0.6000 | 0.4000 | 0.8656 | 0.9489 |
| `v4` | -70.3780 | 18.8646 | 0.2286 | 5.8840 | 0.6000 | 0.4000 | 0.9030 | 0.7915 |
| `v5` | -51.5786 | 14.7611 | 0.4286 | 6.3420 | 0.6000 | 0.4000 | 0.8880 | 0.8383 |
| `v6` | -60.5263 | 16.6857 | 0.3429 | 6.1160 | 0.6000 | 0.4000 | 0.8975 | 0.8170 |
| `v7` | -18.4673 | 7.0406 | 0.6286 | 7.0280 | 0.6000 | 0.4000 | 0.8952 | 0.9361 |
| `v8` | -14.6332 | 6.4880 | 0.6571 | 7.1140 | 0.6000 | 0.4000 | 0.8881 | 0.9404 |

## Nota

Questo benchmark è progettato per rompere le assunzioni più favorevoli del benchmark neutrale. Non è ancora hardware reale, ma è utile per vedere quali versioni reggono meglio a cambi di distribuzione, deadline strette e contesto più avverso.
