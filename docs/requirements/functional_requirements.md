# Functional Requirements

## Objectif

Décrire les fonctionnalités que FuelSight doit fournir afin de répondre aux besoins métier.

---

# FR-001 - Import des données

Description

Le système doit importer les données issues de Google Sheets via un export CSV.

Priorité

Haute

Version

V1

User Stories

US-01
US-02

---

# FR-002 - Validation des données

Description

Le système doit contrôler les données avant leur intégration dans la zone STAGING.

Contrôles

- champs obligatoires
- quantités positives
- assets existants
- dates valides

Priorité

Haute

Version

V1

User Stories

US-03
US-16
US-18

---

# FR-003 - Gestion des transactions

Le système doit permettre :

- l'enregistrement des réceptions ;
- l'enregistrement des distributions ;
- l'enregistrement des transferts ;
- la correction des transactions.

Version

V1

User Stories

US-05 à US-08

---

# FR-004 - Gestion des stocks

Le système doit permettre :

- le calcul du stock théorique ;
- le suivi du stock physique ;
- la mesure des écarts.

Version

V1

User Stories

US-09
US-10

---

# FR-005 - Reporting

Le système doit fournir :

- Dashboard exécutif
- Dashboard consommation
- Dashboard contrôle

Version

V1

User Stories

US-12
US-13
US-15

---

# FR-006 - Qualité des données

Le système doit :

- détecter les doublons ;
- contrôler les index ;
- contrôler les kilométrages ;
- exécuter les tests automatisés.

Version

V1

User Stories

US-16
US-18
US-19

---

# FR-007 - Fonctionnalités futures

Version V2

- alertes
- prévisions
- historisation
- audit

Version V3

- authentification
- gestion des utilisateurs
- application web