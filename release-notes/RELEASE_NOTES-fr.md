# Mai 2021 - Version 1.4.0

- Sur la page de détail d'un produit, un graphique indique le prix d'achat du produit pour chaque réception ainsi que le prix moyen pondéré (ce qu'a coûté chaque produit en moyenne) et le cours moyen auquel les produits ont été achetés (prix moyen non pondéré).
- La selection de fournisseur lors de la création d'un dossier véhicule ou d'un produit a été améliorée.
- Il est désormais possible de choisir quelle adresse du client est utilisée lors de l'édition d'une facture de ticket de caisse.
- Le bouton permettant d'assigner une référence produit à un objet sans référence dans le panier est désormais plus visible.
- Lors de la création d'un nouvel essai véhicule, le libellé de la tâche est désormais auto-généré. Il peut toujours être modifié ce qui annulera l'auto-génération.
- Vous pouvez désormais envoyer un email directement depuis la fiche d'un client. Cela nécessite qu'un client email soit bien défini dans votre système d'exploitation.

## Appels et intégration ringover

- Nous avons ajouté des indicateurs sur les icones des activités téléphone pour une meilleure compréhenssion de ceux-ci
- Vous pouvez désormais commenter une activité téléphonique afin d'y ajouter un résumé de l'appel.
- La liste de vos derniers appels est désormais accéssible directement depuis la bare de navigation principale.

## Bare de navigation

Nous avons revu l'organisation de la bare de navigation principale en regroupant les différents éléments de manière plus logique.

## Amélioration de la navigation du stock

Nous avons revu l'ordre et l'accès par défaut aux vues de stock afin d'améliorer votre productivité.

## Correction de bugs

- Corrige l'impression d'une cloture de caisse qui pouvait être parfois tronquée.
- Corrige le message d'erreur lorsque l'édition d'une facture échoue.
- Corrige le choix de l'identité visuelle pour l'édition de facture de ticket de caisse.
- Corrige un bug d'affichage sur les très longue références dans un panier client.
- Les lettres de l'avatar ne sont désormais jamais affichées sur 2 lignes.
- Les règles de réassort ne fonctionnaient pas sur certains produits aux références exotiques.
- Corrige l'affichage du widget de chiffre d'affaire qui ne se chargait pas dans de rares situations (données du catalogue initial incorrectes)
- Corrige un problème empêchant le démarrage d'un prêt lorsque le niveau de carburant du véhicule n'était pas défini dans le dossier ni mis à jour avant le prêt.

# Mai 2021 - Version 1.3.0

- Vous pouvez désormais éditer les quantités à réserver depuis la modale de gestion du stock et commandes d'un panier
- La suppression des lignes en attente de commande est désormais possible; cependant dans le cas ou une ligne est créée automatiquement il est possible que celle-ci soit recréée si la quantité à commandée dans les panier l'exige.
- Les lignes de commande créées automatiquement ont désormais un petit icone de robot pour être identifiée plus facilement.
- Le nombre de réservations client est maintenant affiché pour chaque produit en attente de commande et vous pouvez accéder aux détails grâce à une modale.
- Les listes de tâches (réception, atelier, prêt véhicule etc.) affiche désormais le filtre sur status correctement et permet de facilement supprimer le filtre ou de ne filtrer que sur les tâches non terminées.
- Le filtre par défaut sur la liste mensualisée des essai véhicules (dans la section client) est désormais supprimé, toutes les tâches sont donc désormais visibles par défaut.
- Le journal en attente de validation de la comptabilité est désormais paginé par mois
- La taille du logo sur les documents a été augmentée

## Identité visuelle

Vous pouvez désormais configurer de multiples identités visuelles en plus du logo standard de la société à l'aide d'une gallerie d'images sur la configuration des informations de la concession.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/identity-cfg.png" width="100%" class="mb-3"/>

Ces identités visuelles sont proposées lors de l'édition d'un document

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/identity-select.png" width="300" class="mb-3"/>

Afin que vos documents reflettent mieux l'identité de la marque ou de votre concession

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/identity-document.png" width="300" class="mb-3"/>

## Intégration avec Ringover

Cette nouvelle version introduit la connection entre Yuzer et votre compte de services téléphonique Ringover. Ceci vous permettra de garder automatiquement le suivi des interractions téléphoniques que vous ou vos collègues ont pu avoir avec un client. Vous recevrez également des notifications in-app permettant d'accéder rapidement à une fiche client lorsqu'un client vous appelle.

### Configuration

Afin de configurer l'intégration, rendez-vous dans la section téléphonie du paneau d'administration et suivez les étapes décrites.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/ringover-cfg.png" width="100%" class="mb-3"/>

Notez que suite à votre authentification sur ringover, la redirection vers le lien désiré est perdue et vous arriverez sur la page principale de votre panneau de configuration ringover. Vous pouvez re-cliquer sur le lien de l'étape 1 afin d'être redirigé vers le bon emplacement.

### Configuration des numéros de téléphone

Une fois le lien avec Ringover établi vous devez configurer dans Yuzer le numéro de téléphone associé à vos employés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/ringover-user.png" width="100%" class="mb-3"/>

### Notifications sur appels

Lorsque vous recevez un appel téléphonique Yuzer va afficher une notification qui vous permettra d'accéder à la fiche du client vous appelant.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/ringover-notification.png" width="300" class="mb-3"/>

### Activité client

Les activités des appels ou SMS reçus par Ringover sont affichés directement sur la page de contact.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/ringover-activity.png" width="600" class="mb-3"/>

## Traitement de stock pour les préparation de véhicules

Lors de l'édition d'un document de cession, vous avez maintenant la possibilité de choisir l'action à effectuer sur le stock pour chacune des lignes du panier.

Vous avez le choix entre :

- Déplacer le stock sur le véhicule : L'emplacement du produit sera déplacé sur le véhicule. Le produit est considéré comme étant toujours en stock.
- Retirer du stock : Le produit est déstocké donc ne sera plus en stock.
- Ne pas impacter le stock : Aucune action sur le stock.

Concrètement, lors de l'édition de la facture de cession, la modale de gestion de stock s'affichera comme à l'habitude.

Vous pouvez alors choisir de ne pas impacter le stock au lieu d'effectuer le prélèvement :

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/stock-process-pick-or-ignore.png" width="400" class="mb-3"/>

Dans ce cas la ligne s'affichera comme tel :

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/stock-process-ignore-display.png" width="400" class="mb-3"/>

Si vous effectuez un prélèvement vous aurez le choix de monter la pièce sur le véhicule (par défaut) ou bien de le déstocker (par exemple si la vente de véhicule aurait déjà impacté le stock) :

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/stock-process-choose-out-or-move.png" width="600" class="mb-3"/>

De nouveaux icônes ont été ajoutés à côté du nombre de quantité traitées pour indiquer comment le stock a été impacter.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.3.0/stock-process-icons.png" width="600" class="mb-3"/>

## Picking de panier par l'application mobile

Il est désormais possible de _préparer_ les paniers clients depuis l'application mobile. Un produit peut être ajouté au panier en tant que nouvelle ligne en même temps qu'il est prélevé (_pick_).

### Accès au panier

Il y a trois façons d'accéder au panier.

- Depuis les _Travaux récents sur l'application de bureau_ (menu latéral) : si vous avez travaillé sur un panier depuis l'application de bureau, vous le retrouverez sur l'application mobile, et inversement.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/last-works.png" width="200" class="mb-3"/>

- Depuis vos tâches, en cliquant sur l'icône de panier en bas à gauche.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/open-basket-from-task.png" width="200" class="mb-3"/>

- En scannant le QR-code de la modale de gestion de stock (cliquez sur le qr-code pour l'agrandir).

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/open-basket-stock.png" height="50" class="mb-3"/>

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/open-basket-stock-qr-code.png" height="50" class="mb-3"/>

### Vue du panier

La vue du panier dans l'application mobile est allégée et adaptée à la préparation du panier. Pour chaque ligne de produit, un compteur indique la quantité déjà préparée et la quantité à préparer.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/basket-detail.png" width="200" class="mb-4"/>

### Préparation du panier

Pour ajouter un produit au panier, quatre informations sont nécessaires :

- le produit,
- l'emplacement du stock depuis lequel il est prélevé,
- la quantité prélevée,
- quelle ligne de panier est ainsi prélevée.

#### Prélever un produit quelconque

Vous pouvez cliquer sur le bouton <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-button.png" height="20"/> pour prélever un produit quelconque, en utilisant _le scanner_ ou _la saisie manuelle_.

- Lorsque **le produit** est renseigné, seules les lignes de panier correspondantes à ce produit restent visibles.
- Lorsque **le produit _et_ l'emplacement** sont renseignés, la quantité _totale_ du produit à préparer pour ce panier est calculée.

<table class="mb-4">
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/basket-detail.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/scan-item.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/scan-location.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/filtered-basket.png" width="200" class="mx-2"/>
    </td>
  </tr>
  <tr class="text-center">
    <td>
      Avant la sélection →
    </td>
    <td>
      → Scan du produit →
    </td>
    <td>
      → Scan de l'emplacement →
    </td>
    <td>
      → Les lignes sont filtrées
    </td>
  </tr>
</table>

Plusieurs actions sont alors possibles :

- cliquer sur le bouton <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-line-item.png" height="20"/> d'une _ligne_ de panier prépare _cette ligne_ (et uniquement cette ligne) avec la quantité de produit indiquée sur le bouton (ici : 20). La quantité restante est mise à jour.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-line-item-lg.png" width="200" class="mb-3"/>

- cliquer sur le bouton <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-group.png" height="20"/> d'un _groupe de tâche_ ou d'un _groupe de facturation_ crée une nouvelle ligne dans le groupe correspondant avec la quantité indiquée (ici : 22) et prépare immédiatement cette ligne.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-group-lg.png" width="200" class="mb-3"/>

- cliquer sur le bouton "Répartir automatiquement" (juste en dessous de la quantité) répartit la quantité sur toutes les lignes existantes du panier. Si la quantité à préparer excède la quantité totale à préparer, vous devrez vous-même créer une ligne de panier comme indiqué ci-dessus.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/auto-pick.png" width="200" class="mb-3"/>

Tant que la quantité n'est pas nulle, ces actions sont toujours disponibles.

#### Prélever un produit pour une ligne de panier particulière

Lorsqu'aucun produit n'est sélectionné, vous pouvez cliquer sur le bouton <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-line-no-item.png" height="20"/> d'une ligne du panier : le produit et la quantité sont alors sélectionnés pour la préparation de cette ligne. Vous n'avez plus qu'à choisir l'emplacement de prélèvement. La saisie manuelle vous est proposée par défaut car les emplacements de votre entrepôt contenant le produit sont affichés.

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.2.0/pick-line-no-item-lg.png" width="200" class="mb-3"/>

Note : si vous avez besoin de prélever le produit depuis plusieurs emplacements différents, vous devez ajuster manuellement la quantité réellement prélevée depuis l'emplacement indiqué, _préparer_ la ligne, puis recommencer l'opération avec un autre emplacement de stockage. (Au final, vous devriez avoir fait un prélèvement pour chaque emplacement de stockage.)

Toute autre action reste possible.

---

# Mai 2021 - Version 1.2.0

- L'écran de détail d'un produit a été revu pour apporter permettre de visualiser l'ensemble des réservations clients et commandes fournisseurs.
- Amélioration du chargement de l'ensemble des lignes à commander.
- Et de leur tri par date de création qui n'était plus appliqué lorsque le filtre par fournisseur était activé.
- Correction de la déselection totale des produits en attente de commande.
- Il est désormais possible de configurer des règles de réassort.
- Correction de l'écran de configuration de la société.
- Améliorations de la gestion du double ajout d'une même réservation lors de la réception.
- Correction de l'export d'une commande lorsqu'aucune configuration n'est définie.
- Le bouton réservé n'est plus cliquable lorsque le stock d'un panier a été traité.

---

# April 2021 - Version 1.1.7

Nous avons corrigé la possibilité d'associer un dossier véhicule en commande ou en attente de commande à un VIN qui n'existe pas ni dans le registre national ni chez un constructeur connecté.

---

# Avril 2021 - 1 (Version 1.1.6)

Bienvenue à la première parution d'avril 2021 de Yuzer.

Cette version introduit une réécriture majeure de la gestion des réservations et commandes du panier à la réception de commandes fournisseurs. Elle a pour objectif de mieux refléter le statut des paniers, des réserations clients et commandes fournisseurs. Les modifications apportées ont également pour objectif de faciliter vos interractions et de rendre l'ensemble des opérations plus fluides et automatiques.

## Nouveau logo

Yuzer arbore désormais son logo définitif. Nous espérons que vous l'aimerez autant que nous!

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/icon.png" width="100"/>

# Nouveautés

Lorsqu'une nouvelle version de l'application démarre, la page nouveauté s'ouvre et vous permet de visualiser immédiatement les nouvelles fonctionalités et améliorations de la version.

Vous pouvez également ré-ouvrir cette page à tout moment en cliquant sur le numéro de version de Yuzer dans le coin en bas à gauche de l'application.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/version-click.png" width="100%"/>

## Nouveau flux de gestion du stock du panier à la réception

Le nouveau flux de gestion des réservation, du stock et des commandes introduit des changements sur de nombreux aspects de l'application et qui sont détaillés ci-dessous.

Les réservations client et commandes fournisseurs sont maintenant totalement disjointes et ne sont reliées qu'à la phase de réception.

Ceci permet plus de flexibilité dans leur gestion et dans la procédure de réception. Il est en effet désormais possible d'annuler l'une des réservations ou commande sans impacter l'autre qui possède son propre flux. Cela rends également possible de parcourir les réservation clients et l'ensemble des commandes produit et leur état.

### Gestion du stock du panier

Nous avons essayé de simplifier la gestion du flux du panier en automatisant pour vous la manière dont les réservations sont faites à la commande mais également d'automatiser ce qui pouvait l'être dans la finalisation du stock de panier.

#### Réservation automatique

Juste avant de créer un bon de commande ou un order de réparation nous effectuons désormais automatiquement la réservation ou commande des éléments du panier.

- Chaque élément en stock devient _Réservé_ dans le stock
- Chaque élément qui n'est pas en stock est automatiquement _Réservé sur les commandes_ et nous créons une ligne _En attente de commande_ dans la gestion des commandes fournisseur.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/auto-reservation-fr.png" width="100%"/>

Vous pouvez bien entendu toujours déclencher la réservation depuis la boite de dialogue de gestion du stock du panier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/manual-reservation-fr.png" width="100%"/>

Comme vous pouvez le constater la gestion de la réservation a été simplifiée et vous pouvez désormais déclencher la réservation pour un groupe de facturation donné ou directement pour l'ensemble du panier.

#### Préparation du stock du panier

La préparation du stock du panier est une nouvelle fonctionalité qui permet de placer certains éléments du stock dans un emplacement spécifique dédié au panier. Ceci permet de s'assurer que, en sus d'avoir _réservé_ le produit "théoriquement" pour un client, celui-ci a bien été _préparé_ et mis de côté dans un emplacement spécifique.

Notre recommandation est que vous gardiez un emplacement spécifique dans votre entrepôt pour les paniers _préparés_ et que vous y gardiez les cartons sur lesquels vous pourrez imprimer les étiquettes correspondant au panier.

Afin de préparer le stock d'un panier, vous devez accéder à la boite de dialogue d'un panier, soit via le bouton _stock/cmd_ du panier, soit depuis une tâche atelier/réception-livraison directement.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/basket-stock-btn.png" width="160"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/task-pick-btn.png" width="160"/>

Depuis cette boite de dialogue vous pouvez cliquer sur les boutons de picking (en vert) de chaque ligne que vous souhaitez préparer. Yuzer va alors essayer de trouver automatiquement le meilleure emplacement depuis lequel prendre le produit. Si cet emplacement n'est pas celui d'ou vous souhaitez prendre le produit vous pouvez alors l'éditer ou ajouter d'autres emplacements si vous prenez les produits depuis plusieurs endroits.

Une fois les informations correctement rentrées vous pouvez cliquer sur bouton _Préparer le stock_. Ceci aura pour effet de déplacer le stock depuis la l'emplacement spécifié vers l'emplacement de préparation dédié au panier.

Note: La préparation est une étape optionnelle mais peut vous simplifier la gestion de votre stock, permettant de garantir une gestion efficace de l'atelier.
Note 2: Le stock préparé est toujours considéré comme _En stock_ il sera effectivement supprimé du stock lors du traitement du stock du panier (à la facturation).

#### Traitement du stock du panier

Le traitement du stock du panier est la dernière étape du processus et va effectivement retirer du stock les pièces et marquer la réservation client comme traitée. Cette étape est automatiquement proposée avant la facturation.

#### Visualiser l'état de réservation d'une ligne dans le panier

Nous avons mis à jour les icônes de visualisation du stock et réservation sur le panier afin que ceux-ci reflettent les nouveaux états de _réservation_ _réservation sur commande_, _préparation_, _traitement_ et _annulation_ des commandes sur le panier.

### Réservation clients

En plus de la gestion du stock sur le panier, nous avons ajouté un meilleur support de la gestion des réservation client ainsi que des écrans qui vous permettent de mieux les consulter. Dans la gestion du stock un nouvel onglet _Réservations client_ fait son apparition et propose deux sous-vues:

- En cours: Où vous permet de consulter les réservations en cours.
- Historique: Où vous pouvez consulter l'ensemble de l'historique des réservation (par date de création de celles-ci).

### Commandes fournisseurs

Alors que l'onglet _Réservations client_ vous permet de consulter les réservation et commandes que des clients vous ont passées, l'onglet _Commandes_ vous permet de gérer et suivre les commandes que vous avez passées à vos fournisseurs. Trois sous-vues sont disponibles à cet effet:

- En attente de commande: Où vous trouverez tous les produits qui n'ont pas encore été commandés mais qui proviennent des réservations des clients ou de placements directs effectués depuis le catalogue. Ceci remplace les _panier fournisseurs_.
- Produits en commande: Où vous pouvez visualiser tous les produits qui sont actuellement en cours de commande et en attente de réception.
- Commandes: Où vous pouvez consulter les commandes passées à vos fournisseurs. Une commande fournisseur regroupe un ensemble de lignes lorsque vous déclanchées celles-ci sur l'écran En attente de commande.

### Réceptions

La gestion des réceptions a été simplifiée et permet désormais d'ajouter les lignes plus rapidement. Cet ajout rapide va automatiquement trouver la meilleure commande ainsi que la meilleure réservation client à associer.

L'affichage des commandes est désormais automatiquement filtré sur le fournisseurs de la commande.

## Amélioration de la sélection du fournisseur

Nous avons simplifié le composant de sélection d'un fournisseur dans certain écrans de l'application, vous permettant de chercher plus efficacement le fournisseur que vous recherchez.

<div class="d-flex justify-content-center">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/new-supplier-select-fr.png" height="150"/>
</div>

Nous allons déployer ce sélecteur sur l'ensemble des écrans permettant la sélection de fournisseurs dans les versions à venir.
