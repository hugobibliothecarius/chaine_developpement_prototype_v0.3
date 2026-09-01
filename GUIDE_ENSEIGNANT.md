# Guide de l'enseignant

Document interne. À déposer dans le dépôt ou à garder de côté, au choix.

---

## Le principe

**`equipes.yml` est la source unique de vérité.** Vous le remplissez une fois en début de session : sigle du cours, établissement, licence, et la composition des équipes.

Il alimente ensuite tout seul la page titre de chaque PDF, le nom de chaque fichier produit, et les avertissements de cohérence. Vos étudiants n'écrivent aucune métadonnée — c'est ce qui rend le dispositif tenable à vingt équipes.

---

## Avant la session

- [ ] Remplir `equipes.yml` : cours, établissement, session, et les vingt équipes
- [ ] Créer un dossier par équipe sous `equipes/`, avec une copie du gabarit dans chacun
- [ ] Se mettre dans la **bypass list** du ruleset (`Repository admin`)
- [ ] Vérifier que `verification` est marqué **Required** dans une pull request d'essai
- [ ] `Settings → General → Pull Requests` → cocher **Automatically delete head branches**
- [ ] `Settings → Moderation options → Interaction limits` → **Limit to repository collaborators**, six mois
- [ ] Inviter les étudiants avec le rôle **Write**
- [ ] Tester le parcours complet depuis un second compte

### Pourquoi la bypass list

GitHub interdit d'approuver sa propre pull request, et vous êtes le seul code owner. Sans exception à votre nom, vous ne pouvez plus rien fusionner dans votre propre dépôt — pas même un renommage de fichier. Les étudiants ne sont pas administrateurs : la contrainte tient entièrement pour eux.

### Le test depuis un second compte

Non facultatif : votre rôle d'administrateur vous cache exactement ce que vous voulez vérifier, et sans second compte vous ne pouvez pas tester l'approbation.

Créez un compte factice, invitez-le en Write, ouvrez une soumission depuis lui, puis approuvez depuis votre compte principal. Vérifiez au passage :

- l'option de commit direct dans `main` est grisée
- le formulaire de soumission se pré-remplit
- un faux matricule (`20481593`) fait bien échouer le contrôle
- le bouton de fusion reste inactif tant que vous n'avez pas approuvé

---

## Corriger une remise

### Lire et commenter

Onglet **Files changed**. Survolez une ligne, cliquez sur le `+` bleu, écrivez.

**Utilisez toujours `Start a review`, jamais `Add single comment`.** Le premier groupe vos remarques et ne les publie qu'à la fin ; le second envoie une notification à chaque commentaire. Sur vingt équipes, la différence est considérable — pour votre boîte de réception comme pour la leur.

### Conclure

Bouton **Submit review**, en haut à droite de l'onglet Files changed :

| Choix | Quand | Effet |
|---|---|---|
| **Comment** | Remarques sans verdict | Ne débloque pas la fusion |
| **Request changes** | Corrections à faire | Bloque la fusion jusqu'à nouvelle révision |
| **Approve** | Travail accepté | Débloque la fusion |

Puis **Submit review**.

### Fusionner

Une fois approuvée, la soumission se fusionne avec **Merge pull request**. La branche se supprime toute seule, et les PDF se génèrent dans la foulée.

Fusionnez vous-même dans la foulée de l'approbation : le rôle Write permet techniquement à un étudiant de cliquer sur Merge une fois l'approbation donnée.

---

## Récupérer les PDF

Onglet **Actions** → dernière exécution de `document-final` sur `main` → section **Artifacts** → `documents-finaux`.

```
equipe-01_tremblay-nguyen-cote_strategie-de-recherche.pdf
equipe-02_belanger-benali-o-connor_strategie-de-recherche.pdf
```

Le numéro vient du **nom du dossier**, jamais du texte de l'équipe : une erreur de numérotation dans leur document ne fausse pas la nomenclature. Les noms de famille viennent de `equipes.yml`. La date est celle du dernier enregistrement de l'équipe, lue dans l'historique Git.

Une équipe absente de `equipes.yml` ressort en `auteurs-non-indiques`, avec un avertissement jaune dans le journal d'exécution — et un autre, plus tôt, dès la pull request.

> **Les artefacts expirent après 90 jours**, plafond non contournable sur un dépôt public. Téléchargez le paquet en fin de session et archivez-le hors de GitHub : c'est votre pièce justificative en cas de contestation de note.

---

## Suivre l'avancement

L'onglet **Pull requests** est votre tableau de bord. Quelques filtres à mettre en signet :

| Filtre | Ce qu'il montre |
|---|---|
| `is:pr is:open review:required` | Ce que vous n'avez pas encore regardé |
| `is:pr is:open review:changes-requested` | En attente de correction par l'équipe |
| `is:pr is:open review:approved` | Approuvées, prêtes à fusionner |
| `is:pr is:open status:failure` | Contrôle automatique en échec |

Le premier est votre file de correction.

---

## Problèmes courants

**« Le contrôle est rouge et je ne comprends pas. »** Le journal indique le fichier et le numéro de ligne. Cause la plus fréquente : une date écrite `20260915`, que la détection prend pour un matricule. Faites écrire `2026-09-15`.

**Le PDF sort en `auteurs-non-indiques`.** L'équipe manque dans `equipes.yml`, ou ses membres y sont encore sous la forme `Nom, Prénom`. C'est votre fichier, pas le leur : corrigez-le et relancez le workflow depuis l'onglet Actions (`Run workflow`).

**« J'ai ouvert deux soumissions par erreur. »** Fermez la seconde sans la fusionner (**Close pull request**). Le travail reste dans la première. La branche ne se supprime pas toute seule à la fermeture — seulement à la fusion.

**« Je ne retrouve plus mon travail. »** L'étudiant est reparti du dossier `equipes/` au lieu de sa soumission. Rien n'est perdu : son texte est sur sa branche, visible depuis l'onglet Pull requests.

**Une équipe a modifié le dossier d'une autre.** Visible dans Files changed : plus d'un fichier apparaît. Demandez la correction via **Request changes** — l'historique garde la trace.

**Un fichier supprimé par accident.** Rien ne disparaît d'un dépôt Git. Ajoutez le chemin du fichier après `/commits/main/` dans l'URL du dépôt : l'historique reste consultable, et le contenu se récupère depuis le commit précédent.

---

## D'une session à l'autre

`Settings → General → Template repository`. Le bouton **Use this template** crée un dépôt neuf, sans historique partagé : une cohorte par instance, sans traîner les remises de l'an dernier.

Pensez aussi à créer une *Release* étiquetée en fin de session (`v1.0-h27`) : elle fige l'état du dépôt et, contrairement aux artefacts, n'expire jamais.
