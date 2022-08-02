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

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/invoice-before-delivery.png" width="550px"/>

### Evolution des options de stock à la facturation

En conséquence de cette nouvelle fonctionalité nous avons revu la boite de dialogue de gestion du stock à la facturation ou à l'édition du bon de livraison. Ceci a des implications dans plusieurs scénario de l'application.

#### Finalisation d'une cession de préparation de véhicule

Pour rappel une préparation de véhicule vous permet d'accessoiriser un véhicule (pour une présentation showroom etc.). Le stock est alors déplacé vers un emplacement de stock réservé au véhicule qui indique que celui-ci est "monté sur le véhicule".

Lors de la finalisation de la cession vous pouvez indiquer:

- Ce qui est en effet monté sur le véhicule (destiné à la vente au client final ou pouvant être démonté en cas de besoin de la pièce dans le cadre d'une autre vente/réparation).
- Ce qui doit-être déstocké (consomable utilisé dans le cadre de la préparation ou produit que l'on ne souhaite pas valoriser lors de la vente).
- Ce qui est sans impacts stock.

Ces options sont désormais clairement matérialisées:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/preparation.png" width="100%"/>

<div class="alert alert-warning">
Attention, un produit choisi sans impacts stock ne génèrera aucun mouvent de stock et celui-ci ne sera pas prélevé. Cette option ne doit-être utilisé qu'en cas de produit que vous décidez de ne pas gérer en stock et n'est pas recommandée.
Elle ne devrait pas être utilisée pour corriger une erreur d'inventaire qui doit l'être à l'aide d'un inventaire partiel permettant ainsi de conserver une bonne tracabilité.
</div>

#### Ajout d'un produit monté sur un véhicule dans un panier

Un changement mineur a été apporté lorsqu'un produit monté au préalable (cf. paragraphe ci-dessus) est détecté comme manquant dans un panier. Nous vous proposons désormais par défaut de le vendre. Cette action est également affichée dans la couleur primaire du thème.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-mounted-add.png" width="450px" />

#### Gestion de la livraison dans le panier.

Afin d'illustrer les modifications apportées à la gestion de la livraison dans le panier nous allons utiliser l'exemple suivant:

- Vente de véhicule (VERSYS 650)
- Accessoires:
  - MONORACK KAWA Z 750 S 05 _444FZ_
  - Haut parleurs _4990010030_
  - MOTOREX FUEL STABILIZER 125ML _00001000015_ (Monté sur le véhicule au préalable)
  - QUALIF SOLID BK MAT 55-56/ TS _BEL7050139_

Le panier est créé avec les éléments ci-dessus et un bon de commande est créé.
Le casque en stock (**QUALIF SOLID BK MAT**) a été réservé automatiquement puis préparé pour être mis de côté immédiatement.
La commande des pièces manquantes en stock (**MONORACK KAWA** et **Haut parleurs**) est effectuée.
Une réception a également été effectuée pour le produit **MONORACK KAWA** (en réservé).

Le statut du panier est donc le suivant:

- MONORACK KAWA **réservé**
- Haut parleurs **en commande**
- MOTOREX FUEL STABILIZER 125ML **monté sur le véhicule**
- QUALIF SOLID BK MAT 55-56/ TS **préparé** (dans un carton destiné au panier)

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-1.png" width="680px" />

##### Edition du bon de livraison initial

Nous allons dans un premier temps effectuer un bon de livraison pour le casque uniquement. Pour cela nous allons dans _Editer_/_Un bon de livraison_:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-2.png" width="180px" />

Nous suivons les étapes et Yuzer ouvre la pop-up de gestion de la livraison. Par défaut Yuzer propose la livraison de tout ce qui est préparé en stock ainsi que du véhicule.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-3.png" width="100%" />

Pour l'instant nous ne souhaitons pas livrer le véhicule nous allons donc sélectionner **Ne pas livrer**.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-4.png" width="100%" />

Nous cliquons alors sur _Livrer_. Un contrôle de la preview du bon de livraison permet de bien constater que seul le casque va être livré.

Le statut des lignes du panier reflète bien la livraison partielle.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-5.png" width="680px" />

##### Edition de la facture en livraison partielle

Nous allons désormais éditer la facture afin de livrer le véhicule _VERSYS 650_ ainsi que le _MONORACK KAWA_ dont la réception a déjà été effecutée. Nous n'avons toujours pas reçu les _Haut parleurs_ et n'allons pas les livrer.

Pour éditer la facture nous allons dans _Editer_/_Les factures_ et suivons les étapes jusqu'à l'ouverture de la pop-up de gestion du stock.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-6.png" width="180px" />

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-7.png" width="100%" />

Le véhicule est par défaut livré mais vous pouvez décider de ne pas le livrer. Aucune pièce n'est actuellement préparée Yuzer n'a donc pas automatiquement décidé de livrer des pièces. Vous devez donc manuellement choisir de

- Destocker: liver en impactant le stock
- Ne pas livrer: le produit devra être livrée ultérieurement
- Sans impact stock: Livrer le produit mais ne pas effectuer d'impacts stock. Attention ceci n'est, comme indiqué dans _Finalisation d'une cession de préparation de véhicule_ pas recommandé sauf cas exceptionnels.

<div class="alert alert-info">Le produit MOTOREX FUEL STABILIZER 125ML qui est monté sur le véhicule est obligatoirement livré avec le véhicule s'il n'est pas démonté dans la cession de démontage.</div>

Dans notre cas nous allons choisir de livrer le produit _MONORACK KAWA_ qui est réservé. Nous utilisons pour cela l'action **Déstocker** sur la ligne concernée.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-8.png" width="100%"/>

Le bouton livrer reste cependant grisé. En effet vous devez valider que vous souhaitez bien facturer malgré des produits non livrés:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-9.png" width="380px" />

Vous pouvez alors livrer et générer la facture. Au niveau de celle-ci le message configuré pour les produits non-livrés est ajouté ainsi que la quantité non livrée (Ceci est utile si une livraison par bon de livraison avait été effectuée partiellement au préalable).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-10.png" width="380px" />

Mon panier est désormais bien facturé mais la réservation client reste active ainsi que la commande.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-11.png" width="680px" />

##### Edition du bon de livraison permettant de livrer le produit restant

Nous allons finalement effecuter la réception de la pièce restante, la réservation étant conservée celle-ci sera automatiquement liée au bon client et panier et pourra être réservée ou préparée.

Une fois effectuée il est possible d'éditer un nouveau bon de livraison afin de finaliser le statut de livraison du panier.

Ayant préparé ma réception le produit est immédiatement indiqué comme à **Déstocker** et peut donc être livré.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/basket-delivery-12.png" width="100%" />

## Age du stock

L'âge du stock est désormais affiché en jours dans la liste de véhicules à côté de la date de réception.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/stock-age-list.png" width="480px" />

Vous pouvez également afficher une colonne âge de stock (pour trier dessus ou si vous utilisez un affichage en table).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/stock-age-column.png" width="180px" />

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
- Lors de la sélection d'un dossier de produit pour la vente ceux-ci sont désormais filtrés par défaut sur le critère "non-réservé". Fonctionalité à venir pour la sélection de dossiers véhicules.
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
- La marge sur le widget de chiffre d'affaire pouvait être incorrecte dans le cas d'annulations, et différer de celle présente dans le widget d'analytique qui était bien correcte.
