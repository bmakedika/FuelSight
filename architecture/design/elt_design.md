# ELT Design

## Étape 1

Google Sheets → Export CSV

---

## Étape 2

Chargement RAW

Tables :

- raw_fuel_transactions
- raw_tank_measurements

---

## Étape 3

Transformation STAGING

Contrôles :

- doublons
- champs obligatoires
- quantités négatives
- cohérence index

---

## Étape 4

Chargement Data Warehouse

Tables :

- dimensions
- faits

---

## Étape 5

Création Data Marts

- inventory
- consumption
- operations

---

## Étape 6

Consommation Power BI