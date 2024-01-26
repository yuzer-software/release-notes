# Janvier 2024 - Version 3.0.x

yuzSection Comptabilité

## Comptabilité

Les numéros de factures ne sont plus remis à zéro chaque mois. Ils sont désormais remis à zéro au premier janvier uniquement.
Si les deux fonctionnement sont légaux, l'administration fiscale a une préférence pour une numérotation annuelle et nous avons décidé de lui faire plaisir.

Note: le numéro sera toujours préfixé par le numéro du mois. Par exemple, si la dernière facture de janvier a pour numéro "Yuz-202401000234", alors la première facture de février aura pour numéro "Yuz-202402000235".

yuzSection Nettoyage paniers et réservations

## Fonctions de nettoyage pour repartir sur de bonnes bases

Nous avons ajouté des fonctionalités d'annulation des anciens paniers et réservations clients. Les prochaines versions de Yuzer ajouteront la possibilité d'annuler les commandes fournisseurs de manière similaire.

Cela vous permettra de repartir sur de bonnes bases pour un meilleur suivi de vos réservations, commandes et stocks.

### Annulation automatisée des anciens paniers

Pour lancer un traidement d'annulation des anciens paniers, rendez vous sur l'écran Client / Paniers; Cliquez sur le bouton _3 petits points_ et choisissez _Annuler les anciens paniers_.

![Annuler les anciens paniers](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/cancel-old-baskets/cancel-baskets_button.webp=400)

Sélectionnez une date et lancez le processus: Tous les panier créés avant la date sélectionnée seront alors annulés.

![Annuler paniers modale](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/cancel-old-baskets/cancel-baskets_modal.webp=400)

Vous pouvez suivre le déroulement du traitement dans un écran accessible via les 3 points vu plus haut en sélectionnant _Résultat des annulations d'anciens paniers_.

### Annulation automatisée des anciennes réservations client

Pour lancer un traitement d'annulation des anciennes réservations client, vous pouvez aller sur les 3 points à droite de l'écran des réservations et cliquer sur "Annuler les anciennes réservations".

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/cancel-old-reservations/cancel-reservations_button.webp"/>

Puis sélectionnez une date et lancez le processus. Toutes les réservations liées à des paniers plus anciens que la date sélectionnée seront alors annulées.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/cancel-old-reservations/cancel-reservations_modal.webp"/>

Vous pouvez alors suivre le déroulement du traitement dans un écran accessible via les 3 points vu plus haut en sélectionnant "Résultat des annulations d'anciennes réservations".

yuzSection Dossiers produits

## Dossiers produits

### Import de dossier à l'aide de la référence de dossier

Il est maintenant possible lors de l'import de dossier, d'utiliser la "Référence de dossier"
pour retrouver et mettre à jour vos dossiers qui par exemple n'auraient pas encore de VIN ou d'immatriculation.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/import.webp"/>

Pour retrouver cette référence, vous pouvez l'afficher dans le listing de vos dossiers.

<img width="600" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/listing.webp"/>

Ou encore l'exporter en cochant le champs "Référence de dossier".

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/export.webp"/>

### Synchronisation d'un dossier

La synchronisation d'un dossier vous permet désormais de choisir quelles valeurs conserver suite à la synchronisation.
Attention : les données importées des fournisseurs sont immédiatement sauvegardées, il vous faudra donc bien spécifier quelles valeurs vous voulez conserver pour les réécrire.

yuzSection Paniers

## Paniers

### Evolutions ergonomiques

- Sous-totaux :
  Les sous-totaux main d'œuvre et produits dans le cadre d'un ordre de réparation sont désormais cachés par défaut.

- Paiements rapides :
  Des boutons de paiement rapide ont été ajoutés au panier. Ceux-ci permettent de payer intégralement, avec un moyen de paiement unique, et facturer rapidement un panier.

- Ajout de produits à tarif *dynamiques* :
  Il est désormais possible d'éditer le prix d'achat d'un produit dans le panier si celui-ci a un prix d'achat à zéro dans le catalogue.
  De plus, si le prix de vente du produit dans le catalogue est à zéro, celui-ci sera demandé à l'utilisateur au moment de l'ajout dans le panier.

- Lors de l'application d'une TVA globale sur un panier il n'est désormais possible que de choisir les taux de TVA spécifiés dans les paramètres d'administration comptable.

### Remboursements simplifiés dans le cadre d'un achat de véhicule

TODO

### Visibilité des documents

// XXX: impactant au support

- Les "Documents édités" sont ceux du groupe de facturation en cours, et non ceux de tous les groupes comme c'était le cas avant.

## Support des paniers permettant la vente de plusieurs dossiers

Changement majeur de Yuzer 3 : il est désormais possible de vendre plusieurs dossiers véhicule dans un panier unique.

Dans cette première itération de Yuzer 3 il est pour l'instant nécessaire d'effectuer des factures (donc des groupes de facturation) différents pour chaque produit. Cette limitation est une contrainte légale pour certains types de produits (les véhicules immatriculables).

Notre design interne et les évolutions à venir permettront de définir les catégories pour lesquelles il est possible de facturer plusieurs produits sur une même facture (les vélos par exemple).

### Paniers de plus de 5 groupes de facturation

La vente multi-produits peut entraîner la création de paniers comportant plus de 5 groupes de facturation. Ces paniers disposent d'une vue révisée et de quelques fonctionnement spécifiques qui sont détaillés ci-dessous.

Cette vue liste des groupes: cliquer sur une ligne fera apparaître seulement ce groupe, et un bouton "retour" permet de revenir sur la liste des groupes.

#### Déplacer une ligne entre deux groupes de facturation

À moins de 5 groupes, il est toujours possible de glisser/déposer une ligne d'un groupe vers l'autre.

À plus de 5 groupes, il vous faut cliquer sur le bouton d'action de la ligne ([⋮]) et sélectionner "Déplacer vers un autre groupe". (Cette option est disponible aussi pour les paniers de moins de 5 groupes.)

### Reprises

Chaque groupe de facturation a maintenant sa liste de reprises. En effet, les reprises sont considérés comme des moyens de paiement. Pour utiliser l'argent d'une reprise sur plusieurs groupes de facturation, il sera nécessaire de passer par la balance client: soit faire une reprise sèche puis utiliser la balance, soit utiliser le crédit du client disponible du fait de la reprise.

### Auto-synchronisations des produits montés sur le dossier

Cette fonctionnalité est en cours de finalisation et sera prochainement disponible. Il n'y aura qu'un seul groupe de session de démontage pour tous les autres groupes et tous les autres produits.

### Envoi à l'atelier

La manière dont les lignes de panier sont liées aux différentes tâches a légèrement changé pour s'adapter à la présence de plusieurs IDPs.

#### Avant.

| n°  | groupe   | ligne        | Tâche associée | Lignes associées à la tâche |
| --- | -------- | ------------ | -------------- | --------------------------- |
|     | Client 1 |              |
| 1   |          | main d'œuvre | Tâche 1        | Ligne 2                     |
| 2   |          | produit      |

#### Aujourd'hui.

Attention: un produit au dessus du produit identifié ne sera donc pas dans la tâche liée à l'IDP.

yuzSection Nouveaux catalogues

## Nouveaux catalogues produits

yuzSection Améliortions et corrections

## Améliortions diverses

## Filtrer les réservations client sur la date de livraison souhaitée

Sur l'écran des réservations client il est désormais possible de filtrer sur la date de livraison souhaitée.

## Corrections

- Le filtre de contacts sur la dernière vente ne se comportait plus correctement.
- Les numéros de comptes alphanumériques sont désormais correctement affichés dans l'écran de ventilation comptable.

## Sécurité

Nous avons amélioré la sécurisation du stockage local, notamment du token de connexion afin d'éviter qu'un appareil volé et corrompu puisse être utilisé par un attaquant pour se connecter à votre compte.

# Notes de la démo — Desktop

## Ergonomie

- Simplification du menu de navigation gauche (le menu à gauche)
  - Le bouton pour choisir le type d'affichage est déplacé le bouton "utilisateur"
  - la configration POS a été déplacée dans Administration

yuzSection Application Mobile

# Application Mobile 3.0.0

Nous avons apporté de nombreuses améliorations à l'application mobile, notamment:

- une notion d'entrepôt courant
- une meilleure accessibilité à vos derniers travaux et tâches
- un assistant pour le picking de vos paniers

<div class="d-flex">
  <div>

## Entrepôt courant

L'emplacement de votre entrepôt est maintenant défini globalement pour toute l'application. Il peut être changé depuis le panneau latéral.

## Panneau latéral

Le panneau latéral a été enrichi:

- Vous pouvez changer d'entité en cliquant sur le nom de l'entité
- Vous voyez votre entrepôt courant. Vous pouvez changer d'entrepôt en cliquant dessus.
- Les derniers travaux faits sur l'application mobile ont été ajoutés
- Les boutons de navigation ont été réorganisés pour être plus accessibles

  </div>
  <div><img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/side-menu.webp"/></div>
</div>

## Écran d'accueil

<div class="d-flex">
  <div>
La page d'accueil a été enrichie pour une navigation plus fluide:

- Le nom de l'entrepôt courant est clairement affiché tout en haut
- Le lien vers le dernier travail est affiché :
  - Par défaut, le dernier travail de l'application de bureau
  - Vous pouvez changer pour le dernier travail de l'application mobile avec le bouton du haut
  - Vous pouvez rafraichir ce travail avec le bouton du bas
  - Pour plus de derniers travaux, ouvrez le menu latéral
- Votre tâche actuelle est affichée. Nous allons de préférence choisir :
  - une tâche "en cours" qui vous est assigné
  - la prochaine tâche "à faire" qui vous est assigné
- Les boutons de navigation ont été réorganisés pour être plus accessibles

  </div>
  <div><img width="610" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/home.webp"/></div>
</div>

## Panier

<div class="d-flex">
  <div>
La vue du panier a été améliorée.

- Nous avons changé les icônes pour qu'ils soient plus compréhensibles:

  - <img width="20" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/person-carry.webp"/> : initialiser le picking manuel (du panier ou de la ligne choisie)
  - <img width="20" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/hand-holding-box.webp"/> : prélever
  - <img width="20" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/people-carry.webp"/> : utiliser l'assistant de picking (_nouveau_, voir ci-dessous)

- Une barre de navigation rapide a été ajoutée en bas:

  1. Retour à la vue de base du panier
  1. Afficher les tâches du panier (avec possibilité d'y aller)
  1. Initialiser le picking manuel (même action que le bouton "manuel" en haut)
  1. Faire le picking assisté (même action que le bouton "assisté" en haut)

    </div>
    <div><img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/basket.webp"/></div>
    <div><img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/basket-tasks.webp"/></div>
  </div>

### Assistant de picking

<div class="d-flex">
  <div>

Avec l'assistant de picking, ce n'est plus vous mais l'assistant qui vous dit où prendre le stock pour chaque produit. Il est bien sûr nécessaire d'avoir un stock bien à jour pour avoir de bons résultats.

L'assistant considère toutes les lignes du panier et tous les emplacements de stock de votre entrepôt, puis vous proposera un chemin qui vous fera faire le moins de déplacement possible.

#### Plan de l'entrepôt

Comme nous n'avons pas le plan des entrepôts, nous trions les emplacements par ordre alphabétique et considérons qu'ils sont tous comme alignés dans un grand couloir.

#### Prélèvement et comptage

Si vous voulez ignorer une instruction de l'algorithme, vous pouvez cliquer sur le bouton "passer" [1]. Vous devrez alors faire le picking manuel à la fin de l'algorithme.

Autrement, allez à l'emplacement proposé, vous avez 2 options de comptage : compter vous-même la quantité ou utiliser le scanner [2]. Utiliser le scanner a l'avantage qu'il vérifiera si le produit a bien la bonne référence.

Notez que vous avez 3 valeurs indiquées:

- [3] la quantité que vous allez effectivement prélever en cliquant sur "Prélever"
- [4] le nombre de produits que vous devez prendre à l'emplacement proposé
- [5] le nombre de produits total à prélever pour le panier

Une fois la quantité ajustée, cliquez sur "Prélever" [6].

  </div>
  <div><img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/basket-picking-assistant.webp"/></div>
  <div><img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/mobile-app/basket-picking-assistant-scanner.webp"/></div>
</div>

## Améliorations diverses

- Sur le détail d'une tâche que vous pouvez passer à "en cours", vous pouvez désormais cliquer sur le bouton "lecture" pour passer la tâche à "en cours".

## Sécurité

Nous avons amélioré la sécurisation du stockage local, notamment du token de connexion afin d'éviter qu'un appareil volé et corrompu puisse être utilisé par un attaquant pour se connecter à votre compte.
