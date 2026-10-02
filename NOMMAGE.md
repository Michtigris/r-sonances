# Conventions de nommage

## Classes

| Type  | Signification             | Exemple      |
|-------|---------------------------|--------------|
| `l-`  | Zone de mise en page      | `l-header`   |
| `is-` | État actif ou temporaire  | `is-active`  |
| `t-`  | Thème visuel              | `t-forest`   |

Les composants suivent BEM : `bloc__élément--variante`.

- Bloc : `bouton`
- Élément du bouton : `bouton__icone`
- Variante du bouton : `bouton--principal`

Les noms sont en français, en minuscules et séparés par des tirets. Le JavaScript utilise `data-*`, pas les classes CSS.

## Composants

Codes des pages : `A` Accueil, `P` Programme, `Ar` Artiste, `B` Billetterie, `I` Infos pratiques, `C` Composants.

| Composant       | Pages       | Variantes principales           |
|-----------------|-------------|---------------------------------|
| `bouton`        | A, Ar, B, C | principal, secondaire, contour  |
| `badge`         | P, Ar, C    | scène, statut, compteur         |
| `carte-artiste` | A, P, Ar, C | standard, compacte, horizontale|
| `carte-pass`    | B, C        | journée, trois jours, camping   |
| `champ`         | B, C        | texte, e-mail, sélection, erreur|
| `filtre`        | P, C        | toutes les scènes, sélectionnée|
| `accordeon`     | I, C        | fermé, ouvert                   |
| `bandeau`       | A, Ar, C    | accueil, scène, information     |
| `navigation`    | Toutes, C   | page active, mobile             |
| `bloc-pratique` | I, C        | accès, horaires, sur place      |

## Sass

| Dossier      | Contenu                                      |
|--------------|----------------------------------------------|
| `abstracts/` | Variables et outils Sass                    |
| `base/`      | Reset, typographie et propriétés CSS         |
| `layout/`    | En-tête, pied de page et grilles             |
| `modules/`   | Composants réutilisables                    |
| `state/`     | États des composants                        |
| `theme/`     | Thèmes des scènes et mode sombre            |

Les valeurs sont centralisées dans `scss/abstracts/_variables.scss` et exposées dans `scss/base/_index.scss`. Les points de rupture restent des variables Sass pour les media queries.