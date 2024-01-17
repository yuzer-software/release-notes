Bonne année 2024 à tous de la part de l'équipe Yuzer !

# Janvier 2024 - Version 3.0.0

## Comptabilité

Les numéros de factures ne sont plus remis à zéro chaque mois. Ils sont désormais remis à zéro au premier janvier uniquement.
Si les deux fonctionnement sont légaux, l'administration fiscale a une préférence pour une numéro annuelle et nous avons décidé de lui faire plaisir.

## Filtrer les réservations client sur la date de livraison souhaitée

Sur l'écran des réservations client il est désormais possible de filtrer sur la date de livraison souhaitée.

## Dossiers produits

### Import de dossier à l'aide de la référence de dossier

Il est maintenant possible lors de l'import de dossier, d'utiliser la "Référence de dossier"
pour retrouver et mettre à jour vos dossiers qui par exemple n'auraient pas encore de VIN ou d'immatriculation.

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/import.webp"/>

Pour retrouver cette référence, vous pouvez l'afficher dans le listing de vos dossiers.

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/listing.webp"/>

Ou encore l'exporter en cochant le champs "Référence de dossier".

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/export.webp"/>

### Synchronisation d'un dossier

La synchronisation d'un dossier vous permet désormais de choisir quelles valeurs conserver suite à la synchronisation.
Attention : les données sont bien synchronisées par défaut et il vous faudra bien spécifier celles que vous souhaiteriez conserver.

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

### Visibilité des documents

## Support des paniers permettant la vente de plusieurs dossiers

Changement majeur de Yuzer 3 : il est désormais possible de vendre plusieurs dossiers véhicule dans un panier unique.

Dans cette première itération de Yuzer 3 il est pour l'instant nécessaire d'effectuer des factures (donc des groupes de facturation) différents pour chaque produit. Cette limitation est une contrainte légale pour certains types de produits (les véhicules immatriculables).

Notre design interne et les évolutions à venir permettront de définir les catégories pour lesquelles il est possible de facturer plusieurs produits sur une même facture (les vélos par exemple).

### Paniers de plus de 5 groupes de facturation

La vente multi-produits peut entraîner la création de paniers comportant plus de 5 groupes de facturation. Ces paniers disposent d'une vue révisée et de quelques fonctionnement spécifiques qui sont détaillés ci-dessous.

#### Déplacer une ligne entre deux groupes de facturation

## Nouveaux catalogues produits

## Corrections

- Le filtre de contacts sur la dernière vente ne se comportait plus correctement.
- Les numéros de comptes alphanumériques sont désormais correctement affichés dans l'écran de ventilation comptable.

## Sécurité

Nous avons amélioré la sécurisation du stockage local, notamment du token de connexion afin d'éviter qu'un appareil volé et corrompu puisse être utilisé par un attaquant pour se connecter à votre compte.

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

## Assistant de picking

<div class="d-flex">
  <div>

Avec l'assistant de picking, ce n'est plus vous mais l'assistant qui vous dit où prendre le stock pour chaque produit. Il est bien sûr nécessaire d'avoir un stock bien à jour pour avoir de bons résultats.

L'assistant considère toutes les lignes du panier et tous les emplacements de stock de votre entrepôt, puis vous proposera un chemin qui vous fera faire le moins de déplacement possible.

### Plan de l'entrepôt

Comme nous n'avons pas le plan des entrepôts, nous trions les emplacements par ordre alphabétique et considérons qu'ils sont tous comme alignés dans un grand couloir.

### Prélèvement et comptage

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
