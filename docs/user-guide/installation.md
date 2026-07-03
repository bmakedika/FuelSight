# Installation Guide

## Objectif

Décrire les étapes nécessaires pour installer FuelSight dans un environnement local.

---

# Prérequis

Les logiciels suivants doivent être installés :

- Git
- Docker Desktop
- PostgreSQL (si Docker n'est pas utilisé)
- Python 3.13+
- Power BI Desktop

---

# Cloner le dépôt

```bash
git clone https://github.com/<username>/FuelSight.git

cd FuelSight
```

---

# Créer un environnement virtuel

```bash
python -m venv .venv
```

---

# Activer l'environnement

Windows

```bash
.venv\Scripts\activate
```

Linux

```bash
source .venv/bin/activate
```

---

# Installer les dépendances

```bash
pip install -r requirements.txt
```

---

# Lancer PostgreSQL

Via Docker :

```bash
docker compose up -d
```

---

# Vérifier la connexion

```bash
python scripts/check_database.py
```

---

# Installation terminée

FuelSight est prêt à être utilisé.