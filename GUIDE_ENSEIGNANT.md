# Corriger les remises

*Guide destiné à l'enseignante. Les consignes pour les équipes sont dans le
[README](README.md).*

Tout se fait dans le navigateur. Il n'y a rien à installer et rien à
configurer. Vous n'avez aucune métadonnée à saisir : la page titre, le nom des
fichiers et la licence sont produits automatiquement.

> Les mots en *italique* sont les termes de GitHub. L'interface n'est pas
> traduite en français, alors ils ne le sont pas ici non plus. Le lexique en
> fin de page les explique. Les mots en **gras** sont des boutons à cliquer.

---

## Votre tableau de bord

Allez dans l'onglet **Pull requests**. Chaque équipe y dépose sa remise sous
forme de *pull request*.

Voici trois filtres à coller dans la barre de recherche. Mettez-les en signet,
vous allez les utiliser souvent.

| Filtre | Ce qu'il montre |
|---|---|
| `is:pr is:open review:required` | ce que vous n'avez pas encore regardé |
| `is:pr is:open review:changes-requested` | les équipes qui doivent corriger |
| `is:pr is:open review:approved` | ce que vous avez approuvé, prêt pour le *merge* |

Le premier filtre, c'est votre file de correction.

---

## Commenter

Ouvrez une *pull request*, puis allez dans l'onglet **Files changed**. Passez
la souris sur une ligne, cliquez sur le `+` bleu et écrivez votre commentaire.

**Utilisez `Start a review` et non `Add single comment`.** Avec `Start a
review`, vos commentaires sont regroupés et publiés seulement à la fin. Avec
`Add single comment`, chaque commentaire envoie un avis tout de suite. Sur
vingt équipes, ça fait une grosse différence, autant pour votre boîte de
réception que pour la leur.

---

## Ce que le contrôle automatique ne voit pas

Le *check* attrape les renseignements personnels — matricules, courriels,
téléphones. Il ne juge pas le contenu : ça, c'est votre travail. Et il y a une
chose précise à surveiller, parce qu'elle **passe au vert sans rien signaler**.

**La syntaxe écrite hors du bloc de code.** Les équations et les descripteurs
vont dans le bloc de code de la section 3, et nulle part ailleurs. Si une
équipe en recopie dans le texte courant, l'affichage sur GitHub reste
parfaitement correct — mais le document final perd les symboles. `diabet$`
devient `diabet`, et `diabet*, diabetic*` sort en italique sans ses
astérisques.

Autrement dit : ce que vous évaluez disparaît du seul document archivé, et
rien ne vous prévient. Si vous voyez une équation ou un descripteur dans le
texte courant, demandez le déplacement avec **Request changes**.

C'est la seule vérification de fond que l'automatisation ne peut pas faire à
votre place.

---

## Conclure

Cliquez sur **Submit review**, en haut à droite. Vous avez trois choix :

- **Request changes** — il y a des corrections à faire. L'équipe modifie son
  texte, vous relisez.
- **Approve** — le travail est accepté.
- **Comment** — vous laissez des remarques sans donner de verdict.

Après avoir approuvé, cliquez sur **Merge pull request**. Le document final se
fabrique tout seul, page titre comprise, et la *branch* de l'équipe disparaît.

Faites le *merge* tout de suite après votre approbation, sans attendre.

---

## Récupérer les documents

Sur la page d'accueil du *repository*, dans la colonne de droite, cliquez sur
**Releases** → **Documents finaux**. Vous y trouverez un PDF par équipe, déjà
titré et nommé.

La liste se met à jour toute seule à chaque fois que vous fusionnez une remise.
Vous n'avez rien à lancer, et rien à faire dans l'onglet **Actions**.

> Ces fichiers n'expirent pas. Téléchargez quand même le paquet à la fin de la
> session : c'est votre pièce justificative si une note est contestée, et une
> copie hors GitHub vaut mieux qu'une seule.

---

## Si quelque chose bloque

**Un ✗ rouge apparaît sous une *pull request*.** Le *check* automatique a
trouvé un renseignement personnel : un matricule, un courriel ou un numéro de
téléphone. L'équipe corrige son texte et le *check* repart tout seul. Vous
n'avez rien à faire.

**Un ⚠ jaune apparaît.** C'est un problème de configuration, pas un problème
de l'équipe. Le *merge* n'est pas bloqué. Signalez-le et continuez.

**GitHub affiche « You cannot approve your own pull request ».** C'est une
règle de GitHub, pas un réglage. Faites le *merge* directement.

**Une équipe ne retrouve plus son travail.** Elle est repartie du dossier
`equipes/` au lieu de sa *pull request*. Rien n'est perdu : son texte est sur
sa *branch* et il est visible dans l'onglet **Pull requests**.

**Une équipe a modifié le dossier d'une autre équipe.** Ça se voit dans **Files
changed** : plus d'un fichier apparaît. Demandez la correction avec **Request
changes**. L'historique garde la trace de ce qui s'est passé.

---

## Lexique

| Terme | Ce que ça veut dire |
|---|---|
| *repository* (dépôt) | l'ensemble des fichiers du cours, avec tout leur historique |
| *commit* (enregistrement) | une modification enregistrée, datée et signée. Rien ne s'efface d'un *commit* |
| *branch* (branche) | une ligne de travail en parallèle. Chaque équipe a la sienne |
| `main` | la *branch* officielle, celle qui fait foi. Personne n'écrit dedans directement |
| *pull request* (demande de fusion) | la demande d'intégrer la *branch* d'une équipe dans `main`. C'est sa remise : le travail, la discussion et votre correction sont tous là |
| *review* (révision) | votre lecture commentée, ligne par ligne |
| *merge* (fusion) | l'intégration du travail accepté dans `main`. Vous seule pouvez le faire |
| *check* (contrôle) | une vérification automatique lancée à chaque *commit*. Celui-ci cherche les renseignements personnels |
| *Actions* | le service de GitHub qui exécute les *checks* et fabrique les PDF. Vous n'avez pas à y aller |
| *release* (version publiée) | l'endroit où les PDF sont publiés, dans la colonne de droite de la page d'accueil. N'expire pas |
| *issue* (ticket) | une question posée par une équipe dans l'onglet **Issues** |

---

Pour tout le reste — la configuration, la liste des équipes, le journal
d'exécution, l'entretien — voyez l'administrateur du *repository*.
