# Correction LaTeX - Comparution du 20 février 2026

Ce dépôt contient le document LaTeX pour la comparution prévue le 20 février 2026.

## Fichier principal

- `comparution_20_fevrier_2026.tex` : Document principal de la comparution

## Structure du document

Le document est organisé en sections :
1. **Page de titre** : Informations générales sur la comparution
2. **Objet de la comparution** : Description de l'objet
3. **Parties présentes** : Liste des parties impliquées
4. **Contexte et faits** : Description détaillée du contexte
5. **Arguments présentés** : Positions des différentes parties
6. **Documents et preuves** : Liste des pièces justificatives
7. **Décisions et conclusions** : Résultats de la comparution
8. **Prochaines étapes** : Actions à venir

## Comment compiler le document

### Avec pdflatex

```bash
pdflatex comparution_20_fevrier_2026.tex
```

### Avec latexmk (recommandé)

```bash
latexmk -pdf comparution_20_fevrier_2026.tex
```

Pour nettoyer les fichiers auxiliaires :

```bash
latexmk -c
```

## Prérequis

- Une distribution LaTeX (TeX Live, MiKTeX, etc.)
- Les packages LaTeX suivants :
  - `inputenc` (encodage UTF-8)
  - `fontenc` (encodage des polices)
  - `babel` (support du français)
  - `geometry` (mise en page)
  - `setspace` (espacement)
  - `fancyhdr` (en-têtes et pieds de page)
  - `enumitem` (listes personnalisées)

## Instructions

1. Remplissez les sections marquées `[À compléter]` dans le document
2. Ajoutez le contenu spécifique à votre comparution
3. Compilez le document pour générer le PDF
4. Vérifiez le résultat et ajustez la mise en forme si nécessaire

## Ressources

### En cas d'erreur de compilation

Consultez le fichier [TROUBLESHOOTING.md](TROUBLESHOOTING.md) pour les solutions aux erreurs courantes, notamment :
- "Paragraph ended before \text@command was complete"
- "Undefined control sequence"
- "Missing $ inserted"

### Documentation LaTeX

Pour plus d'informations sur LaTeX :
- Documentation LaTeX officielle : https://www.latex-project.org/
- Guide de rédaction en français : https://fr.wikibooks.org/wiki/LaTeX