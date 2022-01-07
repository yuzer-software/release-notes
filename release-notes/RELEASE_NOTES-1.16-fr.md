# Janvier 2022 - Version 1.16.0

# Configuration du type d'entité

En préambule d'améliorations sur le transfert de pièces inter-entité Yuzer vous permet de définir sur chacune des entités définies son type:

- Société mère: Société mère indépendante
- Filliale: Société indépendante filliale d'une société mère ou d'une autre filliale
- Établissement / succursale: établissement indépendant (numéro de siret indépendant mais siren égal à l'entreprise)
- Entité logique: Découpage logique dans Yuzer pour structuration sans existance légale spécifique.

L'objectif est de permettre à terme un transfert de stock sans génération de documents entre entité logiques, ou à l'aide de génération de rétrocessions entre établissements. L'échange de pièces entre sociétés nécessite l'établissement d'une facturation et devra être fait via une vente classique.

## C'est corrigé

-
