# Aout 2022 - Version 1.32.0

## Recherches

Nous avons amélioré la recherche dans l'application: il est désormais possible de filtrer sur plusieurs choix d'un même type (par exemple de rechercher tous les dossiers de 2018 et 2020 comme illustré ci-dessous).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/multi-select-search.png" width="120px"/>

## Panier

Dorénavant, Au moment de la génération de la facture, les biens non livrés seront automatiquement réservé/commandé.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/basket-auto_deliver.png"/>

### Ma Marge

Vous aviez l'habitude de voir la marge réalisée par l'entreprise sur le panier. Lorsque plusieurs utilisateurs ont modifié un même panier, la marge réalisée grâce à l'utilisateur courant est désormais affichée comme "Ma marge" en dessous de la marge globale du panier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/my-margin.png" width="1024px"/>

### Statut des paniers

- Le statut de stock des paniers est maintenant reporté par groupe de facturation.
- Sur la liste des paniers, les différents status des groupes de facturations sont affichés : par exemple, ci-dessous, la première ligne indique que tous les groupes de facturation du panier sont "ouverts", "préparés" et "sans paiement"; la deuxième ligne indique que les groupes de facturation sont tous "facturés ou ouvert", "préparé ou traité", "sans paiement ou payés".


<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/basket-statuses.png" width="180px"/>

Remarquez au passage que, comme déjà mentionné, la recherche permet de filtrer plusieurs status du même type (par exemple tous les paniers avec du stock préparé ou réservé).

### Payer plusieurs factures avec un seul paiement

Il est maintenant possible de régler les paiements de plusieurs factures en une seule fois.

Pour ce faire, depuis la fiche contact, cliquer sur "Ajouter des paiements"

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/multi-payment-button.png"/>

Puis dans la fenêtre de paiements, vous pouvez choisir les factures que vous souhaitez solder.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/multi-payment-modal.png"/>

Les remboursements sont maintenant accessibles en utilisant le switch en haut à gauche de la même fenêtre d'ajout de paiement.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/multi-payment-refund.png"/>

## Transferts entre compagnies ou succursales.

Il est enfin possible de suivre le transfert de stock résultant d'une ventre entre vos compagnies ou succursales. Pour faire court:
* Créez un panier pour la société destinatrice
* Éditez un bon de commande ou une facture — des transferts sont créés avec les informations spécifiées
* Allez côté transfert pour Emballez et Envoyez les transferts
* Le destinataire peut aller dans ses transferts pour commencer la réception.

Voici le détail de ces étapes. Faites comme d'habitude votre panier avec comme client la société qui devra recevoir le stock. Vous pouvez préparer le stock en utilisant les fonctionnalités habituelles du panier. Notez que ce processus vous permet donc aussi de commander une pièce pour une autre de vos sociétés tout en gardant la traçabilité complète de la commande jusqu'au transfert.

Enfin, pour réaliser le transfert, il vous suffit d'éditer votre facture (ou un bon de livraison). La fenêtre de gestion du stock s'ouvrira, comme d'habitude, avec une nouvelle option pour configurer (ou désactiver) le transfert (cf. **A** sur l'image "Gestion de stock du panier"). les informations de transfert (cf. **A** sur l'image "Gestion de stock du panier" et l'image "Nouveau transfert"). Lorsque vous cliquez sur "Livrer", un transfert sera créé d'où le stock est prélevé. Dans l'exemple ci-dessous, le premier produit est prélevé de l'entrepôt _Dock 1_ (**B**) et le deuxième produit est prélevé de l'entrepôt _Dock 2_ (**C**).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/basket-modal-on-transfer.png" width="1024px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/new-transfer-from-basket.png" width="800px"/>

Puisque nous avons configuré nos transferts pour qu'ils soient livrés à l'entrepôt _Stockage_, nous avons bien deux nouveaux transferts (créés après édition de la facture). Il n'y a qu'une seule action possible sur cette page: il faut emballer puis envoyer les transferts — même si c'est pour devoir les annuler en effectuant un retour. Le destinataire peut alors consulter ses transferts et commencer la réception de ses pièces.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/new-transfers.png" width="1024px"/>

Côté panier, il est possible d'accéder aux transferts correspondant aux différentes lignes depuis l'affichage de statut de stock.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.32.0/basket-transfer-links.png" width="1024px"/>

## Comptabilité

* Le nom de la caisse a été ajoutée à l'écran des détails journaliers
* La date d'échéance a été ajoutée à l'affichage du journal

## Corrections

* Correction du total des paniers véhicules sur l'écran de liste des paniers
* Correction du rafraichissement des status de paiement des paniers
* Il n'est plus possible de supprimer l'emplacement entrepôt d'un dossier
* Correction d'un bug qui empêchait les événements de mouvement de stock de se charger
* Correction d'un bug pouvant fausser la valeur du mois de la date d'échéance lors de l'export d'un journal.
* Il est à nouveau possible de rembourser un client à partir de la fenêtre de paiement de la fiche d'un contact
