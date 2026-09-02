# Nom du cours — Travaux d'équipe

Tout se fait dans le navigateur. Il n'y a rien à installer et aucune ligne de
commande à taper.

**Vous n'avez aucune information administrative à saisir.** Vos noms, le sigle
du cours, la date et la licence sont ajoutés automatiquement à la page titre du
document final. Vous rédigez, c'est tout.

> Les mots en *italique* sont les termes de GitHub. L'interface n'est pas
> traduite en français, alors ils ne le sont pas ici non plus. Le lexique en
> fin de page les explique. Les mots en **gras** sont des boutons à cliquer.

---

## Une seule fois, avant de commencer

**Rendez votre adresse courriel privée.** Cliquez sur votre photo en haut à
droite → **Settings** → **Emails**, puis cochez **Keep my email addresses
private**.

Sans ce réglage, votre adresse personnelle apparaît publiquement dans
l'historique du *repository*, et on ne peut plus corriger un *commit* déjà
fait. Faites-le avant votre première contribution.

---

## Remettre un travail

### 1. Ouvrir le fichier de votre équipe

`equipes/` → votre dossier → `strategie_recherche.md`

C'est le seul fichier que vous modifiez. Ne touchez pas au dossier d'une autre
équipe : la modification apparaîtrait dans l'historique et votre remise serait
refusée.

### 2. Cliquer sur le crayon

L'icône ✏️ en haut à droite du fichier ouvre l'éditeur. L'onglet **Preview**
vous montre le rendu.

### 3. Rédiger

Les blocs `<!-- ... -->` sont des consignes. Ils n'apparaissent ni sur GitHub
ni dans le document final. Laissez-les, ils ne dérangent personne.

**Toute syntaxe d'interrogation va dans un conteneur**, et il y en a deux.

L'historique de recherche va dans un **bloc de code** — les trois accents
graves ```` ``` ````, déjà en place dans le gabarit. À l'intérieur, rien n'est
interprété : vos troncatures, astérisques, dièses, crochets et barres
obliques sortent exactement comme vous les avez écrits.

Dans les listes de l'analyse en concepts, les termes vont entre **accents
graves simples**. Les champs concernés en contiennent déjà — remplacez le
texte et gardez les accents.

Sans ces conteneurs, les symboles de troncature d'Ovid et d'Embase
disparaissent du document final, même s'ils s'affichent normalement sur
GitHub. C'est exactement ce qui est évalué, alors ne le laissez pas au
hasard.

**N'écrivez aucun matricule, aucune adresse courriel, aucun numéro de
téléphone.** Le *repository* est public et un *check* automatique va refuser le
travail.

**N'écrivez jamais huit chiffres de suite**, où que ce soit : le *check* y voit
un matricule. Écrivez les dates avec des tirets, `2026-09-15`, jamais collées.
Ça vaut aussi pour l'intérieur des blocs de consigne, parce que le *check* lit
le fichier au complet, y compris ce qui ne s'affiche pas à l'écran.

Il y a une exception pour vos références : un **PMID compte huit chiffres lui
aussi**. Il passe s'il porte son étiquette, comme dans `PMID : 30234752`, et il
est refusé s'il est tout seul. Les DOI et les liens PubMed complets passent
sans problème.

**Séparez les grands décomptes par une espace.** Une ligne de recherche qui
ramène plus de dix millions de références donnerait huit chiffres collés, et
le contrôle la refuserait. Écrivez `12 345 678` — c'est aussi la typographie
correcte en français.

### 4. Enregistrer

Cliquez sur **Commit changes…** en haut à droite. Dans la fenêtre :

- **Commit message** : écrivez une courte description, par exemple
  `Équipe 03 — concepts et équations`.
- L'option **Commit directly to the `main` branch** est grisée. C'est normal,
  elle doit l'être.
- L'option **Create a new branch… and start a pull request** est déjà cochée.
  **Laissez le nom proposé tel quel.**

Cliquez sur **Propose changes**.

### 5. Ouvrir la pull request

Un formulaire apparaît, déjà rempli en partie. Ajoutez l'identification de
votre équipe, puis cliquez sur **Create pull request**.

**C'est votre remise.** Cochez ensuite les cases de la grille : elles ne
deviennent cliquables qu'une fois la *pull request* créée.

### 6. Vérifier le check automatique

Regardez au bas de la page, quelques secondes plus tard :

- **✓ vert** — tout va bien.
- **✗ rouge** — un renseignement personnel a été détecté. Cliquez sur
  **Details** pour voir la ligne en cause, corrigez-la comme à l'étape
  suivante, et le *check* repartira tout seul.

Un troisième état, **Skipped**, apparaît à côté de « Production des PDF ».
C'est normal : le document final se fabrique seulement quand votre travail est
accepté.

---

## Continuer à travailler

Votre travail n'est pas figé. Vous pouvez le modifier jusqu'à la date de
remise, mais vous devez revenir **par votre pull request**, pas par le dossier
`equipes/`.

1. Onglet **Pull requests** → ouvrez la vôtre. *Mettez-la en signet, vous allez
   y revenir souvent.*
2. Onglet **Files changed**
3. Cliquez sur les trois points `⋯` à droite du nom du fichier → **Edit file**
4. Modifiez votre texte, puis **Commit changes**. Cette fois, laissez l'option
   de *commit* direct sélectionnée.

Vos modifications s'ajoutent à la même *pull request*. N'en ouvrez pas une
deuxième.

> **Pourquoi ce détour ?** Le dossier `equipes/` affiche la version officielle
> de votre travail, celle qui a déjà été acceptée : elle vit sur la *branch*
> `main`. Votre brouillon en cours, lui, vit sur votre propre *branch*, et vous
> y accédez par votre *pull request*. En passant par elle, vous êtes sûrs de
> modifier le bon fichier.

---

## Après la remise

L'enseignante lit votre travail dans **Files changed** et commente ligne par
ligne. C'est ce que GitHub appelle une *review*.

- **Elle demande des corrections** → modifiez votre fichier comme ci-dessus.
  Ses commentaires restent attachés à la discussion.
- **Elle accepte le travail** → elle fait le *merge* de votre *pull request*.
  Votre travail rejoint le dossier de l'équipe sur `main`, et le document final
  se produit automatiquement, page titre comprise.

Répondez dans la *pull request* plutôt que par courriel : tout reste au même
endroit et vos coéquipiers suivent la discussion.

---

## Règles

1. Une seule *pull request* ouverte par équipe et par travail.
2. Ne modifiez que le fichier de votre équipe.
3. N'utilisez jamais le bouton **Merge pull request**. C'est le rôle de
   l'enseignante.
4. Aucun renseignement personnel dans le document.

---

## Licence

Les stratégies de recherche réunies dans ce dépôt sont diffusées sous licence
**Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Vous êtes libre de les partager et de les adapter, y compris à des fins
commerciales, à condition de créditer les autrices et auteurs.

Chaque stratégie a ses propres autrices et auteurs. Ils sont indiqués sur la
page titre du document : citez la stratégie que vous réutilisez, pas le dépôt
au complet. Le gabarit, les grilles et la chaîne de production sont diffusés
sous la même licence.

Le fichier `LICENSE` contient le texte officiel, en anglais. Le résumé destiné
aux non-juristes se trouve sur le site de Creative Commons, en français :
<https://creativecommons.org/licenses/by/4.0/deed.fr>

---

## Utilisation de l'intelligence artificielle générative

> ### Avec assistance de l'IAg
>
> Étiquette de signalement des bibliothèques de l'Université de Montréal.

L'outillage de ce dépôt — les consignes, le gabarit, le contrôle automatique
des renseignements personnels et la chaîne de fabrication des PDF — a été
conçu avec l'aide de Claude Opus 5 (Anthropic),
entre le 26 août et le 2 septembre 2026. Les décisions de conception, la
vérification des faits et les tests relèvent de [nom, fonction]. L'assistant a
produit en cours de route des affirmations factuelles erronées : chaque énoncé
retenu a été revérifié à la source.

**Cette déclaration ne porte pas sur les travaux déposés ici.** Les stratégies
de recherche sont la production des équipes qui les signent.

Pour votre propre travail, deux règles s'appliquent à l'Université de
Montréal : avoir l'autorisation de l'enseignante, et communiquer votre
utilisation de l'IAg. Le plan de cours prime sur tout ce qui est écrit ici. La
[boîte à outils des bibliothèques](https://boite-outils.bib.umontreal.ca/trouver-evaluer/iag?p=5377614)
explique comment citer, signaler et déclarer.

---

## Lexique

| Terme | Ce que ça veut dire |
|---|---|
| *repository* (dépôt) | l'ensemble des fichiers du cours, avec tout leur historique |
| *commit* (enregistrement) | une modification enregistrée, datée et signée. Rien ne s'efface d'un *commit* |
| *branch* (branche) | une ligne de travail en parallèle. La vôtre porte votre travail en cours sans toucher à la version officielle |
| `main` | la *branch* officielle, celle qui fait foi. Personne n'écrit dedans directement |
| *pull request* (demande de fusion) | la demande d'intégrer votre *branch* dans `main`. Ici, c'est votre remise : votre travail, la discussion et la correction sont tous là |
| *check* (contrôle) | une vérification automatique lancée à chaque *commit*. Le vôtre cherche les renseignements personnels |
| *review* (révision) | la lecture commentée de l'enseignante, ligne par ligne |
| *merge* (fusion) | l'intégration du travail accepté dans `main`. Réservé à l'enseignante |
| *issue* (ticket) | une question posée dans l'onglet **Issues**, visible de tous |

---

## En cas de blocage

Ouvrez une *issue* dans l'onglet **Issues** plutôt que d'écrire un courriel :
la réponse va servir aux autres équipes.

Pour la syntaxe Markdown : [guide de GitHub](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
