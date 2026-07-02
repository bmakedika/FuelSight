# Data

Ce dossier contient les données utilisées par le projet.

## Objectif

Centraliser les données du pipeline, de leur import brut jusqu'à leur mise à disposition pour l'analyse.

## Structure

### raw/

Données importées sans transformation.

Exemples :

- transactions.csv
- tank_measurements.csv

### staging/

Données nettoyées et validées.

### mart/

Données destinées aux analyses et tableaux de bord.

## Convention de nommage

Format : `<domaine>_<YYYYMMDD>.csv`

- `raw/` : `transactions_20260701.csv`, `tank_measurements_20260701.csv`
- `staging/` : `transactions_clean_20260701.csv`
- `mart/` : `consumption_agg_20260701.csv`

La date permet de tracer chaque export sans jamais écraser un fichier existant (voir règle ci-dessous).

## Règles

- Ne jamais modifier les données brutes.
- Toute transformation doit être reproductible.
- Les fichiers sensibles ne doivent pas être versionnés.

## Qualité des données

Les contrôles portent sur :

- Doublons
- Valeurs nulles
- Quantités négatives
- Odomètres incohérents
- Index incohérents

## Sources de données

- Google Sheets
- CSV exportés
- PostgreSQL
