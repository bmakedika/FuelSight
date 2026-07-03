# Use Cases

## Objectif

Décrire les principaux scénarios d'utilisation de FuelSight.

---

## UC-001

Nom

Enregistrer une réception carburant

Acteur principal

Fuel Operator

Précondition

Le carburant vient d'être réceptionné.

Scénario

1. L'opérateur ouvre Google Sheets.
2. Il sélectionne "Réception".
3. Il renseigne :
   - date
   - quantité
   - site
   - opérateur
4. Les données sont enregistrées.
5. Le pipeline les importe dans PostgreSQL.

Résultat attendu

La transaction est disponible dans le Data Warehouse.

---

## UC-002

Nom

Consulter les KPI de consommation

Acteur

Fleet Manager

Scénario

1. Ouvrir Power BI.
2. Sélectionner la période.
3. Filtrer par site.
4. Consulter :
   - consommation
   - stock
   - écarts