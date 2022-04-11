# Avril 2022 - Version 1.22.0

## Produits

Dans la vue de détails d'un produit, vous pouvez maintenant remplacer et définir un prix spécifique pour celui-ci.

<div class="alert alert-warning">
- Les règles de marge, de TVA et de tarification ne sont pas appliquées dans ce cas.
- Ce prix est appliqué pour votre entité seulement
- Les valeurs que vous sauvegardez ne sont pas changées lorsque les prix fournisseurs sont mis à jour (import catalogue, synchronisation automatique, etc).
</div>

Dans la fenêtre d'édition, vous avez le detail des différents prix de produit:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/entity-prices-modal.png" width="650px"/>

Lorsqu'un remplacement a été défini, un icône apparait à côté des prix.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/entity-prices-override-icon.png" width="700px"/>

Sinon, vous pourrez apercevoir les icônes de règle de marge, de TVA ou règle de tarification qui sont appliqués au produit.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/entity-prices-pricing-policy-icons.png" width="700px"/>

Les magasiniers et comptables peuvent consulter la liste des produits ayant un remplacement de prix dans le menu _Magasin > Configuration > Prix remplacés_

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/entity-prices-list.png" width="800px"/>

## Calendrier

- Un sélecteur de date est maintenant accessible pour visualiser directement les tâches d'une journée ou semaine précise.

  <img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/calendar-datepicker.png" width="200px"/>

- Nous avons ajouté un bouton pour rafraichir les tâches de la vue. A noter que vous avez toujours accès au bouton pour _rafraichir toutes les 5 minutes_ sur tableau de bord et que celui-ci est maintenant également présent dans la vue _Calendrier_ et _Kaban_.

  <img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/calendar-refresh-button.png" width="250px"/>

## Améliorations diverses

- Sur une réception, afin d'optimiser la saisie du nombre réservations client, il est maintenant nécessaire d'entrer une quantité avant d'ajouter un produit.

  <img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/reception-quick-add.png" width="300px"/>

- Lorsque vous ajoutez un vélo à un contact, les valeurs des champs de formulaire ne sont plus supprimées lorsque vous modifiez la catégorie.

- Ajout d'un bouton pour remplacer un produit dont le fournisseur n'existe plus.

  <img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.22.0/basket-replace-missing-supplier-product.png" width="450px"/>

## C'est corrigé

- L'annulation d'un panier supprime maintenant le lien dans le dossier associé.
- Le titre des paniers n'étaient pas toujours rafraichi quand on en sélectionne un autre.
