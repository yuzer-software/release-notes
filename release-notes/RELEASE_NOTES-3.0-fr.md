Bonne année 2024 à tous de la part de l'équipe Yuzer!

# Janvier 2024 - Version 3.0.0

## Comptabilité

Les numéros de factures ne sont plus remis à zero chaque mois. Ils sont désormais remis à zero au premier janvier uniquement.
Si les deux fonctionnement son légaux l'administration fiscale ayant une préférence pour une numéro annuelle nous avons décidé de lui faire plaisir.

## Filtrer les réservations client sur la date de livraison souhaitée

Sur l'écran des réservations client il est désormais possible de filtrer sur la date de livraison souhaitée.

## Dossiers produits

### Import de dossier à l'aide de la référence de dossier

Il est maintenant possible lors de l'import de dossier, d'utiliser la "Reférence de dossier"
pour retrouver et mettre à jour vos dossiers qui par exemple n'aura pas encore de VIN ou d'immatriculation.

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/import.png"/>

Pour retrouver cette référence, vous pouvez l'afficher dans le listing de vos dossiers.

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/listing.png"/>

Ou encore l'exporter en cochant le champs "Référence de dossier".

<img width="384" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.0.0/dealer-file-ref/export.png"/>

### Synchronisation d'un dossier

La synchronisation d'un dossier vous permet désormais de choisir quelles valeurs conserver suite à la synchronisation.
Attention les données sont bien synchronisées par défaut et il vous faudra bien spécifier celles que vous souhaiteriez conserver.

## Paniers

### Evolutions ergonomiques

- Sous-totaux:
  Les sous-totaux main d'oeuvre et produits dans le cadre d'un ordre de réparation sont désormais cachés par défaut.

- Paiements rapides:
  Des boutons de paiement rapide ont été ajoutés au panier. Ceux-ci permettent de payer intégralement, avec un moyen de paiement unique, et facturer rapidement un panier.

- Ajout de produits à tarif _dynamiques_:
  Il est désormais possible d'éditer le prix d'achat d'un produit dans le panier si celui-ci a un prix d'achat à zero dans le catalogue.
  De plus, si le prix de vente du produit dans le catalogue est à zero, celui-ci sera demandé à l'utilisateur au moment de l'ajout dans le panier.

- Lors de l'application d'une TVA globale sur un panier il n'est désormais possible que de choisir les taux de TVA spécifiés dans les paramtères d'administration comptable.

### Remboursements simplifiés dans le cadre d'un achat de véhicule

### Visibilité des documents

## Support des paniers permettant la vente de plusieurs dossiers

Changement majeur de Yuzer 3 il est désormais possible de vendre plusieurs dossiers véhicule dans un panier unique.

Dans cette première itération de Yuzer 3 il est pour l'instant nécessaire d'effectuer des factures (donc des groupes de facturation) différents pour chaque produit. Cette limitation est une contrainte légale pour certains types de produits (les véhicules immatriculables).

Notre design interne et les évolutions à venir permettrons de définir les catégories pour lesquelles il est possible de facturer de multiples produits (les vélos par exemple).

### Paniers de plus de 5 groupes de facturation

La vente multi-produits peut entrainer la création de paniers comportant plus de 5 groupes de facturations. Ces paniers disposent d'une vue révisée et de quelques fonctionnement spécifiques qui sont détaillés ci-dessous.

#### Déplacer une ligne entre deux groupes de facturation

## Nouveaux catalogues produits

## Corrections

- le filtre de contacts sur la dernière vente ne se comportait plus correctement.
- Les numéros de comptes alphanumériques sont désormais correctement affichés dans l'écran de ventilation comptable.

## Sécurité

Nous avons amélioré la sécurisation du stockage local, nottament du token de connexion afin d'éviter qu'un appareil volé et corrompu puisse être utilisé par un attaquant pour se connecter à votre compte.

# Application Mobile 3.0.0

## Assistant de picking

## Améliortions diverses

- Les boutons permettant d'enregistrer la quantité dans le cadre d'un inventaire ont été améliorés.

## Sécurité

Nous avons amélioré la sécurisation du stockage local, nottament du token de connexion afin d'éviter qu'un appareil volé et corrompu puisse être utilisé par un attaquant pour se connecter à votre compte.
