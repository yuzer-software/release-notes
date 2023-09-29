# September 2023 - Version 2.16.0

## Opérations entre différents comptes

Auparavant vous pouviez déjà effectuer des opérations de commandes, facturations et livraisons à une autre entité de votre groupe (ou compte Yuzer).
Dorénavant vous pouvez effectuer ces opérations avec une entité Yuzer qui n'est pas de votre groupe, à la condition que les deux entités aient préalablement autoriser cette collaboration.

### Inviter une entité externe à collaborer

En tant que **fournisseur**, pour accepter qu'une entité commande des pièces chez
vous (c'est-à-dire créent des paniers, etc.), vous devez d'abord leur donner
la permission de le faire. Pour cela, allez dans le nouveau menu
`Administration/Redistribution`. Vous pourrez envoyer les coordonnées numériques
de votre entité à votre client, soit par email directement depuis Yuzer, soit par
le moyen de votre choix en copiant le code.

<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/transfer-1-admin-redistribution-code.webp"/>

Le même code peut être partagé à tous ceux qui vous auront pour fournisseur.
Pour cette raison, vous devrez valider l'ajout de nouveaux clients.

### Ajouter un fournisseur Yuzer

En tant qu'entité cliente du fournisseur créez un nouveau fournisseur en utilisant
le code reçu grâce au nouveau bouton prévu à cet effet. Un fournisseur **désactivé**
et **En attente de validation** sera créé. C'est à votre fournisseur de maintenant
valider votre ajout.

<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/transfer-2-admin-supplier-new-from-code.webp"/>

### Accepter d'être fournisseur

Toujours depuis le menu `Administration/Redistribution`, vous pouvez voir tous
vos clients et et l'état des demandes qui vous sont faites. Vous pouvez accepter
ou refuser d'être fournisseur, mais aussi cesser d'être fournisseur. Dès lors
que vous acceptez d'être fournisseur, vous devez choisir un contact à associer
à votre client (vous pouvez créer le contact à la volée ou réutiliser un contact
existant). Notez que ce contact doit être de type **organisation** ou **fournisseur**.
Il ne peut être un simple **personne**.

<img width="700" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.17.0/transfer-3-admin-redistribution.webp"/>

### Transfert inter-compte

Maintenant que vous êtes fournisseur d'une entité Yuzer qui est liée à un de vos
contacts, vous pouvez aller sur sa fiche contact et gérer votre panier comme
vous avez l'habitude, avec la possibilité de l'envoyer par transfert.
