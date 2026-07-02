# SQL

Ce dossier contient tous les scripts SQL nécessaires au fonctionnement de FuelSight.

## Objectif

Automatiser la création, l'alimentation et l'exploitation du Data Warehouse FuelSight.

## Structure

### ddl/

Scripts de création des objets de base de données.

Exemples :

- tables
- index
- contraintes
- vues

### raw/

Scripts liés à la zone RAW.

Objectif :

- stockage des données importées
- conservation des données brutes

### staging/

Scripts de transformation intermédiaire.

Objectif :

- nettoyage
- validation
- normalisation

### warehouse/

Scripts du modèle décisionnel.

Contient :

- dimensions
- tables de faits
- vues analytiques

### marts/

Scripts orientés reporting.

Exemples :

- consommation journalière
- consommation par véhicule
- consommation par générateur
- analyse des écarts

## Convention de nommage

- `ddl_create_tables.sql`
- `stg_clean_transactions.sql`
- `fact_fuel_transactions.sql`
- `mart_consumption_analysis.sql`

## Principes

- Les scripts doivent être idempotents.
- Les transformations doivent être reproductibles.
- Les règles métier doivent être documentées.
- Les vues doivent être optimisées pour Power BI.

## Technologies

- PostgreSQL
- pgAdmin
- Docker PostgreSQL
