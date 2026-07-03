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

---

## Fuel Operator

### fuel_operator_id

Description :
Identifiant unique de l'opérateur carburant.

Type :
INTEGER

---

### fuel_operator_name

Description :
Nom complet de l'opérateur carburant.

Type :
VARCHAR(100)

---

## Receiver

### receiver_id

Description :
Identifiant unique du réceptionnaire.

Type :
INTEGER

---

### receiver_name

Description :
Nom complet de la personne attestant ou réceptionnant le carburant.

Type :
VARCHAR(100)

---

## Location

### location_id

Description :
Identifiant unique du site opérationnel.

Type :
INTEGER

---

### location_name

Description :
Nom du site opérationnel.

Type :
VARCHAR(100)

Exemples :

- Tshikapa
- Kananga

---

## Movement Type

### movement_type_id

Description :
Identifiant unique du type de mouvement.

Type :
INTEGER

---

### movement_type_name

Description :
Nature du mouvement carburant.

Type :
VARCHAR(50)

Valeurs :

- RECEPTION
- DISTRIBUTION
- TRANSFER
- CORRECTION

---

## Tank Measurement

### measurement_id

Description :
Identifiant unique du relevé de réservoir.

Type :
UUID

---

### measurement_date

Description :
Date du relevé.

Type :
DATE

---

### tank_level_cm

Description :
Mesure physique du niveau du carburant.

Type :
NUMERIC(10,2)

Unité :
Centimètre

---

### physical_stock_l

Description :
Volume réellement présent dans le réservoir.

Type :
NUMERIC(10,2)

Unité :
Litre

---

### index_start

Description :
Index de pompe au début de la période.

Type :
NUMERIC(10,2)

---

### index_end

Description :
Index de pompe à la fin de la période.

Type :
NUMERIC(10,2)