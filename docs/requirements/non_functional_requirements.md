# Non Functional Requirements

## Objectif

Décrire les exigences de qualité de la solution.

---

# NFR-001 - Performance

Les traitements ELT doivent permettre la mise à jour quotidienne des indicateurs dans un délai compatible avec les besoins opérationnels.

---

# NFR-002 - Disponibilité

Les données doivent rester accessibles aux utilisateurs autorisés pendant les heures d'exploitation.

---

# NFR-003 - Fiabilité

Les traitements doivent être reproductibles.

Aucune perte de données ne doit être autorisée.

---

# NFR-004 - Maintenabilité

Le code doit être :

- documenté ;
- modulaire ;
- versionné avec Git.

---

# NFR-005 - Traçabilité

Toute correction doit pouvoir être retracée.

Les données RAW ne doivent jamais être modifiées.

---

# NFR-006 - Sécurité

L'accès aux données doit être limité aux utilisateurs autorisés.

Une authentification est prévue en V3.

---

# NFR-007 - Scalabilité

L'architecture doit permettre l'ajout :

- de nouveaux sites ;
- de nouveaux actifs ;
- de nouveaux tableaux de bord.

---

# NFR-008 - Portabilité

FuelSight doit pouvoir être déployé via Docker.