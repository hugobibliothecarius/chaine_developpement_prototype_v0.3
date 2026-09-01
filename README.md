## Description
Chaine de développement pour les travaux étudiants de [SIGLE DU COURS]

### Composantes
- README.md
  - Fichier qui décrit le répertoire, ses composantes et son fonctionnement (ce que vous êtes en train de consulter)
- LICENSE.md
  - Contient la description de la licence Creative Commons.
- PULL_REQUEST_TEMPLATE.md (GRILLE_VERIFICATION_ETUDIANT.md)
  - Grille de vérification. Apparait à l'étudiant lors de la soumission pour correction (ouverture de la *pull request*)
- GRILLE-REVISION.md (GRILLE_CORRECTION_ENSEIGNANT.MD)
  - Grille de correction pour l'enseignant. Apparait lors de [...]
- strategie.md (strategie_recherche.md)
  - Gabarit de la stratégie de recherche à compléter par les étudiants dans le cadre du travail demandé.

## Fonctionnement

### Soumission pour correction (Étudiant) - ouverture de la *pull request*
Détecte et refuse si le fichier strategie.MD contient:
  - un matricule à huit chiffres
  - courriel personnel (autre que @umontreal.ca)

Le cas échéant, un avis à l'attention de l'enseignant apparait dans l'onglet *Checks* 

### Approbation (Enseignant) - *merge* de la *pull request*
Produit un PDF, déposé comme *artefact* `paquet-de-depot` dans l'onglet *Actions*. 
La page titre se génère à partir des premières lignes de `strategie.md`. La page titre indique aussi la licence CC BY.
