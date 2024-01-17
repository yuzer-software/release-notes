# January 2024 - Version 2.18.13

- Lors de l'édition d'un reçu depuis la modale de paiement, les documents attachés au panier n'étaient pas toujours rafraîchis : un message faux apparaissait alors pour dire que la quantité délivrée dans les documents ne correspondait pas à la quantité délivrée dans les réservations. Un utilisateur pouvait alors ouvrir la fenêtre de gestion de stock, ne pas prêter attention aux quantités affichées et faire l'erreur de cliquer sur "corriger les réservations" ce qui annulait le stock qui, lui, était correct.
- Un bug qui empêchait de supprimer de vielles réservations (avant 2021) a été trouvé et résolu.

# December 2023 - Version 2.18.12

Ajout de nouveaux filtres par défauts sur les paniers:

- Paniers facturés / pièces réservées non livrées
- Panier sans documents avec réservations

## Corrections

- L'affichage des zones de stock véhicule n'était plus affiché dans l'écran de stock.

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/stock-browser-vehicles.webp"/>

- Correction d'un problème d'affichage du détail d'une commande lorsque l'utilisateur l'ayant effectué n'était plus affecté au magasin en question.
- Correction des filtres de panier par défaut _Vente de produits sur dossier_ et _Paniers ouverts il y a deux mois et plus_

# December 2023 - Version 2.18.11

Ajout du support du protocole Concert V2 complet sur IP. (Envoi les messages équivalents au protocole Série sur IP.):

- Testé sur un Pax A920 équipé de la surcouche Nepting

# December 2023 - Version 2.18.10

Ajout de la possibilité de rapidement déplacer le stock d'un produit depuis l'application bureau.

Depuis le détail de stock de la fiche d'un produit vous pouvez désormais cliquer sur un nouveau bouton:

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/move-stock-1.webp"/>

Celui-ci ouvre une boite de dialogue vous permettant de sélectionner un emplacement cible ainsi qu'une quantité à déplacer.

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/move-stock-2.webp"/>

À la validation un inventaire de déplacement de stock est automatiquement créé et clôturé.

## Corrections

- Correction d'une bordure rouge sur la boite de dialogue de paiement autour du premier groupe de facturation lorsque celui-ci était sélectionné.
- Correction d'un problème d'affichage sur la sélection du journal dans l'écran des écritures comptables (la taille était trop petite).

# Décembre 2023 - Version 2.18.9

## Corrections

- Correction de l'affichage du formulaire dans la fenêtre de paiement.

# Décembre 2023 - Version 2.18.8

## Corrections

- Correction de la sélection de l'imprimante dans la configuration POS.
- Correction de la boite de dialogue de commentaires dans le panier.
- Correction de l'impossibilité de réordonner les lignes de panier.
- Limitation de la taille des options de sélection qui nuisait à la sélection des emplacements de stock.

# Décembre 2023 - Version 2.18.6

## Commandes

- Si des produits de plusieurs fournisseurs sont commandés, la prévisualisation vous affiche chaque commande qui sera générée.

De plus, il est désormais possible de nommer chaque commande. Cela permet de mieux les identifier dans la liste des commandes par la suite.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/order-modal.webp"/>

<div class="alert alert-info">Note: Un nom de commande par défaut est indiqué afin de conserver la capacité à commander sans nécessité de modifier celui-ci.</div>

- Il est désormais possible de rechercher et filtrer les commandes fournisseur:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/supplier-order-list.webp"/>

## Affichage des niveaux de stock pour les produits identifiés

- Les produits identifiés affichent désormais leur niveau de stock dans la liste des produits de la même manière qu'un produit classique.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/idps-stock-on-product-list.webp"/>

<div class="alert alert-info">Note: L'écran de détail n'a pas encore été mis à jour pour afficher les niveaux de stock. Une prochaine version alignera les informations sur cet écran.</div>

- Par ailleurs l'écran de catalogue d'une catégorie identifiée a été renommé en _Dossiers par produits_

En plus du niveau de stock, il permet désormais de visualiser les dossiers ouverts pour un produit donné.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/dealer-file-stock-by-product.webp"/>

Il est possible de visualiser les dossiers qui ne sont pas liés à une fiche produit à l'aide du bouton _Afficher les IDPs sans modèles_. Une nouvelle ligne est alors ajoutée en tête de la liste des résultats pour consulter ces dossiers.

## Inventaires

### Auto résolution des stocks ayant un inventaire négatif.

Afin de vous aider à résoudre vos inventaires négatifs, une nouvelle fonctionnalité à été ajoutée, disponible uniquement pour les administrateurs.

Pour y accéder vous pouvez cliquer sur le nouveau bouton à côté de "Nouvel inventaire":

<img width="384"  src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/negative-stock-inventory/new-inventory-button.webp"/>

Vous accéderez ensuite la boite de dialogue de création d'inventaire légèrement modifiée dans le cadre de cette fonctionnalité.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.18.0/negative-stock-inventory/new-modal-options.webp"/>

Notez tout d'abord que cette boite de dialogue est à présent figée sur "Inventaire partiel" avec l'option de filtre sur les emplacements avec du stock négatif.

Vous pouvez alors cocher les options que vous souhaitez appliquer:

- **Résoudre les stocks négatifs dont le stock total est négatif ou vide**
  Cette option permet dans le cadre des filtres que vous allez sélectionner, de passer à 0 tout stock négatif, pour un produit dont le stock total, pour votre sélection est négatif.
  Attention car cette fonctionnalité peut augmenter votre total en stock, si des stocks positifs étaient disponible dans d'autres emplacements. Il est donc recommandé de l'utiliser pour un inventaire de tout l'entrepôt

- **Résoudre les stocks négatifs ayant un unique emplacement avec un stock positif**
  Cette option ne change pas votre stock total, mais va déverser le stock positif dans les emplacements ayant un stock négatif.

- **Résoudre les stocks négatifs ayant un unique emplacement avec un stock positif**
  Cette option, similaire à la précédente, ne change pas votre stock total, mais va déverser les stocks positifs dans les emplacements ayant un stock négatif.
  Les stocks seront pris aléatoirement depuis les différents stocks positifs, le résultat ne sera sans doute pas conforme à la réalité de vos stocks.

Attention donc à bien lire la description ainsi que les messages d'avertissement avant de l'utiliser.

## Améliorations diverses

- Il est possible de filtrer les dossiers dans les écrans de liste par:
  - dates de facture d'achat
  - date de facture
  - date limite de paiement.
  - Modèle
  - Année du modèle
- La recherche de contacts par numéros de téléphone a été simplifiée et n'impose plus d'utiliser un format international strict.
- Il est désormais impossible de changer la catégorie d'un produit en produit non stockable si celui-ci est en stock dans n'importe quelle concession.
- Lors d'une vente produit depuis un dossier, la boite de sélection d'un panier du client n'est plus affichée si aucun panier correspondant n'est trouvé.
- Il est désormais possible en analytique de filtrer les forfaits vendus. Ceux-ci ont un prix à zéro étant donné que celui-ci est déjà réparti sur le contenu du forfait pour une meilleure ventilation.

## Corrections

- La boite de dialogue de paiement est désormais correctement remise à jour lorsque le montant du paiement est modifié à l'aide des flèches. Elle était mise à jour correctement uniquement sur une modification clavier.
- Yuzer empêche désormais d'utiliser un ID de parent de variant égal à un l'identifiant du produit.
- Correction de la désélection des email/téléphone dans la boite de dialogue de début de prêt, ainsi que l'édition du contact.
- Correction du paramétrage des configurations de prêts qui n'était plus fonctionnelle.
