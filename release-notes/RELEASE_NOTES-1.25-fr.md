# Mai 2022 - Version 1.25.0

## Affichage de la TVA sur marge

La TVA sur marge qui était déjà bien prise en compte en comptabilité est désormais prise en compte dans les écrans:

- de liste de dossiers
- de détails d'un dossier
- dans les paniers
- dans les chiffres du widget de C.A.
- dans l'analytique

La marge affichée prend donc désormais bien en compte l'impact de la TVA sur marge.

## Stocks

<div class="d-none">
- Vue stock

La vue stock vous permet désormais de visualiser des extractions de stock directement dans Yuzer. Ces extractions peuvent ensuite être sauvegardées en CSV ou XLSX. Ceci remplace les fonctions d'export existant précédamment.

- Paramétrage de l'extraction

Dates

Autre filtres

</div>

### Vue détails de produit

La vue de détails d'un produit a été revue pour apporter plus de lisibilité sur les informations les plus importantes.

L'affichage de l'application en mode _client_ cache les détails du stock, des réservations d'autres clients et des commandes.

<div class="alert alert-warning">
Attention si vous ne voyez plus les informations détaillées du stock c'est que vous êtes en vue client. Pensez à passer en vue concessionaire pour visualiser ceux-ci.
</div>

#### Information rapides sur le stock

Le niveau de stock, la consommation sur le produit et un prévisionnel s'affichent désormais sur la vue produit.

<div class="alert alert-info">
Le prévisionnel est actuellement en bêta et nécessite que le produit ait une antériorité sur l'année précédente.

En effet la consomation étant fortement fluctuante en fonction de la période de l'année nous ne souhaitions pas imposer de vision érronée en fin d'année lorsque l'activité décroit.
Nous allons améliorer cette fonction dans le futur afin de vous permettre de bénéficier de celle-ci sans antériorité.

</div>

_Note: Le graphique de prix d'achat du stock du produit, qui n'était pas le plus utilisé, disparait temporairement et reviendra dans une version ultérieure._

#### Correction de la valeur d'achat d'un évènement

Vous pouvez désormais corriger la valeur d'achat d'un évènement depuis l'interface.

Dans le cas d'une réception le prix de la ligne de réception associée est également mis à jour.

<div class="alert alert-warning">
A noter que la mise à jour dans la réception ne sera pas effectuée:
 - Si le stock a été fusionné d'une reférence produit vers une autre (ou d'un fournisseur à un autre)
 - Sur certains évènements de réception anciens

Ces désagréments ne sont valable que sur les évènements antérieurs à cette version. Il sera possible dans le futur de bien mettre à jour les évènements de réception avec le prix de leur ligne y compris sur des stock fusionnés.

</div>

<div class="d-none">
- Changement du prix d'achat moyen pondéré.

Le changement du prix d'achat moyen

</div>

### Inventaires

Il est désormais possible de faire des inventaires sur un sous-ensemble de produits et non plus uniquement d'emplacements.

A noter que cette option n'est disponible que si tout le stock ou un ensemble d'emplacements sont inventoriés. Elle n'a en effet pas de sens dans le cadre d'un inventaire vide.

## Paravol

Il est désormais possible d'effectuer l'enregistrement de gravage d'un vélo paravol automatiquement à la vente.

## C'est corrigé

- Certaines colonnes dans l'analytique n'étaient pas exportées avec le bon format dans excel.
- Le regroupement par dates dans l'analytique n'affichait pas celles-ci correctement.
- Les catégories filtrées dans le widget de C.A. sont bien pré-cochées lors la modification de celles-ci.
- Sur la vue des dossiers véhicules le filtre ouverts/clôturés lors d'un changement d'entité ne peut plus être dans un état inconsistent avec la liste affichée.
