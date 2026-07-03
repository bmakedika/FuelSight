# Data Requirements

## Objectif

Décrire les exigences relatives aux données.

---

# Sources

Les données proviennent de :

- Google Sheets
- Exports CSV

---

# Zones de données

- RAW
- STAGING
- Data Warehouse
- Data Mart

---

# Historisation

Les données RAW doivent être conservées sans modification.

Les corrections doivent être historisées.

---

# Qualité

Les contrôles obligatoires portent sur :

- quantités positives
- dates valides
- assets existants
- index cohérents
- kilométrages croissants

---

# Intégrité

Toutes les clés étrangères doivent référencer des dimensions existantes.

---

# Traçabilité

Chaque enregistrement doit conserver :

- date de création
- auteur
- date de modification
- auteur de modification

---

# Conservation

Les données historiques ne doivent jamais être supprimées.