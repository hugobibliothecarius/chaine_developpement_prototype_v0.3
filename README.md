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

## À lire avant de commencer : votre travail sera publié sous votre nom

Ce n'est pas un devoir qui reste entre vous et l'enseignant

### Ce qui va se passer

Vos noms figureront sur la page titre du document final, sous licence
**Creative Commons Attribution 4.0**. Le *repository* est public : n'importe
qui peut le consulter, aujourd'hui ou demain. Les travaux retenus seront
ensuite déposés dans **Papyrus**, le dépôt institutionnel de l'Université de
Montréal, où ils recevront une adresse permanente et pourront être cités.

Concrètement, la licence CC BY permet à quiconque de reprendre et d'adapter
votre stratégie, y compris à des fins commerciales, **à condition de vous
créditer**. C'est aussi pour ça que vos noms y sont : sans eux, personne ne
saurait qui créditer.

### C'est permanent

Un *repository* Git conserve tout. Une fois vos noms enregistrés, **ils y
restent**, même si :

- la ligne est retirée du fichier plus tard ;
- votre équipe décide finalement de ne pas déposer dans Papyrus ;
- vous quittez le cours.

Il n'y a pas de bouton pour effacer un enregistrement déjà publié. C'est la
même raison qui rend le réglage de la section suivante urgent plutôt que
facultatif.

### Si vous ne le voulez pas

**Parlez-en à l'enseignante avant de commencer à travailler.** Une voie de
remise non publique existe : vous serez évalués sur le même travail, sans que
votre nom soit publié. Vous n'avez pas à vous justifier, et ce choix n'a aucune
incidence sur votre note.

Cette décision doit être prise en amont. Une fois vos noms inscrits, ils demeureront.

---

## À faire avant avant de commencer

**Rendez votre adresse courriel privée.** Cliquez sur votre photo en haut à
droite → **Settings** → **Emails**, puis cochez **Keep my email addresses
private**.

Sans ce réglage, votre adresse personnelle apparaît publiquement dans
l'historique du *repository* — et comme pour vos noms, on ne peut plus
corriger un *commit* déjà fait. Faites-le **avant** votre première
contribution : c'est le seul moment où c'est possible.

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
ni dans le document final.

**Laissez-les en place, écrivez en dessous.** Ils ne dérangent personne —
personne ne les voit. Mais les effacer alourdit beaucoup la relecture de
l'enseignante : elle verrait quarante lignes de consigne supprimées pour
quinze lignes de votre travail, et devrait chercher les vôtres là-dedans.

**Toute syntaxe d'interrogation va dans un bloc de code** — les trois accents
graves ```` ``` ````, déjà en place dans la section 3 du gabarit. À
l'intérieur, rien n'est interprété : vos troncatures, astérisques, dièses,
crochets et barres obliques sortent exactement comme vous les avez écrits.

**Ailleurs, n'écrivez aucune syntaxe.** Ne recopiez pas un descripteur ou une
équation dans le texte courant : hors d'un bloc de code, les symboles de
troncature d'Ovid et d'Embase disparaissent du document final, même s'ils
s'affichent normalement sur GitHub. C'est exactement ce qui est évalué, alors
ne le laissez pas au hasard.

**Et ne faites pas passer votre historique par un traitement de texte.**
Collez-le directement de la base de données vers le bloc de code. Word et
Google Docs remplacent automatiquement les guillemets droits par des
guillemets courbes : votre ligne

```
limit 7 to yr="2000 -Current"
```

deviendrait `yr=“2000 -Current”`, et la requête ne fonctionnerait plus. Le
changement est invisible à l'œil, personne ne vous en avertira, et c'est votre
équation qui serait fautive. Les sections en prose, elles, vous pouvez les
brouillonner où vous voulez.

Les descripteurs et les équations vivent dans l'historique, et le reste du
document y renvoie par le numéro de ligne.

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

**Le message de *commit* devient le titre de votre remise.** Commencez-le par
votre numéro d'équipe :

```
Équipe 03 — concepts et équations
```

C'est par ce titre que l'enseignante vous retrouve dans sa liste. Effacez le
texte que GitHub propose — « Update strategie_recherche.md » ne dit pas qui
vous êtes, et sa file de correction en compterait vingt identiques.

Pour le reste, ne changez rien : GitHub ne vous laisse pas écrire directement
dans `main` — l'option est grisée, ou absente selon la version de l'interface —
et la création d'une branche est déjà choisie. **Laissez le nom proposé tel
quel.**

Validez. Le bouton s'appelle **Commit changes** ou **Propose changes** selon la
version ; les deux font la même chose.

### 5. Ouvrir la pull request

Un formulaire apparaît, déjà rempli en partie. Complétez l'identification de
votre équipe — le numéro d'équipe, le travail, et vos **identifiants GitHub**,
pas vos noms. Puis cliquez sur **Create pull request**.

> **Pourquoi des identifiants ici, et vos noms sur le document.** Les
> identifiants servent à vous mentionner dans la discussion. Vos noms, eux,
> sont déjà inscrits par l'administrateur du dépôt et figurent sur la page
> titre du document final, sous licence CC BY — c'est votre travail, il est
> publié, cité et déposé dans Papyrus sous votre signature. Une attribution
> anonyme n'aurait aucune valeur sous cette licence.

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

Deux façons de corriger, selon ce qu'elle a écrit.

**Si sa remarque contient une suggestion** — un encadré qui montre la ligne
corrigée — vous n'avez rien à éditer. Un bouton sous l'encadré applique sa
correction directement. C'est le cas le plus fréquent pour une faute de
syntaxe.

**Sinon**, il faut modifier le fichier. Un détail pratique : l'éditeur
n'affiche pas les commentaires. Ouvrez donc votre remise dans un onglet, pour
lire les annotations dans **Files changed**, et l'éditeur dans un second.
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
5. Pour votre propre usage de l'IA générative : l'autorisation de l'enseignante
   est requise, et vous devez déclarer votre utilisation. Le plan de cours prime
   sur tout ce qui est écrit ici. La [boîte à outils des
   bibliothèques](https://boite-outils.bib.umontreal.ca/trouver-evaluer/iag?p=5377614)
   explique comment citer, signaler et déclarer.

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

---

<sub><strong>Avec assistance de l'IAg</strong>. Les consignes, le gabarit et l'automatisation de ce dépôt ont été conçus avec l'aide de Claude Opus 5 (Anthropic), en août et septembre 2026. Les décisions, la vérification et les tests relèvent de Hugo Bernier, bibliothécaire - expérience numérique en recherche de l'Université de Montréal. Cette déclaration ne porte pas sur les travaux déposés ici.</sub>
