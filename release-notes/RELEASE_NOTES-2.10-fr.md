# Avril 2022 - Version 2.10.x

## Commande à une autre entité Yuzer

Cette mise à jour apporte des modifications majeures au flux de commandes à une autre entité Yuzer:

- commande chez une autre entité,
- gestion au niveau des paniers des commandes réalisées chez vous,
- envoi de la commande par un transfert,
- réception de la commande.

À chacun de ces niveaux, de nombreuses améliorations ont été apportées.

### Commande

Vous pouvez, depuis l'écran de commandes, sélectionner une entité auprès de laquelle placer une commande de pièces. Au moment où la commande est placée, un panier est créé dans sur fiche contact dans l'entité fournisseur.

### Panier

En tant que fournisseur d'une autre entité, vous pouvez sélectionner cette entité parmis vos contacts et sélectionner les paniers automatiquement créés qui correspondent aux commandes qui vous ont été faites. Vous gérez le stock, les paiements et les éditions des documents comme pour tout panier.

Au moment de l'édition d'un bon de livraison ou d'une facture, vous pouvez décider d'envoyer le contenu de ce panier par un transfert.

### Transferts

Depuis la page du transfert, vous pouvez cliquer sur "Recevoir" pour créer une nouvelle réception qui contient le contenu de ce transfert.

### Receptions

L'écran des réceptions contient de nombreuses nouveautés.

- distinction entre bon de livraison et entrée en stock
- Choix de l'action par défaut à appliquer aux réservations clients: réserver, préparer ou laisser Yuzer choisir
- nouvelle vue de rangement (réception par emplacement de stockage)
- filtre d'erreurs amélioré
- impression possible des étiquettes

#### Bon de livraison

La section gauche, "bon de livraison", vous permet d'avoir ce qui concerne le bon de livraison et doit correspondre à ce que vous avez reçu du fournisseur. C'est donc dans cette partie que sont les prix et les liens vers les commandes.

- **Référence**. Il n'est plus nécessaire d'avoir la référence du produit dans un catalogue: le produit qui entrera en stock pourra être défini dans la partie "entrée en stock" (ci-dessous).
- **Prix**. Vous pouvez renseigner au choix le prix unitaire ou le prix total de la ligne, en fonction de ce que votre fournisseur vous a donné. Dans le cas où vous renseigneriez le prix unitaire, Yuzer se chargera de calculer le total.
- **Commandes**. Il est maintenant possible de lier une ligne de réception à plusieurs commandes. Vous ne devriez donc n'avoir plus qu'une seule ligne pour chaque référence.

Nous avons aussi ajouté une ligne de total qui vous indiquera le nombre de lignes et le montant total de la réception.

#### Entrée en stock

Grosse nouveauté de cette version, il est possible de recevoir un produit en tant qu'un ou que plusieurs autres produits. Vous pouvez :

- changer la référence du produit (inclus le cas où la référence du fournisseur, écrite sur le bon d'achat, n'existe pas dans votre catalogue)
- changer la référence et la quantité reçue: par exemple recevoir un baril de 208L d'huile en tant que 208 fois un litre de la même huile
- décomposer un produit en plusieurs produits: par exemple recevoir une planche de pins en tant que 200 pins rouges, 100 pins bleus, etc.

La modale de décomposition est présentée ci-dessous. Pour ce qui est de l'entrée en stock, pour chaque produit reçu, vous devez définir les emplacements de stockage et les réservations. Là encore, la sélection des emplacements de stockage a été améliorée et uniformisée avec plus de raccourcis sur les emplacements par défaut.

#### Décomposition des produits

En cliquant sur "Éditer l'entrée en stock", vous pourrez accéder à la configuration de décomposition d'un produit. Elle vous permet de définir comment 1 produit source peut être décomposé en plusieurs produits (cibles de décomposition).

La coche "Sauver la configuration à la validation" vous permet de sauvergarder en base la décomposition lorsque vous la validez. Ainsi, elle pourra être réutilisée. La coche "Appliquer automatiquement à la réception" servira dans des versions ultérieures de Yuzer à appliquer automatiquement la décomposition lors de la réception du produit source.

### Factures d'achat

## Application mobile

L'application mobile a été améliorée ! En plus des modifications nécessaires dûes aux changements sur les réceptions, elle se voit dotée d'un scanner amélioré.

### Scanner

Partout dans l'application, le composant de scanner a été amélioré et possède un nouveau mode optimisé pour les scanners externes (type eyoyo).

|                                                           Scanner avec la caméra                                                           |                                                     Scanner avec un périphérique externe                                                     |
| :----------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-text-scanner.webp" width="320px"/> | <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-camera-scanner.webp" width="320px"/> |

### Réceptions

La lisibilité de la liste des réceptions a été améliorée: augmentation de la taille du texte, des icônes, couleurs, etc.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.10.0/mobile-reception-list.webp" width="320px"/>

De même la liste des lignes d'au sein d'une réception.

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

|                                                             Sélection de protuit (2)                                                             |                                                             Sélection d'emplacement (3)                                                              |
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
