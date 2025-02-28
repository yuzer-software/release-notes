# Mars 2025 - Version 3.12.x

yuzSection Export de catalogues

Yuzer permet aux éditeurs de catalogues de permettre la configuration d'un export automatisé de ceux-ci. Les catalogues exportés peuvent alors être téléchargés par les autres utilisateurs abonnés à celui-ci.

Depuis un catalogue dont vous êtes l'éditeur, rendez-vous dans l'onglet _Exportation_

![Catalog export](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-catalog.webp?w=100%)

Vous pouvez ici visualiser les jobs d'exportation si certains sont définis ou en créer un nouveau avec le bouton _Nouveau_.

A la création d'un nouvel export une fenêtre de configuration s'ouvre et vous permet de configurer

- le nom du catalogue exporté (il peut-être différent du nom du catalogue en fonction du format ou des filtres que vous pourriez définir).
- une description
- Le format du fichier csv exporté (dont le choix des colonnes)

![Catalog export format](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-modal-format.webp?w=100%)

- Et dans l'onglet filtres la configuration des éléments à exporter

![Catalog export filter](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-modal-filter.webp?w=100%)

L'export est exécuté chaque nuit et vous pouvez alors lancer le téléchargement du catalogue depuis l'écran du catalogue dans YUZER à l'aide du bouton télécharger (cf. première capture d'écran ci-dessus).

||| Les exports de catalogues peuvent également être retrouvés depuis la section automates.

![Catalog export filter](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-automation.webp?w=100%)

yuzSection Écran client et marketing

Vous pouvez désormais configurer un media à afficher sur votre écran déporté:

![Customer screen marketing configure](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/cust-screen-marketing.webp?w=100%)

- Quand aucun panier n'est actif
  ![Customer screen no basket](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/marketing-nobasket.webp?w=100%)

- Quant un panier est actif
  ![Customer screen basket](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/marketing-basket.webp?w=100%)

yuzSection Général

# Tâches commerciales

Vous pouvez désormais facilement créer une tâche de suivi depuis une tâche existante à J+2/4/7.

![Task follow up](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/task-follow-up.webp?w=100%)

## Divers

- Amélioration de la persistence des configuration calendrier sur les vues commercial et atelier.
- Amélioration de la réinitialisation de mot de passe (un email valide pour l'utilisateur reste requis).
- Amélioration mineure de l'affichage des variants sur le détail d'une fiche produit.

- Correction de raffraichissement sur l'écran de calendrier lors de l'accès à une date par le sélecteur de dates.
- Correction de la connexion lors de certains cas d'expiration de token aux limites.
- Correction de comportements de pré-sélection dans un panier multi-groupes (écran de paiement etc.).
- Correction de la configuration d'une catégorie de tarification dans une règle d'enrichissement de catalogue.
- Les réservations de stock affichent désormais la référence produit et son label par défaut sur tous les écrans.

Comme toujours n'hésitez pas à exprimer, en toute courtoisie, auprès de nos équipes support vos demandes!
