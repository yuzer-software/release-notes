# Juillet 2021 - Version 1.8.0

## Paniers

- Vous pouvez désormais envoyer un panier véhicule à l'atelier même si le véhicule n'a pas de VIN associé (par exemple parce qu'il est en commande).

## Sélection d'un client (tâches, panier, etc.)

- Lors de la sélection d'un client, les véhicules de celui-ci sont désormais affichés.

- Dans certains cas, il est nécessaire de sélectionner à la fois client et un de ses véhicules. C'est pourquoi il est dorénavant possible de sélectionner le véhicule en même temps que le client.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/select-user-modal.png"/>

## Configuration de valeurs par défaut pour les prêts

- Dans la partie administration il y a maintenant un nouvel onglet "Configuration des prêts de véhicules" qui permet de configurer des valeurs par défaut
  pour les différents types de prêts.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loans-config.png"/>

## Ajouts des coûts de préparation et maintenance dans le calcul de marge d'un véhicule

Lorsqu'une cession de préparation ou maintenance est facturée, le montant impacte désormais la marge du véhicule. La liste de cessions est visible sur la fiche du dossier de véhicule.
A noter que les cessions qui ne sont pas facturées ne sont pas pris en compte et une icone d'alerte est affichée à la place du montant.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/dealer-file-cessions.png"/>

Aussi, lors de l'édition d'un document sur une vente véhicule, un message d'alerte sera affiché si Yuzer détecte qu'une cession lié au dossier véhicule n'a pas été facturé.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/billing-document-warning.png"/>
