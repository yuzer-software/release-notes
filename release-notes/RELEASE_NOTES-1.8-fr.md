# Juillet 2021 - Version 1.8.0

- Amélioration du support de certaines plaques d'immatriculations de type A-00-A.
- Vous pouvez désormais envoyer la préparation d'une vente véhicule à l'atelier avec un modèle de véhicule (sans VIN associé).
- Vous pouvez désormais utiliser la molette de la souris pour modifier les quantités.
- Vous pouvez changer le status des tâches directement de _à faire_ à _fait_ sur les listes de tâches.

## Paniers

- Vous pouvez désormais envoyer un panier véhicule à l'atelier même si le véhicule n'a pas de VIN associé (par exemple parce qu'il est en commande).

## Sélection d'un client (tâches, panier, etc.)

- Lors de la sélection d'un client, les véhicules de celui-ci sont désormais affichés.
- Dans certains cas, il est nécessaire de sélectionner à la fois client et un de ses véhicules. C'est pourquoi il est dorénavant possible de sélectionner le véhicule en même temps que le client.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/select-user-modal.png" width="100%"/>

## Complétion du document de prêt véhicule

Nous avons ajouté de nouvelles informations dans le document de prêt de véhicule:

- La date de début (date à laquelle est généré le document)
- La date de fin (calculée à partir de la date précédente ainsi que la durée du prêt)
- Distance maximale
- Frais journalier
- Frais de carburant

### Configuration de valeurs par défaut pour les prêts

- Dans la partie administration il y a maintenant un nouvel onglet "Configuration des prêts de véhicules" qui permet de configurer des valeurs par défaut pour les différents types de prêts.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loans-config.png"/>

### Démarrage du prêt

Lorsque vous démarrez un prêt, Yuzer pré-rempli les champs ajoutés à l'aide des informations configurées par défaut. Vous pouvez alors les ajuster de manière spécifiques pour votre client.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loan-start-modal.png" width="100%"/>

Les informations sont alors ajoutées à votre document de prêt.

<div class="d-flex justify-content-center">
    <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loan-start-modal.png"/>
</div>

## Ajouts des coûts de préparation et maintenance dans le calcul de marge d'un véhicule

Lorsqu'une cession de préparation ou maintenance est facturée, le montant impacte désormais la marge du véhicule. La liste de cessions est visible sur la fiche du dossier de véhicule.
A noter que les cessions qui ne sont pas facturées ne sont pas pris en compte et une icone d'alerte est affichée à la place du montant.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/dealer-file-cessions.png"/>

Aussi, lors de l'édition d'un document sur une vente véhicule, un message d'alerte sera affiché si Yuzer détecte qu'une cession lié au dossier véhicule n'a pas été facturé.

<div class="d-flex justify-content-center">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/billing-document-warning.png"/>
</div>

# Nouvelle disposition de l'écran d'édition de panier

Les groupes de facturation sont désormais placés dans des onglets pour une meilleure lisibilité.

Vous pouvez toujours effectuer le déplacement des lignes du panier à travers les groupes par un drag-and-drop. Dans le cas ou plusieurs groupes de facturation cible sont présent il vous faudra dans un premier temps pré-selectionner le groupe cible.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/basket-tabs-multi.gif" width="100%"/>

# C'est corrigé

- Yuzer n'empêchait pas l'utilisateur de générer deux documents de reprise pour le même véhicule à partir de deux paniers de reprise différents.
