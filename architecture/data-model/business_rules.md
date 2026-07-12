# Business Rules

Règles de gestion appliquées aux données FuelSight. Numérotation `RM-XXX` (Règle Métier), alignée sur `data_model.md`.

---

## RM-001

Nom : Mouvement unique

Règle : Une transaction doit appartenir à un seul type de mouvement.

---

## RM-002

Nom : Quantité positive

Règle : Toute transaction doit posséder une quantité supérieure à zéro.

Contrôle :

```
quantity_liters > 0
```

---

## RM-003

Nom : Asset valide

Règle : Toute transaction doit référencer un asset existant dans le référentiel.

---

## RM-004

Nom : Correction traçable

Règle : Toute correction doit être enregistrée comme une nouvelle transaction, et historisée.

---

## RM-005

Nom : Historisation obligatoire (RAW)

Règle : Les données RAW ne peuvent jamais être modifiées. Aucune suppression physique n'est autorisée.

---

## RM-006

Nom : Alimentation des dimensions

Règle : Les dimensions sont alimentées uniquement depuis les données validées (zone STAGING).

---

## RM-007

Nom : Contrôle kilométrique

Règle : Le kilométrage (odometer) d'un véhicule doit être supérieur ou égal au précédent relevé.

---

## RM-008

Nom : Contrôle index

Règle : L'index de pompe (pump index) doit être croissant entre deux relevés.

---

## RM-009

Nom : Unicité des transactions

Règle : Une transaction ne doit pas constituer un doublon d'une transaction déjà enregistrée (même date, même asset, même quantité, même type de mouvement).
