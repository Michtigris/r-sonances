# Maquette Figma — Festival Résonances (export pour Claude)

Ce dossier remplace l'accès au fichier Figma. Tout a été extrait du `.fig` d'origine.

## Contenu
- `screens/*.png` — **capture de chaque frame** (1440px de large). C'est la référence visuelle : à regarder en premier pour chaque page.
- `pages/*.md` — **spec détaillée de chaque frame** : arborescence des calques (noms BEM d'origine), texte exact, police/taille/graisse, couleurs hex, bordures, rayons, positions et dimensions.
- `tokens.css` — variables CSS du guide visuel (couleurs, scènes, typo, espacements, rayons).
- `images/` — photos utilisées, nommées d'après l'artiste ou l'usage (`hero.jpg`, `lune-rousse.jpg`…). Crédits dans `pages/00_-_Guide_visuel.md`.

## Pages
| Frame | Capture | Spec |
|---|---|---|
| 00 · Guide visuel | screens/00_-_Guide_visuel.png | pages/00_-_Guide_visuel.md |
| 01 · Accueil | screens/01_-_Accueil.png | pages/01_-_Accueil.md |
| 02 · Programme | screens/02_-_Programme.png | pages/02_-_Programme.md |
| 03 · Fiche artiste | screens/03_-_Fiche_artiste.png | pages/03_-_Fiche_artiste.md |
| 04 · Billetterie | screens/04_-_Billetterie.png | pages/04_-_Billetterie.md |
| 05 · Infos pratiques | screens/05_-_Infos_pratiques.png | pages/05_-_Infos_pratiques.md |
| 06 · Composants | screens/06_-_Composants.png | pages/06_-_Composants.md |

## Comment lire les specs
- `**nom-du-calque** [frame] L×H @(x,y)` : un bloc. Les noms suivent du BEM (`card card--headliner theme-lake`, `button button--primary`, `l-grid`, `l-header`…) → **réutiliser ces noms comme classes CSS**.
- `shape L×H @(x,y) fill:… border:… radius:…` : le fond/bordure du bloc parent (= son `background`, `border`, `border-radius`).
- `TEXT "…" — Inter 700 16px/… #hex` : texte exact à reprendre mot pour mot.
- `@(x,y)` = position absolue dans la page de 1440px. Sert à déduire marges, paddings et gaps (ex. conteneur à x=120 → largeur 1200px centrée).
- `image:xxx.jpg` = photo dans `images/` (en `object-fit: cover`).

## À savoir
- La maquette est en positionnement absolu (pas d'auto-layout) : **construire en flex/grid**, ne pas recopier les coordonnées en `position: absolute`.
- Les interlignes et graisses de référence sont celles du guide visuel (`tokens.css`), pas le « normal » des specs. Le titre principal est en graisse 800.
- Les bordures sont « intérieures » dans Figma : un `radius:7px` sur une bordure 2px correspond au `--radius-sm` (6px).
- Un bouton « Mode sombre » est prévu dans le header ; aucune maquette du thème sombre n'est fournie.
- Maquette desktop uniquement (1440px) : le responsive est à concevoir.
