# October 2025 - Version 4.3

yuzSection 4.3.10 et suiv.

Corrections :
- Sélecteur de la catégorie de produits dans les règles de tarifications
- Ouverture du menu pour les garanties de dossiers produits
- Bugs sur certains historiques de dossiers produits
- Édition de la marque d'un dossier produit

yuzSection 4.3.9

## Tables

Nous avons fait des améliorations ergonomiques et de performances sur les tables.

  - Le nombre de sous-lignes sur les lignes d'agrégations sont affichées en petit à côté du bouton d'expansion.

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/4_3_9-pinned-row.webp?w=520px)

  - La suppression d'une colonne peut se faire directement depuis le header

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/4_3_9-remove-button.webp?w=200px)

## Dossiers véhicules

### Liste

La liste des véhicules devrait être parfaitement fluide et s'afficher instantanément.

Vous pouvez paramétrer la vue "liste" pour afficher certaines propriétés.

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/4_3_9-dealer-file-list-properties.webp?w=900px)

### Détail

Petite amélioration ergonomique.

## Réceptions

À la clôture d'une réception, vous êtes redirigé vers l'écran de rangement plutôt que vers la liste des réceptions.

## Détail produits

Dans Yuzer, les kits ne sont pas directement stockable, mais c'est leur contenu qui est en stock. Nous avons donc supprimé l'affichage de la "disponibilité" dans le cas des kits pour éviter toute confusion.

Nous avons ajouté le préfixe catalogue aux références produits sur la liste des réservations. Dans le cas du détail produit, si certaines réservations sont pour une référence équivalente, nous le soulignons.

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/4_3_9-reservations-with-prefix.webp?w=520px)


## Améliorations diverses

Contacts
  - Le numéro client est affiché avec une taille normale (elle était petite)

Exports
  - Les colonnes des export en xlsx ont une largeur mieux adaptée au contenu.

Analytiques
  - Une formule vide pour la colorisation personnalisée est toujours remplie. Pour mieux le faire comprendre, nous affichons "Sinon" dans ce cas là.

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/4_3_9-else.webp?w=220px)

## Corrections

Contacts
  - Le `mailto` utilise l'adresse du contact!

Analytiques
  - Correction du calcul du prix total lors d'une réduction appliquée sur le total
  - La colorisation personnalisée prend le dessus sur les couleurs existantes (cf. marges)

Administration
  - Possibilité de modifier le service de commande d'un fournisseur
  - Correction de l'accès aux boutons de désactivation ou réactivation d'un utilisateur
  - Correction du chargement des détails de votre entité (qui pouvait échouer dans certains cas)

yuzSection 4.3.3 à 4.3.8

# 30 septembre — Version 4.3.8

Améliorations :
  - Vous pouvez supprimer vos CGV, ce qui permet à une entité d'hériter des CGV de l'entité parente. (Faites attention à ne pas supprimer les CGV de l'entité parente !)

Corrections :
  - La valeur "exonéré de TVA" d'un contact s'affiche correctement lors de la ré-édition de ce contact.

# 29 septembre — Version 4.3.7

Améliorations :
  - Ajout de vérifications côté UI pour vous éviter des erreurs avec Yuzer Pay
  - Possibilité de choisir la TVA pour la main d'œuvre

Corrections :
  - Les catégories sont bien ré-ordonnées (préservant l'ordre d'avant la 4.3)
  - Correction du sélecteur de pays (on ne pouvait plus choisir que la France)
  - Les commentaires peuvent à nouveau être agrandis !
  - Possibilité de détacher un dossier de produit identifié lié à un panier qui n'existerait plus.

# 29 septembre — Version 4.3.5

Améliorations :
  - Possibilité de réparer l'état de stock d'un panier "client de passage" après une désynchronisation
  - L'utilisateur ne peut plus faire l'erreur d'annuler un panier avec du stock livré

Corrections :
  - Problème de rafraîchissement lors d'un re-placement de commande
  - Corrections de chargement et de synchronisation des données sur l'analyse des dossiers du réseau

yuzSection Gestion des contacts

## Distinction des organisations gouvernementales

Les organisations gouvernementales (mairies etc.) ont désormais un type de contact spécifique.

## Champs spécifiques par pays

yuzLeft

De nouveaux champs spécifiques par pays sont désormais disponibles. Cela permet de mieux remplir les informations d'entreprises qui sont spécifiques pour chaque pays.

Nous avons également continué à améliorer la lisibilité de la fiche contact, les données de pièces d'identité sont désormais plus lisibles, la galerie est désormais par défaut minimisée.
N'hésitez pas à revenir vers nous pour nous faire part de vos retours.

yuzRight

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/country_fields.webp?w=320px)

yuzEnd

## Recherche de contacts

Un service de recherche et auto-complétion des informations d'un contact est désormais proposé pour les entreprises et organisations gouvernementales Françaises.

![Enterprise search 1](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/enterprise_search_1.webp?w=600px)

||| Attention, comme indiqué ce service implique un coût au clic de _0,08_ euros (au 1er octobre 2025) par recherche.

![Enterprise search 2](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/enterprise_search_2.webp?w=500px)

## Exonérations de TVA

Il est désormais possible d'indiquer une raison à l'exonération de TVA qui sera indiquée sur les documents (factures etc.).

YUZER vous assiste pour définir l'exonération ainsi que la mention légale dans le cas d'une vente intra-communautaire ou internationale.

- À la création d'un contact
- À l'édition de celui-ci
- À l'ouverture de tout panier

Si le contact n'est pas exonéré alors que l'adresse de votre société et celle du contact indiquent clairement une vente soumise à exonération, une fenêtre est proposée permettant de mettre à jour directement et rapidement le contact.

![Exoneration suggestion](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/exonerated_1.webp?w=450px)

|| Ce procédé n'est pas appliqué pour les contacts qui sont déjà spécifiés comme exonérés car YUZER n'a pas moyen de contrôler si une raison tierce pousse à la non-exonération.

La raison d'exonération est affichée sur les documents générés.

![Exoneration reason](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/exonerated_2.webp?w=800px)

yuzSection Import de Panier

## Import de contenu dans un panier

Les améliorations permettent d'apporter plus de fluidité dans l'import des fichiers de type _EPC Honda_.

- Le format de fichier sélectionné est conservé même lorsque celui-ci n'est pas cohérent avec l'extension du fichier (Honda EPC expose en effet des csv avec une extension txt).
- Il est désormais possible d'entrer facilement un séparateur `Tab`
- Les colonnes affichées pour la configuration du mapping des fichiers csv prennent désormais en compte la ligne ayant le plus de colonnes parmi les 10 premières lignes du fichier.

Vous pouvez aussi désormais configurer des références comme main d'œuvre dans ce type d'imports:

- Entrez la référence de la M.O. et appuyez sur +

![Import paniers Ajout M.O.](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/basket-content-import.webp?w=600px)

- Configurez la correspondance sur la M.O. YUZER

![Import paniers Correspondance M.O.](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/basket-content-import-2.webp?w=600px)

## Import multiple de paniers

||| Attention cette fonctionnalité ne propose aujourd'hui qu'un format spécifique.

Vous pouvez désormais importer un fichier excel contenant le contenu d'un ou de plusieurs paniers qui seront créés automatiquement.

### Format

TODO / explication du format pris en compte

### Association du client

TODO / explication du matching client (par tags aujourd'hui)

yuzSection Analytiques

## Widget de table

Nous avons ajouté des fonctionnalités d'affichage au widget de tables.

### Mettre des niveaux en colonnes

Un nouveau bouton dans la configuration des colonnes du widget de table est disponible (entre "Grouper par" et "Colonnes visibles") et vous permet de choisir la manière dont vous descendez dans les niveaux.

![New button position](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-grouped-in-headers.webp?w=800px)

Les nouveaux modes d'affichages vous permettent, lorsque vous descendez d'un niveau, de déplacer les lignes en colonnes et d'afficher ainsi tous leurs enfants, comme illustré ci-dessous.

yuzLeft

![Table Level 1](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-grouped-in-headers-L1.webp?w=240px)

yuzRight

![Table Level 2](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-grouped-in-headers-L2.webp?w=800px)

yuzEnd

Dans le cas où vous appliquez cette option sur plusieurs niveaux, certaines colonnes peuvent ne pas exister dans tous les chemins: dans l'exemple ci-dessus, nous voyons bien qu'il n'y a pas de `TIE-INTERCEPTOR` avec l'état `Occasion`. Toutefois, pour des questions de symétrie, il est parfois désirable d'afficher tout de même toutes les colonnes.

Yuzer vous offre donc ces trois modes :

yuzLeft

![available options](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-grouped-in-headers-options.webp?w=50px)

yuzRight

- `A`: L'ancien comportement: afficher les enfants de la ligne sélectionnée
- `B`: Déplacer toutes les lignes en nouvelles colonnes, retirer les colonnes sans valeur.
- `C`: Déplacer toutes les lignes en nouvelles colonnes, garder les colonnes sans valeur.

yuzEnd

yuzLeft

Mode `B` appliqué au niveau 2.

![Keep empty columns](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-grouped-in-headers-L3-existing-only.webp?w=553px)

yuzRight

Mode `C` appliqué au niveau 2.

![Drop empty columns](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-grouped-in-headers-L3-all.webp?w=500px)

yuzEnd

### Styles personnalisés

Il est possible d'ajouter un style conditionnel aux colonnes.

- Sélectionnez le pinceau au niveau de l'en-tête de la colonne
- Définissez une formule de condition (si la formule est vide, le style s'appliquera toujours). Note sur les formules ci-dessous.
- Choisissez le style à appliquer si cette formule est vraie : au choix, la couleur du texte, la couleur de fond, ou les deux.
- Vous pouvez appliquer plusieurs conditions successives. Seule la première est appliquée. Terminer par une condition vide vous permet de définir un cas "par défaut".

![Analytics styling](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-styling.webp?w=450px)

### Formules

Vous pouvez utiliser des formules pour définir les styles de colonnes personnalisés (voir ci-dessus). Il s'agit d'un texte qui sera interprété par Yuzer.

Vous disposez des opérateurs unaires suivants :

- `+` plus unaire
- `-` négation arithmétique
- `!` négation logique

Vous disposez des opérateurs binaires suivants (classés par ordre de priorité décroissante — le plus prioritaire d'abord) :

- `%` modulo (reste de la division entière)
- `/` division
- `*` multiplication
- `-` soustraction
- `+` addition
- `==` égalité (vrai si les deux opérandes sont égales)
- `!=` différence (vrai si les deux opérandes sont différentes)
- `>=` supériorité large
- `<=` infériorité large
- `>` supériorité stricte
- `<` infériorité stricte
- `&&` conjonction (vrai si les deux opérandes sont vraies)
- `||` disjonction (vrai si l'une des deux opérandes sont vraies)

Vous disposez des fonctions mathématiques suivantes :

- `abs` valeur absolue d'un nombre
- `ceil` arrondi supérieur - plus petit entier supérieur ou égal au nombre
- `floor` arrondi inférieur - plus grand entier inférieur ou égal au nombre
- `round` arrondi au nombre entier le plus proche. Si la partie fractionnaire est `.5`, arrondit toujours vers le haut. Exemples :
  - `-1.5` → `-1`
  - `-0.5` → `0`
  - `0.5` → `1`
  - `1.5` → `2`
  - `2.5` → `3`
- `sqrt` racine carrée
- `pow` puissance - `pow(base, exposant)`
- `min` minimum entre plusieurs valeurs - `min(val1, val2, ...)`
- `max` maximum entre plusieurs valeurs - `max(val1, val2, ...)`
- `log` logarithme naturel (base e)
- `exp` exponentielle (e^x)
- `sin` sinus (radians)
- `cos` cosinus (radians)
- `tan` tangente (radians)

Notes :

- Les priorités des opérateurs suivent l'ordre mathématique standard (plus la priorité est élevée, plus l'opérateur est évalué en premier)
- Les opérateurs unaires ont la priorité la plus élevée
- Les parenthèses peuvent être utilisées pour modifier l'ordre d'évaluation


## Analytiques de Réseaux

Un nouvel écran d'analyse est disponible pour les produits identifiés distribués par un réseau. Si votre entité est possède un réseau, vous pouvez extraire des données d'analyses concernant vos dossiers et ceux de vos adhérents (avec une liaison entre les deux).

### Source de données

Vous pouvez choisir les dossiers à charger pour une période déterminée (comme d'habitude) et appliquer des conditions pour choisir quels dossiers vous intéressent. Les conditions sont disponibles pour les dossiers des adhérents au réseau et pour vos dossiers.

Au state du chargement des données, il faut et il suffit qu'une des conditions soit satisfaites pour que le dossier soit chargé.

![Data source configuration](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-network-config.webp?w=100%)

Voici la liste des conditions possibles, applicables aux dossiers des adhérents ou à vos dossiers. Vous retrouverez les informations sur la fiche du dossier, comme illustré ci-après.

- Conditions sur base d'événements pendant la période sélectionnée. Pour chaque dossier, la condition est validée si la date en question est dans la période sélectionnée.
  - Commandé au fournisseur : estimation essentiellement basé sur la date de création du dossier (`A`) — nous ne gardons _pas encore_ la date de passage en commande bien qu'il soit possible de passer un dossier de "à commander" à "commandé".
  - Acheté au fournisseur : date de facture d'achat (`C`)
  - Devrait être réceptionné : basé sur la date de livraison estimée disponible dans les informations d'achat du dossier (`D`)
  - Réceptionné : basé sur la date de réception (`B`)
  - Affecté au contact : basé sur la date d'affectation du dernier contact affecté
  - Commandé pour un client : date du bon de commande pour le dernier contact affecté (`E`)
  - Devrait être livré : date d'estimation de livraison (`F`)
  - Délivré : basé sur la date de livraison (`G`)
  - Facturé : basé sur la date de la facture (`H`)
- Conditions sur base de d'états pendant la période sélectionnée :
  - En commande : si la période sélectionnée chevauche la période entre la date de commande (~`A`) et la date de réception (`B`)
  - En stock : si la période sélectionnée chevauche la période entre la date de réception (`B`) et la date de livraison (`G`)
  - Avec le client actuel affecté : si la date d'affectation à un client est avant la fin de la période sélectionnée
  - Avec la commande client actuelle : si la date du bon de commande (`E`) est avant la fin de la période sélectionnée
  - Avec la facture actuelle : si la date de la facture (`H`) est avant la fin de la période sélectionnée
  - Sans facture (actuelle) : si la date de la facture (`H`) est après le début de la période sélectionnée

![Dealer file dates](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/analytics-network-dealer-file-dates.webp?w=100%)

### Données

Une fois les données chargées, nous essayons de faire correspondre les dossiers adhérents et fournisseurs. Pour les dossiers affiliés sans identifiants (typiquement commandés), nous utilisons la référence produit et l'affectation du dossier fournisseur au contact correspondant à l'adhérent.

Chaque ligne contient donc des informations :
- sur le réseau
- sur le dossier adhérent (s'il est défini)
- sur le dossier fournisseur (s'il est défini) — au moins le dossier adhérent ou fournisseur est défini
- sur le contact correspondant à l'adhérent (si dossier adhérent ou dossier fournisseur associé à un adhérent)
- sur le produit identifié correspondant au dossier fournisseur (à défaut au dossier adhérent)

### Colonnes

En plus des colonnes qui permettent de visualiser les données de dossiers, de produit identifié et de contact, nous avons ajouté des colonnes particulières.

#### Colonnes de contexte

Les colonnes vous permettent de grouper les données sur un certain temps.

- Année: permet de grouper les données par année
- Mois: permet de grouper les données par mois — nécessite de grouper par `année`
- Jour du mois: permet de grouper les données par jour du mois — nécessite de grouper par `mois`

#### Colonnes de comptes

Ces colonnes servent à compter les dossiers. Ce sont des sous-colonnes de "Dossier adhérent" ou "Dossier propriétaire du réseau", disponibles pour les deux types de dossier.

- Colonnes "Nb. (Événements)" : ces colonnes servent à compter des événements ; par exemple, la colonne "Facturé" vous permet de compte le nombre de dossiers facturés sur la période sélectionnée.
- Colonnes "Nb. (État)" :
  - En commande : nombre de dossiers qui sont ont été en commande au cours de la période. Si la période est d'un mois, et si un dossier est en commande au premier jour du mois (puis stocké), et un autre mis en commande au dernier jour du mois, alors il est considéré qu'il y a eu en tout 2 dossiers en commande ce mois-ci.
  - En stock
  - En commande au dernier jour de la période
  - En stock au dernier jour de la période
  - En commande ou en stock au dernier jour de la période
  - Facturé aux _n_ derniers mois de la période : nécessite de charger au moins _n_ mois...
  - Moyenne de facturation mensuelle sur les _n_ derniers mois de la période
  - Couverture de stock (Mois) : nombre de mois pendant lesquelles le stock actuel peut satisfaire la demande moyenne des 6 derniers mois (nécessite de charger au moins 6 mois).
  - Écart (6m) : différentiel entre la somme stock et commandes en fin de période et le stock vendu ces 6 derniers mois (nécessite de charger au moins 6 mois)

yuzSection Intégrations

## Ringover

Un connecteur Ringover premium est désormais disponible. Lorsque celui-ci est activé, vous pouvez afficher les transcriptions et écouter les appels directement depuis YUZER.

Sur une fiche contact, les activités liées à Ringover disposent désormais de boutons pour lire l'enregistrement de l'appel et charger la transcription.

La transcription du premier appel est automatiquement chargée.

![Ringover Premium](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/ringover_premium.webp?w=400px)

Une fois la lecture lancée vous pouvez controller celle-ci depuis YUZER.

![Ringover Premium 2](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/ringover_premium_2.webp?w=400px)

## Suzuki

- Le catalogue Suzuki est désormais synchronisé avec une source officielle chaque jour.
- Le placement automatique de commandes est implémenté et attend la mise en place du service en production par les équipes informatiques Suzuki.

## CUBE

Le catalogue CUBE actuel devient déprécié. En effet les références CUBE ne sont pas unique dans le temps. Pour éviter qu'un produit de votre "vieux" stock ne change de désignation dans YUZER au gré d'un recyclage de référence par le constructeur nous avons introduit une nouvelle référence, affichée en plus de la référence réelle.

Un nouveau catalogue est disponible, utilisant cette nouvelle fonctionnalité afin de garantir une utilisation et un affichage sur base de la référence usuelle tout en garantissant l'unicité d'une référence interne fournie par Planet'Fun.

## Honda

- Une intégration avec la technologie de réception AutoVHC sélectionnée par Honda a été implémentée et sera mise à l'essai chez les concessionaires concernés.

yuzSection Général

## Améliorations

- Vous pouvez désormais sélectionner les domaines sur lesquels vos entités sont affectées. Ainsi, si votre license vous donne accès aux marchés vélo et moto mais qu'une de vos boutiques travaille sur le marché vélo uniquement et une autre sur le marché moto uniquement, cela peut-être configuré.

Les catalogues accessibles dans la recherche de catalogues à ajouter prennent en compte le marché du catalogue d'une part et celui auquel vous avez accès d'autre part pour ne proposer que les éléments qui vous intéressent.

- Un nouveau marché _Énergie du bâtiment_, proposant de nouvelles catégories spécifiques, est désormais disponible pour les vendeurs de cheminées et poêles à bois.

## Corrections
