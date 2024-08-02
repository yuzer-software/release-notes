# April 2021 - Version 1.1.7

Nous avons corrigé la possibilité d'associer un dossier véhicule en commande ou en attente de commande à un VIN qui n'existe pas ni dans le registre national ni chez un constructeur connecté.

---

# Avril 2021 - 1 (Version 1.1.6)

Bienvenue à la première parution d'avril 2021 de Yuzer.

Cette version introduit une réécriture majeure de la gestion des réservations et commandes du panier à la réception de commandes fournisseurs. Elle a pour objectif de mieux refléter le statut des paniers, des réserations clients et commandes fournisseurs. Les modifications apportées ont également pour objectif de faciliter vos interractions et de rendre l'ensemble des opérations plus fluides et automatiques.

## Nouveau logo

Yuzer arbore désormais son logo définitif. Nous espérons que vous l'aimerez autant que nous!

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/icon.png" width="100"/>

# Nouveautés

Lorsqu'une nouvelle version de l'application démarre, la page nouveauté s'ouvre et vous permet de visualiser immédiatement les nouvelles fonctionnalités et améliorations de la version.

Vous pouvez également ré-ouvrir cette page à tout moment en cliquant sur le numéro de version de Yuzer dans le coin en bas à gauche de l'application.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/version-click.png" width="100%"/>

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

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/auto-reservation-fr.png" width="100%"/>

Vous pouvez bien entendu toujours déclencher la réservation depuis la boite de dialogue de gestion du stock du panier.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/manual-reservation-fr.png" width="100%"/>

Comme vous pouvez le constater la gestion de la réservation a été simplifiée et vous pouvez désormais déclencher la réservation pour un groupe de facturation donné ou directement pour l'ensemble du panier.

#### Préparation du stock du panier

La préparation du stock du panier est une nouvelle fonctionnalité qui permet de placer certains éléments du stock dans un emplacement spécifique dédié au panier. Ceci permet de s'assurer que, en sus d'avoir _réservé_ le produit "théoriquement" pour un client, celui-ci a bien été _préparé_ et mis de côté dans un emplacement spécifique.

Notre recommandation est que vous gardiez un emplacement spécifique dans votre entrepôt pour les paniers _préparés_ et que vous y gardiez les cartons sur lesquels vous pourrez imprimer les étiquettes correspondant au panier.

Afin de préparer le stock d'un panier, vous devez accéder à la boite de dialogue d'un panier, soit via le bouton _stock/cmd_ du panier, soit depuis une tâche atelier/réception-livraison directement.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/basket-stock-btn.png" width="160"/>
<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/task-pick-btn.png" width="160"/>

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
  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.1.0/new-supplier-select-fr.png" height="150"/>
</div>

Nous allons déployer ce sélecteur sur l'ensemble des écrans permettant la sélection de fournisseurs dans les versions à venir.
