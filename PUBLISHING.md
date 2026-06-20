# Pubblicazione rapida su GitHub

Questa cartella è già pronta per essere usata come repository.

## Flusso minimo

```bash
git init
git add .
git commit -m "Initial publication of the neuro-adaptive OS paper"
git branch -M main
git remote add origin <URL-del-repository>
git push -u origin main
```

## Per pubblicare anche la versione web

1. apri il repository su GitHub
2. vai in `Settings` -> `Pages`
3. scegli il branch `main`
4. usa la cartella root `/`
5. salva

GitHub Pages userà `index.html` come pagina iniziale del progetto.

## Nota

Il repository contiene un paper concettuale con basi tecniche e riferimenti, ma non presenta ancora risultati sperimentali definitivi.

## Licenze del repository

Per mantenere il progetto aperto in modo permanente:

- il codice usa `AGPL-3.0-or-later`
- la documentazione usa `CC BY-SA 4.0`

Mantieni visibili anche i file:

- `LICENSE`
- `LICENSE-CODE`
- `LICENSE-DOCS`
- `CITATION.cff`
