# Janvier 2022 - Version 1.16.8

## Améliorations diverses

- Vous pouvez désormais lors d'un export de stock exporter les emplacements, les catégories du produit ainsi que la date de dernière entrée en stock.

Sont considérées comme entrées en stock les réceptions, et, si le produit n'a pas de réceptions la date la plus ancienne d'inventaire ou initialisation.
Les retours (par panier négatif) n'impactent pas cette date.

# Janvier 2022 - Version 1.16.7

## C'est corrigé

- Les modifications sur l'export des commandes de la version précédente causaient une regression sur l'export excel et sur l'export d'un fichier texte sans header fixe.

# Janvier 2022 - Version 1.16.6

## Amélioration des exports de commandes

- Les configuration d'export de commandes ont été améliorées permettant de supporter les formats txt des commandes Triumph et Kawazaki et csv de KTM/Husqvarna/GasGas entre autres.
- Les commandes automatiques Honda sont désormais supportées par Yuzer et la création d'une commande dans Yuzer aura pour effet de créer la commande dans le système Honda.

## C'est corrigé

- Lorsqu'une réception définissait la préparation d'un produit client mais que celui-ci était annulé ou facturé avant la clôture de cette réception le produit apparaissait quand même comme préparé. C'est désormais corrigé et la réception sera en erreur sur la clôture nécessitant la suppression du lien avec la réservation client (celle-ci n'ayant plus lieux d'être).
- La coloration des ventes d'occasion dans le widget de ventes de dossiers ainsi que la répartition des mois de l'année n-1 a été corrigée.

# Janvier 2022 - Version 1.16.4

## C'est corrigé

- La mise à jour des informations de permis de conduire dans le cadre d'un nouveau prêt de véhicule échouait lors de la première saisie.
- L'ajout d'un nouveau widget de ventes dossier véhicules ou produit n'affichait pas correctement le widget depuis la possibilité d'ajouter de multiples types de dossier sur celui-ci.
- Quelques scénarios de validation de coherence dans les prix du paniers étaient trop stricts (la validation du prix incluant TVA validait uniquement le cas ou celle-ci était calculée depuis le prix HT ce qui pouvait dans certains cas d'arrondi poser un problème lorsque le prix HT était calculé depuis le prix TTC). Nous considérons donc valide les deux options désormais.

# Janvier 2022 - Version 1.16.3

## Améliorations diverses

- Nous avons amélioré et unifié l'expérience utilisateur sur plusieurs écrans d'imports de données.
- La recherche de client par numéro de client est désormais possible.
- Il est désormais impossible d'imprimer les étiquettes de stock si la configuration n'est pas sauvegardée au préalable.
- Nous avons ajouté le support des identifiants maritimes pour les moto-marines.
- Nous avons ajouté un ensemble d'attributs pour les moto-marines.

## Configuration du type d'entité

En préambule d'améliorations sur le transfert de pièces inter-entité, Yuzer vous permet de définir sur chacune des entités définies son type:

- Société mère: Société mère indépendante
- Filiale: Société indépendante filiale d'une société mère ou d'une autre filiale
- Établissement / succursale: établissement indépendant (numéro de Siret indépendant mais siren égal à l'entreprise)
- Entité logique: Découpage logique dans Yuzer pour structuration sans existence légale spécifique.

L'objectif est de permettre à terme un transfert de stock sans génération de documents entre entité logiques, ou à l'aide de génération de rétrocessions entre établissements. L'échange de pièces entre sociétés nécessite l'établissement d'une facturation et devra être fait via une vente classique.

## Affichage des éditeurs d'un contact

La personne ayant créé une fiche contact et la dernière personne l'ayant modifiée sont désormais affichés sur le détail de celle-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.16.0/contact-creator.png" height="90"/>

## Amélioration des widgets

Il est désormais possible de sélectionner plusieurs catégories dans le widget de chiffre d'affaire.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.16.0/turnover-widget-cat-selector.png" height="90"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.16.0/turnover-widget-cat-select.png" height="90"/>

Le widget de ventes permet quand à lui de cumuler les ventes de plusieurs types de dossiers (véhicules et vélos par exemple).

## Améliorations sur comptabilité:

### Gestion des dates d'échéance par fournisseur

Vous pouvez désormais configurer des configuration de dates d'échéances par fournisseur.

Lors de la création d'une facture d'achat, ou à l'édition de celle-ci, vous pouvez alors séléctionner une des configurations pré-définie.

### Nous avons ajouté des règles de comptabilité spécifiques pour les factures d'achat.

L'écran de configuration a été légèrement modifié et la sélection du type de règle s'effectue désormais à l'aide d'un selecteur.

Il est désormais possible de définir des règles spécifiques pour les achats intra-communautaires.

### Amélioration de l'export automatique comptable

Vous pouvez désormais exporter vos fichiers de tiers en sus de vos fichiers d'écriture comptable par ftp. De plus nous avons ajouté le libellé du moyen de paiement en tant que colonne sélectionnable dans les fichiers d'exports.

## C'est corrigé

- Sur les petits widget la configuration pouvait être tronquée. Le défilement a été correctement mis en place pour éviter le problème.
- Les paniers étaient mal re-synchronisé lorsqu'un VIN était affecté à un véhicule _à commandé_ ou _en commande_ causant une erreur lors du traitement du stock du panier.
- Les prix lors de l'ajout d'un dossier vélo ou autres produits identifiés dans un panier utilisent bien ceux du dossier et non du produit catalogue.
