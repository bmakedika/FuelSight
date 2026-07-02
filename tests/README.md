# Tests

Ce dossier contient les tests du projet.

## Objectif

Garantir la qualité et la fiabilité des traitements.

## Structure

### Tests de validation

Vérification des règles métier.

Exemples :

- Quantité supérieure à zéro
- Date valide
- Asset existant

### Tests de cohérence

Exemples :

- Odomètre croissant
- Index pompe cohérent
- Stock non négatif

### Tests ELT

Validation du chargement :

- Raw → Staging
- Staging → Data Warehouse

### Tests SQL

Validation :

- Vues
- Tables de faits
- Dimensions

## Résultat attendu

Chaque exécution des tests doit produire :

- Nombre de tests exécutés
- Nombre de succès
- Nombre d'échecs
- Rapport d'erreurs
