# Glossaire

## Termes métier

### Asset

Équipement consommant du carburant.

Exemple :

- Véhicule
- Camion
- Générateur

### Dipstick

Mesure physique du niveau de carburant réalisée dans le réservoir.

### Écart

Différence entre stock théorique et stock physique.

### Fuel Transaction

Opération impliquant une entrée ou une sortie de carburant.

### Index pompe

Valeur numérique affichée par le compteur de distribution de carburant. L'écart entre deux index permet de déterminer le volume théorique distribué durant une période donnée.

### Location

Site opérationnel.

Exemples :

- Tshikapa
- Kananga

### Movement Type

Catégorie de mouvement enregistrée pour une Fuel Transaction (réception, distribution, transfert, correction).

### Odomètre

Compteur kilométrique d'un véhicule indiquant la distance totale parcourue. Utilisé pour calculer les indicateurs de consommation (litres par kilomètre).

### Stock Physique

Stock réellement observé dans le réservoir.

### Stock Théorique

Stock calculé à partir des mouvements enregistrés.

### Tank Measurement

Enregistrement combinant trois éléments réalisés lors d'un relevé : la mesure physique du niveau de carburant (Dipstick), le relevé des index de compteur de pompe (Index pompe), et le calcul d'écart éventuel entre stock théorique et stock physique.

Correspond à la table `raw_tank_measurements` du modèle de données.

## Rôles / Acteurs

### Fleet Manager

Responsable de la gestion opérationnelle de la flotte et du suivi des ressources associées.

### Fuel Operator

Personne responsable de la distribution du carburant ; également chargée de l'enregistrement des transactions et du suivi opérationnel des mouvements de stock.

### Receiver

Personne qui réceptionne ou atteste la quantité de carburant distribuée (chauffeur, vigile, réceptionnaire, ou toute personne chargée de confirmer l'opération).

## Termes techniques

### ADR (Architecture Decision Record)

Document qui enregistre une décision d'architecture importante, son contexte, les alternatives envisagées et ses conséquences.

### Data Mart

Sous-ensemble spécialisé du Data Warehouse destiné à répondre à un besoin analytique spécifique.

Exemple :

- Consommation carburant
- Contrôle des stocks
- Analyse des actifs

### Data Warehouse

Base de données optimisée pour l'analyse décisionnelle.

### ELT

Extract, Load, Transform.

### KPI

Indicateur Clé de Performance.

### RAW

Zone de stockage contenant les données importées sans modification ni transformation. Elle constitue la copie fidèle des données sources.

### Staging

Zone intermédiaire utilisée pour nettoyer, contrôler et normaliser les données avant leur intégration dans le Data Warehouse.

### Star Schema

Modèle dimensionnel composé d'une table de faits centrale reliée à plusieurs tables de dimensions. Optimisé pour les analyses et les outils de Business Intelligence.

## Projet & Processus

### FuelSight

Plateforme d'analyse décisionnelle dédiée à la gestion des opérations carburant.

### Operational Decision Making

Processus consistant à utiliser les données disponibles pour orienter les décisions quotidiennes liées à la gestion des ressources et des opérations.
