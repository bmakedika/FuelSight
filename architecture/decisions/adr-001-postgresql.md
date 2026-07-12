# ADR-001

## Décision

Utiliser PostgreSQL comme base de données principale.

## Statut

Acceptée

## Contexte

Le projet nécessite :

- un moteur SQL robuste ;
- un support analytique ;
- une compatibilité Power BI.

## Alternatives

- MySQL
- SQLite
- SQL Server Express

## Justification

PostgreSQL offre :

- stabilité ;
- performances analytiques ;
- coût nul ;
- forte adoption.

## Conséquences

Toute la couche ELT reposera sur PostgreSQL.