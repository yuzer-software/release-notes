# Septembre 2023 - Version 2.17.0

## Opérations entre différents comptes

Auparavant vous pouviez déjà effectuer des opérations de commandes, facturations et livraisons à une autre entité de votre groupe (ou compte Yuzer).
Dorénavant vous pouvez effectuer ces opérations avec une entité Yuzer qui n'est pas de votre groupe, à la condition que les deux entités aient préalablement autoriser cette collaboration.

### Inviter une entité externe à collaborer

En tant que **fournisseur**, pour accepter qu'une entité commande des pièces chez vous (c'est-à-dire créent des paniers, etc.), vous devez d'abord leur donner la permission de le faire.
Pour cela, allez dans le nouveau menu `Administration/Redistribution`. Vous pourrez envoyer les coordonnées numériques de votre entité à votre client, soit par email directement depuis Yuzer, soit par le moyen de votre choix en copiant le code.

<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/transfer-1-admin-redistribution-code.webp"/>

Le même code peut être partagé à tous ceux qui vous auront pour fournisseur. Pour cette raison, vous devrez valider l'ajout de nouveaux clients.

### Ajouter un fournisseur Yuzer

En tant qu'entité cliente du fournisseur créez un nouveau fournisseur en utilisant le code reçu grâce au nouveau bouton prévu à cet effet.
Un fournisseur **désactivé** et _**En attente de validation**_ sera créé.
C'est à votre fournisseur de maintenant valider votre ajout.

<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/transfer-2-admin-supplier-new-from-code.webp"/>

### Accepter d'être fournisseur

Toujours depuis le menu `Administration/Redistribution`, vous pouvez voir tous vos clients et l'état des demandes qui vous sont faites. Vous pouvez accepter ou refuser d'être fournisseur, mais aussi cesser d'être fournisseur. Dès lors que vous acceptez d'être fournisseur, vous devez choisir un contact à associer à votre client (vous pouvez créer le contact à la volée ou réutiliser un contact existant).
Notez que ce contact doit être de type **organisation** ou **fournisseur**. Il ne peut être un simple **personne**.

<img width="700" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/transfer-3-admin-redistribution.webp"/>

### Transfert inter-compte

Maintenant que vous êtes fournisseur d'une entité Yuzer qui est liée à un de vos contacts, vous pouvez aller sur sa fiche contact et gérer votre panier comme vous avez l'habitude, avec la possibilité de l'envoyer par transfert.

## Produits sur dossier

### Ajouts de nouveaux champs

Nous avons ajouté 2 nouveaux champs:

- Le numéro de livre de police
- La date de limite de paiement

Comme pour la _date de livraison estimée_ en version _2.16.x_, ces champs peuvent être afficher la vue _liste des dossiers_.

<img width="384"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/dealer-file-list-column-filter.webp"/>

### L'ordre des onglets

Nous avons changé l'ordre des onglets de la liste de dossiers pour avoir l'onglet _Tout le stock_ en première position.

<img width="384"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/dealer-file-list-tabs.webp"/>

Aussi, Yuzer affichera le dernier onglet sélectionné lorsque vous revenez sur le menu.

<img width="384"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/dealer-files-back-to-last-tab.gif"/>

### Export de stock

Vous pouvez maintenant sélectionner plusieurs entités sur l'export de dossiers.
Nous avons également ajouté la colonne _Entité_ dans la sélection du _Dossier produit_ d'avoir l'information du propriétaire du dossier dans le fichier export.

<img width="480"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/dealer-file-export.webp"/>

## Export de contacts

Vous pouvez maintenant sélectionner plusieurs entités sur l'export de contacts.

<img width="480"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/contacts-export.webp"/>

## Corrections

- Correction de l'annulation de crédit client qui était en erreur lors de l'annulation d'une facture.
- Il n'est plus possible de changer la catégorie d'un produit dans une catégorie "non-stockable" si le produit est en stock dans une entité. Il vous faudra d'abord corriger le stock existant de l'entité en question avant de pouvoir effectuer le changement.
