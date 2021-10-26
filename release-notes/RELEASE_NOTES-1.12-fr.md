# Octobre 2021 - Version 1.12.0

Améliorations diverses:

- Dans les écrans affichant des listes de produits commandés (_En attente de commande_, _Détail de commande_) nous affichons désormais la référence avant le libellé du produit comme dans les autres écrans de l'application.

# Ajout dans le panier depuis la liste ou fiche de produit

L'ajout de produits dans un panier, ou à commander, depuis la liste de produits a été amélioré et est désormais aussi disponible depuis la fiche article.

Vous pouvez toujours spécifier un nombre de produits à ajouter mais un bouton _+1_ permet d'ajouter rapidement une unité au panier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/item-quick-add-nbr.png" height="64"/>

- L'icône change en fonction du contexte que ce soit
  pour l'ajout dans un panier:

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/item-quick-add-basket.png" height="64"/>

- ou pour l'ajout dans les produits à commander au fournisseur:

  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/item-quick-add-order.png" height="64"/>

# Gestion des documents d'identité d'un contact

<div class="row">
  <div class="col">
Vous pouvez désormais ajouter à un contact les pièces d'identité suivantes:

- Permis de conduire
- Pièce d'identité nationale
- Passeport

</div>
  <div class="col">
    <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/identity-docs.png" height="320"/>
  </div>
</div>

# Gestion des marges recommandées à la vente

La gestion des marges de vente minimales a été ajoutée dans l'onglet **Gestion commerciale**/**configuration commerciale** du paneau d'administration.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/recommended_margins.png" height="380"/>

Vous pouvez ici définir des règles sur la gestion des marges à la vente. Il est possible d'être informatif ou restrictif (sachant qu'un utilisateur administrateur pourra toujours effectuer une vente malgré la configuration spécifée).

<div class="alert alert-info mb-1 mt-1">
Ces configurations ne sont appliquées que pour les paniers de véhicules et de produits identifiés. Les ordres de réparations et vente de pièces ne sont pas concernées.
</div>

Une fois configurées, nous affichons un avertissement sur la mage du panier ou véhicule si celle-ci ne respecte pas la règle.

Lors de l'édition du panier:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/basket-margin-warn.png" width="100%"/>

Ainsi qu'avant l'édition des divers documents:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/basket-margin-warn-invoice.png" height="380"/>

Dans le cas ou l'option permettant d'empêcher la facturation d'un panier dont la marge est inférieure à celle souhaitée yuzer affiche l'alerte lors de l'édition en rouge et empêche l'édition de documents:

<div class="d-flex justify-content-center">
  <div class="mr-2">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/basket-margin-error.png" height="48"/>
  </div>
  <div class="ml-2">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/basket-margin-block.png" height="140"/>
  </div>
</div>

<div class="alert alert-warning mb-1 mt-1">
Les règles basées sur l'âge du stock nécessitent que le dossier renseignent une date de réception pour être appliquées.
</div>

# Amélioration de la gestion des attributs des produits

Nous avons modifié et amélioré la gestion des attributs des produits. Ceux-ci ont été revus en fonction des différentes catégories.

<div class="alert alert-info mt-1 mb-1">
Nous allons effectuer des mises à jour dans les mois à venir pour améliorer leur remplissage et utilisation dans les catalogues. Ils sont également une première pierre dans l'amélioration de la gestion du catalogue produit et la future gestion des produits parents.
</div>

# Extension de la vente par dossier à toute catégories

Le système de gestion de stock et vente par dossier, qui était réservé jusqu'à présent aux véhicules est désormais étendu à n'importe quelle catégorie suivant la configuration de Yuzer.

Dans ce système, chaque produit est identifié de manière unique. Il est bien entendu particulièrement adapté aux véhicules, ou le VIN est l'identifiant de référence, mais trouve également écho dans le monde du vélo. Et pourrait-être étendu à d'autres cas.

Les contraintes de cette gestion sont les suivantes:

- Chaque produit doit-être identifié de manière unique (on ne peut pas utiliser de numéro de série commun à plusieurs produits mais il faut bien un numéro totalement unique).
- Les catégories qui auraient été désignée comme devant-être identifiées ne doivent plus être gérée dans le stock classique mais à travers un dossier (comme pour les véhicules)
- Il est possible de faire une préparation de ces dossier de "produits identifiés" qui peuvent alors contenir d'autres produtis comme étant "montés sur sur le produit identifié"
- Lors d'une vente il faut sélectionner le dossier que l'on veut lier à la vente afin de pouvoir la réaliser (il n'y a plus de notion de picking classique du stock)
- Il est possible d'associer de tels produits à un client et d'effectuer une reprise de ces produits (qui auront alors leur dossier d'occasion)
- Il faut bien entendu ne pas entrer dans le stock classique de tels produits (les réceptions de ces produits doivent être effectuées à travers la création d'un dossier et non via une réception dans l'onglet de stock)
- Aujourd'hui le nombre de produits identifiés dans un panier est limité à un, comme pour les véhicules. Cette limitation sera supprimée dans le futur.

## Configuration des _catégories identifiables_

Si vous souhaitez vendre des produits autre que les véhicules (vélos par exemple) à travers ce modèle plutôt qu'à travers un modèle classique, vous devez configurer une catégorie identifiable.

Dans l'écran d'administration un nouvel onglet _Catégories identifiables_ vous permet d'accéder au menu de configuration de ces catégories.

Vous y retrouvez la possibilité d'activer ou non la gestion des véhicules (qu'il est impossible de vendre autrement que par le modèle de dossier véhicule).

Vous pouvez créer une nouvelle catégorie identifiable à l'aide du bouton **+** qui ouvre alors la boite de dialogue suivante vous permettant de configurer les champs suivants:

- Préfixe: Une chaine de catactère utilisée dans le cadre de la numérotation des dossiers; chaque catégorie identifiable doit avoir son propre préfixe et aura une numérotation différente.
- Libellé: Le nom de la catégorie telle qu'elle sera affichée dans l'application
- Catégorie: La catégorie Yuzer cible de la gestion par identification et dossier
- Fournisseurs: Une liste optionnelle de fournisseurs cible de l'identification; si spécifiée seul les produits de ces fournisseurs seront traités par identification dans cette catégorie. Les produits des autres fournisseurs seront alors gérés en stock de manière classique. Laissez cette option vide pour traiter toute la catégorie de manière unifiée.

## Liste de mes dossiers identifiés

De nouveaux onglets s'ajoutent ou se substituent (en fonction de la configuration ci-dessus) afin de vous permettre de gérer vos dossiers de produits identifiés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.12.0/dealer-file-list.png" width="100%"/>

## Associer un produit identifié à un client

De la même manière

## Création d'un nouveau panier de vente de produit identifié

##

## Actions rapides du menu principal

# C'est corrigé

- La TVA est correctement recalculée dans un certain nombre de cas très particuliers:
  - lorsqu'un groupe de facturation devient une CESSION (la marge est alors aussi adaptée),
  - lorsque l'acheteur d'un véhicule est changé pour un contact exonéré de TVA,
  - lorsqu'une vente de véhicule se fait depuis un dealer file avec un contact exonéré de TVA.
- Après avoir édité ou modifié les prix d'un véhicule, les changements sont visibles lorsqu'on revient sur le catalogue.
- Après avoir modifié un véhicule (une instance ou un dossier), les changements sont visibles lorsqu'on revient sur la liste.
- Lors de l'édition d'un document de cession dans le cadre d'une préparation véhicule les produits qui sont enlevé du stock et non déplacés sur le véhicule ont leur prix correctement mis à jour
- Dans la vue jour du calendrier _unassigned_ est désormais bien traduit à _NON ASSIGNE_
- Les véhicules peuvent bien être changé de statut de _En attente de commande_ à _Commandé_
- Le scrolling de la vue jour du calendrier a été corrigé dans le cas de mécaniciens nombreux (les boutons de changement de vue ne sont plus sujets à celui-ci).
- Lors d'une recherche globale les actions de _Recherche avancée_ pré-complètent la recherche sur laquelle vous êtes redirigés avec le texte entré.
