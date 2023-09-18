# September 2023 - Version 2.16.0

## Opérations entre différents comptes

Auparavant vous pouviez déjà effectuer des opérations de commandes, facturations et livraisons à une autre entité de votre groupe (ou compte Yuzer).
Dorénavant vous pouvez effectuer ces opérations avec une entité Yuzer qui n'est pas de votre groupe, à la condition que les deux entités aient préalablement autoriser cette collaboration.

### Lier un contact à une entité externe

En tant que fournisseur, pour accepter qu'une entité commande des pièces chez
vous (c'est-à-dire créent des paniers, etc.), vous devez d'abord leur donner
la permission de le faire. Pour cela, allez dans le nouveau menu
`Administration/Codes d'association` et cliquez sur `Ajouter`. Choisissez une
date d'expiration, et validez. Notez qu'une fois que la date d'expiration est
atteinte, vous devrez soit la repousser soit re-générer un code (si vous ne
souhaitez pas d'expiration, vous pouvez configurer une date très loin dans le futur).

<img width="400" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-1-admin.webp"/>

Vous verrez le détail du code généré. Vous pouvez :

- l'envoyer par mail (bouton `enveloppe`) ou par tout autre moyen de
  votre choix en le copiant (bouton `copier`)
- ajouter un libellé personnalisé pour vous rappeler son objet ou son destinataire,
- voir le nom de l'entité Yuzer qui a utilisé ce code
- voir la date d'expiration du code
- révoquer le code pour cesser de travailler avec l'entité sus-mentionnée,
  ou le réactiver.

<img width="500" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-2-detail.webp"/>

En tant qu'entité cliente du fournisseur :

- assurez-vous d'abord que votre fournisseur est lié à une fiche client:

<img width="700" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-3-supplier-is-linked-to-contact.webp"/>

- sur la fiche client, cliquez sur le bouton "lien". Une modale s'ouvre.

<img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-4-pair-button.webp"/>

- Copiez/collez le code envoyé par votre fournisseur et validez (tapez `Entrée`).

<img width="500" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-5-enter-code.webp"/>

- L'entité de votre fournisseur est désormais liée à votre fiche contact.

<img width="330" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-6-is-linked.webp"/>

<br />

## Produits sur dossier

Vous pouvez désormais ajouter une date de livraison estimée provenant de votre fournisseur dans l'encadrer _Informations d'achats_ de la fiche.

Vous pouvez également afficher le numéro de commandes et la date de livraison estimée dans la liste de dossiers.

Pour ce faire, il suffit d'activer l'affichage de ces colonnes:
<img width="480" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/dealer-file-list-column-filter.webp"/>

### Import Excel

Nous avons ajouter la possible d'importer des produits sur dossier à partir de fichier Excel.

Yuzer se base sur les identifiants d’autorité (VIN, immatriculation, etc.) pour savoir si un dossier existe déjà.
Par défaut, si Yuzer lève une erreur s'il détecte qu'un dossier ouvert existe déjà.

Vous pouvez activer l’option _Écraser les valeurs des dossiers existants_ pour forcer la mise à jour des valeurs liées au dossier.
A noter que les attributs liés au produit identifié ne peuvent être mis à jour.

<br />

## Impression des étiquettes produits

Il est maintenant possible d'ordonner les étiquettes pour les imprimer par ordre de référence produit.

<img width="480" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/printing-price-tag.webp"/>

A noter que par défaut, les étiquettes sont triées par order d'ajout.

<br />

## Analytiques

Nous avons ajouter un filtre sur l'état du dossier, permettant ainsi d'exclure les dossiers _Démo_ par exemple.

<img width="360" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/analytics-dealer-file-state-filter.webp"/>

<br />

## Améliorations diverses

- Yuzer affiche désormais le prix d'achat au moment de la facturation sur les lignes du panier lorsque le groupe de facturation a été facturé.

## Corrections

- Sur les formulaires d'édition de prix, la marge est maintenant recalculée après modification du prix d'achat.
