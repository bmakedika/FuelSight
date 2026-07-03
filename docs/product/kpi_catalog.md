# KPI Catalog

## Objectif

Décrire l'ensemble des indicateurs métier utilisés dans FuelSight.

---

# KPI-001

Nom

Stock théorique

Description

Volume calculé à partir des mouvements enregistrés.

Calcul

Stock initial
+ Réceptions
- Distributions
± Corrections

Source

fact_fuel_transactions

Dashboard

Executive

Fréquence

Temps réel

---

# KPI-002

Nom

Stock physique

Description

Stock observé lors du dernier contrôle tank.

Source

fact_tank_measurements

Dashboard

Executive

---

# KPI-003

Nom

Écart de stock

Calcul

Stock physique - Stock théorique

---

# KPI-004

Nom

Consommation par actif

Calcul

Somme(quantity_liters)

Dimension

Asset

---

# KPI-005

Nom

Consommation mensuelle

Agrégation

Mois

---

# KPI-006

Nom

Volume distribué

Filtre

Movement Type = DISTRIBUTION

---

# KPI-007

Nom

Volume reçu

Filtre

Movement Type = RECEPTION

---

# KPI-008

Nom

Nombre d'anomalies

Description

Nombre de contrôles qualité en échec.

Source

Tests SQL