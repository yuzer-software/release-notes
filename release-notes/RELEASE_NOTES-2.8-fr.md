# Mars 2022 - Version 2.8.x

# Tickets de caisse dématérialisés

Seuls documents qui n'étaient pas dématérialisés dans Yuzer, les tickets de caisse rejoignent factures et autres documents afin de pouvoir être envoyés par email au lieu d'être imprimés.

Cette contrainte est obligatoire à partir du 1er avril.

# Analytiques

- Il est désormais possible de filtrer les données d'une source de donnée par niveau pour une entité donnée. Cela permet sur un même tableau de bord de disposer de visualisations spécifiques à une entité, et d'autres à une autre entité.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/ana_entity_filter.png" width="240px"/>

- Vous pouvez désormais configurer l'affichage des tables, leur titre, réduire la hauteur des lignes ou afficher ou non les bordures.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/ana_table_config.png" width="240px"/>

- Correction de la fonction _cumulatif_ sur les graphiques
- Correction de traductions

# Amélioration des synchronisations des tâches

Désormais, lorsque tous les produits d'un panier sont reçus à la clôture d'une réception, la tâche du panier passe du statut _En attente de fournisseur_ au statut _En attente de réception_ si la tâche de réception du panier n'est pas faite ou _A faire_ si la tâche de réception du panier est effectuée.

# Remises intégrales en comptabilité

Vous pouvez désormais choisir de comptabiliser une ligne remisée en intégralité (dans le cadre d'une vente client) sur le compte de cession cadeau clientèle plutôt que mouvementer un compte de produit et de remise.

Afin d'activer cette fonctionnalité rendez-vous dans vos paramètres de comptabilité et cochez la case associée :

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/accountancy_cession.png" width="100%"/>

# Impression des étiquettes avec information recyclage

Vous pouvez désormais imprimer les étiquettes avec l'ajout des informations de recyclage si vous le souhaitez. Si le packaging du produit que vous vendez ne le contient pas vous devez désormais imprimer une étiquette incluant les informations.

# Regroupement de fiches produits identiques

Cette fonctionnalité permet d'établir une correspondance entre plusieurs références fournisseurs, afin d'indiquer qu'il s'agit d'un seul et même produit. L'unique fiche produit indique alors toutes les références fournisseurs. La référence principale est celle qui est utilisé par défaut lorsque l'on passe commande.

Certaines correspondances sont établies automatiquement par Yuzer, en particulier pour les produits des catalogues BIHR, SADEM, Michelin et Pirelli.

Noter qu'il existe maintenant une notion de priorité sur les catalogues auxquels une entité (point de vente, etc.) est abonné. Ceci permet d'indiquer une préférence entre les fournisseurs, et impactera donc la référence principale. De plus chaque entité peut déclarer ses propres correspondances, qui n'affecteront alors que celle-ci.

Cette fonctionnalité est pour le moment restreinte à quelques comptes beta-testeurs. Mais elle sera très prochainement ouverte à tous.

# Nouvelles intégrations de catalogues

Les catalogues des marques

- Prorima
- Chaft
- Trophy

ont été ajoutés à la base de catalogues disponibles.

# Amélioration de la fusion catalogues

Vous pouvez désormais choisir ne fusionner que les références de produits que vous avez en stock. Pour cela il suffit de cocher l'option `Charger seulement les produits possédant réservations, commandes ou évènements de stock` avant de sélectionner le catalogue cible.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/catalog_merge_load_stock_only.png" width="896px"/>

Nous avons aussi ajouté des filtres et une pagination sur l'écran de résolution de produits manquants afin de faciliter la saisie ainsi que la navigation.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/catalog_merge_filters.png" width="896px"/>

# Oubli de la release note 2.7.x: Liste des tickets

À partir de la version 2.7 tous les tickets sont automatiquement affichés dans l'onglet _Ticket de caisse et acompte_ qui a été renommé pour être plus explicite. Dans les versions précédentes les tickets de caisses étaient affichés par défaut et il fallait désactiver un filtre pour visualiser l'ensemble des reçus.

Il est également possible d'appliquer différents filtres, sur le type de ticket (ticket de caisse ou acompte):

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/receipt_list.png" width="100%"/>

et pour l'ensemble des documents sur les montants :

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.8.0/receipt_list_amount_filter.png" width="240px"/>
