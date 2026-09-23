# Connectors

Les connecteurs fournissent une interface modulaire entre PRIICE et les sources externes.

Chaque connecteur devra documenter :

- les types d’entrée acceptés ;
- les types d’entités produites ;
- la source et la provenance ;
- les limitations et conditions d’accès ;
- les délais / rate limits ;
- les erreurs possibles.

Le MVP visera au minimum cinq mécanismes de collecte, parmi : DNS, RDAP, ASN, certificats TLS, sous-domaines, registres d’organisations, Web public ou autres sources ouvertes compatibles.
