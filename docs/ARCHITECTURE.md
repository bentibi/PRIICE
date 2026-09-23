# Architecture PRIICE

## Principes

PRIICE adopte une architecture Web modulaire afin de séparer l’interface, l’API, la persistance et les connecteurs de collecte. Une source externe ne doit pas devenir une dépendance structurelle du projet.

## Flux principal

Utilisateur → Frontend → API → Orchestrateur → Connecteurs → Normalisation → Base de données → Corrélation → Restitution.

## Stack cible

- Frontend : React / TypeScript
- Backend : Python / FastAPI
- Base : PostgreSQL
- Asynchrone : Redis + Celery/RQ si nécessaire
- Déploiement : Docker / Docker Compose
- Reverse proxy : Caddy ou Nginx
- CI/CD : GitHub Actions

## Modèle de domaine

- Case / Investigation
- Entity
- Relationship
- Source
- Note
- Event
- Report

## Entités MVP

- Personne
- Organisation
- Domaine
- Adresse IP

## Connecteurs

Chaque connecteur doit déclarer :
- ses types d’entrée ;
- les données qu’il produit ;
- les limites et délais ;
- les erreurs possibles ;
- la provenance des résultats.

## Corrélation

- pas de fusion irréversible sur un simple nom similaire ;
- relations candidates avec statut et justification ;
- score éventuel explicable ;
- validation, rejet ou maintien en hypothèse par l’analyste ;
- provenance conservée.

## UX

- fiche d’entité comme vue principale ;
- pivots en un clic ;
- graphe filtrable comme vue secondaire ;
- timeline pour les événements datés ;
- rapport distinguant faits, hypothèses, sources et notes.

## Sécurité

- secrets hors dépôt ;
- validation stricte des entrées ;
- principe du moindre privilège ;
- journalisation sans secrets ;
- timeouts et quotas sur les connecteurs ;
- contrôle des dépendances ;
- aucune fonction de contournement d’accès privé ou d’authentification.
