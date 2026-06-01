# Formulaire de regulation automatique

Formulaire LaTeX de revision pour le cours de regulation automatique.
Format dense : A4 paysage, 3 colonnes, boites `tcolorbox` coloriees par chapitre.

[![Build PDF](../../actions/workflows/build.yml/badge.svg)](../../actions/workflows/build.yml)

## Télécharger le PDF

[**Dernière version compilée (PDF)**](../../releases/latest/download/main.pdf)

## Contenu

- `main.tex` : document principal (préambule, macros, gestion des versions)
- `chapitre1.tex` … `chapitre6.tex` : contenu du formulaire
- `assets/` : ressources PDF et documents de référence (notes de cours, énoncés)

### Chapitres

| # | Titre | Sujet |
|---|-------|-------|
| 1 | Introduction & Modélisation | pôles, gain statique/permanent, ordre/type |
| 2 | Laplace & Fonctions de transfert | transformées, théorèmes, retard pur |
| 3 | Systèmes 1ᵉʳ et 2ⁿᵈ ordre | réponses temporelles, dépassement, ζ/ωₙ |
| 4 | Réponse fréquentielle & Bode | tracé asymptotique, Nyquist, réponse harmonique |
| 5 | Stabilité & Marges | critère du revers, marges de gain/phase |
| 6 | Régulateurs & Boucle fermée | P/I/PI/PD/PID, compensation pôle-zéro, synthèse fréquentielle |

## Versions

Deux versions sont sélectionnées par un flag dans `main.tex` :

| Version | Chapitres | Flag dans `main.tex` |
|---------|-----------|----------------------|
| **Te1** | 1–4 (modélisation + Bode) | `\TEtrue` |
| **Full** | 1–6 (couvre le cours ch.1 à 8) | `\TEfalse` *(défaut actuel)* |

Pour changer de version, modifier la ligne dans [main.tex](main.tex) :

```latex
\TEtrue   % version Te1 (chapitres 1–4)
% ou
\TEfalse  % version complète (chapitres 1–6)
```

## Compilation locale

```bash
latexmk -pdf -interaction=nonstopmode main.tex
```

Pour nettoyer les fichiers intermediaires :

```bash
latexmk -c
```

## Notes

- La version complète est conçue pour tenir sur **6 pages** A4 paysage.
- Les fichiers intermediaires LaTeX sont ignores via `.gitignore`.
- Le PDF est compilé et publié automatiquement via GitHub Actions à chaque push.
