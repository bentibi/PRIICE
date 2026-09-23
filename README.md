# PRIICE

**Plateforme de Recherche, d’Investigation, d’Identification et de Corrélation d’Entités**  
**Platform for Research, Investigation, Identification & Correlation of Entities**

PRIICE est une plateforme open-source d’investigation OSINT conçue pour partir d’une personne, d’une organisation ou d’une infrastructure numérique, agréger des informations publiques, les structurer en entités, relier ces entités et produire une investigation sourcée, lisible et reproductible.

## Vision

L’objectif de PRIICE est de simplifier l’investigation multi-source : l’utilisateur commence par une entité, consulte une fiche synthétique, pivote vers les éléments liés, visualise les relations uniquement lorsqu’il en a besoin et génère un rapport d’investigation sourcé.

Le graphe n’est donc pas l’interface principale : PRIICE privilégie une navigation guidée par entités, sources et pivots.

## MVP S1 — PRIICE Core

- création et gestion de dossiers d’investigation ;
- entités initiales : Personne, Organisation, Domaine, Adresse IP ;
- au moins 5 mécanismes ou connecteurs OSINT ;
- normalisation des résultats ;
- provenance systématique des données ;
- relations et navigation par pivot ;
- fiches d’entités ;
- graphe filtrable ;
- statuts de relation : confirmé, probable, à vérifier, hypothèse, rejeté ;
- génération automatique d’un rapport sourcé ;
- déploiement reproductible via Docker Compose ;
- documentation technique et utilisateur.

## Vision S2 — PRIICE Intelligence

- Entity Resolution et déduplication avancées ;
- scoring explicable ;
- timeline enrichie ;
- présence publique et pseudonymes ;
- Threat Intelligence / STIX ;
- collaboration et historique d’investigation ;
- watchlists et détection d’évolution ;
- rapports avancés.

## Stack envisagée

- Backend : Python / FastAPI
- Frontend : React / TypeScript
- Base de données : PostgreSQL
- Tâches asynchrones : Redis + Celery/RQ si nécessaire
- Déploiement : Docker / Docker Compose
- Reverse proxy : Caddy ou Nginx
- CI/CD : GitHub Actions

## Structure du dépôt

```text
backend/
frontend/
connectors/
docs/
```

## Cadre d’utilisation

PRIICE traite des informations accessibles dans un cadre légitime depuis des sources ouvertes. Le projet n’est pas conçu pour contourner des mécanismes d’accès, collecter des secrets, exploiter des données volées, harceler ou automatiser du doxxing.

## Statut

Side Quest M1 2026-2027 — École 2600.  
Phase actuelle : cadrage et constitution de l’équipe.
