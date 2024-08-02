# Juin 2021 - Version 1.6.0

- Vous pouvez désormais modifier le libellé d'un produit dans un panier.
- Le taux de marge est maintenant affiché dans l'encadré _Résumé_ du panier de vente véhicule lorsque le filtre d'affichage des prix d'achats et marges est désactivé.
- Il est désormais possible de filtrer par fournisseur sur la page _Produits en commande_
- Nous avons ajouté un saut de page sur les documents pdf générés afin de séparer les conditions de ventes et vous permettre de ne pas les imprimer si vous le souhaitez.
- Améliorations de la performance de l'affichage du journal comptable lorsque de nombreuses lignes sont chargées.
- Les ajouts de produits dans une réception lorsque le filtre de zone est défini sont fait dans cette zone si ils ne sont pas liés à un client (ils restent associé au panier client dans le cas contraire);
- Vous pouvez désormais filtrer les paniers par dates de clôture. Un panier est considéré comme clôturé quand il est entièrement soldé et facturé ou quand il est annulé.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/baskets-filtering-closed-date.png" width="400" class="mx-2"/>

- La liste des activités des contacts affiche désormais l'auteur, nous avons également légèrement amélioré les icônes de celle-ci.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/contact-activities.png" width="500" class="mx-2"/>

- Nous avons ajouté la possibilité de rapidement ajouter des produits en réassort depuis la page _En attente de commande_

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/waiting-order-quick-add.png" width="100%"/>

## Éviter la duplication des contacts

Lorsque vous créez un nouveau contact nous recherchons automatiquement les duplicats potentiels afin d'éviter la création de doublons.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/contact-duplicates.png" width="100%"/>

Plusieurs champs sont pris en comptes et cela devrait vous éviter de vous tromper.

Si le contact que vous recherchez est présent dans la liste il vous suffit de cliquer dessus pour aller directement à sa fiche.

## Auto-validation et export des données comptables

Nous avons ajouté l'auto-validation des factures, reprises et cessions en comptabilité.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/accountancy-auto-validation.png" width="200" class="mx-2"/>

Si les options sont activées le passage en comptabilité sera effectué automatiquement depuis nos serveurs une fois le document édité.
Si la validation automatique des écritures à valider est également activée nous écrirons automatiquement les écritures dans le journal. En cas d'erreur dans l'écriture (mapping incomplet, autre) vous retrouverez les écritures à avec les informations d'echec dans les écritures à valider.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/accountancy-to-validate.png" width="100%"/>

Il est également possible de configurer un export journalier des données comptables sur un serveur FTPS de votre choix.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/accountancy-ftp-config.png" width="200" class="mx-2"/>
<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/accountancy-to-validate.png" width="200" class="mx-2"/>

Le fichier sera généré chaque nuit avec le contenu des nouvelles lignes de journal depuis le dernier export.

## Nouvelles fonctionnalités sur la réception

### Ré-ouverture

Il est maintenant possible de ré-ouvrir une réception clôturée pour y ajouter de nouvelles lignes.
Les lignes traitées ne sont pas modifiables.

### Annulation

L'annulation d'une réception est maintenant possible. Vous pouvez choisir d'annuler seulement quelques lignes ou toutes les lignes de la réception.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-new-menu.png" width="320"/>

Une ligne annulée est affichée avec un texte grisé avec l'icône <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-ban-icon.png" width="16" />, comme ci-dessous.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-canceled-line.png" width="1024"/>

Lors de l'annulation, les différentes actions suivantes sont exécutées pour chacune des lignes pour essayer de revenir à l'état avant clôture:

- Annulation des quantités de stock sur l'emplacement de réception
- Annulation des prix de stock pour le produit (prix FIFO, prix moyen)
- Si existant, annulation de la ligne de commande associée
- Si existant, annulation de la réservation/préparation pour un client

Il se peut que les emplacements spécifiés lors de la réception aient été mis à jour entre la clôture et l'annulation.
Dans le cas où la quantité est trop faible (_quantité de l'emplacement < quantité reçue_), une fenêtre sera affichée pour vous demander de résoudre et spécifier les emplacements à impacter pour l'annulation.

L'image suivante montre la fenêtre de validation.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-cancellation-modal-1.png" width="1024"/>

Nous constatons qu'une ligne avait été clôturé avec 4 quantités reçues, toutes stockées à l'emplacement: _Showroom/Étagère 1/ Planche 1/ Paquet 1_.
Cependant, l'emplacement ne contient plus que 2 unités du produit.

Pour l'exemple, nous choisissons d'ajouter l'annulation de 2 quantités sur l'_Emplacement inconnu_.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-cancellation-modal-2.png" width="1024"/>

A noter que le nombre d'articles et le total du prix incluant remises sont calculés en ignorant les lignes annulées.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-infos.png" width="384"/>

### Filtrage des lignes

Des filtres ont été ajoutés pour pouvoir cacher les lignes traitées ou annulées.
Cela devrait faciliter la lisibilité en particulier sur la modification d'une relative grosse réception qui aurait été ré-ouverte.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/reception-new-filters.png" width="896"/>

## Coûts opérationnels et primes

Nous avons fait évoluer la gestion des primes sur un dossier véhicule en l'aggrémentant d'une gestion des coûts opérationnels.
Si les primes réduisent le prix d'achat d'un véhicule, les coûts opérationnels l'augmentent et vont ainsi réduire la marge liée au véhicule.

### Coûts opérationnels généraux

Si les coûts opérationnels sont gérés par dossier vous pouvez définir une configuration globale qui est utilisée pour initialiser ceux-ci lorsqu'un nouveau dossier est créé. Cette configuration n'est pas synchronisée sur les dossiers existant mais ne sera appliquée que lors de la création d'un nouveau dossier.

Afin de configurer ceux-ci rendez vous à l'onglet configurer de la section véhicules. Vous pouvez ici configurer un ensemble de coûts opérationnels:

- Les coûts opérationnels sur véhicules neufs qui sont ajoutés pour toute création d'un dossier de véhicule neuf
- Les coûts opérationnels sur véhicules neufs spécifiques à certains fournisseurs (qui sont ajoutés lors d'une création de dossier de véhicule neuf lorsque le fournisseur selectionné correspond).
- Les coûts opérationnels sur véhicules d'occasion qui sont ajoutés lors de la création d'un dossier de véhicule d'occasion, à l'exception pour le moment d'une reprise.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/operational-costs-config.png" width="100%"/>

Lors de la création d'un dossier ces coûts sont ajoutés:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/dealer-file-create-operational-costs.png" width="100%"/>

Vous remarquerez que nous avons également amélioré l'affichage de l'ajout de dossier afin de rendre tout cela plus clair.

### Coûts opérationnels, primes et dossier véhicule

La visualisation d'un dossier véhicule a été revue pour plus de clarté. Elle apporte également un ensemble d'améliorations significatives sur la gestion des primes et donc des coûts opérationnels.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/dealer-file-detail.png" width="100%"/>

Comme vous pouvez le constater chaque prime possède désormais un libellé ainsi que son montant calculé (une fois appliqué au prix d'achat lors de pourcentages sur celui-ci par exemple).

Il est également possible de visualiser le prix d'achat incluant l'ensemble des primes et coûts opérationnels (à l'exception des primes à la vente non sélectionnées; voir ci-après) ainsi que de la marge les prenant en compte.

L'édition des primes et coûts opérationnels peut se faire comme avant mais ajoute donc le libellé ainsi qu'une option permettant d'inclure ou non les primes à la vente dans le calcul du prix d'achat incluant primes et de la marge associée.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.6.0/dealer-file-costs-bonus-edit.png" width="100%"/>

## Correction de bugs

- Sur la page _Produits en commande_ le groupement par fournisseur empêchait un tri par date effectif.
- Correction du retour sur la navigation dans un onglet positionné sur une vue du stock.
