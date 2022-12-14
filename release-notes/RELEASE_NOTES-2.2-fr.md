# 12 Décembre 2022 - Version 2.2.3

## Normalisation des marques

<div class="alert alert-warning">ATTENTION CHANGEMENT IMPORTANT</div>

La gestion des marques dans Yuzer se normalise. En effet, le champ libre existant dans les versions précédentes pouvait causer des différences dans les noms ou formattages qui limitait l'exploitation de l'information marque dans les différents écran de l'application ou dans les analytiques.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/brand_select.png" width="512px"/>

Le champ libre est donc remplacé par un sélecteur qui permet de choisir une marque dans un référentiel normalisé. Ce référentiel de marque peut-être accédé à travers l'onglet _Administration / Marques_:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/brand_list.png" width="512px"/>

Si une marque venait à manquer, vous pourez créer depuis cet écran une nouvelle marque qui ne sera visible, tant que celle-ci n'aura pas été validée par les équipes Yuzer, que par votre concession.

### Migration des données:

Les marques ont toutes été remplacées dans les données de produit existantes.

<div class="alert alert-info">Seuls les produits et produits identifiés ont été migrés. Les autres données (paniers, ventes etc.) seront nettoyées ultérieurement.
Nous attendons en effet vos retour sur les éventuelles complétions de marques avant d'effectuer ces opérations.
</div>

Les anciennes marques qui n'ont pas été migrées à l'identique sont toujours affichées sur les écrans de produit.

### Ajout d'une nouvelle marque

Vous pouvez ajouter une nouvelle marque depuis le menu _Administration / Marques_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/brand_new.png" width="512px"/>

## Séparation des catalogues et fournisseurs

Autre modification apportée par la version 2.2 de Yuzer, les fournisseurs sont désormais séparés de la notion de catalogue.
Ce point est plus proche de la réalité et permet de mieux exprimer la différence entre l'éditeur d'un catalogue et le fournisseur de celui-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/catalog_list.png" width="1024px"/>

L'écran de gestion des fournisseurs reste accessible comme avant. Cependant:
 - Le bouton permettant de "partager un fournisseur" qui partagait en réalité uniquement son catalogue disparait.
 - Le fournisseur ne porte plus de catalogue (ajouter un fournisseur n'ajoutera pas d'accès à ses produits).
 - La gestion des fournisseurs est désormais focalisée sur ce qu'est un fournisseur. Il permet de configurer le numéro du fournisseur et des informations relatives aux aspects comptables et commande.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/catalog_detail.png" width="1024px"/>

Note: Les fournisseurs ayant des services de passage commande automatisés tels que KTM par exemple doivent toujours être ajoutés depuis cet écran à travers les fournisseurs officiels. Le service de commande est en effet directement lié à la notion de fournisseur.

<div class="alert alert-info">La migration des données a ajouté automatiquement pour vous les catalogues nécessaires et les a associés au bon fournisseur, sauf dans le cas des catalogues SADEM.</div>

### Adhérents SADEM

Si vous êtes un adhérent SADEM et utilisez leur catalogues l'intégralité des catalogues a été ajoutée à votre compte, garantissant ainsi l'accès à l'ensemble des produits auquels vous aviez déjà accès au préalable.
SADEM édite de nombreux catalogues avec des tarifs correspondant à ceux que vous pouvez avoir chez un fournisseur spécifique. Les catalogues sont édités par couple marque/fournisseur.

Les fournisseurs n'ont pu être automatiquement associé lors de la migration. Vous devez donc effectuer vous même cette opération en allant dans le menu catalogue, en recherchant SADEM, en éditant celui-ci et en re-configurant le fournisseur. Ce point permettra une meilleure gestion de la commande des produits SADEM une fois bien configuré.

## Export automatique des stock dossiers

Vous pouvez désormais exporter vos stock dossier de la même manière que vos stock produits via un export automatique nocturne. Pour cela rendez vous dans l'onglet _Administration / Automates_ 

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/export_files.png" width="1024px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.2.0/export_files_2.png" width="1024px"/>


## Améliorations invenatires

La validation des inventaires ainsi que des écrans de résumé ont été ajoutés afin de vous aider à la validation de deux-ci et à une meilleure exploitation de leur résultats.
