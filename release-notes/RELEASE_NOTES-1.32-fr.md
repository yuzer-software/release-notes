# 3 Novembre 2022 - Version 1.32.12

## Correction

Lors de l'édition d'une cession, les cessions attachées au panier n'étaient pas rafraîchies et la nouvelle cession n'était donc pas prise en compte. Le stock, lui, avait correctement été impacté et rafraîchi. En conséquence, un message prétendait que le stock était désynchronisé avec les documents, et la fenêtre de gestion de stock permettait de "réparer" cette fausse desynchronization.

Si vous avez cliqué sur "Réparer les réservations" dans ce contexte, le stock et les documents ont probablement été désynchronisés en annulant le traitement du stock lié à la cession. Vous devrez alors probablement annuler la cession (le stock ne bougera pas puisqu'il a déjà été annulé) et rééditer la cession (le stock sera ainsi correctement traité).

# 26 Octobre 2022 - Version 1.32.10

## Correction

- Le prix d'achat total du panier n'était pas correctement caché en mode client.
- L'affichage du crédit client dans la boite de dialogue de paiement était celui du client principal du panier et non celui du groupe de facturation. Celui-ci était contrôlé par la suite mais cela pouvait entrainer une situation peu compréhensible.

# 16 Octobre 2022 - Version 1.32.9

## Correction

- Correction de l'affichage agrégé de certaines colonnes comme les noms de client dans les tables (analytique principalement), causant un mauvais chargement de l'écran.

# 10 Octobre 2022 - Version 1.32.8

## Statut des paniers

Sur la liste des paniers, les statuts de stock sont ceux des lignes de panier. Auparavant (à la 1.32.8), ces statuts étaient ceux des groupes de facturation, c'est-à-dire l'agrégation des statuts des lignes des groupes : si un panier avait un groupe de facturation avec deux lignes ayant des états de stock différents, un seul statut de stock était remonté. À présent, les deux statuts sont remontés.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/1.32.8-basket-status.png" width="250px"/>

# 2 Octobre 2022 - Version 1.32.7

## Amélioration de l'ergonomie de l'export des dossiers véhicules

Sur l'export des dossiers, lorsqu'un filtre sur la date de clôture est défini, les boutons de filtres "Tous", "Ouvert" ou "Clôturé" ne sont tout simplement plus disponibles, ce qui évite toute confusion relative au filtre.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/1.32.7-export.png" width="250px"/>

# Septembre 2022 - Version 1.32.6

## Correction

Lors d'un export de dossiers véhicules, les boutons de filtres "Tous" / "Ouvert" ou "Clôturé" écrasaient le filtre de sélection de date de clôture. Un nouveau bouton "Filtre" permet de résoudre ce problème.

# Septembre 2022 - Version 1.32.5

## Correction

- L'affichage de 'Ma marge' sur un panier est rafraîchi lors d'un changement de remise sur une ligne.
- Le filtre 'En stock' se désactive bien sur le catalogue de produits.

# Septembre 2022 - Version 1.32.4

## Correction

- de la facturation d'un produit non stockable à une autre entité du même compte Yuzer en l'absence d'autres produits stockables.

# Septembre 2022 - Version 1.32.3

## Recherches

Sur la liste des paniers, le sélecteur d'utilisateur (Créé par) a un champ de recherche.

## Corrections

- Le sélecteur de rôles attribués aux utilisateurs est réparé.
- La mise à jour des propriétés d'un produit est réparée.
- L'édition d'un bon de livraison ou d'une facture à une autre entité de votre de groupe pour certains types de paniers (dont véhicule) est réparée.
- Depuis la 1.32.2, sélectionner un filtre estompait la table, mais l'estompage était perdu lorsqu'on passait d'un filtre à un autre.

# Septembre 2022 - Version 1.32.2

## Recherches

Nous avons amélioré la recherche dans l'application: il est désormais possible de filtrer sur plusieurs choix d'un même type (par exemple de rechercher tous les dossiers de 2018 et 2020 comme illustré ci-dessous).

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/multi-select-search.png" width="120px"/>

## Panier

Dorénavant, Au moment de la génération de la facture, les biens non livrés seront automatiquement réservé/commandé.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/basket-auto_deliver.png"/>

### Ma Marge

Vous aviez l'habitude de voir la marge réalisée par l'entreprise sur le panier. Lorsque plusieurs utilisateurs ont modifié un même panier, la marge réalisée grâce à l'utilisateur courant est désormais affichée comme "Ma marge" en dessous de la marge globale du panier.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/my-margin.png" width="1024px"/>

### Statut des paniers

- Le statut de stock des paniers est maintenant reporté par groupe de facturation.
- Sur la liste des paniers, les différents statuts des groupes de facturations sont affichés : par exemple, ci-dessous, la première ligne indique que tous les groupes de facturation du panier sont "ouverts", "préparés" et "sans paiement"; la deuxième ligne indique que les groupes de facturation sont tous "facturés ou ouvert", "préparé ou traité", "sans paiement ou payés".

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/basket-statuses.png" width="180px"/>

Remarquez au passage que, comme déjà mentionné, la recherche permet de filtrer plusieurs statuts du même type (par exemple tous les paniers avec du stock préparé ou réservé).

## Transferts entre compagnies ou succursales.

Il est enfin possible de suivre le transfert de stock résultant d'une vente entre vos compagnies ou succursales. Pour faire court:

- Créez un panier pour la société destinatrice
- Éditez un bon de commande ou une facture — des transferts sont créés avec les informations spécifiées
- Allez côté transfert pour Emballez et Envoyez les transferts
- Le destinataire peut aller dans ses transferts pour commencer la réception.

Voici le détail de ces étapes. Faites comme d'habitude votre panier avec comme client la société qui devra recevoir le stock. Vous pouvez préparer le stock en utilisant les fonctionnalités habituelles du panier. Notez que ce processus vous permet donc aussi de commander une pièce pour une autre de vos sociétés tout en gardant la traçabilité complète de la commande jusqu'au transfert.

Enfin, pour réaliser le transfert, il vous suffit d'éditer votre facture (ou un bon de livraison). La fenêtre de gestion du stock s'ouvrira, comme d'habitude, avec une nouvelle option pour configurer (ou désactiver) le transfert (cf. **A** sur l'image "Gestion de stock du panier"). les informations de transfert (cf. **A** sur l'image "Gestion de stock du panier" et l'image "Nouveau transfert"). Lorsque vous cliquez sur "Livrer", un transfert sera créé d'où le stock est prélevé. Dans l'exemple ci-dessous, le premier produit est prélevé de l'entrepôt _Dock 1_ (**B**) et le deuxième produit est prélevé de l'entrepôt _Dock 2_ (**C**).

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/basket-modal-on-transfer.png" width="1024px"/>

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/new-transfer-from-basket.png" width="800px"/>

Puisque nous avons configuré nos transferts pour qu'ils soient livrés à l'entrepôt _Stockage_, nous avons bien deux nouveaux transferts (créés après édition de la facture). Il n'y a qu'une seule action possible sur cette page: il faut emballer puis envoyer les transferts — même si c'est pour devoir les annuler en effectuant un retour. Le destinataire peut alors consulter ses transferts et commencer la réception de ses pièces.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/new-transfers.png" width="1024px"/>

Côté panier, il est possible d'accéder aux transferts correspondant aux différentes lignes depuis l'affichage de statut de stock.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.32.0/basket-transfer-links.png" width="1024px"/>

## Comptabilité

- Le nom de la caisse a été ajoutée à l'écran des détails journaliers
- La date d'échéance a été ajoutée à l'affichage du journal

## Corrections

- Correction du total des paniers véhicules sur l'écran de liste des paniers
- Correction du rafraichissement des statuts de paiement des paniers
- Il n'est plus possible de supprimer l'emplacement entrepôt d'un dossier
- Correction d'un bug qui empêchait les évènements de mouvement de stock de se charger
- Correction d'un bug pouvant fausser la valeur du mois de la date d'échéance lors de l'export d'un journal.
- Il est à nouveau possible de rembourser un client à partir de la fenêtre de paiement de la fiche d'un contact
