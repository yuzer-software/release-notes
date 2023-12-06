# December 2023 - Version 2.18.5

## Commandes

Si des produits de plusieurs fournisseurs sont commandés, la pré-visualisation vous affiche chaque commande qui sera générée.

De plus, il est désormais possible de nommer chaque commande. Cela permet de mieux les identifier dans la liste des commandes par la suite.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/order-modal.png"/>

Note: Un nom de commande par défaut est indiqué afin de conserver la capacité à commander sans nécessité de modifier celui-ci.

## Inventaires

### Auto résolution des stocks ayant un inventaire négatif.

Afin de vous aider à résoudre vos inventaires négatifs, une nouvelle fonctionnalité à été ajoutée, disponible uniquement pour les administrateurs.

Pour y accéder vous pouvez cliquer sur le nouveau bouton à côté de "Nouvel inventaire":

<img width="384"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/negative-stock-inventory/new-inventory-button.png"/>

Vous accéderez ensuite la modale de création d'inventaire légèrement modifiée dans le cadre des cette fonctionnalité.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/negative-stock-inventory/new-modal-options.png"/>

Notez tout d'abord que cette modale est à présent figée sur "Inventaire partiel" avec l'option de filtre sur les emplacements avec du stock négatif.

Vous pouvez alors cocher les options que vous souhaitez appliquer:

- Résoudre les stocks négatifs dont le stock total est négatif ou vide.
  Cette option permet dans le cadre des filtres que vous allez sélectionner, de passer à 0 tout stock négatifs, pour un produit dont le stock total, pour votre sélection est négatif.
  Attention car cette fonctionnalité peut augmenter votre total en stock, si des stocks positifs étaient disponible dans d'autres emplacements. Il est donc recommandé de l'utiliser pour un inventaire de tout l'entrepôt

- Résoudre les stocks négatifs ayant un unique emplacement avec un stock positif
  Cette option ne change pas votre stock total, mais va déverser le stock positif dans les emplacements ayant un stock négatif.

- Résoudre les stocks négatifs ayant un unique emplacement avec un stock positif
  Cette option, similaire à la précédente, ne change pas votre stock total, mais va déverser les stocks positifs dans les emplacements ayant un stock négatif.
  Les stocks seront pris aléatoirement depuis les différents stocks positifs, le résultat ne sera sans doute pas conforme à la réalité de vos stocks.

Attention donc à bien lire la description ainsi que les messages d'avertissement avant de l'utiliser.

## Améliorations diverses

## Corrections
