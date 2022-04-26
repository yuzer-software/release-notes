# Avril 2022 - Version 1.22.5

## C'est corrigé
- Attention: Les données du widget main d’oeuvre sur les statistiques de tâches (hors chiffre d’affaire et temps facturés) étaient erronées. En effet un filtre permettant de ne compter que les tâches planifiées ne fonctionnait pas correctement et l’ensemble des tâches étaient prise en compte résultant en une prise en compte excessive des tâches et double comptage du temps. Ceci a été corrigé et les données visibles seront donc impactées.
- Les données du widget de main d’oeuvre sont désormais bien mise à jour au changement d’entité.
- La configuration du widget de main d’oeuvre a été améliorée, les assignés disponibles ainsi que taux de M.O. disponibles dans les filtres ne sont désormais plus dépendants des données chargées.
- L’affichage de l’analytique a été légèrement amélioré afin de limiter le décalage de taille de colonnes sur un scroll.
- Les exports de données des tables analytiques et widget M.O. exportent les champs dates et numériques dans un format reconnu par excel.
- Correction des prix remisés sur l’analytique.

# Avril 2022 - Version 1.22.4

## C'est corrigé
- Le placement du nouveau selecteur de date dans le calendrier (atelier etc) est désormais bien positionné en bas à gauche du bouton et visible dans tout contexte.

# Avril 2022 - Version 1.22.3

## C'est corrigé
- Correction d'une erreur empêchant l'impression correcte d'étiquettes produits

# Avril 2022 - Version 1.22.2

## C'est corrigé
- Une erreur empêchait de sélectionner le véhicule d'un contact avec celui-ci dans l'édition d'une tâche

# Avril 2022 - Version 1.22.1

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
