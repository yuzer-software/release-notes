# Novembre 2025 - Version 4.5

yuzSection 4.5.4 et suivantes

# Application mobile 4.3.2 (Android)

Les scanners externes (type eyoyo) ne fonctionnaient pas toujours bien : il manquait parfois quelques caractères lorsque celui-ci émettait trop rapidement les lettres. Nous avons travaillé dur à l'optimisation des performances dans ces scénarios à travers une nouvelle option.

Nous avons modifié le bouton "changement de mode" pour ouvrir une modale avec les options suivantes :
  * mode: `caméra` ou `scanner` (ce que faisait le bouton auparavant)
  * un toggle "Optimisation du scanner externe" exclusivement réservé aux scanners qui émettent le résultat du scan comme s'il s'agissait d'un clavier.

Aussi, comme seulement le caractère "retour à la ligne" ne passait pas, empêchant de valider le texte, nous avons ajouté un bouton "valider quand même" (check vert) : lorsque le scanner affiche le warning "inactif", relisez le code, et s'il est correct, cliquez sur ce bouton pour valider le scan. Sinon, il vous faudra re-scanner comme auparavant.


# 4.5.4

- Correction d'export de table (édition de stock) où la ligne d'en-tête était décalée d'un vers la droite et où une ligne vide pouvait apparaître après les en-têtes.
- Il est possible d'accéder aux Cerfas des reprises même si l'entité n'a pas le catalogue du produit associé au véhicule.
- Correction d'un problème de rafraichissement du détail d'un produit (notamment le nom du catalogue) lorsqu'on passait directement d'un produit à l'autre (par exemple avec les "derniers travaux").


yuzSection Catalogue

Les catalogues contiennent à la fois des produits et des modèles de paniers.
Dans certains cas, les modèles peuvent encombrer la recherche si vous ne les utilisez pas.

Il est désormais possible de désactiver les modèles de paniers dans un catalogue.

Pour cela, rendez-vous dans le menu `Administration > Catalogue`, sélectionnez le catalogue souhaité puis cliquez sur le bouton `Modèles` pour les désactiver.

![Catalog usages config](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.5/catalog-usages-config.webp?w=480px)

yuzSection Général

## Améliorations

- Ajout du support de la référence d'affichage pour les dossiers vélo.
- Ajout du support de la référence d'affichage pour les références parentes.
- Ajout d'une fonction de recherche dans la liste et l'édition des modèles de commentaires.
- Il est maintenant possible de réceptionner un vélo via la création et association automatique avec un nouveau dossier.

## Corrections

- Correction de la vue 'Administration > Yuzer Pay > Frais bancaire' qui ne s'affichait plus dans certains cas.
- Correction des pages de release notes qui n'affichaient plus certaines versions.
