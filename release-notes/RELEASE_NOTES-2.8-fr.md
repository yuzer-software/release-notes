# Mars 2022 - Version 2.8.x

# Tickets de caisse dématérialisés

Seuls documents qui n'étaient pas dématérialisés dans Yuzer, les tickets de caisse rejoignent factures et autres documents afin de pouvoir être envoyé par email au lieu d'être imprimé.

Cette contrainte est obligatoire à partir du 1er avril.

# Analytiques

- Il est désormais possible de filtrer les données d'une source de donnée par niveau pour une entité donnée. Cela permet sur un même tableau de bord de disposer de visualisations spécifiques à une entité, et d'autres à une autre entité.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.8.0/ana_entity_filter.png" width="240px"/>

- Vous pouvez désormais configurer l'affichage des tables, leur titre, réduire la hauteur des lignes ou afficher ou non les bordures.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.8.0/ana_table_config.png" width="240px"/>

- Correction de la fonction _cumulatif_ sur les graphiques
- Correction de traductions

# Amélioration des synchronisation des tâches

Désormais, lorsque tous les produits d'un paniers sont reçus à la clôture d'une réception, la tâche du panier passe du statut _En attente de fournisseur_ au statut _En attente de réception_ si la tâche de récéption du panier n'est pas faite ou _A faire_ si la tâche de réception du panier est effecutée.

# Remises intégrales en comptabilité

Vous pouvez désormais choisir de comptabiliser une ligne remisée en intégralité (dans le cadre d'une vente client) sur le compte de cession cadeau clientèle plutôt que mouvementer un compte de produit et de remise.

Afin d'activer cette fonctionalité rendez vous dans vos paramètres de comptabilité et cochez la case associée:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.8.0/accountancy_cession.png" width="100%"/>

# Impression des étiquettes avec information recyclage

Vous pouvez désormais imprimer les étiquettes avec l'ajout des informations de recyclage si vous le souhaitez. Si le packaging du produit que vous vendez ne le contient pas vous devez désormais imprimer une étiquette incluant les informations.

# Fusions des produits

Nous allons progressivement offrir à tous l'ouverture de notre fonctionnalité de fusion de fiches produits. Cette fonctionnalité vous permet de déclarer plusieurs fiches produits de plusieurs catalogues comme étant identiques.

Certaines fusions sont proposées automatiquement par le système, c'est particulièrement le cas pour les catalogues

- BIHR: Fusions des anciennes/nouvelles références)
- SADEM:
- Michelin
- Pirelli

Cette fonctionnalité sera mise à disposition de tous dans la version 2.9.0. N'hésitez pas à vous rapprocher de notre support en cas de questions afin

# Nouvelles intégrations de catalogues

Les catalogues des marques

- Prorima
- Chaft
- Trophy

ont été ajoutés à la base de catalogues disponibles.

# Oubli de la release note 2.7.x: Liste des tickets

A partir de la version 2.7 tous les tickets sont automatiquement affichés dans l'onglet _Ticket de caisse et acompte_ qui a été renommé pour être plus explicite. Dans les versions précédentes les tickets de caisses étaient affichés par défaut et il fallait désactiver un filtre pour visualiser l'ensemble des reçus.

Il est également possible d'appliquer différents filtres, sur le type de ticket (ticket de caisse ou acompte):

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.8.0/receipt_list.png" width="100%"/>

et pour l'ensemble des documents sur les montants:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.8.0/receipt_list_amount_filter.png" width="240px"/>
