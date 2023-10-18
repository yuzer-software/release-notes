# Octobre 2023 - Version 2.16.4

## Corrections

- Correction des totaux dans la vue de commandes
- Lors de la suppression d'une ligne de panier de type _produit identifié_, les informations du client et panier sont désormais supprimées du dossier si ce dernier était lié au panier.

# Octobre 2023 - Version 2.16.3

## Corrections

- Le mapping de catégories fournisseurs dans le cadre des règles d'enrichissement de produits catalogues n'était pas correctement enregistré dans le cas de mapping conditionnel.
- Les catégories fournisseurs et catégories de tarification fournisseurs n'étaient pas mise à jour à l'édition d'un produit dans un catalogue local.

# September 2023 - Version 2.16.0

## Produits sur dossier

Vous pouvez désormais ajouter une date de livraison estimée provenant de votre fournisseur dans l'encadré _Informations d'achats_ de la fiche.

Vous pouvez également afficher le numéro de commandes et la date de livraison estimée dans la liste des dossiers.

Pour ce faire, il suffit d'activer l'affichage de ces colonnes:

<img width="480" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/dealer-file-list-column-filter.webp"/>

### Import Excel

Nous avons ajouté la possible d'importer des produits sur dossier à partir d'un fichier Excel.

Yuzer se base sur les identifiants d’autorité (VIN, immatriculation, etc.) pour savoir si un dossier existe déjà.
Par défaut, Yuzer lève une erreur s'il détecte qu'un dossier ouvert existe déjà.

Vous pouvez activer l’option _Écraser les valeurs des dossiers existants_ pour forcer la mise à jour des valeurs liées au dossier.
À noter que les attributs liés au produit identifié ne peuvent être mis à jour.

## Impression des étiquettes produits

Il est maintenant possible d'ordonner les étiquettes pour les imprimer par ordre lexicographique sur la référence des produits.

<img width="480" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/printing-price-tag.webp"/>

À noter que par défaut, les étiquettes sont triées par ordre d'ajout.

## Analytiques

Nous avons ajouté un filtre sur l'état du dossier, permettant ainsi d'exclure les dossiers _Démo_ par exemple.

<img width="360" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/analytics-dealer-file-state-filter.webp"/>

## Édition de stock

Vous pouvez désormais éditer et exporter le stock de plusieurs entités à la fois.
La liste des entités dépend de vos droits d'accès.

<img width="860" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.16.0/stock-entity-filter.webp"/>

## Améliorations diverses

- Yuzer affiche désormais le prix d'achat au moment de la facturation sur les lignes du panier lorsque le groupe de facturation a été facturé.

## Corrections

- Sur les formulaires d'édition de prix, la marge est maintenant recalculée après modification du prix d'achat.
