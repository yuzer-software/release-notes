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
