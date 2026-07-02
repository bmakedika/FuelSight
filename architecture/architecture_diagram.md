# Architecture Diagram

## Vue d'ensemble

FuelSight suit une architecture ELT permettant de transformer les données opérationnelles carburant en indicateurs décisionnels.

## Architecture cible

```
+--------------------+
|   Fuel Operator    |
+---------+----------+
          |
          v
+--------------------+
|   Google Sheets    |
| (Source unique)    |
+---------+----------+
          |
          v
+--------------------+
|  Export CSV        |
+---------+----------+
          |
          v
+--------------------+
| PostgreSQL RAW     |
+---------+----------+
          |
          v
+--------------------+
| PostgreSQL STAGING |
+---------+----------+
          |
          v
+--------------------+
| Data Warehouse     |
| (Star Schema)      |
+---------+----------+
          |
          v
+--------------------+
| Data Mart          |
+---------+----------+
          |
          v
+--------------------+
| Power BI           |
+---------+----------+
          |
          v
+--------------------+
| Fleet Manager      |
+--------------------+
```

## Description des couches

### Source

Google Sheets constitue la source officielle des données.

### RAW

Stockage des données brutes sans transformation.

### STAGING

Nettoyage et validation des données.

### Data Warehouse

Organisation des données selon un modèle dimensionnel.

### Data Mart

Optimisation des analyses métier.

### Power BI

Consommation des indicateurs et des KPI.

## Sécurité

- Contrôle des accès Google Sheets
- Authentification PostgreSQL
- Historisation des modifications