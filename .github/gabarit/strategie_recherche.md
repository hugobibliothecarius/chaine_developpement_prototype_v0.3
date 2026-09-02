<!-- ─────────────────────────────────────────────────────────────────
     Vous n'avez aucune information administrative à saisir.
     Vos noms, le sigle du cours, la date et la licence sont ajoutés
     automatiquement à la page titre du PDF.

     Les blocs comme celui-ci sont des consignes. Ils n'apparaissent ni
     sur GitHub ni dans le PDF.

     LAISSEZ-LES EN PLACE. Ils ne coûtent rien — personne ne les voit —
     et les effacer alourdit énormément ce que l'enseignante doit relire :
     quarante lignes de consigne supprimées pour quinze lignes de travail.
     Écrivez simplement en dessous.

     DEUX RÈGLES DE SAISIE, ET C'EST TOUT :

     1. Toute syntaxe d'interrogation va dans un bloc de code — les
        trois accents graves ```. Les blocs sont déjà en place, en
        section 3. À l'intérieur, rien n'est interprété : vos
        troncatures, astérisques, dièses, crochets et barres obliques
        sortent exactement comme vous les avez écrits.

        Ailleurs qu'entre ces accents, n'écrivez aucune syntaxe. Les
        descripteurs et les équations ne se recopient pas dans le
        texte courant : ils vivent dans l'historique, et on y renvoie.

        Collez l'historique DIRECTEMENT de la base de données vers le
        bloc. Word et Google Docs remplacent les guillemets droits par
        des guillemets courbes, et yr="2000 -Current" devient une
        requête invalide sans que rien ne vous le signale.

     2. N'écrivez jamais huit chiffres de suite. Mettez des tirets dans
        les dates. Séparez les grands décomptes par une espace :
        écrivez 12 345 678, jamais collé. Un PMID passe s'il porte son
        étiquette.

     Rédigez, c'est tout.
     ───────────────────────────────────────────────────────────────── -->


## 1. Question de recherche

**Question :**
<!-- Une ou deux phrases. Une question, pas un sujet : « metformine et
     insuffisance rénale » est un sujet ; « chez un patient diabétique
     de type 2 avec un DFG sous 30, peut-on maintenir la metformine »
     est une question. -->

**Pertinence clinique :**
<!-- Quelle décision cette recherche doit éclairer, et pour qui. Deux ou
     trois phrases. Ce n'est pas un paragraphe sur l'importance générale
     du sujet : c'est ce qui change selon la réponse trouvée. -->


## 2. Analyse en concepts

<!-- Ici, le raisonnement seulement, en français courant. Les termes
     eux-mêmes — descripteurs, mots-clés, troncatures, champs — vivent
     en section 3, dans l'historique : les écrire deux fois n'ajoute
     rien, et hors d'un bloc de code leurs symboles se perdent.

     Ce que l'historique ne peut pas dire, c'est pourquoi. C'est ce que
     cette section demande.

     Un bloc par concept. Dupliquez-le autant de fois que nécessaire et
     renumérotez. -->

### Concept 1 —

- **Portée retenue :**
  <!-- Ce que le concept inclut, et surtout ce qu'il exclut. Une
       frontière mal posée se paie plus tard, en bruit ou en silence. -->
- **Explode :** oui / non — pourquoi :
  <!-- Pour chaque descripteur où la question se pose. Exploser ramène
       tous les termes plus spécifiques : c'est un choix d'exhaustivité,
       pas un réflexe. -->
- **Choix du vocabulaire :**
  <!-- Pourquoi ces descripteurs plutôt que d'autres. Pourquoi ces
       mots-clés en plus du vocabulaire contrôlé. Pourquoi ces champs
       d'interrogation. -->

### Concept 2 —

- **Portée retenue :**
- **Explode :** oui / non — pourquoi :
- **Choix du vocabulaire :**


## 3. Stratégies exécutées

<!-- Une section par base interrogée. C'est la partie qui rend votre
     travail reproductible : quelqu'un doit pouvoir rejouer votre
     recherche à partir de ces seules lignes.

     L'historique va dans un bloc de code, numéroté ligne par ligne,
     avec le décompte de chaque ligne. Nommez vos blocs de concepts
     entre crochets, comme le fait la convention professionnelle. -->

### Base 1 —

<!-- Le nom exact, le segment et la couverture, tels qu'affichés par la
     plateforme. Exemple : Ovid MEDLINE(R) ALL <1946 au 28 mai 2025> -->

- **Plateforme et interface :** <!-- Ovid, EBSCO, interface native… -->
- **Mode d'interrogation :** <!-- Advanced ou Basic, chez Ovid -->
- **Date d'exécution :** <!-- format AAAA-MM-JJ, tirets compris -->

**Historique de recherche**

```
#    Recherche                                                    Résultats
1    
2    
3    
```

<!-- Modèle, pour la forme attendue :

#    Recherche                                                    Résultats
1    exp Cardiac Surgical Procedures/                             256 597
2    exp Thoracic Surgical Procedures/                            390 485
3    (cardiac* or cardiothorac*).ti,ab,kf.                        453 322
4    or/1-3  [chirurgie cardiothoracique]                         770 224
5    simulation training/                                           8 049
6    or/5-5  [simulation]                                           8 049
7    4 and 6  [croisement]                                          2 431
8    limit 7 to yr="2000 -Current"                                  2 277
9    limit 8 to (english or french)  [résultats retenus]            2 210
-->

**Filtres appliqués :**
<!-- Renvoyez au numéro de la ligne de l'historique, et justifiez.
     Par exemple : « ligne 8, années 2000 et suivantes — la simulation
     haute fidélité n'existait pas avant ». Ou : aucun filtre, et
     pourquoi. Un filtre de langue ou de date exclut des références :
     il se justifie, il ne se subit pas.
     Ne recopiez pas la syntaxe ici — elle est dans l'historique. -->

**Légende des opérateurs employés**

```
Ne gardez que ce que vous avez réellement utilisé.
```

<!-- Modèle, à adapter à votre base :

ti = titre          ab = résumé          kf = mot-clé d'indexation
tw = titre + résumé + mots-clés          fs = qualificatif flottant
/           terme d'indexation (descripteur)
exp         le descripteur et tous ses termes plus spécifiques
adj3        mots à trois positions ou moins l'un de l'autre, tout ordre
*           toutes les variantes de suffixe de la racine
?           remplace un caractère ou aucun
freq=n      seuil d'occurrences du terme dans la notice
-->

### Base 2 —

- **Plateforme et interface :**
- **Mode d'interrogation :**
- **Date d'exécution :**

**Historique de recherche**

```
#    Recherche                                                    Résultats
1    
2    
3    
```

**Filtres appliqués :**

**Légende des opérateurs employés**

```
```

### Dédoublonnage

<!-- Combien de références au total, combien après retrait des doublons,
     et par quel moyen. -->

- **Total avant dédoublonnage :**
- **Total après :**
- **Moyen employé :** <!-- fonction de la plateforme, Zotero, EndNote… -->


## 4. Critères d'inclusion et d'exclusion

<!-- Ce qui a servi à trier les résultats, pas ce qui a servi à les
     trouver. Les filtres de la section 3 sont autre chose. -->

**Inclusion**

- Critère — justification :

**Exclusion**

- Critère — justification :


## 5. Journal de recherche

<!-- Consignez chaque tentative, y compris celles qui n'ont rien donné :
     les impasses font partie du raisonnement et sont évaluées. Un bloc
     par tentative. -->

### 2026-MM-JJ —

- **Ce que nous avons essayé :**
- **Résultats obtenus :**
- **Ce que nous en avons tiré :**


## 6. Ajustements et bilan

<!-- Qu'avez-vous modifié en cours de route, et pourquoi ?
     Que feriez-vous différemment en reprenant depuis le début ?
     Quelle est la limite connue de votre stratégie ? -->


## 7. Références retenues

<!-- Selon le style de citation demandé dans le plan de cours.

     Un PMID compte huit chiffres, autant qu'un matricule. Le contrôle
     automatique l'accepte seulement s'il porte son étiquette, comme
     dans « PMID : » ou « PMID: ». Un identifiant tout seul sera refusé.
     Les DOI et les liens PubMed complets passent sans problème. -->

1.
2.
3.


## 8. Filiation

<!-- Si ce travail dérive d'une stratégie déjà versée dans le
     repository, collez son permalien ici et dites ce que vous en avez
     repris. Sinon, écrivez : travail original. -->
