# Data Dictionary

## Asset

### asset_id

Description :
Identifiant unique d'un actif.

Type :
INTEGER

Exemple :
1001

---

### asset_code

Description :
Code unique de l'actif.

Type :
VARCHAR(50)

Exemple :
068CD465

---

### asset_type

Description :
Type d'actif.

Valeurs :

- LIGHT_VEHICLE
- TRUCK
- GENERATOR

Type :
VARCHAR(30)

---

## Fuel Transaction

### transaction_id

Description :
Identifiant unique de transaction.

Type :
UUID

---

### transaction_date

Description :
Date de l'opération.

Type :
DATE

---

### quantity_liters

Description :
Volume concerné par la transaction.

Type :
NUMERIC(10,2)

Unité :
Litre

---

### movement_type

Description :
Nature de la transaction.

Valeurs :

- RECEPTION
- DISTRIBUTION
- TRANSFER
- CORRECTION

---

### odometer

Description :
Kilométrage du véhicule.

Type :
NUMERIC

Applicable :

- LIGHT_VEHICLE
- TRUCK

---

### hourmeter

Description :
Compteur horaire.

Applicable :

- GENERATOR

---

### remark

Description :
Commentaire libre.