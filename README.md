# Nom du cours — Travaux d'équipe

Tout se fait dans le navigateur. Rien à installer, aucune ligne de commande.

**Vous n'avez aucune information administrative à saisir.** Vos noms, le sigle du cours, la date et la licence sont ajoutés automatiquement à la page titre du document final. Vous rédigez, c'est tout.

---

## Une seule fois, avant de commencer

**Rendez votre adresse courriel privée.** Votre photo en haut à droite → `Settings` → `Emails` → cochez **Keep my email addresses private**.

Sans ce réglage, votre adresse personnelle apparaît publiquement dans l'historique du dépôt, et un enregistrement déjà fait ne peut plus être corrigé. Faites-le avant votre première contribution.

---

## Remettre un travail

### 1. Ouvrir le fichier de votre équipe

`equipes/` → votre dossier → `strategie_recherche.md`

C'est le seul fichier que vous modifiez. Ne touchez pas au dossier d'une autre équipe : la modification apparaîtrait dans l'historique et la remise serait refusée.

### 2. Cliquer sur le crayon

L'icône ✏️ en haut à droite du fichier ouvre l'éditeur. L'onglet **Preview** montre le rendu.

### 3. Rédiger

Les blocs `<!-- ... -->` sont des consignes : ils n'apparaissent ni sur GitHub ni dans le document final. Laissez-les, ils ne dérangent personne.

**N'écrivez aucun matricule, aucune adresse courriel, aucun numéro de téléphone.** Le dépôt est public et un contrôle automatique refusera le travail.

Écrivez les dates sous la forme `2026-09-15`. Écrite `20260915`, une date ressemble à un matricule et fait échouer le contrôle.

### 4. Enregistrer

Bouton **Commit changes…** en haut à droite. Dans la fenêtre :

- **Commit message** : une courte description, par exemple `Équipe 03 — concepts et équations`
- L'option **Commit directly to the `main` branch** est grisée. C'est normal, elle doit l'être.
- L'option **Create a new branch… and start a pull request** est déjà cochée. **Laissez le nom proposé tel quel.**

Cliquez sur **Propose changes**.

### 5. Ouvrir la soumission

Un formulaire apparaît, déjà pré-rempli. Complétez l'identification, puis cliquez sur **Create pull request**.

**C'est votre remise.** Cochez ensuite les cases de la grille : elles ne deviennent cliquables qu'une fois la soumission créée.

### 6. Vérifier le contrôle automatique

En bas de la page, quelques secondes plus tard :

- **✓ vert** — tout va bien.
- **✗ rouge** — un renseignement personnel a été détecté. Cliquez sur **Details** pour voir la ligne en cause, corrigez-la (étape suivante), le contrôle repartira tout seul.

Un troisième état, **Skipped**, apparaît à côté de « Production des PDF ». C'est normal : le document final ne se fabrique qu'une fois votre travail accepté.

---

## Continuer à travailler

Votre travail n'est pas figé : vous pouvez le modifier jusqu'à la date de remise. Mais il faut revenir **par votre soumission**, pas par le dossier `equipes/`.

1. Onglet **Pull requests** → ouvrez la vôtre. *Mettez-la en signet, vous y reviendrez souvent.*
2. Onglet **Files changed**
3. Les trois points `⋯` à droite du nom du fichier → **Edit file**
4. Modifiez, puis **Commit changes** — cette fois, laissez l'option de commit direct sélectionnée.

Vos modifications s'ajoutent à la même soumission. N'en ouvrez pas une seconde.

> **Pourquoi ce détour ?** Le dossier `equipes/` affiche la version officielle du travail, celle qui a déjà été acceptée. Votre brouillon en cours vit dans votre soumission. En passant par elle, vous êtes sûrs de modifier le bon fichier.

---

## Après la remise

L'enseignant lit votre travail dans **Files changed** et commente ligne par ligne.

- **Des corrections sont demandées** → modifiez votre fichier comme ci-dessus. Les commentaires restent attachés à la discussion.
- **Le travail est accepté** → l'enseignant fusionne la soumission. Votre travail rejoint le dossier de l'équipe, et le document final est produit automatiquement, page titre comprise.

Répondez dans la soumission plutôt que par courriel : tout reste au même endroit, et vos coéquipiers suivent la discussion.

---

## Règles

1. Une seule soumission ouverte par équipe et par travail.
2. Ne modifiez que le fichier de votre équipe.
3. N'utilisez jamais le bouton **Merge pull request** — c'est le rôle de l'enseignant.
4. Aucun renseignement personnel dans le document.

---

## En cas de blocage

Ouvrez une *issue* dans l'onglet **Issues** plutôt que d'écrire un courriel : la réponse servira aux autres équipes.

Syntaxe Markdown : [guide de GitHub](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

