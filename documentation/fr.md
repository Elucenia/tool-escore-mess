<!-- ELUCENIA technical documentation · escore-mess · fr · no clinical/professional/rights approval -->

# MESS (score de gravité d’un membre gravement lésé)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/escore-mess)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Lésion osseuse et des parties molles

`energia`

- `1` — Faible énergie (plaie par arme blanche, fracture simple, projectile d’arme de poing)
- `2` — Énergie moyenne (fracture ouverte ou multiple, luxation)
- `3` — Haute énergie (accident à grande vitesse, projectile de fusil)
- `4` — Très haute énergie (ci-dessus + contamination majeure)

### Ischémie du membre

`isquemia`

- `0` — Sans ischémie
- `1` — Pouls diminué ou absent, perfusion normale
- `2` — Absence de pouls, paresthésies, recoloration capillaire lente
- `3` — Membre froid, paralysé, insensible

### Ischémie depuis plus de 6 heures ?

`tempo`

- `0` — Non
- `1` — Oui

### Choc

`choque`

- `0` — Pression artérielle systolique toujours \> 90 mmHg
- `1` — Hypotension transitoire
- `2` — Hypotension persistante

### Âge

`idade`

- `0` — \< 30 ans
- `1` — 30 à 50 ans
- `2` — \> 50 ans

## Édition de la méthode

MESS/Johansen 1990 : 4 domaines, ischémie doublée \>6 h ; aucune décision automatique d’amputation

## Formule documentée

MESS = lésion osseuse/tissus mous (1 à 4) + ischémie (0 à 3, doublée si durée supérieure à 6 h) + choc (0 à 2) + âge (0 à 2).

## Limites et population

Le MESS original a été développé dans de petits groupes présentant un traumatisme grave du membre inférieur. L’association du seuil ≥7 à l’amputation dans ces groupes ne constitue ni une règle universelle ni une indication automatique. La sauvegarde du membre dépend d’une évaluation multidisciplinaire et de conditions cliniques non résumées par le score.

## Références

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

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

MESS < 7 : plage de sauvetage du membre dans la série originale

| Détails du résultat | |
| --- | --- |
| Points d’ischémie | 1 |

Le MESS ne décide pas à lui seul : l’indication d’amputation primaire relève de l’équipe (orthopédie, chirurgie vasculaire et plastique), le patient étant stabilisé.


### 2

MESS ≥ 7 : dans la série originale, tous les membres ayant ce score ont été amputés

| Détails du résultat | |
| --- | --- |
| Points d’ischémie | 4 (doublés : ischémie > 6 h) |

Le MESS ne décide pas à lui seul : l’indication d’amputation primaire relève de l’équipe (orthopédie, chirurgie vasculaire et plastique), le patient étant stabilisé.


### 3

MESS ≥ 7 : dans la série originale, tous les membres ayant ce score ont été amputés

| Détails du résultat | |
| --- | --- |
| Points d’ischémie | 2 |

Le MESS ne décide pas à lui seul : l’indication d’amputation primaire relève de l’équipe (orthopédie, chirurgie vasculaire et plastique), le patient étant stabilisé.

