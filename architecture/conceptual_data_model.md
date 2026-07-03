# Conceptual Data Model

## Objectif

Décrire les principales entités métier de FuelSight indépendamment de toute technologie.

---

## Entités

### Asset

Représente un équipement consommant du carburant.

Types :

- Light Vehicle
- Truck
- Generator

---

### Fuel Transaction

Représente un mouvement carburant.

Types :

- Réception
- Distribution
- Transfert
- Correction

---

### Tank Measurement

Représente une mesure physique effectuée sur un réservoir.

---

### User

Représente un utilisateur de la plateforme.

Rôles :

- Fuel Operator
- Fleet Manager

---

### Location

Représente un site opérationnel.

Exemples :

- Tshikapa
- Kananga

---

### Movement Type

Catégorie de mouvement enregistrée.

---

## Relations

```
User
  | réalise
  v
Fuel Transaction

Asset
  | reçoit
  v
Fuel Transaction

Location
  | contient
  v
Asset

Location
  | possède
  v
Tank Measurement

Fuel Transaction
  | appartient à
  v
Movement Type
```