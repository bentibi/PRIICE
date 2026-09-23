# Roadmap PRIICE

## S1 — PRIICE Core

Objectif : obtenir un MVP complet, démontrable de bout en bout.

### Cadrage
- benchmark des outils existants ;
- définition des besoins ;
- modèle d’entités et de relations ;
- architecture ;
- maquettes UX ;
- backlog et critères d’acceptation.

### Socle
- FastAPI ;
- React / TypeScript ;
- PostgreSQL ;
- Docker Compose ;
- CI initiale.

### Fonctionnalités cœur
- dossiers d’investigation ;
- Personne, Organisation, Domaine, Adresse IP ;
- relations typées ;
- sources et dates de collecte ;
- notes analyste ;
- navigation par pivot ;
- graphe filtrable ;
- statuts de confiance.

### Collecte
- framework de connecteurs ;
- au moins 5 mécanismes de collecte OSINT ;
- normalisation ;
- gestion des erreurs, délais et limitations.

### Restitution
- vue synthétique ;
- rapport HTML sourcé ;
- export PDF si le planning le permet.

### Qualité
- tests automatisés sur fonctions critiques ;
- validation des entrées ;
- gestion des secrets ;
- documentation utilisateur et technique ;
- tests utilisateurs et itération UX.

## S2 — PRIICE Intelligence

Objectif : enrichir PRIICE sans dégrader la simplicité du produit.

- Entity Resolution ;
- déduplication avancée ;
- scoring explicable ;
- timeline enrichie ;
- recherche étendue de présence publique ;
- pseudonymes et comptes publics ;
- collaboration ;
- historique d’investigation ;
- watchlists et détection d’évolution ;
- Threat Intelligence ;
- STIX ;
- rapports avancés ;
- API externe documentée.
