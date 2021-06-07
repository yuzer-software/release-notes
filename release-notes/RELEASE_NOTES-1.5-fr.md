# Juin 2021 - Version 1.5.0

- Nous avons amélioré la synchronisation des informations entre le panier et le dossier véhicule lorsqu'un véhicule à été mise à jour. Il est aussi maintenant possible de forcer la mis à jour à partir du menu contextuel du véhicule du panier.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.5.0/sync-basket-dealer-file.png" width="200" class="mx-2"/>

## Mise à jour de l'algorithme de réservation automatique

Lorsqu'un produit doit être commandé car il manque de stock, l'algorithme va tenter de réserver d'abord parmi la quantité des _Réservée en commande_ avant de réserver le stock physique.

> Par exemple:
>
> Supposons qu'un client voudrait acheter 3 unités d'un produit dont il ne reste plus que 2 stock.
> Supposons aussi que ce produit possède la règle de réassort suivante: "au minimum 1 en stock et doit être commandé par lot de 2".
>
> Lors de la réservation du panier,
> Avant: l'algorithme aurait créé 2 unités en _Attente de commande_ et enregistre 2 _Réservé_ en stock et 1 _Réservé en commande_ pour le panier.
> Maintenant: l'algorithme crée toujours 2 unités en _Attente de commande_ mais enregistre désormais 1 _Réservé_ en stock et 2 _Réservés en commande_ pour le panier.
>
> Si nous changeons la règle en: "au minimum 2 en stock et doit être commandé par lot de 2".
> Avant: l'algorithme aurait créé 4 unités en _Attente de commande_ pour respecter la règle du minimum de 2 en stock, et enregistre 2 _Réservé_ en stock et 1 _Réservé en commande_ pour le panier.
> Maintenant: l'algorithme crée toujours 4 unités en _Attente de commande_ pour respecter la règle mais enregistre 0 _Réservé_ en stock et 3 _Réservés en commande_ pour le panier.
>
> Et enfin si le produit ne possède pas de règle de réassort, il n'y a pas de changement.
> L'algorithme crée 1 unités en _Attente de commande_ et enregistre 2 à _Réservé_ en stock et 1 en _Réservé en commande_ pour le panier.

A noter qu'il est toujours possible de forcer la quantité à réserver pour une ligne de panier.

## Correction de bugs

- Corrige un problème empêchant de fermer une réception avec une ligne pour préparer 2 lignes différentes sur un panier pour le même produit.
