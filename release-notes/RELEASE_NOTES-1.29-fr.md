# Aout 2022 - Version 1.29.0

## Facturation sans livraison

Dans les versions précédentes de Yuzer la facturation de produit impliquait automatiquement la livraison des produits. Si cela reste valable pour les tickets de caisses, il est désormais possible d'éditer une facture dont une sous-partie ne sera pas livrée.

Ceci permet de préciser une information sur la facture indiquant, par exemple, la nécessité d'un retrait ultérieur dans un point de retrait magasin. A noter également que, dans le cas ou un produit non-livré fait l'objet d'une réservation client, celle-ci restera active et pourra être résoudre à la réception.

### Autoriser la facturation sans livraison

L'activation de la fonctionalité permettant de ne pas imposer une livraison complète à la facturation peut-être configurée dans _Administration / Gestion commerciale / Configuration commerciale_:

<div class="alert alert-warning">
Attention, cette fonctionalité peut être soumise à la juridiction locale et reste l'activation de celle-ci reste la responsabilité de la concession.
</div>

En plus de l'activation ou non de la fonctionalité vous pouvez également indiquer un message qui sera ajouté sur les lignes de factures non livrées.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/invoice-before-delivery.png" />

### Evolution des options de stock à la facturation

La boite de dialogue permettant de gérer le stock panier impacté par une facturation ou bon de livraison évolue.

## Age du stock

L'âge du stock est désormais affiché en jours dans la liste de véhicules à côté de la date de réception.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/stock-age-list.png" />

Vous pouvez également afficher une colonne âge de stock (pour trier dessus ou si vous utilisez un affichage en table).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/stock-age-column.png" />

<div class="alert alert-warning">Si vous avez groupé vos véhicules et que vous triez par âge, le tri sera effectif à l'intérieur d'un groupe. En effet un tri "à plat" serait antinomique avec le groupement.</div>

Cette colonne peut également être exportée.

## Emplacement de rangement par défaut

Afin de faciliter vos réceptions, il est maintenant possible de définir, dans un écran de configuration dédié, situé dans Stock -> Emplacement entrepôt
des emplacements par défaut par entrepôt, en fonction des marques et catégories des produits que vous recevez.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/default-dispatching-conf.png" />

Ainsi, lors de vos réceptions, l'emplacement défini sera automatiquement attribué à vos produits.
De plus, il est possible de définir plusieurs emplacements, et il sera alors très simple de passer de l'un à l'autre tel que montré ci dessous.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/default-dispatching-reception.png" />

## Améliorations diverses

- Les numéros de clients ajoutés sur les documents le sont également désormais sur les tickets de caisses.
- Le bon de livraison peut désormais être généré sans signature (pour une signature papier) comme les autres documents.
- Lors de la sélection d'un dossier de produit pour la vente ceux-ci sont désormais filtrés par défaut sur le critère "non-réservé".
- La sous catégorie des produits identitiés est désormais affichée sur la liste des dossiers et peut-être utilisée pour les filtrer.
- Dans les filtres personalisés de l'analytique il est désormais possible de visualiser et utiliser les filtres d'une entité parente même lorsque des filtres personalisés complémentaires ont été définis localement.
- Les configurations des écrans analytiques sont désormais héritées de la même manière que les configurations des filtres et donc disponible même si une configuration spécifique est définie.

## Corrections

- Le retour d'un produit sur une annulation de facture ou lors d'une facturation en quantité négative faisait rentrer le produit avec un prix d'achat catalogue.
  - Dans le cas ou le produit est retourné suite à une annulation de facture il rentre à la valeur de stock correspondant à sa sortie.
  - Dans le cas ou il rentre sur un nouveau panier avec une quantité négative il rentre à la valeur de stock actuelle.
- Les paiements sur un panier de produit avec acheteur n'étaient pas redirigés sur la balance du client mais sur celui de l'acheteur alors que le montant de la facture mouvementait bien la balance du client.
- Des messages d'erreurs de validation de montant sur les factures d'achat incluant taxe étaient erronés lorsque liés à des lignes de réception.
- Lorsqu'un bon de commande est annulé et qu'un dossier véhicule reste attaché au panier, un message est affiché sur celui-ci afin de prévenir que, la vente ayant été annulée il devrait être détaché. Ce message persistait si une facture était émise néanmoins. Ce n'est désormais plus le cas.
- Le bouton de clôture d'un dossier de produit identifié si celui-ci était ouvert alors que la facture venait bien d'être soldée à postériori ne déclenchait pas d'actions (il fallait passer par le panier).
