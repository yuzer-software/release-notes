# Mai 2022 - Version 1.25.6

## Configuration des opérations commerciales

Nous avons ajouté la fonctionnalité d'opérations commerciales avec un système de règle, la possibilité d'imprimer des étiquettes qui reflètent les prix de l'opération commerciale.

### Menu et liste des opérations

La configuration des opérations commerciales est accessible depuis le menu `Administration > Gestion commerciale > Opérations commerciales`. Les opérations commerciales de l'année sont affichées. Il est possible d'en créer une.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/commercial-operation-list.png" width="800px"/>

### Création et configuration

Le même menu est utilisé pour la création et la configuration d'une opération commerciale. Quelques remarques :
  - sont nécessaires le libellé, les dates et **au moins une règle**.
  - vous ne pourrez **plus changer les dates** une fois l'opération commerciale sauvegardée, mais ce sera possible à la prochaine mise à jour.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/commercial-operation-creation.png" width="800px"/>

La configuration des règles est en partie similaire à celle des cartes de fidélité.
* Chaque règle a un type (pour l'instant, un seul type de règle est disponible : la remise en pourcentage du prix)
* Des paramètres (le pourcentage de remise à appliquer)
* Deux listes de conditions
  * Une liste de conditions de satisfaction
  * Une liste de conditions de non-satisfaction
  * La remise s'applique si au moins une condition de satisfaction est remplie (il en faut donc une) et si aucune condition de non-satisfaction est remplie (il peut n'en être aucune).

Vous pouvez aussi ajouter deux commentaires:
* Un commentaire qui sera ajouté à chaque groupe de facturation d'un panier bénéficiant de l'offre
* Un commentaire qui sera ajouté à chaque ligne de panier qui bénéficie de l'offre

Voici un exemple d'une règle "Remise en pourcentage du prix"

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/commercial-operation-config.png" width="600px"/>

N'oubliez pas de sauvegarder vos modifications !

### Validation d'une opération commerciale

Une opération commerciale non validée ne sera jamais appliquée. Nous sommes en train de terminer quelques tests avant d'autoriser la validation des opérations commerciales. Vous ne pouvez donc que les configurer et imprimer les étiquettes correspondantes.

### Impression des étiquettes pour une ou plusieurs opérations commerciales

Yuzer vous permet d'imprimer des étiquettes pour certains produits (depuis `Stock > Étiquettes`) ou les étiquettes pour tout votre stock (depuis `Stock > Stock > Étiquettes`). Ces deux menus ont été dotés d'options pour imprimer les prix relatifs à une ou plusieurs opérations commerciales. Si un produit correspond à plusieurs opérations commerciales, la meilleure remise sera appliquée.

* Imprimer certaines étiquettes (et définir la configuration d'impression)
  - vous pouvez choisir au centre de l'écran vos opérations commerciales
  - vous pouvez choisir dans les options d'impression si l'opération commerciale a ou non un prix barré et la taille de la police de ce prix.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/commercial-operation-print-one.png" width="800px"/>

* Imprimer tout le stock

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/commercial-operation-print-all-stock.png" width="700px"/>


# Mai 2022 - Version 1.25.0

## Affichage de la TVA sur marge

La TVA sur marge qui était déjà bien prise en compte en comptabilité est désormais prise en compte dans les écrans:

- de liste de dossiers
- de détails d'un dossier
- dans les paniers
- dans les chiffres du widget de C.A.
- dans l'analytique

La marge affichée prend donc désormais bien en compte l'impact de la TVA sur marge. Lorsqu'une TVA sur marge est appliquée le montant de TVA est indiqué avec un icône 'marge' représenté par un camembert.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/vat-margin-basket.png" width="460px"/>

## Stocks

- Vue stock

Les fonctions d'export de stock et l'écran de stock négatif ont été remplacées par une fonction d'édition du stock.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-browse.png" width="100%"/>

Celle-ci vous permet de configurer l'édition du stock suivant de multiples critères:

- La date d'extraction.
- L'entrepôt et emplacements de l'entrepôt.
- Les références dont certains emplacements ont un stock négatif.
- Les produits inconnus (possible lorsque le fournisseur a été supprimé ou que le produit a était géré dans un catalogue personnalisé et que celui-ci a été supprimé par un opérateur).
- Les fournisseurs et marques.
- Les catégories de produit.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-list-cfg.png" width="650px"/>

Vous pouvez également sélectionner les colonnes à afficher dans l'écran de configuration.

Une fois la configuration validée, la liste affichée vous permet de grouper le contenu par un ou plusieurs critères de votre choix. Vous pouvez alors exporter le détail ou les agrégations en CSV ou XLSX.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-list.png" width="650px"/>

<div class="alert alert-info m-1">
Ne pas sélectionner les colonnes d'emplacements (entrepôt, zone, étagères, planches et paquet) permet d'agréger les quantités et valeurs totales. Par exemple si seule la zone est sélectionné mais ni les étagères, planches et paquet alors les quantités seront agrégées par zone.
</div>

### Vue détails de produit

La vue de détails d'un produit a été revue pour apporter plus de lisibilité sur les informations les plus importantes.

L'affichage de l'application en mode _client_ cache les détails du stock, des réservations d'autres clients et des commandes. Les détails du produit sont eux automatiquement affichés ainsi qu'une vue simplifiée de la disponibilité produit (prenant en compte les réservations).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/item-detail-client.png" width="100%"/>

<div class="alert alert-warning">
Attention si vous ne voyez plus les informations détaillées du stock c'est que vous êtes en vue client. Pensez à passer en vue concessionaire pour visualiser ceux-ci.
</div>

#### Information rapides sur le stock

Le niveau de stock, la consommation sur le produit et un prévisionnel s'affichent désormais sur la vue produit.

La couleur de l'encadré _Disponible_ est dépendant de la disponibilité du produit:

- Vert lorsque le produit est en stock
- Jaune lorsqu'il existe une disponibilité sur des pièces commandées (commandées et non-réservées)
- Rouge lorsque le produit n'est pas disponible en stock et n'a pas été commandé.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-quick-info.png" width="440px"/>

Si des pertes ont été relevées lors d'un inventaire celle-ci apparaissent aussi dans un encadré spécifique.

<div class="alert alert-info">
Le prévisionnel est actuellement en bêta et nécessite que le produit ait une antériorité sur l'année précédente.

En effet la consommation étant fortement fluctuante en fonction de la période de l'année nous ne souhaitions pas imposer de vision erronée en fin d'année lorsque l'activité décroit.
Nous allons améliorer cette fonction dans le futur afin de vous permettre de bénéficier de celle-ci sans antériorité.

</div>

_Note: Le graphique de prix d'achat du stock du produit, qui n'était pas le plus utilisé, disparait temporairement et reviendra sous une autre forme dans une version ultérieure._

#### Liste d'évènements de mouvement de stock

La liste des évènements de mouvement de stock d'un produit est désormais mensualisée. Il est possible d'un coup d'oeil de visualiser les mois au cours desquels des évènements de stock ont été générés. Ceux-ci ont en effet une pastille verte à la droite du nom du mois.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-event-price-edit-list.png" width="100%"/>

#### Correction de la valeur d'achat d'un évènement

Il est également possible désormais de corriger la valeur d'achat d'un évènement depuis cette même liste d'évènements de stock en cliquant sur le bouton éditer en face du PA HT. Seul les utilisateurs _ADMIN_ et _COMPTABLE_ peuvent actuellement utiliser cette fonctionnalité.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-event-price-edit-modal.png" width="450px"/>

Dans le cas d'une réception le prix de la ligne de réception associée est également mis à jour.

<div class="alert alert-warning">
A noter que la mise à jour dans la réception ne sera pas effectuée:
 - Si le stock a été fusionné d'une référence produit vers une autre (ou d'un fournisseur à un autre)
 - Sur certains évènements de réception datant de plus de deux mois.

Ces désagréments ne sont valable que sur les évènements antérieurs à cette version. Il sera possible dans le futur de bien mettre à jour les évènements de réception avec le prix de leur ligne y compris sur des stock fusionnés.

</div>

#### Changement du prix d'achat moyen pondéré.

En plus de la modification du prix d'achat d'un évènement (qui impacte le prix d'achat moyen pondéré), il est également possible de modifier directement celui-ci depuis la fiche produit.

Ceci permet de prendre en compte une dévaluation de stock par exemple ou d'effectuer une correction rapide. Un évènement de stock sera alors généré afin qu'un re-calcul de valeur de PAMP depuis les évènements conserve bien la valeur indiquée. Bien entendu les évènements futurs de réception impacteront à nouveau le PAMP.

La modification se fait depuis l'encart _stock_ de la vue de détail d'un produit.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-edit-wapp.png" width="650px"/>

Et ouvre la popup suivante:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/stock-edit-wapp-modal.png" width="450px"/>

### Inventaires

Il est désormais possible de faire des inventaires sur un sous-ensemble de produits et non plus uniquement d'emplacements.

A noter que cette option n'est disponible que si tout le stock ou un ensemble d'emplacements sont inventoriés. Elle n'a en effet pas de sens dans le cadre d'un inventaire vide.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/inventory.png" width="650px"/>

## Filtrage des balances

Il est désormais possible de filtrer les balances client dans la vue balance. Vous pouvez filtrer par montant ou par nom de client.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.25.0/balance.png" width="100%"/>

## Paravol

Il est désormais possible d'effectuer l'enregistrement de gravage d'un vélo Paravol automatiquement à la vente.

Le vélo doit avoir un identifiant Paravol enregistré au préalable. L'enregistrement est alors automatiquement effectué lors de la facturation. Et peut-être relancé en cas d'échec, ou si l'identifiant a été spécifié ultérieurement, manuellement depuis la ligne de vélo du panier facturé.

## Améliorations diverses

- Un lien vers le panier est désormais disponible dans la liste des réservations produit d'une fiche client.

## C'est corrigé

- Certaines colonnes dans l'analytique n'étaient pas exportées avec le bon format dans excel.
- Le regroupement par dates dans l'analytique n'affichait pas celles-ci correctement.
- Les catégories filtrées dans le widget de C.A. sont bien pré-cochées lors la modification de celles-ci.
- Sur la vue des dossiers véhicules le filtre ouverts/clôturés lors d'un changement d'entité ne peut plus être dans un état inconsistent avec la liste affichée.
- Les identifiants de produit de M.O. dans l'analytique sont désormais bien ceux enregistrés dans la configuration de la M.O.
