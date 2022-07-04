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

A la création d'un nouveau panier les tags clients associés sont désormais affichés au niveau du groupe.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/basket_contact_tags.png" width="380px"/>

Le listing des paniers vous permet alors d'utiliser ceux-ci pour filtrer les paniers.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/basket_list_filter_tags.png" width="100%"/>

## Export des dossiers véhicules / produits

L'export des dossiers véhicules permet désormais l'export des dossiers clôturés et ouverts dans un même fichier. Les filtres doivent toujours être configurés sur l'écran précédent mais sont désormais rappelés sur la fenêtre d'export.

De plus, il est maintenant possible, dans la configuration de l'export, de définir de nouvelles colonnes de valeurs (marge, prix de vente ou d'achat etc...)
filtrées sur des catégories ou des filtres personnalisés, permettant ainsi d'agglomérer et d'analyser les lignes d'une facture.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/Revenue_analysis.png" width="600px"/>

## Analytiques

L'affichage des colonnes lorsque peu d'entre elles sont sélectionnées n'est plus aligné à droite mais s'étends bien sur l'ensemble de l'écran.

### Amélioration de la configuration

L'écran d'analytique évolue pour apporter plus de clarté et simplicité dans sa configuration.

#### Gestion des données locales

L'analytique comme dans les versions précédentes stocke locallement certaines données afin de fournir un chargement plus rapide. Par le passé les données stockées ne pouvaient être supprimées simplement et nécessitaient une intervention dans les dossiers de données d'application de la machine.

Désormais lors de l'arrivée sur l'écran d'analytiques vous devez _Faire confiance à cette machine_ afin d'autoriser le stockage local:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_trust.png" width="100%"/>

Vous pouvez également _Révoquer la machine_ afin de supprimer toutes les données locales. Attention effectuer ceci aura un coût de performance non-négligeable si vous continuez d'utiliser la machine.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_revoke.png" width="100%"/>

#### Gestion de vos configurations

Le bouton de configuration à droite vous permet de retrouver les configurations que vous avez déjà créé ou d'en créer une nouvelle.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_configs.png" width="100%"/>

Le bouton Ajouter ouvre une boite de dialogue vous offrant des options de configurations similaire à la version précédente.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_new_config.png" width="100%"/>

Vous pouvez réorganiser vos configurations afin de retrouver vos préférées plus facilement.

<div class="m-2 alert alert-info">
Lorsque vous quitez l'analytiques vous retrouvez la dernière configuration ouverte, à moins que Yuzer ai été redémarré, dans ce cas c'est la première configuration de la liste qui est affichée.
</div>

Une fois une configuration affichée les données sont chargées et affichées. L'écran vous permet alors de modifier directement la période, les filtres et l'affichage (sélection des colonnes).

<div class="d-flex">
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_dates.png" width="380px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_filters.png" width="580px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_columns.png" width="640px"/>
</div>

Les filtres ont été enrichis de filtres rapides similaires à ceux existant dans les widgets.

Lorsque vous modifiez une configuration yuzer vous fourni un apperçu de la modification fondé uniquement sur une sous-partie des données pour des raisons de performance. Ceci vous permet de faire plusieurs modifications de suite plus rapidement. Cliquez sur _Afficher_ afin d'afficher la table avec l'ensemble des résultats.

De plus un ensemble de boutons sont immédiatements disponibles afin:

- D'annuler vos changements
- Dupliquer la configuration afin de la sauvegarder dans une nouvelle configuration
- Sauvegarder vos modifications dans la configuration actuelle.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_save_revert.png" width="380px"/>

#### Affichage des primes et coûts

De nouvelles colonnes sont disponibles désormais dans l'analytiques en plus des colonnes et options déjà existantes qui demeurent inchangées.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_new_cols.png" width="380px"/>

Elles permettentent d'afficher les différents montants de primes, coûts opérationnels ou cession qui sont définies sur une fiche véhicule ou produit identifié.

Contrairement aux options de facturations et au montant déjà existant prenant en compte le prix d'achat incluant coût et primes qui est basé sur les montants à la facturation (et n'est jamais changé), les données des nouvelles colonnes sont récupérées depuis les dossiers véhicules dynamiquement.
Elles sont cependant, pour des raisons de performances et fonctionnelles stockées locallement comme les autres données et ne seront raffraichies que sur demande explicite de l'utilisateur (pour le mois en cours ou pour le mois dernier uniquement).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/analytics_refresh.png" width="280px"/>

## Tri des tables

La plupart des tables peuvent désormais être triées. Le tri peut-être effectué sur plusieurs colonnes dans l'ordre inverse du click (ce comportement est équivalent à celui que l'on peut avoir dans excel par exemple lorsque l'on effectue un premier tri sur une colonne puis que l'on re-trie le tableau sur une autre colonne).

Afin d'activer le tri, il suffit de clicker sur le bouton correspondant de la colonne que l'on souhaite trier. Un nouveau click change l'ordre du tri et un troisième click supprime le tri sur la colonne. L'icône de tri de la colonne principale (dernière à avoir été triée) est affiché en bleu.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/table_sort.png" width="100%"/>

## Améliorations diverses

- Des liens vers le panier et le client ont été ajoutés dans l'écran de clotûre de caisse.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/cash_desk_links.png" width="600px"/>

- La recherche sur les tags existants dans l'application n'est plus sensible à la casse (majuscules/minuscules) ni aux signes diatriques (accents, cédilles).
- L'affichage des propriétés d'un vélo a été amélioré.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/velo_props.png" width="100%"/>

- Les options de format des étiquettes de stock sont plus claires et contiennent de nouvelles options dont la disposition du texte et la possibilité d'empêcher le retour à la ligne d'un texte trop long (qui est alors tronqué).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.27.0/layout_tags.png" width="100%"/>

## C'est corrigé

- La fusion du stock lors d'une fusion de fournisseurs a été corrigée. Une erreur empêchait son bon déroulement.
- La création d'une facture d'achat avec dates d'échéances du fournisseur avait une date de facture décallée.
