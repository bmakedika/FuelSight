# Requirements Traceability Matrix (RTM)

## Objectif

La Requirements Traceability Matrix (RTM) assure la traçabilité des exigences métier jusqu'à leur implémentation technique et leur validation.

Elle permet de vérifier que :

- chaque besoin métier est couvert ;
- chaque fonctionnalité est justifiée ;
- chaque User Story répond à un besoin identifié ;
- chaque règle métier est appliquée ;
- chaque exigence est implémentée dans le modèle de données ;
- chaque indicateur métier est alimenté correctement.

---

# Matrice de Traçabilité

| Business Requirement | Functional Requirement | User Story | Business Rule | Data Model | KPI |
|----------------------|------------------------|------------|---------------|------------|-----|
| BR-001 Centralisation des données carburant | FR-001 Import des données | US-01, US-02 | RM-005 | raw_fuel_transactions | Taux de réussite des chargements |
| BR-001 Centralisation des données carburant | FR-002 Validation des données | US-03 | RM-006 | stg_fuel_transactions | Taux de données valides |
| BR-001 Centralisation des données carburant | FR-003 Gestion des transactions | US-05, US-06, US-07 | RM-001, RM-002 | fact_fuel_transactions | Nombre de transactions |
| BR-002 Historisation des transactions | FR-007 Fonctionnalités futures | US-24 | RM-004, RM-005 | fact_fuel_transactions | Historique disponible |
| BR-003 Contrôle du stock théorique | FR-004 Gestion des stocks | US-09 | RM-001 | mart_inventory | Stock théorique |
| BR-004 Contrôle du stock physique | FR-004 Gestion des stocks | US-10 | RM-008 | fact_tank_measurements | Stock physique |
| BR-005 Mesure des écarts | FR-004 Gestion des stocks | US-10 | RM-008 | mart_inventory | Écart de stock |
| BR-006 Analyse de la consommation par asset | FR-005 Reporting | US-12 | RM-007 | mart_consumption | Consommation par actif |
| BR-006 Analyse de la consommation par asset | FR-005 Reporting | US-13 | RM-007 | mart_consumption | Consommation mensuelle |
| BR-007 Identification des anomalies | FR-006 Qualité des données | US-16 | RM-002 | stg_fuel_transactions | Nombre de doublons détectés |
| BR-007 Identification des anomalies | FR-006 Qualité des données | US-17 | RM-007 | mart_consumption | Nombre d'anomalies détectées |
| BR-007 Identification des anomalies | FR-006 Qualité des données | US-18 | RM-007, RM-008 | fact_fuel_transactions | Contrôles qualité |
| BR-007 Identification des anomalies | FR-006 Qualité des données | US-19 | RM-001 à RM-008 | Ensemble du Data Warehouse | Taux de réussite des tests |
| BR-008 Sécurisation de l'accès aux données | FR-007 Fonctionnalités futures | US-21 | - | Authentification | Nombre d'utilisateurs autorisés |
| BR-008 Sécurisation de l'accès aux données | FR-007 Fonctionnalités futures | US-22 | - | Gestion des utilisateurs | Nombre de rôles configurés |
| BR-008 Sécurisation de l'accès aux données | FR-007 Fonctionnalités futures | US-23 | - | Application Web | Nombre d'utilisateurs actifs |

---

# Correspondance des identifiants

## Business Requirements

| ID | Description |
|----|-------------|
| BR-001 | Centralisation des données carburant |
| BR-002 | Historisation des transactions |
| BR-003 | Contrôle du stock théorique |
| BR-004 | Contrôle du stock physique |
| BR-005 | Mesure des écarts |
| BR-006 | Analyse de la consommation par asset |
| BR-007 | Identification des anomalies |
| BR-008 | Sécurisation de l'accès aux données |

---

## Functional Requirements

| ID | Description |
|----|-------------|
| FR-001 | Import des données |
| FR-002 | Validation des données |
| FR-003 | Gestion des transactions |
| FR-004 | Gestion des stocks |
| FR-005 | Reporting |
| FR-006 | Qualité des données |
| FR-007 | Fonctionnalités futures |

---

## Règles Métier

| ID | Description |
|----|-------------|
| RM-001 | Mouvement unique |
| RM-002 | Quantité positive |
| RM-003 | Asset valide |
| RM-004 | Correction traçable |
| RM-005 | Historisation obligatoire |
| RM-006 | Validation avant alimentation des dimensions |
| RM-007 | Contrôle kilométrique |
| RM-008 | Contrôle des index |

---

# Vérification de la couverture

La matrice doit être mise à jour à chaque évolution du produit.

Avant chaque version, vérifier que :

- chaque Business Requirement est couvert par au moins une Functional Requirement ;
- chaque Functional Requirement est couverte par une ou plusieurs User Stories ;
- chaque User Story possède une implémentation dans le modèle de données ou le pipeline ELT ;
- chaque KPI est alimenté par une table du Data Warehouse ou d'un Data Mart ;
- chaque règle métier est implémentée dans les traitements SQL ou Python.

---

# Maintenance

La Requirements Traceability Matrix est un document vivant.

Elle doit être revue :

- lors de la création d'une nouvelle User Story ;
- lors de l'ajout d'une nouvelle règle métier ;
- lors de chaque nouvelle version (V1, V2, V3) ;
- avant toute mise en production.