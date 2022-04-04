# Avril 2022 - Version 1.21.0

## Catalogues

### Partage de catalogues entre entités

Vous pouvez désormais partager un de vos catalogues fournisseur avec d'autres entités du groupe. Depuis votre liste de fournisseurs (_Administration_ / _Fournisseurs_) un bouton _Partager_ fait son apparition en face de vos catalogues locaux.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/supplier-list-share.png" width="500"/>

Une fois actionné une modal s'ouvre alors vous permettant de visualiser:

- Avec qui le catalogue est déjà partagé
- Avec qui le catalogue peut-être partagé

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/supplier-list-share.png" width="500"/>

Le partage doit se faire aujourd'hui cible par cible et il n'est pas possible de sélectionner plusieurs cibles d'un coup; ce point sera amélioré dans le futur.

Une fois une cible sélectionnée vous pouvez partager le catalogue. qui devient alors visible dans la liste des fournisseurs en tant que catalogue communautaire.

Pour rappel il existe trois icônes qui vous permettent de visualiser les types de syncronisation et mise à jour sur les catalogues:

<div>
<img class="ml-5 d-inline-block" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/catalog-local.png" width="46"/>
<span>Calogue local que vous avez créé. Vous pouvez éditer les produits à votre convenance.</span>
</div>
<div>
<img class="ml-5 d-inline-block" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/catalog-community.png" width="46"/>
<span>Calogue communautaire qui a été partagé avec vous. Vous pouvez éditer les produits et toute modification sera répercutée sur l'ensemble des autres utilisateurs du catalogue.</span>
<div>
<div>
<img class="ml-5 d-inline-block" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/catalog-automatic.png" width="46"/><span>Catalogue managé dans lequel vous ne pouvez effectuer de modifications.</span>
<div>

### Fusion de fournisseurs/catalogues

Une fois les catalogues partagé il est probable que vous souhaitiez vous débarasser de catalogues existant en doublons.
Il est possible pour cela d'utiliser la fonction de fusion de fournisseurs. Cette fonction vous permet de controler la consistence du catalogue cible mais également migrer

- votre stock vers les nouvelles références catalogue
- vos réservations en cours
- vos commandes en cours

<div class="m-2 alert alert-warning">Attention, les références des éventuels transferts ne seront pas migrées. Nous vous recommandons donc de les résoudre avant d'effectuer la fusion.</div>

Afin d'effectuer une fusion selectionnez le fournisseur que vous souhaitez fusionner puis cliquez sur le bouton suivant:

## Tableau de bord

### Widget de M.O.

### Utilisations de filtres personnalisés

Les filtres personnalisés qui seraient incompatibles avec le widget de chiffre d'affaires sont clairement exhibés.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/custom-filter-in-turnover-widget.png" width="500"/>

## Panier

Nous indiquons désormais clairement pourquoi une ligne avec préparations ne peut pas être supprimée.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/delete-line-with-preparations.png" width="500"/>

## Modèle de panier: import Honda

Honda fournit des modèles de panier au format CSV qu'il est désormais possible d'importer dans Yuzer.

- Vous devez au préalable avoir Honda comme fournisseur.
- Depuis la page des modèles, cliquez sur "Importer Honda".

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/new-honda-import.png" width="300"/>

- Suivez les instructions: téléchargez les fichiers fournis par Honda, puis remplissez les champs comme indiqué.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/honda-import.png" width="800"/>

- Cliquez sur "Charger": tous les modèles importés seront créés.

<div *dmsHasAnyAuth="['ROLE_ACCOUNTANT']">

## Réceptions

Les lignes des réceptions sont réceptions sont triées par date d'ajout mais toutefois groupées par identifiant de produit, ce qui est généralement désirable. En conséquence, il est possible que des lignes soient réordonnées sur des opérations d'ajout ou de suppression de lignes, ce qui était parfois déconcertant pour l'utilisateur qui pouvait croire que davantage de produit avait été ajouté que ce qu'il n'avait demandé ou, lors d'une suppression, que plusieurs lignes avaient été supprimées. Par exemple, si un produit 890479 a été ajouté à la réception, puis une dizaine d'autres lignes, puis à nouveau du 890479 et que cela crée une nouvelle ligne, alors toutes les lignes de 890479 seront groupées ensemble en tête de liste. Si cette dernière ligne venait à être supprimée, les autres lignes retrouveraient leurs place en fin de liste, donnant l'impression qu'elles ont été supprimées.

Nous avons donc ajouté un message indiquant lorsque des lignes sont réordonnées avec la possibilité de filtrer les lignes impactées (comme illustré ci-dessous).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/warn-reception.png" width="900"/>

## Comptabilité

### TVA déductible à l'achat par taux de TVA

Il est maintenant possible de configurer les comptes de TVA déductible à l'achat par taux de TVA.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/vat-config.png" width="500"/>

</div>

## Améliorations diverses

- Lorsque vous créez un ordre de réparation à partir d'une tâche d'atelier, le panier est maintenant nommé à partir du libellé de la tâche.

## C'est corrigé

- Dans la boite de dialogue de sélection d'un contact, vous n'être maintenant plus redirigé vers la page de détails lors de la sélection d'un véhicule.
- La tâche de l'atelier n'était pas synchronisée lors de l'ajout d'un modèle de panier qui contient de la main d'oeuvre.
