<!-- ─────────────────────────────────────────────────────────────────
     Vous n'avez aucune information administrative à saisir.
     Vos noms, le sigle du cours, la date et la licence sont ajoutés
     automatiquement à la page titre du PDF.

     Les blocs comme celui-ci sont des consignes. Ils n'apparaissent ni
     sur GitHub ni dans le PDF. Laissez-les ou supprimez-les.

     TROIS RÈGLES DE SAISIE, ET C'EST TOUT :

     1. Tout ce qui est syntaxe d'interrogation va dans un bloc de code
        — les trois accents graves ```. À l'intérieur, rien n'est
        interprété : vos troncatures, astérisques, dièses et crochets
        sortent tels quels. C'est là que va l'historique de recherche.

     2. Dans les listes de la section 2, entourez les termes d'accents
        graves simples. Les champs prévus en contiennent déjà.

     3. N'écrivez jamais huit chiffres de suite. Mettez des tirets dans
        les dates. Séparez les grands décomptes par une espace :
        écrivez 12 345 678, jamais collé. Un PMID passe s'il porte son
        étiquette.

     Rédigez, c'est tout.
     ───────────────────────────────────────────────────────────────── -->


## 1. Question de recherche

<!-- Une stratégie de recherche existe toujours pour quelqu'un. Situez
     la demande avant de formuler la question. -->

**Contexte de la demande :**
<!-- Le cas clinique ou le mandat. Aucun renseignement identifiant. -->

**Question :**
<!-- Une ou deux phrases. -->

**Pertinence clinique :**
<!-- Un court paragraphe : pourquoi cette question mérite d'être posée. -->

**Type de recherche visé :**
<!-- Question ponctuelle, revue de portée, revue systématique… Ce choix
     détermine l'exhaustivité attendue. -->


## 2. Analyse en concepts

<!-- Un bloc par concept. Dupliquez-le autant de fois que nécessaire et
     renumérotez.

     Exemples de ce qui va entre accents graves :
       Descripteurs   `exp Cardiac Surgical Procedures/`
       Mots-clés      `cardiothoracic surgery`
       Troncatures    `cardiothorac` suivi du symbole de la base
       Champs         `.ti,ab,kf.` -->

### Concept 1 —

- **Portée retenue :** <!-- ce que le concept inclut, et ce qu'il exclut -->
- **Vocabulaire contrôlé**
    - Thésaurus et version : `remplacez ce texte, gardez les accents graves`
    - Descripteurs : `remplacez ce texte, gardez les accents graves`
    - Explode : oui / non — pourquoi :
    - Qualificatifs employés : `remplacez ce texte, gardez les accents graves`
- **Vocabulaire libre**
    - Mots-clés : `remplacez ce texte, gardez les accents graves`
    - Troncatures et variantes : `remplacez ce texte, gardez les accents graves`
    - Champs interrogés : `remplacez ce texte, gardez les accents graves`
    - Opérateurs de proximité : `remplacez ce texte, gardez les accents graves`

### Concept 2 —

- **Portée retenue :**
- **Vocabulaire contrôlé**
    - Thésaurus et version : `remplacez ce texte, gardez les accents graves`
    - Descripteurs : `remplacez ce texte, gardez les accents graves`
    - Explode : oui / non — pourquoi :
    - Qualificatifs employés : `remplacez ce texte, gardez les accents graves`
- **Vocabulaire libre**
    - Mots-clés : `remplacez ce texte, gardez les accents graves`
    - Troncatures et variantes : `remplacez ce texte, gardez les accents graves`
    - Champs interrogés : `remplacez ce texte, gardez les accents graves`
    - Opérateurs de proximité : `remplacez ce texte, gardez les accents graves`


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
<!-- Chaque filtre, avec sa justification. Ou : aucun, et pourquoi.
     Un filtre de langue ou de date exclut des références : il se
     justifie, il ne se subit pas. -->

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
