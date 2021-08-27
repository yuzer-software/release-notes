# Août 2021 - Version 1.9.0

## Modification des catégories de produit

Nous avons séparé la catégorie "Autres services et taxes" en "Autres services" d'une part et "Autres taxes" d'autre part afin d'automatiser, dans le futur, l'application de la TVA à ces catégories. Toutefois, le processus de renommage ne peut pas être totalement automatisé et requiert votre attention.

Nous avons renommé la catégorie _Autres services et taxes_ en _Autres services_ dans tous les catalogues, mais nous n'avons pas effectué de renommage ailleurs, et en particulier dans les règles de comptabilité. Nous vous demandons donc :

<div class="alert alert-danger">
  <ul>
    <li>
      de bien vérifier vos règles de comptabilité (Comptabilité > Configuration des comptes)<br/>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/accountancy-rule.png"/>
    </li>
    <li>de bien vérifier que les catégories des produits dans les paniers ouverts existants sont correctes</li>
    <li>
      de bien vérifier que les produits désormais dans "Autres services" ne devraient pas être dans "Autres taxes" (vous pouvez utiliser le filtre comme ci-dessous)<br/>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/search-for-other-services.png" height="160"/>
    </li>
  </ul>
</div>

## Contacts

- Le numéro d'immatriculation des véhicules du client sont désormais affichés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/vehicle-registration.png" height="140"/>

## Stock négatif

Dans Stock -> Onglet Stock, il a maintenant un nouveau bouton "Stock négatif" permettant d'afficher tout les produits ayant un stock négatif dans au moins un lieu.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/negative-stock.png" height="160"/>

## Surcharge de prix

Il est possible de surcharger le prix d'un vehicule, lorsqu'il n'appartient pas à une concession.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/override_prices.gif" height="160"/>

## Date de facture d'achat

Dans la fiche de véhicule, vous pouvez dorénavant retrouver et modifier la date de facture d'achat.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/purchase-invoice-date.png" height="160"/>
