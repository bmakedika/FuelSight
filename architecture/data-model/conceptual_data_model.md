# Conceptual Data Model

## Objectif

Décrire les principales entités métier de FuelSight indépendamment de toute technologie.

Le MCD représente uniquement les concepts métier nécessaires à la gestion des opérations carburant et à la production des indicateurs de pilotage.

---

# Entités

## Location

Représente un site opérationnel.

Exemples :

- Tshikapa
- Kananga

---

## Asset

Représente un équipement consommant du carburant.

Types :

- Light Vehicle
- Truck
- Generator

Exemples :

- 068CD465
- 068CD200
- GEN-TSHIKAPA-011

---

## Fuel Operator

Personne responsable de la distribution du carburant.

Exemples :

- Jean
- Patrick
- Sylvain

---

## Receiver

Personne qui réceptionne ou atteste la quantité distribuée.

Le Receiver peut être :

- un chauffeur ;
- un vigile ;
- un réceptionnaire ;
- toute personne chargée de confirmer l'opération.

Exemples :

- David Munganga
- Mukendi
- Kabamba

---

## Movement Type

Catégorie de mouvement de carburant.

Types :

- Réception
- Distribution
- Transfert
- Correction

---

## Fuel Transaction

Représente un mouvement de carburant.

Chaque transaction est réalisée par un Fuel Operator et concerne un Asset.

Exemples :

- Distribution de carburant
- Réception de carburant
- Transfert de carburant
- Correction de stock

---

## Tank Measurement

Représente un contrôle physique du stock carburant.

Un Tank Measurement combine :

- une mesure Dipstick ;
- un relevé des index pompe ;
- un calcul d'écart éventuel.

---

# Relations

## Location contient Asset

Cardinalité :

Location (1,N)
Asset (1,1)

Une Location peut contenir plusieurs Assets.

Un Asset appartient à une seule Location.

---

## Location possède Tank Measurement

Cardinalité :

Location (1,N)
Tank Measurement (1,1)

Un site possède plusieurs relevés de contrôle.

Un relevé appartient à un seul site.

---

## Asset est concerné par Fuel Transaction

Cardinalité :

Asset (1,N)
Fuel Transaction (1,1)

Un Asset peut être impliqué dans plusieurs transactions.

Une transaction concerne un seul Asset.

---

## Fuel Operator réalise Fuel Transaction

Cardinalité :

Fuel Operator (1,N)
Fuel Transaction (1,1)

Un Fuel Operator peut réaliser plusieurs transactions.

Une transaction est réalisée par un seul Fuel Operator.

---

## Receiver réceptionne Fuel Transaction

Cardinalité :

Receiver (1,N)
Fuel Transaction (1,1)

Un Receiver peut réceptionner plusieurs transactions.

Une transaction possède un seul Receiver.

---

## Movement Type catégorise Fuel Transaction

Cardinalité :

Movement Type (1,N)
Fuel Transaction (1,1)

Un type de mouvement peut être utilisé dans plusieurs transactions.

Une transaction appartient à un seul type de mouvement.