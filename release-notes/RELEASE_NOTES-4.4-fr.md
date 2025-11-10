# October 2025 - Version 4.4

yuzSection 4.4.6 et suivantes

# 4.4.6

## Améliorations

- Vous pouvez désormais filtrer par entités sur le tableau des balances de clients.

# 4.4.7 (6 novembre) et 4.4.8 (10 novembre)

- Amélioration de la taille de la colonne "mois" (analytiques)
- Tables :
  - correction du rendu lorsque la table a une barre de défilement horizontale
  - correction du rendu lorsque la table a une hauteur plus grande que celle de l'écran (ce qui peut typiquement se produire si vous définissez un tableau de bord analytiques sur un certain écran puis que vous le consultez sur un autre écran).
- Purchase invoice :
  - correction du bouton pour "Corriger le prix d'achat" de *toutes* les réceptions
 

## Corrections



yuzSection Stock

## Définir l'action de préparation client par défaut pour les réceptions

A partir de l'écran `Administration > Gestion du stock`, vous pouvez désormais configurer une action par défaut concernant les réservations client pour l'édition de vos réceptions.

![Default reception configuration](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/default-reception-configuration.webp?w=640px)

## Annulation de préparations

Nous avons ajouté la possibilité d'annuler des préparations clients depuis l'écran `Stock > Réservation client`.

![Cancel reservations](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/cancel-reservations.webp?w=640px)

![Cancel reservations modal](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/cancel-reservation-modal.webp?w=480px)

yuzSection Catalogue

## Source de données

Nous avons ajouté la possibilité de visualiser les sources de données qui ont aidé à construire la fiche d'un produit.

![Data source item details](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/data-source-item-details.webp?w=640px)

![Data source modal](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/data-source-modal.webp?w=640px)

Voici la liste des différentes source de données:

- Mise à jour automatique: Mise à jour automatique par Yuzer
- Import local: Import à partir de fichiers via le menu catalogue.
- Intelligence artificielle: Fonction bêta.
- Enrichissement: Des règles d'enrichissement ont été appliquées.
- Édition communautaire: Édition manuelle provenant des autres entités différentes ayant un droit d'écriture sur le catalogue.
- Édition manuelle: Édition manuelle faite par l'éditeur du catalogue.

Ces sources de données sont listées par ordre de priorité. C'est à dire qu'un libellé défini par une édition manuelle remplace un libellé provenant d'un import local.

## Règles d'enrichissements

Nous avons ajouté la condition `est vide` dans la définition de règles.

![Enrichment rules](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/enrichment-rules-is-empty-condition.webp?w=480px)

yuzSection Intégrations

## CUBE

### Configuration des règles de marges à l'achat

Dans l'onglet `Marges à l'achat` d'un catalogue, une nouvelle option permet désormais d'interpréter la valeur configurée comme un coefficient diviseur du prix TTC.
Ainsi, la marge calculée sera égale à `Prix TTC / coefficient`.

![Catalog margin rules](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/catalog-margin-rules.webp?w=640px)

### Intégration des commandes

L'intégration de commandes avec le système de CUBE est maintenant disponible.

Pour l'activité:

1. Allez dans le menu `Administration > Fournisseurs`.

2. Recherchez le fournisseur CUBE.

![Cube supplier config](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/cube-supplier-config-1.webp?w=640px)

3. Éditez et sélectionnez le service de commande pour le catalogue CUBE.

![Cube supplier config edit](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/cube-supplier-config-2.webp?w=640px)

### Synchronisation des stock de vélos

Une fois que vous avez un accès CUBE valide, un batch se lance toutes les nuits pour synchroniser votre stock de vélo dans le système de CUBE.
Concrètement, vous retrouverez vos dossiers vélo ouverts dans le système CUBE.

### Configuration de l'accès

![Cube acess](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.4/cube-access.webp?w=480px)

Nous avons ajouté la possibilité de renseigner votre ID de point de vente.
Si vous gérez plusieurs points de vente, l'ID définit:

- l'adresse de livraison utilisée lors du passage de commandes.
- le point de vente cible pour la synchronisation des stocks de vélos.

Si aucun ID de point de vente n'est renseigné, celui défini par défaut chez CUBE sera utilisé pour les commandes.

|| Ce champs est touefois obligatoire pour activer la synchronisation des stocks.

yuzSection Général

## Améliorations

- Lorsque cliquez sur la notification d'appel entrant, si la fiche cliente n'existe pas, vous êtes maintenant redirigé vers le formulaire de création d'une fiche contact.
- Vous pouvez désormais filtrer par entités dans la balance des clients.
- Lors d'un paiement avec un terminal Yuzer Pay, un message d'erreur est désormais affiché quand la caisse sélectionnée n'est pas associée au terminal.
- Il est désormais possible de modifier la marque sur la fiche d'un produit identifié.

## Corrections

- Diverses corrections sur les tableaux analytiques.
- Diverses corrections concernant les écrans de commandes et réceptions.
