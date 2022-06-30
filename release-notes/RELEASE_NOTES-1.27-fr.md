# Juin 2022 - Version 1.27.0

## Ajout d'un journal d'achat spécifique pour les reprises

Dans les paramètres de comptabilité il est désormais possible d'assigner un journal spécifique aux reprises.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/tradein_journal.png" width="600px"/>

Pensez à bien sauvegarder la configuration une fois modifié (en bas de l'écran).

## Cerfa 15776-02

Vous pouvez désormais éditer un cerfa 15776-02 directement depuis le panier de reprise d'un véhicule.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/trade_in_cerfa.png" width="100%"/>

Vous devez avoir un dossier attaché afin de pouvoir créer celui-ci.

## Filtre des paniers

Vous pouvez désormais retrouver des paniers en fonction des tags des clients associés.

<div class="m-2 alert alert-warning">
Note: Lors de la modification des tags d'un contacts seul les nouveaux paniers seront impactés. La mise à jour des anciens paniers lors d'un changement de tags sera disponible dans une version future.
</div>

## Export des dossiers véhicules / produits

L'export des dossiers véhicules permet désormais l'export des dossiers clôturés et ouverts dans un même fichier.

## Analyitiques

L'affichage des colonnes lorsque peu d'entre elles sont sélectionnées n'est plus aligné à droite mais s'étends bien sur l'ensemble de l'écran.

## Tri des tables

La plupart des tables peuvent désormais être triées. Le tri peut-être effectué sur plusieurs colonnes dans l'ordre inverse du click (ce comportement est équivalent à celui que l'on peut avoir dans excel par exemple lorsque l'on effectue un premier tri sur une colonne puis que l'on re-trie le tableau sur une autre colonne).

Afin d'activer le tri, il suffit de clicker sur le bouton correspondant de la colonne que l'on souhaite trier. Un nouveau click change l'ordre du tri et un troisième click supprime le tri sur la colonne. L'icône de tri de la colonne principale (dernière à avoir été triée) est affiché en bleu.

## Améliorations diverses

- Des liens vers le panier et le client ont été ajoutés dans l'écran de clotûre de caisse.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/cash_desk_links.png" width="600px"/>

- La recherche sur les tags existant dans l'application n'est plus sensible à la casse (majuscules/minuscules) et aux diatriques (accents, cédilles).
- L'affichage des propriétés d'un vélo a été amélioré.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/velo_props.png" width="100%"/>

## C'est corrigé

- La fusion du stock lors d'une fusion de fournisseurs a été corrigée. Une erreur empêchait son bon déroulement.
