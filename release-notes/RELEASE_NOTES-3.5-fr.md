# June 2024 - Version 3.5.x

|| Attention, n'oubliez pas de consulter la release note de la version 3.4.x. Celle-ci a en effet été livrée à travers la 3.5.x et comporte de nombreux éléments importants.

yuzSection Recherche de produit par référence exacte

Les composants d'ajout de références disposent d'un nouveau bouton : s'il est activé, nous irons chercher le produit (unique) correspondant au préfixe catalogue et à l'identifiant renseigné.

![dealer file brand](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.5.0/fetch-product-by-exact-reference.webp)

yuzSection Dossiers et ventes produits identifiés

- Nous validons désormais que la marque est bien définie lors de la création d'un dossier. Vous pouvez de plus éditer celle-ci directement à la création si celle-ci est incorrecte.

![dealer file brand](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.5.0/dealer_file_brand.webp?w=100%)

yuzSection Tâches, atelier et prêts

- Amélioration de la vue _Timeline_ permettant d'afficher de longues périodes. Les évènements trop petits sont agrégés. Cliquer dessus permet d'effectuer un zoom sur la période.
- Améliorations des headers de la vue _Timeline_ pour que leur positionnement soit correct (les semaines ne sont plus alignées avec les mois mais avec leur positionnement temporel réel)

![Timeline](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.5.0/timeline.webp?w=100%)

yuzSection Écran client

Cette version introduit la possibilité d'afficher sur un second écran une fenêtre dédiée au client.

|| L'écran client est une fonctionnalité disponible gratuitement le temps de sa bêta. Les modalités de souscription seront précisées lorsque la fonctionnalité sera intégralement disponible.

Afin d'activer l'écran client, rendez-vous dans la _configuration POS_ et cochez _Afficher l'écran client_.

![Customer screen](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.5.0/customer_screen.webp?w=100%)

Celle-ci affiche le contenu du panier de manière simplifiée ainsi que les coordonnées du client, lui permettant de rapidement valider celles-ci.

||| Si vous pouvez utiliser n'importe quel second écran pour l'afficher nous vous recommandons d'attendre nos recommandations techniques avant d'investir dans un quelconque matériel. Les fonctionnalités interactives à venir nécessiterons un matériel compatible.

yuzSection Administration et APIs

# Messages et Conditions générales de ventes

Vous pouvez désormais ajouter une image qui sera affichée à la fin des message ou condition générales de ventes.

# Clé d'APIs et RGPD

- Ajout d'un paramètre pour qu'une clé d'API ait un accès aux données anonymisées uniquement. Cela permet de transmettre vos données de facturation ou bon de commande à un tiers sans véhiculer d'informations clients autre que le numéro de celui-ci.

![API keys](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.5.0/annonimization.webp?w=100%)

yuzSection Analytiques

Les analyses des ventes peuvent désormais être effectuées également sur les catégories éditeur et non uniquement sur les catégories Yuzer.

![Editor categories](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.5.0/editor_categories.webp?w=100%)

Cela vous permet de travailler dans un langage commun avec celui d'un de vos fournisseurs. La même possibilité sera bientôt disponible pour les analytiques de stock.

yuzSection Général

## Améliorations

- Amélioration des performances et stabilité.
- Uniformisation de certaines pages du menu d'administration
- Depuis l'historique d'une carte cadeau, sur une ligne de paiement, vous pouvez désormais naviguer directement vers le client ou le panier.

## Corrections

- Correction des couleurs d'impression lorsque l'utilisateur utilises un thème sombre.
- Correction de la sélection des catégories dans les filtres personnalisés.
- Correction de l'affichage des identités visuelles dans la boite de dialogue permettant leur sélection à l'édition d'un document (certains ratios ne s'affichaient pas convenablement).

## Corrections 3.5.6

- Correction de l'envoi d'email lors de l'édition d'un bon de commande.
