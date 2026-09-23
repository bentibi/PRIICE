# Architecture initiale

## Vue d’ensemble

PRIICE adopte une architecture Web modulaire séparant présentation, logique métier, collecte et persistance.

```text
Utilisateur
   ↓
Frontend React / TypeScript
   ↓ REST API
Backend Python / FastAPI
   ↓
Orchestrateur d’enrichissement
   ↓
Connecteurs OSINT
   ↓
Normalisation
   ↓
PostgreSQL
   ↓
Corrélation / validation
   ↓
Fiche entité / Graphe / Timeline / Rapport
```

## Modèle de domaine

### Case
Dossier d’investigation : titre, description, statut, dates, propriétaire.

### Entity
Objet investigué ou découvert : type, valeur canonique, attributs, statut.

### Relationship
Lien typé entre deux entités : type, statut, confiance, justification.

### Source
Origine d’une information : type, nom, URL/référence, date de collecte, métadonnées.

### Note
Annotation d’un analyste sur un dossier ou une entité.

### Event
Événement daté utilisé dans la timeline.

### Report
Rapport généré depuis un dossier d’investigation.

## Types d’entités MVP

- Personne
- Organisation
- Domaine
- Adresse IP

## Principes de corrélation

- pas de fusion irréversible sur un nom similaire ;
- une relation candidate conserve sa justification ;
- un score éventuel doit rester explicable ;
- l’analyste peut confirmer, rejeter ou conserver une hypothèse ;
- la provenance est conservée après validation.

## API initiale envisagée

- `/cases`
- `/entities`
- `/relationships`
- `/sources`
- `/connectors`
- `/reports`

## Déploiement S1

Docker Compose monohôte :

- reverse proxy ;
- frontend ;
- backend ;
- PostgreSQL ;
- Redis / worker uniquement si nécessaire.

Les microservices et une base graphe spécialisée ne sont pas retenus par défaut au S1 afin de limiter la complexité.
