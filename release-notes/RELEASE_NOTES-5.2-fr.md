# Juillet 2026 - Version 5.2

yuzSection Cartes cadeaux

Nous avons amélioré la gestion des cartes cadeaux : il est désormais possible de vendre une carte cadeau et d'enregistrer un paiement avec une carte cadeau gérée par une entité partageant une gestion juridique (succursale ou entité logique).

## Configuration

La configuration d'un moyen de paiement de type carte cadeau a été modifiée afin de permettre de créer une configuration utilisant une carte cadeau gérée par une autre entité du groupe.

![gift-card-config-1-select-type](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.2/gift-card-config-1-select-type.webp?w=896px)

Une configuration de carte cadeau gérée par une entité du groupe signifie que c'est cette entité qui gère et génère les séquences de codes-barres. L'entité pour laquelle la configuration est créée, quant à elle, ne peut que vendre la carte et l'utiliser comme moyen de paiement.
Dans la configuration, l'entité sélectionnable partage obligatoirement la même gestion juridique que l'entité courante. Il en va de même pour la carte cadeau cible : seules les cartes cadeaux configurées comme moyen de paiement par l'entité cible sont proposées.

![gift-card-config-2-select-gift-card](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.2/gift-card-config-2-select-gift-card.webp?w=896px)

À noter que lors de la sélection de la carte cadeau cible, une aide a été implémentée pour pré-remplir automatiquement les champs libellé, numéro de compte et code journal, dans la mesure du possible, avec les mêmes valeurs que celles définies par l'entité sélectionnée.

![gift-card-config-3-filled](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.2/gift-card-config-3-filled.webp?w=896px)

yuzSection Général

## Administration

- Il est maintenant possible d'assigner un même numéro comptable pour différents fournisseurs
- Ajout de la possibilité de configurer l'export comptabilité pour Honda et Suzuki.

## Comptabilité

- Affichage de la marque sur les lignes du dossier de produit identifié de la facture d'achat.
- Amélioration de la configuration des journaux. La configuration des journaux peuvent désormais hériter de l'entité parent. Il est également possible de supprimer un journal.
- Correction du filtre min-max pour la liste des soldes clients
- Amélioration sur les filtres pour le rapprochement de réceptions sur la facture d'achat.
- Il est désormais possible de mettre à jour la référence d'un numéro de dossier sur une facture d'achat ayant été validée.

## Panier

- Possibilité d'ajouter les frais de carte grises sur une ligne de panier sans dossier
- Correction de l'affichage de l'avertissement relatif à l'exonération de TVA sur le panier.
- Il n'est plus possible de prendre un paiement d'un montant de ZÉRO.

## Produits

- Ajout de la catégorie airbag pour les motocycles
- Correction des conflits lors de la synchronisation de dossiers de produits identifiés

## Divers

- Correction de l'affichage de l'icône de l'utilisateur dans les cellules de tableaux
- Correction de certains filtres de prix qui interprétaient les montants exprimés en centimes (valeur × 100).
