# Mai 2021 - Version 1.4.0

- Sur la page de détail d'un produit, un graphique indique le prix d'achat du produit pour chaque réception ainsi que le prix moyen pondéré (ce qu'a coûté chaque produit en moyenne) et le cours moyen auquel les produits ont été achetés (prix moyen non pondéré).
- La selection de fournisseur lors de la création d'un dossier véhicule ou d'un produit a été améliorée.
- Il est désormais possible de choisir quelle adresse du client est utilisée lors de l'édition d'une facture de ticket de caisse.
- Lors de la création d'un nouvel essai véhicule, le libellé de la tâche est désormais auto-généré. Il peut toujours être modifié ce qui annulera l'auto-génération.
- Vous pouvez désormais envoyer un email directement depuis la fiche d'un client. Cela nécessite qu'un client email soit bien défini dans votre système d'exploitation.
- Le bouton permettant d'assigner une référence produit à un objet sans référence dans le panier est désormais plus visible.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/basket-button.png" width="200" class="mx-2"/>
- Sur l’écran _En attente de commande_, la configuration des colonnes épinglées sont maintenant conservées lorsque vous revenez sur la page.
- Ajout d’un bouton pour rafraichir la liste et les statuts des produits _en attente de commande_.
- Il est maintenant possible d’annuler une ligne de _produits en commande_. Quand vous annulez une ligne, toutes les quantités non reçues sont marquées comme _annulée_. Si besoin, vous pouvez éditer cette quantité à partir de l’écran détaillés des commandes pour la remettre en statut _commandée_.
- Ajout d’un bouton pour rafraichir le statut d'une commande sur l'écran de détails.
- Il est maintenant possible d'accéder à la commande, en lien avec une ligne, à partir de la vue _Produits en commande_.
- Lors de la facturation, les administrateurs peuvent maintenant choisir de ne pas impacter le stock pour tout type de panier. Pour ce faire, il suffit de cliquer sur le bouton _Options étendues_ dans la fenêtre _Gestion de stock du panier_. A noter que la possibilité d'ignorer l'impact stock était déjà présent dans le cadre d'une préparation de véhicule et reste disponible aux utilisateurs ayants droit.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/admin-ignore-stock-impact.png" width="200" class="mx-2"/>
- Les tickets de caisse n'affichent maintenant que le prénom suivi de la première lettre du nom de l'utilisateur.

## Appels et intégration ringover

- Nous avons ajouté des indicateurs sur les icônes des activités téléphone pour une meilleure compréhension de ceux-ci
- Vous pouvez désormais commenter une activité téléphonique afin d'y ajouter un résumé de l'appel.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/call-comment.png" width="300" class="mx-2"/>

- La liste de vos derniers appels est désormais accéssible directement depuis la bare de navigation principale.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/missed-call-pill.png" width="300" class="mx-2"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/recent-call-list.png" width="300" class="mx-2"/>

## Bare de navigation

Nous avons revu l'organisation de la bare de navigation principale en regroupant les différents éléments de manière plus logique.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/navbar.png" width="100%"/>

Vous trouvez désormais à gauche votre contexte de travail:

- La concession sur laquelle vous êtes connecté
- Et l'entrepôt dans lequel vous travaillez

Vient ensuite les raccourcis vous permettant de créer rapidement:

- Un panier vide pour une vente rapide à un client de passage par exemple / Le panier est créé sans client mais vous pouvez toujours le ré-associer par la suite.
- Un essai véhicule
- Un rendez vous atelier

Ainsi que la barre de recherche qui vous permet d'accéder à un client ou véhicule.

Enfin, la dernière section se focalise sur votre historique:

- Votre historique d'activité sur l'application bureau
- Votre historique d'activité sur l'application mobile / qui vous permet de rapidement passer de l'un à l'autre
- Votre historique d'appels téléphoniques si vous bénéficiez de l'intégration ringover

Et comme avant le bouton permettant d'afficher ou non les marges et prix d'achat dans l'application.

## Amélioration de la navigation du stock

Nous avons revu l'ordre et l'accès par défaut aux vues de stock afin d'améliorer votre productivité.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/stock-tabs.png" width="100%"/>

Lorsque vous accédez à l'onglet stock, vous êtes désormais directement redirigés vers l'onglet 'En attente de commande'.

De plus l'ordre des onglets a été modifié pour mieux refléter l'ordre logique d'un flux stock.

## Correction de bugs

- Corrige l'impression d'une cloture de caisse qui pouvait être parfois tronquée.
- Corrige le message d'erreur lorsque l'édition d'une facture échoue.
- Corrige le choix de l'identité visuelle pour l'édition de facture de ticket de caisse.
- Corrige un bug d'affichage sur les très longue références dans un panier client.
- Les lettres de l'avatar ne sont désormais jamais affichées sur 2 lignes.
- Les règles de réassort ne fonctionnaient pas sur certains produits aux références exotiques.
- Corrige l'affichage du widget de chiffre d'affaire qui ne se chargeait pas dans de rares situations (données du catalogue initial incorrectes)
- Corrige un problème empêchant le démarrage d'un prêt lorsque le niveau de carburant du véhicule n'était pas défini dans le dossier ni mis à jour avant le prêt.
