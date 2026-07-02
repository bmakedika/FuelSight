# ADR-003

## Décision

Utiliser un modèle dimensionnel en étoile.

## Statut

Acceptée

## Contexte

Le projet nécessite :

- l'analyse ;
- l'agrégation ;
- le reporting Power BI.

## Justification

Le Star Schema :

- simplifie les requêtes ;
- améliore les performances ;
- facilite la compréhension métier.

## Conséquences

Le Data Warehouse sera construit autour :

- de tables de faits ;
- de tables de dimensions.
