# Trousse de test — dépôt d'une stratégie de recherche

Dépôt d'essai pour vérifier, en une demi-journée, que la chaîne
GitHub → Papyrus tient debout. Contenu fictif, aucun travail étudiant réel.

Cinq fichiers, aucun YAML, aucun script. L'étudiant ne rédige que
`strategie.md` ; il saisit ensuite ses métadonnées directement dans le
formulaire de dépôt de Papyrus.

## Mise en place

Le dépôt doit être **public** : sur un compte gratuit, la protection de
branche et les minutes d'exécution ne le sont que là — et il n'y a rien de
confidentiel ici.

**1. Glissez tous les fichiers visibles de ce dossier** dans
*Add file → Upload files*, puis *Commit changes*.

**2. Créez ensuite le seul fichier caché**, à la main. Ce chemin est imposé
par GitHub : les chaînes ne sont lues que dans `.github/workflows/`.

*Add file → Create new file*, et tapez dans la case du nom :

    .github/workflows/paquet.yml

Les barres obliques créent les dossiers. Collez le contenu de
`paquet.yml.txt`, puis *Commit changes*.

> Ne tentez pas de glisser un dossier commençant par un point : le Finder
> le masque, `Cmd+A` ne le sélectionne pas, et il sera silencieusement omis.
> Taper le chemin contourne le problème.

## Ce que la chaîne fait

Deux choses, à deux moments différents.

**À l'ouverture d'une demande de fusion, et à chaque fusion** — elle refuse le
document si un matricule à huit chiffres ou un courriel nominatif y traîne.
Le signal apparaît donc dans l'onglet *Checks* avant que l'enseignante ne lise
le travail : le garde-fou prévient au lieu de constater. Aucun formulaire ne
le remplace.

**À la fusion seulement** — elle produit un PDF uniforme, déposé comme artefact
`paquet-de-depot` dans l'onglet Actions. La page de titre vient des premières
lignes de `strategie.md` : c'est le seul endroit visible où la licence
apparaîtra, la notice Papyrus ne comportant pas de champ de licence.

Un document refusé échoue en quelques secondes, l'installation de LaTeX n'ayant
pas lieu.

Elle ne produit plus de fiche de métadonnées : l'étudiant remplit la notice
directement dans Papyrus.

## Protocole

1. **Test 1 — correction.** Modifier une ligne de l'équation dans
   `strategie.md`, en choisissant *Create a new branch and start a pull
   request*. Vérifier que la liste de vérification s'affiche d'elle-même,
   cocher les cases **après** la création de la pull request, commenter une
   ligne précise dans l'onglet *Files changed*, puis fusionner.
2. **Test 2 — la chaîne.** À la fusion, onglet Actions : télécharger
   l'artefact et vérifier le PDF, page de titre comprise.
3. **Test 3 — le garde-fou.** Écrire un faux matricule à huit chiffres dans
   `strategie.md`. L'exécution doit échouer, avec un X rouge à l'étape
   « Refuser les renseignements personnels » et le message en français dans les
   annotations du résumé — sans avoir à ouvrir les journaux.
4. **Test 4 — Papyrus.** Ouvrir une notice existante de la collection
   Production étudiante, cliquer le connecteur Zotero : la référence et le
   PDF sont-ils captés ? Puis remplir le formulaire de dépôt jusqu'à
   l'étape de la licence, sans soumettre.

## La question qui décide

Le *diff* ligne par ligne — tout l'intérêt de git ici — fonctionne sur du
texte brut. Il ne fonctionne pas sur un fichier Word, et pas du tout sur un
Excel. Les équipes remettent aujourd'hui du Word ou de l'Excel.
**Accepteront-elles d'écrire l'équation en texte brut ?** Si la réponse est
non, git perd l'essentiel de son avantage.

## Ce qui ne se transpose pas vers GitLab

Les concepts, oui : pull request ↔ merge request, Actions ↔ CI, gabarit de PR
↔ gabarit de MR. Le fichier de chaîne devra être réécrit en `.gitlab-ci.yml`
à la racine — également un fichier caché. Considérez-le comme jetable.
