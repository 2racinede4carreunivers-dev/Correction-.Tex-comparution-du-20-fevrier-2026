# Guide de dépannage LaTeX

## Erreur : "Paragraph ended before \text@command was complete"

Cette erreur survient généralement lorsqu'il y a un problème avec les accolades ou les symboles mathématiques.

### Causes communes et solutions

#### 1. Accolades manquantes dans les commandes `\text{}`

**Problème :**
```latex
Dans cette configuration, les puissances $n_\text{max$ sont...
```

**Solution :**
```latex
Dans cette configuration, les puissances $n_{\text{max}}$ sont...
```

#### 2. Mode mathématique non fermé

**Problème :**
```latex
Les puissances $n_ sont élevées...
```

**Solution :**
```latex
Les puissances $n$ sont élevées...
ou
Les puissances $n_i$ sont élevées...
```

#### 3. Indices/exposants sans contenu ou mal formés

**Problème :**
```latex
$n_$ ou $n^$ ou $n_\text{max sans accolade}$
```

**Solution :**
```latex
$n_i$ ou $n^2$ ou $n_{\text{max}}$
```

### Comment localiser l'erreur

1. **Regardez le numéro de ligne** : L'erreur indique `[35]` - cherchez autour de la ligne 35
2. **Cherchez les expressions mathématiques** : Utilisez `Ctrl+F` pour chercher `$` dans votre fichier
3. **Vérifiez chaque paire** : Assurez-vous que :
   - Chaque `$` a un `$` de fermeture
   - Chaque `{` a un `}` correspondant
   - Chaque `\text{` se termine par `}`
   - Les indices `_` et exposants `^` ont du contenu

### Checklist de vérification

Pour chaque formule mathématique dans votre document :

- [ ] Les symboles `$...$` sont bien appariés
- [ ] Si vous utilisez `\text{...}`, les accolades sont complètes
- [ ] Les indices `_` ont un contenu : `$x_i$` ou `$x_{indice}$`
- [ ] Les exposants `^` ont un contenu : `$x^2$` ou `$x^{exposant}$`
- [ ] Les accolades `{...}` sont équilibrées

### Exemple correct avec formules mathématiques

```latex
\section{Analyse mathématique}

Dans cette configuration asymétrique chaotique, les puissances $n_{\text{max}}$ 
sont définies par l'équation suivante :

\begin{equation}
    n_{\text{max}} = \sum_{i=1}^{k} n_i^2
\end{equation}

où $n_i$ représente la puissance à l'itération $i$ et $k$ est le nombre 
total d'itérations.
```

### Commandes utiles pour les mathématiques

```latex
% Mode mathématique en ligne
$x^2 + y^2 = z^2$

% Mode mathématique en bloc (centré)
\begin{equation}
    E = mc^2
\end{equation}

% Texte dans les formules
$n_{\text{maximum}}$

% Indices et exposants
$x_i$, $x_{ij}$, $x^2$, $x^{2n+1}$

% Fractions
$\frac{a}{b}$

% Sommes et produits
$\sum_{i=1}^{n} x_i$, $\prod_{i=1}^{n} x_i$
```

## Autres erreurs courantes

### "Undefined control sequence"

Ajoutez les packages nécessaires en haut du document :
```latex
\usepackage{amsmath}  % Pour les formules avancées
\usepackage{amssymb}  % Pour les symboles spéciaux
```

### "Missing $ inserted"

Vous utilisez des commandes mathématiques hors du mode mathématique.
Entourez-les de `$...$` :
```latex
% Incorrect
La variable x_i est définie...

% Correct
La variable $x_i$ est définie...
```

## Ressources

- [Aide sur les formules mathématiques en LaTeX](https://fr.wikibooks.org/wiki/LaTeX/Math%C3%A9matiques)
- [Guide des symboles mathématiques](https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols)
