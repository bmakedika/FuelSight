# Configuration Guide

## Objectif

Décrire la configuration de FuelSight.

---

# Variables d'environnement

Créer un fichier :

```
.env
```

Exemple :

```
DB_HOST=localhost

DB_PORT=5432

DB_NAME=fuelsight

DB_USER=postgres

DB_PASSWORD=********
```

---

# Google Sheets

Configurer :

- le document source
- les droits d'accès
- le dossier Google Drive

---

# Docker

Les paramètres Docker sont définis dans :

```
docker-compose.yml
```

---

# Power BI

Configurer :

- connexion PostgreSQL
- fréquence de rafraîchissement