# 27 Avril 2022 - Version 2.10.4

Corrections:

- le bouton d'édition d'un bon de livraison était désactivé dans le cas d'un transfert intra-société
- lorsque le menu de sélection de produits proposait de sélectionner une ligne avec un bouton `[+]`, celui-ci ne faisait rien (il fallait cliquer sur la ligne)

# Avril 2022 - Version 2.10.x

La version 2.10 est une version majeure et apporte les changements suivants:

- Programmes de fidélité:
  - Ajout de remise en pourcentage sur la marge
  - Application automatique à la création de nouveaux paniers
- Commandes intra-groupes
- Transferts améliorés et uniformisés
- Réception:
  - Conversion de produits
  - Meilleur support des références inconnues
  - Écrans bureau et mobiles revus et améliorés
- Factures d'achat:
  - Impact du PA des réceptions et PAMP stock
- Dossiers véhicules:
  - Prise en compte des cessions de maintenance post-vente dans les marges affichées
- Analytique:
  - Ajout d'une colonne "Nombre de documents" comptant les annulations en -1
- Chat support: vous pouvez désormais depuis Yuzer ouvrir un chat avec nos équipes support.

Si vous êtes magasinier nous vous conseillons fortement de prendre le temps de lire cette release note.

## Programmes de fidélité

Les programmes de fidélités prennent une portée un peu plus large avec l'ajout de la remise en pourcentage sur la marge.

Appliqués sur une autre société du groupe ils permettent ainsi de définir votre politique de tarification dans le cas de transferts intra-groupe mais extra-société.

### Configuration

La configuration nécessite un rôle ADMIN et se situe dans _Administration / Gestion commerciale / Cartes cadeaux et fidélité / Programmes de fidélité_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/fidelity_1.webp" width="100%"/>

Vous pouvez alors créer ou éditer un programme de fidélité et y configurer:

- Le nom du programme (Libellé)
- Optionnellement:
  - Le commentaire qui apparaitra en bas de la facture (Commentaire du groupe de facturation)
  - Le commentaire qui apparaitra suite à la ligne impactée
- Si le programme de fidélité doit s'appliquer automatiquement sur les nouveaux paniers.
- La remise à appliquer en fonction de contraintes diverses.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/fidelity_2.webp" width="100%"/>

_Ci-dessus: Exemple de configuration d'un programme intra-groupe permettant une vente à prix coûtant_

À noter que les remises de fidélités sont non-cumulables avec les opérations commerciales ou remises configurées manuellement. La meilleure remise disponible est automatiquement appliquée.

### Application et visualisation

Sur les nouveaux paniers l'application du programme de fidélité a changé. La ligne de remise globale ajoutée par le passé a été supprimée et une remise immédiate est appliquée sur chaque ligne en lieu et place.

Les commentaires spécifiés (pour la facture ou pour les lignes) sont également ajoutés le cas échéant.

## Commandes intra-groupes

Les commandes intra-groupes vous permettent de bien modéliser et valider la prise en charge d'une commande qui est réalisée par l'intermédiaire d'une autre entité du groupe. Les lignes ainsi commandées sont bien regroupées dans une commande et quittent par la même occasion l'écran _En attente de commande_.

Les produits listés sur l'écran en question peuvent donc provenir de deux scénarios principaux:

- Le produit est bien à commander à un fournisseur
- Le stock connu par Yuzer n'est pas à jour:
  - Une commande n'a pas été renseignée dans Yuzer et sa réception n'a pas été complétée alors que des pièces ont déjà été sorties.
  - Erreur d'inventaire.

### Pré-requis

Afin de pouvoir commander à une société intra-groupe il faut que celle-ci soit considérée comme fournisseur possible sur le catalogue sélectionné.

Chaque catalogue peut comporter plusieurs fournisseurs, il est ainsi possible par exemple, d'avoir comme fournisseur _KTM_ et une autre concession _KTM_ de votre groupe.

Un ADMIN peut effectuer la configuration dans _Administration / Catalogue_ en sélectionnant le catalogue souhaité puis en cliquant sur éditer.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/catalog_supplier_1.webp" width="100%"/>

Il est alors possible d'ajouter le fournisseur intra-groupe.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/catalog_supplier_2.webp" width="460px"/>

### Effectuer une commande

Depuis l'écran _En attente de commande_ vous pouvez désormais filtrer par fournisseur. Les différentes entités de votre groupe sont désormais automatiquement ajoutées comme fournisseur, vous permettant de les sélectionner.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_order_1.webp" width="100%"/>

Vous pouvez également, si vous le souhaitez affiner la recherche en sélectionnant un des catalogues que le fournisseur peut adresser.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_order_2.webp" width="480px"/>

Finalement sélectionnez les pièces que vous souhaitez commander et cliquez sur commander (ici nous commandons un T-Shirt KTM lié à un panier client).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_order_3.webp" width="100%"/>

Avant la commande, un résumé est affiché vous permettant de contrôler sa validité.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_order_4.webp" width="800px"/>

Une fois validée, la commande est placée et Yuzer vous redirige vers le détail de celle-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_order_5.webp" width="100%"/>

Au moment où la commande est placée, un panier est créé dans sur fiche contact dans l'entité fournisseur. Ce panier est également automatiquement commandé, ce qui permet de réserver les pièces en stock ou de les mettre en attente de commande si elles ne sont pas en stock.

### Panier de commande et transfert intra-groupe

Désormais tous les transferts doivent s'effectuer en passant par un panier. Dans le cas ou les produits ont été commandés via une commande intra-groupe, le panier créé automatiquement dans l'étape décrite ci-dessus est visible sur la fiche contact de l'entité ayant effectué la commande.

Ainsi la commande effectuée dans l'exemple ci-dessus par _Corruscant_ chez _Gallactic Empire_ est visible, pour un utilisateur de _Gallactic Empire_ sur la fiche contact de _Corruscant_:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_basket_1.webp" width="100%"/>

De plus le panier a bien été automatiquement réservé/commandé.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_basket_2.webp" width="100%"/>

Dans notre exemple le T-Shirt KTM n'était pas en stock chez _Gallactic Empire_ celui-ci a donc été automatiquement ajouté dans les produits _En attente de commande_ afin qu'il puisse-t-être commandé à un fournisseur de _Gallactic Empire_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_transitive_order.webp" width="100%"/>

La suite est équivalente à n'importe quel panier client classique. Dans notre exemple le magasinier de _Gallactic Empire_ a effectué la commande du T-Shirt chez KTM, en a effectué la réception en préparant le T-Shirt pour le panier de _Corruscant_ et le panier est prêt à être facturé.

<div class="alert alert-info">
Dans notre exemple, <i>Corruscant</i> est une société indépendante de <i>Gallactic Empire</i> bien qu'intra-groupe, c'est pour cela qu'une facture doit-être éditée. L'enregistrement de la facture d'achat est, dans ce cas, automatiquement créé chez <i>Corruscant</i>.
Si <i>Corruscant</i> était une entité logique ou une branche de la même société que <i>Gallactic Empire</i> alors seul un bon de livraison serait à éditer.
</div>

Comme le client est une société intra-groupe, au moment de l'édition d'un bon de livraison ou d'une facture, le contenu du panier peut-être envoyé à travers un transfert.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/intra_group_basket_3.webp" width="100%"/>

Cliquez alors sur _Livrer et envoyer le transfert_, puis éditez la facture ou le bon de livraison afin que celui-ci soit prêt à recevoir par Corruscant.

### Transferts

Depuis la page du transfert, vous pouvez cliquer sur "Recevoir" pour créer une nouvelle réception qui contient le contenu de ce transfert.

## Receptions

L'écran des réceptions contient de nombreuses nouveautés.

- Distinction entre bon de livraison et entrée en stock
- Choix de l'action par défaut à appliquer aux réservations clients: réserver, préparer ou laisser Yuzer choisir
- Nouvelle vue de rangement (réception par emplacement de stockage)
- Filtre d'erreurs amélioré
- Impression possible des étiquettes

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/reception_1.webp" width="100%"/>

### Ajouts de produits

La quantité pour l'ajout de lignes de produits est désormais configurée sur 1 par défaut. De plus l'ajout consécutif de la même référence deux fois de suite n'ajoute pas de nouvelle ligne mais augmente la quantité de la ligne existante. Cela permet une utilisation plus efficace d'une douchette à la réception.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/reception_edit_1.webp" width="380px"/>

Par ailleurs le comportement de l'association des réservations clients peut désormais être configuré:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/reception_edit_2.webp" width="240px"/>

Lorsque auto est sélectionné Yuzer détermine si la pièce doit-être préparée ou ajoutée au stock et réservée sur la base des critères suivants:

- Si, lorsque la ligne est ajoutée à la réception, le panier client a une date de livraison définie et que celle-ci se situe dans le passé ou dans un intervalle d'une semaine suivant la réception alors le produit est préparé.
- Dans le cas contraire, le produit est réservé.

Tout autre sélection applique l'option choisie.

Nous avons par ailleurs ajouté la possibilité de tout préparer/réserver dans le cas où vous n'auriez pas choisi l'option souhaitée au préalable et que le comportement ne vous convenait pas.

 <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/reception_edit_3.webp" width="240px"/>

### Bon de livraison

La section gauche, "bon de livraison", vous permet d'avoir ce qui concerne le bon de livraison et doit correspondre à ce que vous avez reçu du fournisseur. C'est donc dans cette partie que sont les prix et les liens vers les commandes.

- **Référence**. Il n'est plus nécessaire d'avoir la référence du produit dans un catalogue: le produit qui entrera en stock pourra être défini dans la partie "entrée en stock" (ci-dessous).
- **Prix**. Vous pouvez renseigner au choix le prix unitaire ou le prix total de la ligne, en fonction de ce que votre fournisseur vous a donné. Dans le cas où vous renseigneriez le prix unitaire, Yuzer se chargera de calculer le total.
- **Commandes**. Il est maintenant possible de lier une ligne de réception à plusieurs commandes. Vous ne devriez donc n'avoir plus qu'une seule ligne pour chaque référence.

Nous avons aussi ajouté une ligne de total qui vous indiquera le nombre de lignes et le montant total de la réception.

### Entrée en stock

Grosse nouveauté de cette version, il est possible de recevoir un produit en tant qu'un ou que plusieurs autres produits. Vous pouvez:

- changer la référence du produit (inclus le cas où la référence du fournisseur, écrite sur le bon d'achat, n'existe pas dans votre catalogue). Cela permet également de résoudre des difficultés rencontrées dans les transferts entre entités ne disposant pas des mêmes catalogues.
- changer la référence et la quantité reçue: par exemple recevoir un baril de 208L d'huile en tant que 208 fois un litre de la même huile
- décomposer un produit en plusieurs produits: par exemple recevoir une planche de pins en tant que 200 pins rouges, 100 pins bleus, etc.

La modale de décomposition est présentée ci-dessous. Pour ce qui est de l'entrée en stock, pour chaque produit reçu, vous devez définir les emplacements de stockage et les réservations. Là encore, la sélection des emplacements de stockage a été améliorée et uniformisée avec plus de raccourcis sur les emplacements par défaut.

### Décomposition des produits

En cliquant sur "Éditer l'entrée en stock", vous pourrez accéder à la configuration de décomposition d'un produit. Elle vous permet de définir comment 1 produit source peut être décomposé en plusieurs produits (cibles de décomposition).

 <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/reception_product_compose_1.webp" width="240px"/>

La coche "Sauver la configuration à la validation" vous permet de sauvegarder en base la décomposition lorsque vous la validez. Ainsi, elle pourra être réutilisée. Si vous cochez "Appliquer automatiquement à la réception", une réception ultérieure de ce produit sera automatiquement décomposée avec cette décomposition ("Sauver la configuration à la validation" doit être coché).

 <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/reception_product_compose_2.webp" width="240px"/>

### Nouvelle vue rangement

La nouvelle vue _rangement_ vous permet d'avoir un listing de la réception par emplacement de stock. Les paniers client préparés sont placés en premier.

## Factures d'achat

Comme indiqué ci-dessus, les factures d'achat provenant de transferts intra-groupes sont désormais automatiquement créées par Yuzer dans la société cible.

L'autre nouveauté est la possibilité de mettre à jour les prix d'achat d'une réception clôturée depuis la validation de la facture d'achat correspondante (pour les lignes effectivement liées aux réceptions).

## Chat support

Vous pouvez désormais ouvrir une fenêtre de chat pour communiquer avec notre équipe support directement depuis Yuzer.

<div class="d-flex">
<div>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/support_chat_1.webp" width="48px"/>
</div>
<div>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/support_chat_2.webp" width="240px"/>
</div>
</div>

## Application mobile

L'application mobile a été améliorée ! En plus des modifications nécessaires dûes aux changements sur les réceptions, elle se voit dotée d'un scanner amélioré.

### Scanner

Partout dans l'application, le composant de scanner a été amélioré et possède un nouveau mode optimisé pour les scanners externes (type eyoyo). Il est possible de passer de l'un à l'autre à tout moment, comme illustré ci-dessous.

- Le bouton (2) permet de changer le type de scanner
- Le bouton (3) permet de fermer le scanner (et ainsi laisser plus de place à la lisibilité)
- Le bouton (1) active la lampe — seulement dans le cas où la caméra est utilisée.

|                                                            Scanner avec la caméra                                                            |                                                    Scanner avec un périphérique externe                                                    |
| :------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-camera-scanner.webp" width="320px"/> | <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-text-scanner.webp" width="320px"/> |

### Réceptions

La lisibilité de la liste des réceptions a été améliorée: augmentation de la taille du texte et des icônes, ajout de couleurs, etc.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-list.webp" width="320px"/>

De même la liste des lignes au sein d'une réception.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-detail.webp" width="320px"/>

#### Ajout d'éléments au bon de livraison

L'ajout des éléments a été revu. Le flux pour ajouter un élément a été explicité par quatre boutons:

- Le premier bouton (1) efface tout ce qui a été sélectionné (produit, emplacement, quantité)
- Le second bouton (2) permet de choisir le produit à ajouter
- Le troisième bouton (3) permet de choisir l'emplacement
- Le quatrième bouton (4) valide la sélection.

Lorsqu'un emplacement est sélectionné, vous pouvez l'effacer avec la croix grise à côté de l'emplacement (5).

Lorsque vous êtes en mode de sélection de produit (2), vous pouvez effacer la référence textuelle en cliquant sur la croix grise à côté de la référence (6).

Dès qu'un produit a été ajouté, le mode de sélection de produit (2) est sélectionné.

|                                                             Sélection de produit (2)                                                             |                                                             Sélection d'emplacement (3)                                                              |
| :----------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-add-item.webp" width="320px"/> | <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-add-location.webp" width="320px"/> |

|                                                           Aperçu avant validation sur (4)                                                            |                                                       Après ajout, la ligne apparaît en (7)                                                        |
| :--------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-add-validate.webp" width="320px"/> | <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-add-result.webp" width="320px"/> |

#### Détails d'une ligne et modification de l'entrée en stock

La modale de détail d'une ligne réception a aussi été revue. Elle se ferme par le bouton en haut à gauche (1). Le bouton en haut à droite permet d'activer ou de désactiver le mode d'édition. Attention cependant: une fois en mode d'édition, les modifications sont immédiates, contrairement à ce qui était fait avant. Quitter le mode d'édition ne sert donc pas d'étape de validation des changements.

Comme sur l'application de bureau, on retrouve ci-dessous la partie "Bon de livraison" (3) et la partie "Entrée en stock" (4).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-line-detail.webp" width="320px"/>

Une fois en mode édition, il est possible :

- de supprimer toute la ligne avec la poubelle en haut à gauche
- de lier la ligne avec des commandes avec le bouton (3)
- de configurer la décomposition du produit (ou le changement de référence) (4)
- pour chaque produit entré en stock:
  - d'ajouter un emplacement de stockage (5)
  - de modifier la quantité ou de supprimer un emplacement de stockage (6)
  - de gérer les réservations pour ce produit (7)

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-line-edit.webp" width="320px"/>

La décomposition d'un produit permet de faire la même chose que côté application de bureau. Dans l'exemple ci-dessous, nous avons choisi de faire entrer dans notre stock le fut de 208L d'huile en tant que 208 bidons d'un litre, ce qui nous permettra de travailler au litre par la suite.

Vous pouvez supprimer des cibles de décompositions avec le bouton (2), passer en mode d'ajout avec le bouton (1) et configurer la décomposition avec les options (3). Dans le cas où vous auriez choisi de sauvegarder en base la configuration de ce produit à la validation (3), le bouton "supprimer" vous permet de supprimer la décomposition de la base.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-line-edit-conversion.webp" width="320px"/>

En mode d'ajout, vous retrouvez la même présentation d'ajout de produit que sur l'entrée en bon de livraison (2) — la sélection d'emplacement n'était bien sûr pas disponible.

Vous devez quitter le mode d'ajout (1) pour pouvoir valider la décomposition.

|                                                                             Mode d'ajout                                                                              |                                                                             Validation                                                                              |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-line-edit-conversion-add-item.webp" width="320px"/> | <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-line-edit-conversion-resume.webp" width="320px"/> |

Une fois toutes les modifications faites au niveau de la ligne de réception, la vue en lecture seule (hors édition) vous permet de voir de manière compacte ce que vous avez fait. Ici, nous avons bien rangé 2x208 litres (416) dans deux emplacements différents.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-line-detail-resume.webp" width="320px"/>
