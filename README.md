# Le bon moment pour braquer

Petite application web (un seul fichier, aucune installation) qui fait comprendre,
en vue de dessus, l'effet de **braquer trop tôt ou trop tard** dans un virage.

## Jouer

Ouvrir `index.html` dans un navigateur, ou la version en ligne si GitHub Pages est activé.

- **↑** accélérer · **↓** freiner · **← →** braquer · **R** recommencer
- Sur mobile : boutons tactiles à l'écran.

## Le principe

Trois repères sur la piste : le **point de braquage** (orange), la **corde / apex**
(rouge), la **sortie** (verte), plus la **trajectoire idéale** en bleu.

Pendant que tu roules, l'appli détecte quand tu commences à tourner et te dit en direct :

- **braquer trop tôt** → tu coupes le virage et tu ressors large ;
- **braquer trop tard** → tu manques la corde et tu pars large aussi ;
- **au bon moment** → tu passes la corde et tu ressors sur la trajectoire idéale.

Détail réaliste : plus tu vas vite, plus la voiture tourne large pour un même
braquage. C'est ce qui fait sentir qu'il faut anticiper le virage.

## Mode démo

Ajouter un paramètre à l'URL pour voir la voiture se piloter seule :

- `index.html?demo=early` → braquage trop tôt
- `index.html?demo=good` → au bon moment
- `index.html?demo=late` → braquage trop tard

## Technique

HTML + Canvas 2D, sans dépendance. Physique de type « modèle vélo » : la rotation
dépend de la vitesse et de l'angle de braquage (rayon de virage constant à braquage constant).
