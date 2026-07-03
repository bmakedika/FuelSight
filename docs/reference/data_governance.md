# Data Governance

## Objectif

Définir les responsabilités liées aux données FuelSight.

## Rôles

### Fuel Operator

Responsabilités :

- Saisie des transactions
- Saisie des contrôles tank

### Fleet Manager

Responsabilités :

- Validation des données
- Analyse des KPI
- Correction des anomalies

### Product Owner

Responsabilités :

- Evolution du produit
- Priorisation du backlog

## Règles

### Création

Les données doivent être créées uniquement à partir du modèle officiel.

### Modification

Les données historiques ne doivent pas être modifiées.

### Correction

Toute correction doit être traçable.

### Suppression

Les suppressions sont interdites.

Une correction doit être enregistrée sous forme de nouvelle transaction.

## Qualité

Contrôles obligatoires :

- Date valide
- Quantité positive
- Asset existant
- Référentiel conforme

## Traçabilité

Chaque enregistrement doit conserver :

- Date création
- Auteur
- Date modification