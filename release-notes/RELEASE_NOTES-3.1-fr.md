# Février 2024 - Version 3.1.x

yuzSection Commande

## Sous-vues

L'écran _En attente de commande_ a évolué et propose plusieurs sous-vues:

![Sous vues En attente de commande](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.1.0/orders/order_1.webp?w=100%)

- Réservations sans produit défini:
  Cette sous vue affiche les réservations émannant de lignes de panier qui n'ont pas de référence. Il est recommandé de les traiter le plus tôt possible étant donné que celles-ci pourraient impacter des commandes à passer.
- Stock négatif
  Cette sous-vue affiche les lignes en attente de de commandes générées par le bot Yuzer alors que le stock produit était négatif en entrepôt. Elles sont donc clairement dues à un mauvais enregistrement/répercution de données stock. Un inventaire des produits de cette vue est souhaitable.
- Autres
  Cette sous-vue affiche les lignes en attente de de commandes générées par le bot Yuzer alors que le stock produit était positif ou par les employés.
  Il n'y a pas de raisons claire d'avoir une suspicion mais la qualité de la remonté du bot dépends de la correction des niveaux de stock et des réservations et commandes enregistées.
- Tous
  Cette sous-vue affiche toutes les lignes en attente de commande, négative ou non.

A noter que certains boutons peuvent ne pas être affiché ou ne pas être proposés en fonction des lignes existantes. Par exemple s'il n'existe pas de réservations sans produit défini, ni de lignes générées alors que le stock était négatif, seule la vue Tous est accessible.

### Traiter les réservations sans produit défini

En cours d'écriture: explique comment traiter ces lignes (vérifier si une ref existe déjà, si non la retrouver et créer, puis remplacer la ligne dans le panier).

### Gérer les commandes en stock négatif

Il y a deux manières de traiter ces lignes.

- Effectuer un inventaire des produits en question. C'est en général la meilleure action à effectuer.
- Valider la ligne pour que celle-ci ne soit plus considérée comme suspecte si l'on est certain que la quantité proposée est effectivement à commander.

![Valider stock négatif](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.1.0/orders/order_2.webp?w=100%)

| Note: il est aussi possible de valider les lignes du bot depuis les sous-vues _Autres_ ou _Tous_. Cela permet de vous assigner à la ligne en question et de valider manuellement les besoins de commandes proposés par le bot ou par un de vos collègues.

![Valider d'un autre utilisateur](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.1.0/orders/order_3.webp?w=100%)

- Si une quantité différente doit-être commandée il suffit d'ajouter une nouvelle commande pour cette référence avec la bonne quantité.

## Filtre employés

Il est désormais possible de filtrer les lignes _En attente de commande_ en utilisant un filtre employé. Cela permet de ne sélectionner que les lignes qui ont bien été validées par un, ou plusieurs utilisateurs référents.

## Autres améliorations

- Possibilité d'annuler les anciennes commandes et anciennces commandes en attente
- Un panier est maintenant créé chez l'entité du fournisseur lorsqu'on place une commande créée manuellement (par l'onglet commandes).
  - Il est possible de commander un modèle de véhicule par ce biais, celui-ci pourra alors être transféré puis réceptionné et lié à un dossier.

yuzSection Général

## Améliorations diverses

- Il est maintenant possible de définir des règles spécifique pour une référence produit dans le programme de fidélité.
- Les différentes étapes composant le flux de facturation sont désormais orchestrées par nos serveurs pour plus de stabilité. Les autres flux (édition des bons de commandes etc.) suivront le même chemin dans les versions à venir. Cela devrait vous prémunir d'incohérences en cas d'erreurs réseau entre vos postes et nos serveurs.

## Corrections

- Correction du mapping pour les couleurs standardisées sur l'import de dossier.
- Il est maintenant possible d'éditer un ticket de caisse avec un produit unique (import depuis un modèle) dans le panier.
