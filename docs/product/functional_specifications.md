# Functional Specifications

## Objectif

Vue narrative des fonctionnalités de FuelSight, organisée par domaine métier. Pour le détail traçable (priorité, version, User Stories associées), voir [`functional_requirements.md`](../requirements/functional_requirements.md) - ce document décrit le même périmètre sous une forme descriptive, structurée autour des mêmes identifiants `FR-XXX` pour éviter toute numérotation parallèle.

---

# Collecte & Transactions (FR-001, FR-003)

- Saisie des transactions (réceptions, distributions, transferts, corrections)
- Validation des données à la saisie
- Export CSV

---

# Pipeline ELT (FR-001, FR-002)

- Chargement RAW
- Nettoyage et validation STAGING
- Chargement Data Warehouse

---

# Gestion des stocks (FR-004)

- Stock théorique
- Stock physique
- Contrôle des écarts

---

# Reporting (FR-005)

- Dashboard exécutif
- Dashboard consommation
- Dashboard contrôle

---

# Qualité des données (FR-006)

- Détection des doublons
- Contrôle du kilométrage
- Contrôle des index

---

# Administration (FR-007 - hors V1)

- Audit - V2
- Authentification - V3
- Gestion des utilisateurs - V3
