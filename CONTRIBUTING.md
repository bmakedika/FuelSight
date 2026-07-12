# Contribuer à FuelSight

## Documentation

Le point d'entrée de toute la documentation est [docs/README.md](docs/README.md). Chaque dossier possède aussi son propre `README.md` local décrivant son contenu et ses conventions.

## Convention de commits

FuelSight suit [Conventional Commits](https://www.conventionalcommits.org/), avec la règle : **une action = un commit**.

Types utilisés :

| Type | Usage |
|---|---|
| `feat` | Ajout d'une fonctionnalité |
| `fix` | Correction d'un bug ou d'un affichage cassé |
| `docs` | Ajout ou modification de documentation |
| `chore` | Mise en place, configuration, réorganisation |
| `test` | Ajout ou modification de tests |
| `refactor` | Réécriture sans changement de comportement |
| `style` | Mise en forme, sans impact fonctionnel |
| `perf` | Amélioration de performance |

Exemple :

```
feat(ingestion): ajout du script d'export Google Sheets vers CSV
```

Pour rattacher un commit à une User Story du [Product Backlog](docs/governance/FuelSight_Product_Backlog.pdf), ajouter une référence en pied de message :

```
feat(ingestion): ajout du script d'export Google Sheets vers CSV

Ref: US-01
```

## Versioning

Le projet suit [SemVer](https://semver.org/) : les versions `0.x.x` correspondent à la phase de mise en place (pré-MVP), la version `1.0.0` marque le MVP fonctionnel (périmètre V1 du [Backlog](docs/governance/FuelSight_Product_Backlog.pdf)).

Les changements sont documentés dans le `CHANGELOG.md`, au format [Keep a Changelog](https://keepachangelog.com/).

## Workflow de développement d'une User Story

1. Partir de `main` à jour.
2. Créer une branche dédiée : `feature/<id-story>-<résumé-court>` (ex. `feature/us-01-export-csv`).
3. Développer par commits atomiques (`feat`, `fix`, `test`...).
4. Vérifier que les tests passent (voir [tests/README.md](tests/README.md)).
5. Fusionner dans `main`.
6. Une fois tout le périmètre d'une version livré, poser un tag Git correspondant (ex. `v1.0.0`).

## Langue

La documentation est rédigée en français ; les termes techniques établis (Business Case, ADR, Star Schema, etc.) sont conservés en anglais.
