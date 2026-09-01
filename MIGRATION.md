# Migration du prototype v0.3 vers le dispositif de production

*Septembre 2026*

Ce document consigne ce qui a changé, et surtout **pourquoi**. Les décisions sont plus utiles que la chronologie : dans un an, la question ne sera pas « qu'est-ce qui a été fait » mais « pourquoi est-ce fait comme ça, et puis-je le changer ».

---

## Point de départ

Le prototype v0.3 comportait :

- un seul `strategie_recherche.md` à la racine
- un workflow unique produisant un PDF et cherchant les renseignements personnels
- une grille de correction et une grille de vérification étudiante
- une licence Creative Commons

Il fonctionnait — pour un seul utilisateur. Trois choses cédaient dès la deuxième équipe.

---

## Décisions de structure

### 1. Un fichier par équipe, pas un fichier partagé

**Constat.** Vingt équipes modifiant le même fichier racine produisent vingt pull requests en conflit les unes avec les autres. Chaque fusion casse les dix-neuf autres.

**Décision.** `equipes/equipe-NN/strategie_recherche.md`. Les pull requests ne se touchent plus jamais.

**Écarté : un dépôt privé par équipe.** Cloisonnement parfait, mais vingt dépôts à administrer, et surtout : la visibilité entre équipes est pédagogiquement voulue. Les étudiants peuvent lire les stratégies des autres et s'en inspirer.

### 2. Dépôt public, pas privé

**Constat.** Les rulesets — la fonction qui ferme `main` à l'écriture directe — ne sont gratuits que sur les dépôts publics. Un dépôt privé exigerait GitHub Pro, Team ou Enterprise, donc une demande de statut enseignant et un délai de vérification.

**Décision.** Public. Cohérent par ailleurs avec la licence CC BY et une visée de dépôt dans Papyrus.

**Conséquences assumées.** Le contrôle des renseignements personnels devient critique plutôt que confortable. Le fork ne peut pas être empêché. La marche arrière est illusoire : repasser en privé ne rappelle ni les copies, ni les caches des moteurs de recherche.

---

## Décisions sur les métadonnées

### 3. `equipes.yml` comme source unique de vérité

C'est la décision qui a le plus réduit le travail de tout le monde, et elle est arrivée en deux temps.

**Première tentative, écartée.** Un en-tête YAML dans le fichier de chaque équipe, contenant noms, date et sigle de cours. Techniquement satisfaisant : pandoc y lisait directement la page titre. Mais il faisait saisir aux étudiants des données administratives — vingt occasions de casser un en-tête, vingt dates à écrire, et un sigle de cours à corriger vingt fois en cas de faute de frappe.

**Décision retenue.** Tout dans un fichier que l'enseignant remplit une fois par session. Il alimente la page titre, le nom des fichiers PDF, et les avertissements de cohérence.

Les étudiants n'écrivent plus **aucune** métadonnée. Leur fichier commence directement à « Question de recherche ».

### 4. Le numéro d'équipe vient du dossier, jamais du texte

Une équipe qui se trompe de numéro dans son document ne fausse pas la nomenclature. Le chemin du fichier fait autorité.

### 5. La date vient de l'historique Git

`git log -1 --format=%ad` sur le fichier précis. C'est la date du dernier enregistrement réel de l'équipe, impossible à antidater dans le texte.

---

## Décisions sur le parcours étudiant

### 6. Pas de renommage de branche

**Écarté.** Une convention `equipe-03/travail-1`, lisible d'un coup d'œil dans la liste des branches.

**Retenu.** Le nom proposé par GitHub, `prenomnom-patch-1`, déjà identifiant. Une consigne de moins, une source d'erreurs de frappe en moins. L'équipe est identifiée par le formulaire de pull request.

### 7. Listes plutôt que tableaux Markdown

Le gabarit comportait quatre tableaux. Aligner un tableau Markdown à la main, dans une zone de texte sans aide à la saisie, est pénible — et un tableau mal aligné casse le rendu.

Des listes structurées portent la même information sans le risque.

### 8. Consignes en commentaires HTML

`<!-- ... -->` n'apparaît ni sur GitHub ni dans le PDF. Les étudiants n'ont plus à supprimer les consignes au fur et à mesure : elles peuvent rester en place sans polluer le rendu.

### 9. Revenir par la pull request, pas par le dossier

Le point le plus contre-intuitif du dispositif, et celui qui génèrera le plus de questions. Le dossier `equipes/` montre la version officielle ; le brouillon en cours vit dans la soumission. Le README détaille le chemin : *Pull requests → Files changed → ⋯ → Edit file*.

---

## Décisions de gouvernance

### 10. Ruleset avec contrôle obligatoire

Le contrôle des renseignements personnels était informatif : il s'affichait dans l'onglet Checks, sans empêcher la fusion. Inscrit dans « Require status checks to pass », il devient bloquant — pour les étudiants comme pour l'enseignant.

### 11. Bypass list : `Repository admin`

**Erreur de conception initiale, corrigée.** La consigne était de laisser la bypass list vide, par principe. Conséquence non anticipée : GitHub interdisant d'approuver sa propre pull request, et l'enseignant étant le seul code owner, il devenait incapable de fusionner quoi que ce soit dans son propre dépôt — pas même un renommage de fichier.

Les étudiants ne sont pas administrateurs : la contrainte tient entièrement pour eux.

### 12. Rôle Write, pas Read

Sans droit d'écriture, un étudiant ne peut pas créer de branche dans le dépôt : GitHub le renverrait vers un fork, détour inutile pour des débutants. Le ruleset reste plus fort que le rôle Write.

---

## Bugs corrigés

### Le contrôle qui ne contrôlait rien

Le workflow examinait `strategie.md`, alors que le fichier s'appelait `strategie_recherche.md`. Sur un fichier introuvable, `grep` renvoie le code 2 : la condition `if` était fausse, la branche d'erreur jamais atteinte, et l'étape déclarée réussie.

Le garde-fou était en place et vert depuis le début. Il n'avait jamais rien examiné.

**Leçon.** Un contrôle qui n'échoue jamais n'est pas rassurant, il est suspect. Testez-le avec une entrée qui doit échouer.

### L'artefact jamais téléversé

`path: paquet\` — la barre oblique inverse, restée d'un copier-coller, était prise au pied de la lettre.

### Les prénoms pris pour des noms de famille

L'extraction prenait le dernier mot de chaque auteur. Avec la convention `Tremblay, Léa`, elle produisait `lea` au lieu de `tremblay`. Les deux conventions sont maintenant acceptées, même mélangées : virgule présente → ce qui la précède ; sinon → le dernier mot.

### Le contre-exemple qui déclenchait le détecteur

Le gabarit portait la consigne `<!-- écrivez 2026-09-15, jamais 20260915 -->`. Huit chiffres consécutifs : le détecteur les a trouvés, dans les vingt fichiers d'un coup.

**Leçon, désormais consignée dans les trois documents d'accompagnement.** La détection lit le fichier brut, commentaires HTML compris. Jamais huit chiffres à la suite, nulle part — pas même pour illustrer ce qu'il ne faut pas écrire.

---

## Limites acceptées

Aucune n'a de solution dans le cadre retenu. Elles sont documentées pour éviter qu'on les redécouvre.

| Limite | Portée | Atténuation |
|---|---|---|
| Rétention des artefacts : 90 jours | Plafond des dépôts publics, non contournable | Télécharger en fin de session, ou passer par une *Release* |
| Le fork ne peut pas être empêché | Propre aux dépôts publics | Aucune. À assumer avant d'ouvrir le dépôt |
| Le rôle Write donne accès à tout le dépôt | GitHub n'offre pas de permission par dossier | La pull request rend toute intrusion visible ; l'historique la rend traçable |
| Un étudiant peut fusionner après approbation | Propre au rôle Write | Fusionner soi-même dans la foulée de l'approbation |
| Consentement et Loi 25 | Travail évalué, publié, hébergé aux États-Unis | Comptes pseudonymes autorisés, adresses courriel masquées, voie de remise non publique pour qui refuse |

---

## Écarté d'emblée

**GitHub Classroom.** L'outil conçu exactement pour ce scénario a été retiré le 28 août 2026 — quatre jours avant cette migration. Site et API décommissionnés. Deux partenaires reprennent ses fonctions si l'autocorrection devient un besoin : Codio, et Classroom 50.

**Un dépôt par équipe.** Voir décision 1.

**Signature GPG des commits.** Le ruleset l'offre. Insurmontable pour un cours non technique.

---

## État au terme de la migration

Fonctionnel et vérifié : ruleset actif, contrôle bloquant, vingt dossiers d'équipe, chaîne de production des PDF validée de bout en bout.

Reste au peuplement : noms réels dans `equipes.yml`, invitation des étudiants avec le rôle Write, et un test complet depuis un second compte — le seul angle mort restant, puisque le statut d'administrateur montre une interface que les étudiants ne verront jamais.

---

## Pour la suite

Le nom du dépôt porte encore son numéro de version. Les étiquettes Git et les *Releases* font ce travail mieux, et l'URL cesse alors de changer à chaque itération. Le moment de renommer est celui du transfert vers une organisation.

`Settings → General → Template repository` permettra ensuite une instance neuve par cohorte, sans traîner les remises de l'année précédente.
