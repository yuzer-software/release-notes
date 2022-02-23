# Février 2022 - Version 1.18.5

# C'est corrigé

- Le filtre sur les tâches non-assignées est maintenant fonctionnel.
- Vous pouvez à nouveau éditer les prix sur les lignes de paniers de cession.

# Février 2022 - Version 1.18.4

# Améliorations diverses

- Lorsque vous ajoutez des produits dans un groupe de facturation de type "cession", le prix de vente corresponds désormais à la valeur du prix d'achat moyen pondéré du stock s'il existe.

# C'est corrigé

- La TVA d'achat est maintenant correctement enregistrée lors de la sauvegarde des prix, en particulier sur les dossiers. Par conséquent, vous ne devriez plus avoir de messages d'avertissement causés par cette erreur lors de la facturation de vos nouveaux dossiers.

# Février 2022 - Version 1.18.3

# Améliorations diverses

- Vous pouvez désormais modifier les tags d'un contact.
- Lors de la création d'un nouveau dossier vous êtes désormais redirigés vers le détail de celui-ci.
- Lorsqu'une commande est passée pour un fournisseur, vous êtes désormais redirigés vers la page de détail de la commande.
- Lorsqu'une tâche est marquée comme "Fait" toutes ses sous-tâches le sont également. Ceci n'était effectué qu'à la clôture dans les versions précédentes.

# Transferts inter-entité

Il est désormais possible de faire des transferts de stock entre différentes entités.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/transfer-create.png" height="500"/>

## Liste des transferts

La liste des transferts recense les transferts depuis ou vers cette entité (y inclus les transferts intra-entité). Dans le cas d'un transfert inter-entité, le nom de l'entité est affiché en gras.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/transfer-list.png" height="200"/>

## Liste des réceptions

- Nous avons inversé les colonnes "Fournisseur" et "Entrepôt" de la liste des réceptions: la lecture est plus naturelle puisque le "Fournisseur" est l'expéditeur et "Entrepôt" la destination. Cela correspond aussi davantage à ce qui est représenté côté Transferts.
- Lorsqu'une réception est une réception d'un transfert inter-entité, nous n'affichons pas le nom de l'entrepôt comme "Fournisseur" mais seulement le nom de l'entité.
- Lorsqu'une réception est une réception d'un transfert, nous avons remplacé le numéro de livraison (qui correspondait à un identifiant interne du transfert) par un lien vers le transfert.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/reception-list.png" height="85"/>

# Gestion des bons de livraison

Il est désormais possible d'établir un bon de livraison avant la facturation. Le bon de livraison implique la sortie immédiate du produit du stock et peut-être remis à votre client.

Il permet notamment de permettre de conserver un panier ouvert pour permettre des livraisons régulière puis une facturation mensuelle de l'ensemble des éléments livrés.

# Recherche des contacts

Vous pouvez désormais ajouter un ensemble de filtres lors de la recherche d'un contacts:

- Par marque de véhicule possédé
- Puis par modèle (il faut sélectionner la marque au préalable)
- Par année du véhicule
- Par tags

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/contact-filter.png" height="650"/>

# Amélioration de l'affichage des CGV

Complétant les améliorations apportées sur la version précédente vous permettant de définir une police et une taille spécifique nous avons ajouté la possibilité de disposer vos CGV en colonnes.

Rendez vous dans la section _Administration / Gestion commerciale / Messages et CGV_ puis cliquez sur le bouton d'édition se situant en haut à droite de la page.

Sélectionnez les CGV que vous souhaitez éditer et définissez le nombre de colonnes. Nous avons constaté que la configuration suivante permet un bon résultat:

- Nombre de colonnes: 3
- Police: Arial Narrow
- Taille: 2

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/cgv_nb_cols.png" height="80"/>

# Marges dans les paniers

Les prix d'achat sont désormais récupérés depuis le stock (prix d'achat moyen pondéré) pour afficher la marge réelle en sus de la marge catalogue dans le panier.

Ce même prix est bien utilisé dans les cessions éditées.

Lorsque le produit n'a pas encore été stocké le prix d'achat utilisé reste le prix catalogue. Un indicateur vous permet de savoir quel prix est utilisé.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/basket-purchase-stock-price.png" height="106"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/basket-purchase-catalog-price.png" height="150"/>

# Améliorations du widget de main d'oeuvre

Des options de configuration du widget ont été ajoutées:

Vous pouvez donc:

- Configurer l'affichage des données sous forme de table.
- Trier la main d'oeuvre facturée ou en cession
- Filtrer par type de panier

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/workforce-widget-settings.png" height="320"/>

- Il est désormais possible de définir une période glissante plutôt qu'une période fixe

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/sliding-period-workforce.png" height="280"/>

L'affichage des données sous forme de table est par défaut à plat:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/workforce-widget-table.png" height="380"/>

Vous pouvez glisser une colonne afin de grouper les données

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/workforce-widget-table-groupped.png" height="380"/>

Notez que le groupement n'est pour l'instant pas sauvegardé et doit-être effectué directement sur le widget. Ceci fera l'objet d'une amélioration dans le futur.

Enfin il est possible d'exporter en CSV les données de la table, soit l'ensemble des lignes sans regroupement, soit seulement les lignes regroupées.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/workforce-widget-export.png" height="160"/>

# Analyses des ventes

Nous avons ajouté une fonctionnalité d'analyse des ventes qui vous permet de définir sur une période donnée un ensemble de filtres et agrégations vous permettant de mieux analyser l'activité vente de votre magasin.

La fonctionnalité est disponible en bêta et nous allons apporter de régulières améliorations à celle-ci.

Parmi les limitations actuelles, les filtres personnalisés et tableaux de bords sauvegardés sont disponibles sur une entité et l'ensemble de ses entités filles à moins que l'entité fille définisse ses propres filtres ou ses propres tableaux de bords. Dans ce cas les tableaux de bords de l'entité fille remplacent celle de son parent plutôt que de s'ajouter à ceux-ci.

Si vous souhaitez ne configurer les éléments qu'une seule fois il vous faudra donc effectuer les étapes de configuration sur votre entité parente.

## Filtres personnalisés des produits

La création de filtres personnalisés vous permet de définir des filtres de produits complexes pouvant être réutilisés dans les analyses pour filtrer les données.

Vous pouvez filtrer aujourd'hui sur les champs principaux d'un produit et appliquer plusieurs types de conditions.

## Création d'une analyse

Avant de créer une analyse vous devez sélectionner une période d'analyse. Vous pouvez définir la période que vous souhaitez de date à date, ou utiliser un des boutons rapides pour définir celle-ci.

Une fois les données chargées, Yuzer vous présente l'écran de configuration d'analyse. Celui-ci vous permet de définir un ensemble de filtres (dont les filtres personnalisés que vous auriez pu définir au préalable), les différentes colonnes d'agrégation de l'analyse, ainsi que les colonnes à afficher en plus des colonnes d'agrégations pour les lignes détaillées.

Les lignes telles que les prix, les quantités mais aussi les numéros de clients, numéros d'acheteur ou identifiant du document peuvent voir leur valeurs ou nombre de valeurs distinctes agrégé(e)s.

## Visualisation d'une analyse

Une fois l'analyse configurée vous pouvez visualiser le tableau contenant les données de celles-ci. Dans cette première version il n'est pas encore possible de configurer un graphique à partir d'une analyse ni de grouper ceux-ci dans une même page.

Vous pouvez néanmoins dès à présent exporter les données des tableaux générés, en utilisant l'export soit des détails soit des agrégations.

## Facturé par et Ajouté par

La personne qui a ajouté une ligne dans le panier (_Ajouté par_) est désormais différenciée de celle qui a facturé (_Facturé par_). Cette donnée, qui sera ajoutée dans le futur au widget de chiffre d'affaire, est dès à présent disponible dans la nouvelle fonctionnalité d'analyse.

# Amélioration de l'affichage des indisponibilités sur le planning

Les personnes qui sont totalement indisponible sur une journée données ont un affichage désormais plus visible qu'un simple taux d'utilisation à 100%. Le contraste de période de fermeture du midi a également été augmenté.

Cette première amélioration ne prends pas encore en compte les indisponibilité du matin ou de l'après midi uniquement. Seule les personnes absentent la journée entière sont affectées. De même si l'affichage est modifié nous n'empêchons pas encore la planification de tâches à l'employé absent.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.18.0/unavailability-planning.png" height="320"/>

# C'est corrigé

- Les coûts opérationnels ajoutés lors de la création d'un nouveau dossier sont désormais bien calculés et ne nécessitent plus d'édition de ceux-ci sur la page de détail.
- La fonctionnalité s'adapter à l'écran devrait bien s'appliquer lorsque la vue calendrier est quittée et réouverte. Attention cependant, si vous avez accès aux pages calendrier commercial et atelier la sauvegarde du paramètre est indépendante pour chacune de ces vues.
- L'ajout de modèles dans une cession ne recopie plus les prix avec marges et TVA et va de plus bien récupérer le prix d'achat moyen pondéré du stock.

# Application mobile

## Transferts inter-entité

L'application mobile supporte elle aussi les transferts inter-entité : création, modification, envoi, réception, etc.

## Codes à barres

Certains codes à barres étaient mal interprétés (certains caractères invisibles pouvaient être présents, ce qui empêchait de trouver la référence sans une intervention manuelle pour supprimer le caractère indésirable). Nous avons amélioré la lecture de ces codes à barres. Si d'autres codes n'étaient pas lus correctement, merci de les envoyer au support !

## Expertises et tâches

Lorsqu'une tâche est liée à un panier et à un véhicule, il était déjà possible de créer des expertises photos pour ce véhicule directement depuis la tâche, mais la tâche n'était pas automatiquement liée au panier. Voici qui est corrigé !
