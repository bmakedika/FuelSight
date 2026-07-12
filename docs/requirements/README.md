# Requirements

Ce dossier détaille les exigences fonctionnelles, non fonctionnelles et de reporting, ainsi que leur traçabilité.

## Objectif

Décliner les besoins métier (`gouvernance/business_requirements.md`) en exigences techniques précises et traçables.

## Structure

- [Functional Requirements](functional_requirements.md) - FR-001 à FR-007, avec User Stories associées
- [Non Functional Requirements](non_functional_requirements.md) - NFR-001 à NFR-008 (performance, sécurité, maintenabilité...)
- [Data Requirements](data_requirements.md) - sources, zones, qualité, intégrité, traçabilité
- [Reporting Requirements](reporting_requirements.md) - RR-001 à RR-006, exigences des dashboards
- [Requirements Traceability Matrix](requirements_traceability_matrix.md) - traçabilité BR ↔ FR ↔ US ↔ RM ↔ Data Model ↔ KPI

## Convention de nommage

Identifiants préfixés par domaine : `BR-XXX` (besoin métier, dans `gouvernance/`), `FR-XXX` (exigence fonctionnelle), `NFR-XXX` (non fonctionnelle), `RR-XXX` (reporting), `RM-XXX` (règle métier, RM-001 à RM-009, dans `architecture/data-model/`).
