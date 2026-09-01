## Description

## Fonctionnement

### Soumission pour correction (Étudiant) - ouverture de la *pull request*
Détecte et refuse si le fichier strategie.MD contient:
  - un matricule à huit chiffres
  - courriel personnel (autre que @umontreal.ca)

Le cas échéant, un avis à l'attention de l'enseignant apparait dans l'onglet *Checks* 

### Approbation (Enseignant) - *merge* de la *pull request*
Produit un PDF, déposé comme *artefact* `paquet-de-depot` dans l'onglet *Actions*. 
La page titre se génère à partir des premières lignes de `strategie.md`. La page titre indique aussi la licence CC BY.

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
