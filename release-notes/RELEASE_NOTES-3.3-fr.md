# Avril 2024 - Version 3.3.x

yuzSection Contacts

Deux filtres ont été ajoutés :

- État du contact (Client, Employé, Prospect, Fournisseur)
- Commercial (dernier utilisateur à avoir travaillé pour ce contact)

![Kawazaki import](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/contact-filter.webp?w=300px)

yuzSection Produits

## Import des modèles Kawazaki

Les _dealers_ Kawazaki ont maintenant accès à l'import des modèles (ou forfaits) Kawazaki.

![Kawazaki import](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/kawazaki-model-import.webp?w=300px)

## Réseaux

Les réseaux sont maintenant restreints aux catalogues sélectionnés. Après un changement de catalogue, il faudra attendre le lendemain pour que toutes les disponibilités de stock soient mises à jour.

||| N'oubliez pas de configurer vos réseaux existants avec les catalogues que vous souhaitez partager !

![Catalogues partagés avec un réseau](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/catalog-network.webp?w=600px)

yuzSection Dossiers

## Disponibilité réseau

Lors de la dernière version, nous avons introduits la notion de _réseau_ et la possibilité de voir les niveaux de stock de votre réseau.

Dans cette version, vous pouvez voir de manière analogue le stock de produits identifiables de votre réseau (vue "Dossiers par produits").

![Catalogues partagés avec un réseau](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/dealer-file-network-availability.webp?w=1000px)

## Galeries de documents des dossiers

Pour rappel, dans la précédente version, nous avions ajouté deux galeries de documents à vos dossiers. Chaque dossier a donc :

- une galerie partagée liée aux informations d'achat (en lecture seule)
- une galerie privée
- une galerie pargagée liée à la vente

Le propriétaire de la galerie d'achat est votre fournisseur, et il peut supprimer des documents. Vous pouvez, si vous le voulez, copier
tous les documents de la galerie d'achat dans votre galerie privée en un seul click à l'aide d'un nouveau bouton.

![Copie des documents d'une galerie](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/gallery-copy.webp?w=400px)

# Primes à l'achat et marge

Lors de la configuration des primes à l'achat, il est possible de choisir de l'inclure ou non dans la "marge incluant primes et coûts", mais cette information n'était pas visible sur la liste des primes et coûts, pouvant donner lieu à une incompréhension. Nous avons ajouté une petite coche pour rendre la chose explicite :

![Liste des primes et coûts](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/costs/all.webp?w=900px)

yuzLeft

![Prime exclue du calcul de marge](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/costs/exc.webp?w=180px)

yuzRight

![Prime inclue dans le calcul de marge](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/costs/inc.webp?w=200px)

yuzEnd

yuzSection Analytiques de stock

Une nouvelle fonctionnalité très attendue de Yuzer. Le menu _analytiques_ se voit doté de deux nouveaux onglets après "Analyse des ventes" : "Analyse du stock" et "Analyse des stock et ventes".

La configuration des tableaux de bords, filtres, source de données, tables et graphiques est similaire à celle des "Analyse des ventes".

![Menu analytiques](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/analytics/analytics-header.webp?w=600px)

yuzSection Général

## Améliorations diverses

- Quelques améliorations de performances des tables.

## Corrections diverses

- Affichage des références multiples (codes barres, EAN, etc.) de produits lorsque plusieurs identifiants sont disponibles pour la même autorité (par exemple si un produit a deux "codes barres" valides).
- Correction de l'ordre d'affichage des entités dans la modale de disponibilité du stock.
- Correction de traductions
- Rétablissement du comportement à la facturation d'une carte fidélité déjà activée (il est possible de la ré-activer plutôt que d'échouer).
- Correction d'arrondis à la configuration de taux de la TVA
