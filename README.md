# Nom du cours — Dépôt des travaux d'équipe

Bienvenue. Ce dépôt sert à rédiger et à remettre les travaux d'équipe du cours.

Vous travaillez **directement dans l'interface web de GitHub** : aucune installation, aucune ligne de commande.

---

## Structure du dépôt

```
gabarit/
    strategie_recherche.md      ← modèle de référence, à ne pas modifier
equipes/
    equipe-01/
        strategie_recherche.md  ← le fichier de l'équipe 1
    equipe-02/
        strategie_recherche.md
    ...
```

**Chaque équipe travaille uniquement dans son propre dossier.** Ne modifiez jamais le dossier d'une autre équipe : la modification serait visible dans l'historique et la remise serait refusée.

Vous pouvez consulter le travail des autres équipes. C'est voulu — inspirez-vous des bonnes idées, mais le contenu que vous soumettez doit être le vôtre.

---

## Comment remettre un travail

### 1. Ouvrir votre fichier

Allez dans `equipes/` → votre dossier d'équipe → `strategie_recherche.md`

### 2. Passer en mode édition

Cliquez sur l'icône de crayon (**Edit this file**) en haut à droite du fichier.

### 3. Rédiger

Écrivez votre travail. L'onglet **Preview** montre le rendu final.

Vous pouvez enregistrer autant de fois que vous le souhaitez avant la date de remise : chaque enregistrement s'ajoute à la même pull request.

### 4. Enregistrer

Cliquez sur **Commit changes…** en haut à droite. Une fenêtre s'ouvre :

| Champ | Quoi mettre |
|---|---|
| **Commit message** | Une courte description : `Équipe 03 — ajout des concepts clés` |
| **Extended description** | Facultatif, laissez vide |
| **Commit directly to the `main` branch** | Cette option est **désactivée** — c'est normal |
| **Create a new branch… and start a pull request** | Déjà sélectionnée, laissez-la ainsi |
| **Nom de la branche** | Remplacez le nom proposé par `equipe-03/travail-1` |

Cliquez sur **Propose changes**.

### 5. Ouvrir la pull request

GitHub affiche une page de création de pull request. Remplissez le formulaire qui apparaît (numéro d'équipe, membres), puis cliquez sur **Create pull request**.

**C'est votre remise.** L'enseignant reçoit automatiquement une demande de révision.

### 6. Les enregistrements suivants

Une fois la pull request ouverte, retournez simplement au même fichier, cliquez sur le crayon, modifiez, et enregistrez — mais cette fois choisissez **Commit directly to the `equipe-03/travail-1` branch**. Vos modifications s'ajoutent à la pull request déjà ouverte.

---

## Ce qui se passe ensuite

L'enseignant lit votre travail dans l'onglet **Files changed** de la pull request et y laisse ses commentaires, ligne par ligne.

- **Des corrections sont demandées** → modifiez votre fichier sur la même branche, les commentaires restent attachés au fil de discussion.
- **Le travail est accepté** → l'enseignant fusionne (*merge*) la pull request. Votre travail rejoint la branche `main`.

Répondez aux commentaires dans la pull request plutôt que par courriel : tout reste au même endroit.

---

## Règles

1. Une seule pull request ouverte par équipe et par travail.
2. Ne modifiez que les fichiers de votre dossier d'équipe.
3. N'utilisez pas le bouton **Merge pull request** : c'est le rôle de l'enseignant.
4. Les trois membres de l'équipe doivent apparaître dans le fichier et dans la pull request.

---

## Aide

- Syntaxe Markdown : [Basic writing and formatting syntax](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- Un blocage technique ? Ouvrez une *issue* dans l'onglet **Issues** plutôt qu'un courriel : les autres équipes profiteront de la réponse.
