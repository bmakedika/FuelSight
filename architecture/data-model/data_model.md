# Data Model

## Objectif

Documenter le modèle logique et analytique utilisé par FuelSight.

---

# Architecture Data

Google Sheets → RAW → STAGING → DATA WAREHOUSE → DATA MART → POWER BI

---

# Modèle Conceptuel

Voir `conceptual_data_model.md` pour le détail des entités, de leurs types et de leurs relations.

---

# Modèle Logique

## raw_fuel_transactions

Stockage des données importées depuis Google Sheets.

Colonnes :

- transaction_id
- transaction_date
- asset_code
- quantity
- movement_type
- created_by
- created_at

---

## raw_tank_measurements

Stockage des contrôles tank.

Colonnes :

- measurement_id
- measurement_date
- tank_level_cm
- physical_stock_l
- index_start
- index_end

---

# Tables de Dimensions

## dim_date

Permet les analyses temporelles.

Attributs :

- date_id
- date
- day
- month
- quarter
- year

---

## dim_asset

Référentiel des équipements.

Attributs :

- asset_id
- asset_code
- asset_type

---

## dim_location

Référentiel des sites.

Attributs :

- location_id
- location_name

---

## dim_fuel_operator

Référentiel des opérateurs carburant.

Attributs :

- fuel_operator_id
- fuel_operator_name

---

# dim_receiver

Référentiel des réceptionnaires.

Attributs :

- receiver_id
- receiver_name

---

## dim_movement_type

Référentiel des mouvements.

Attributs :

- movement_type_id
- movement_type_name

---

# Tables de Faits

## fact_fuel_transactions

Mesure principale du système.

Mesures :

- quantity_liters

Clés :

- date_id
- asset_id
- fuel_operator_id
- receiver_id
- location_id
- movement_type_id

Mesures complémentaires :

- odometer
- hourmeter

---

## fact_tank_measurements

Mesure des stocks physiques.

Mesures :

- physical_stock
- tank_level_cm
- stock_difference

Clés :

- date_id
- location_id

---

# Data Marts

## mart_inventory

Analyse des stocks.

Indicateurs :

- stock physique
- stock théorique
- écart

---

## mart_consumption

Analyse de la consommation.

Indicateurs :

- consommation par véhicule
- consommation par camion
- consommation par générateur

---

## mart_operations

Analyse opérationnelle.

Indicateurs :

- volume distribué
- volume reçu
- volume transféré

---

# Règles Métier

Voir `business_rules.md` pour le détail complet des règles (RM-001 à RM-008).

---

# Qualité des Données

Contrôles :

- doublons
- quantités négatives
- dates invalides
- assets inconnus
- index incohérents
- odomètres incohérents

---

# Traçabilité

Chaque enregistrement doit conserver :

- date de création
- utilisateur créateur
- date de modification
- utilisateur modificateur