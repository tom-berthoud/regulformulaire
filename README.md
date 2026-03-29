# Formulaire de regulation automatique

Formulaire LaTeX de revision pour le cours de regulation automatique.

[![Build PDF](../../actions/workflows/build.yml/badge.svg)](../../actions/workflows/build.yml)

## Télécharger le PDF

[**Dernière version compilée (PDF)**](../../releases/latest/download/main.pdf)

## Contenu

- `main.tex` : document principal
- `chapitre1.tex` a `chapitre6.tex` : contenu du formulaire
- `assets/` : ressources PDF et documents de reference

## Compilation locale

```bash
latexmk -pdf -interaction=nonstopmode main.tex
```

Pour nettoyer les fichiers intermediaires :

```bash
latexmk -c
```

## Notes

- Le projet est concu pour tenir sur 6 pages A4 paysage.
- Les fichiers intermediaires LaTeX sont ignores via `.gitignore`.
- Le PDF est compilé et publié automatiquement via GitHub Actions à chaque push.
