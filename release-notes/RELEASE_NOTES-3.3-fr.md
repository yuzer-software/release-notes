# Avril 2024 - Version 3.3.x

yuzSection Contacts

## Filtres clients

Deux filtres ont été ajoutés :

- État du contact (Client, Employé, Prospect, Fournisseur)
- Commercial (dernier utilisateur à avoir travaillé pour ce contact)

![Kawazaki import](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/contact-filter.webp?w=300px)

yuzSection Produits

## Import des modèles Kawasaki

Les _dealers_ Kawasaki ont maintenant accès à l'import des modèles (ou forfaits) Kawasaki.

![Kawasaki import](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/kawasaki-model-import.webp?w=300px)

## Réseaux

Les réseaux sont maintenant restreints aux catalogues sélectionnés. Après un changement de catalogue, il faudra attendre le lendemain pour que toutes les disponibilités de stock soient mises à jour.

||| N'oubliez pas de configurer vos réseaux existants avec les catalogues que vous souhaitez partager !

![Catalogues partagés avec un réseau](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/catalog-network.webp?w=600px)

yuzSection Dossiers

## Cerfa 13749 — Immatriculation d'un véhicule neuf

Le nouveau Cerfa pour l'immatriculation des véhicules (13749) est disponible (vente de véhicule neuf) !

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

- L'analyse des stock vous permet de construire des tables et des graphiques représentant l'état ou l'évolution de votre stock.

- L'analyse des stock et ventes va chercher toutes les données de facturation et l'état du stock du dernier mois (@Luc: dernier mois ou mois courant?) de la période spécifiée. Elle peut être utilisée pour réévaluer la valeur actuelle de votre stock en fonction de votre chiffre d'affaires d'une période donnée.

La configuration des tableaux de bords, filtres, source de données, tables et graphiques est similaire à celle des "Analyse des ventes".

![Menu analytiques](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.3.0/analytics/analytics-header.webp?w=600px)

## Analyse ABC

L'analyse ABC propose de trier en trois catégories l'ensemble des produits. Elle se base sur le principe que 20% des produits représente en réalité 80% de la valeur de stock (ou du chiffre d'affaire). L'idée est donc de grouper en 3 catégories vos produits en trois catégories :

- A: les x% (par exemple 15%) de produits représentant le plus de valeur
- B: les y% (par exemple 40%) de produits représentant le plus de valeur qui ne sont pas dans A
- C: tous les autres produits.

Yuzer vous permet de définir les seuils pour les valeurs de `x` et `y` sus-mentionnés.

Yuzer définit plusieurs colonnes basées sur ABC pour l'analyse du stock.

- PP ABC: utiliser la méthode ABC en se basant sur le prix d'achat (PP: purchase price)
- CP ABC: utiliser la méthode ABC en se basant sur le prix catalogue (CP: catalog price)

## Analyse des stocks

Attention, les données sur chargées par mois : un produit apparaîtra (potentiellement) une fois par mois, il conviendra donc de grouper vos données par mois, sans quoi certaines opérations risquent de ne pas avoir de sens. Par exemple, si un produit reste en stock avec une quantité de 1 toute l'année, la somme des quantités sur l'année sera de 12.

yuzSection Général

## Améliorations diverses

- Quelques améliorations de performances des tables.

## Corrections diverses

- Affichage des références multiples (codes barres, EAN, etc.) de produits lorsque plusieurs identifiants sont disponibles pour la même autorité (par exemple si un produit a deux "codes barres" valides).
- Correction de l'ordre d'affichage des entités dans la modale de disponibilité du stock.
- Correction de traductions
- Rétablissement du comportement à la facturation d'une carte fidélité déjà activée (il est possible de la ré-activer plutôt que d'échouer).
- Correction d'arrondis à la configuration de taux de la TVA
