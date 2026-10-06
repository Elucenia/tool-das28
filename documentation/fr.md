<!-- ELUCENIA technical documentation · das28 · fr · no clinical/professional/rights approval -->

# DAS28 (VS et CRP)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/das28)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Articulations douloureuses (sur 28)

`tjc`

intervalle: 0–28

### Articulations gonflées (sur 28)

`sjc`

intervalle: 0–28

### Évaluation globale de santé par le patient (échelle visuelle)

`gh`

mm · intervalle: 0–100

### Vitesse de sédimentation (VS)

`vhs`

mm/h · facultatif · intervalle: 1–150

### Protéine C-réactive (CRP)

`pcr`

mg/L · facultatif · intervalle: 0–300

## Édition de la méthode

DAS28-VS/Prevoo 1995 et DAS28-CRP/Wells 2009 ; 28 articulations ; constante CRP 0,96

## Formule documentée

DAS28-VS = 0,56 × √(douloureuses) + 0,28 × √(gonflées) + 0,70 × ln(VS) + 0,014 × évaluation globale.

DAS28-CRP = 0,56 × √(douloureuses) + 0,28 × √(gonflées) + 0,36 × ln(CRP + 1) + 0,014 × évaluation globale + 0,96 (CRP en mg/L).

## Limites et population

Le DAS28 de 1995 a été développé pour l’activité de la polyarthrite rhumatoïde, avec un compte de 28 articulations et des comparaisons à l’évaluation clinique de rhumatologues. La variante avec CRP n’est pas automatiquement équivalente à celle avec VS ; formule, unités et seuils doivent correspondre à la source et à l’édition utilisées.

## Références

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Activité modérée de la polyarthrite rhumatoïde


### 2

Rémission de la polyarthrite rhumatoïde


### 3

Activité élevée de la polyarthrite rhumatoïde


### 4

Activité modérée de la polyarthrite rhumatoïde

Le DAS28-CRP donne habituellement des valeurs plus faibles que le DAS28-ESR : avec les mêmes seuils, la rémission peut être surestimée.

