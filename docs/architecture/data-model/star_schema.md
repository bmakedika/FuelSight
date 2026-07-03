# Star Schema

## Objectif

Définir le modèle dimensionnel utilisé par FuelSight pour l'analyse décisionnelle.

---

# Vue Globale

```
                 dim_date
                     |
dim_asset ---- fact_fuel_transactions ---- dim_fuel_operator
                     |
               dim_receiver
                     |
            dim_movement_type
                     |
               dim_location
```

```
                 dim_date
                     |
        fact_tank_measurements
                     |
               dim_location
```

---

# Dimensions

## dim_date

Attributs :

- date_id
- date
- day
- month
- quarter
- year

---

## dim_asset

Attributs :

- asset_id
- asset_code
- asset_type

Valeurs :

- LIGHT_VEHICLE
- TRUCK
- GENERATOR

---

## dim_fuel_operator

Attributs :

- fuel_operator_id
- fuel_operator_name

---

## dim_receiver

Attributs :

- receiver_id
- receiver_name

---

## dim_movement_type

Attributs :

- movement_type_id
- movement_type_name

Valeurs :

- RECEPTION
- DISTRIBUTION
- TRANSFER
- CORRECTION

---

## dim_location

Attributs :

- location_id
- location_name

---

# Fact Tables

## fact_fuel_transactions

Mesures :

- quantity_liters

Clés :

- date_id
- asset_id
- fuel_operator_id
- receiver_id
- movement_type_id
- location_id

Mesures complémentaires :

- odometer
- hourmeter

---

## fact_tank_measurements

Mesures :

- physical_stock_l
- tank_level_cm
- stock_difference

Clés :

- date_id
- location_id

Mesures complémentaires :

- pump_index_start
- pump_index_end

---

# Data Marts

## mart_inventory

Indicateurs :

- stock physique
- stock théorique
- écart stock

---

## mart_consumption

Indicateurs :

- consommation par véhicule
- consommation par générateur
- consommation par camion

---

## mart_operations

Indicateurs :

- volumes reçus
- volumes distribués
- volumes transférés