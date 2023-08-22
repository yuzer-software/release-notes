# Juillet 2023 - Version 2.14.5

- Correction des recherches liées aux identifiants de variant.

# Juillet 2023 - Version 2.14.4

- Correction apportée à la gestion des lignes de forfaits dans l'analytique pour correctement prendre en compte uniquement le contenu.

# Juillet 2023 - Version 2.14.0

## Modèles de panier

Un modèle de panier peut:

- Soit être ajouté en tant que forfait. Dans ce cas, seul le prix global est affiché sur le panier dans lequel il est utilisé et les éléments sont affichés sans prix.
- Soit être ajouté en l'état.

<img width="1096" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/basket-template-2.webp"/>

La nouvelle cible de Yuzer est le comportement suivant:

- Les modèles ajoutés en tant que forfait ont un prix fixe qui n'est pas mis à jour à l'ajout
- Les modèles ajoutés en l'état verront leur tarifs mis à jour à l'ajout.

Afin de ne pas vous impacter immédiatement, une option a été ajoutée afin que le comportement précédent reste actif. Vous devez effectuer la configuration de l'option si vous souhaitez que le nouveau comportement soit appliqué dès maintenant.

<img width="986" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/basket-template-1.webp"/>

Cette option est temporaire et les versions futures de Yuzer adopteront le comportement défini ci-dessus. Si certain de vos modèles ajoutés en l'état devraient avoir un prix fixe vous devez les configurer en tant que forfaits afin que ces tarifs n'évoluent pas à l'ajout lorsque le nouveau comportement sera appliqué de manière standard.

## Catalogue produit

### Gestion des variants

Le catalogue de produit permet désormais de regrouper les variants d'un même produit afin de simplifier la recherche et l'accès à ceux-ci. Afin de grouper plusieurs produits d'un même catalogue ensemble il faut définir pour ceux-ci un identifiant de variant commun.

La référence parente est venue s'ajouter aux différents champs d'édition:

<img width="986" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/variant-edit.webp"/>

Lors d'une recherche vous pouvez désormais visualiser les différents variants regroupés ensemble

<img width="1096" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/variant-list.webp"/>

Et changer efficacement de l'un à l'autre dans la vue de détails d'un produit

<img width="1096" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/variant-detail.webp"/>

<div class="alert alert-info">
Nous améliorons la prise en charge des variants dans les catalogues supportés officiellement par Yuzer et sur lesquels nous disposons d'information quand au support des variants.
</div>

### Règles d'enrichissement de catalogues

Afin de permettre de bénéficier plus efficacement de la gestion des variants, nous avons également amélioré la configuration des règles d'enrichissement des catalogues.

Dans les versions précédentes vous pouviez configurer les éventuelles catégories de tarification fournisseur et les catégories Yuzer depuis des informations de produit.

Ces paramétrages sont désormais plus consistants quel que soit le champ enrichi, et d'autres champs peuvent être définis comme, par exemple l'identifiant de référence parente aux variants (voir ci-dessus).

#### Définir une étape d'enrichissement

Afin d'éditer les règles rendez vous dans _Administration/Catalogue_ puis cliquez sur un catalogue dont vous êtes l'éditeur.

Cliquez alors sur _Éditer_ afin de modifier les règles:

<img width="1096" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-1.webp"/>

Le bouton _Ajouter_ au niveau principal (en bleu) vous permet d'ajouter une étape d'enrichissement. Vous pouvez alors configurer l'étape d'enrichissement:

<img width="464" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-2.webp"/>

#### Filtre

_Ajouter un filtre_ vous permet de définir un filtre afin que l'étape ne soit appliquée qu'à certains éléments du catalogue (par exemple les t-shirts uniquement en utilisant un filtre sur la catégorie)

#### Règles d'extraction

_Ajouter_ une règle d'extraction permet de définir une règle afin d'analyser un champ (en général la référence du produit) pour en extraire des informations.

Ces informations extraites seront alors disponible dans le cadre des règles d'enrichissement (voir ci-dessous).

Plusieurs opérations peuvent être utilisées afin d'extraire des informations.

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-3.webp"/>

- _Découpe par délimiteur_: Dans le cas où votre référence contient des informations séparées par un délimiteur, vous pouvez utiliser cette règle afin d'extraire les différents groupes. Par exemple, la référence "_ref parente-couleur-taille_" délimite les informations avec un "-", on peut donc utiliser le paramétrage suivant:

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-4.webp"/>

- _Sous-chaines de caractères à tailles fixes_: Cette règle permet d'extraire des sous parties de la référence (en préfixe ou suffixe) qui ont une taille de caractères définies.

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-5.webp"/>

- _Pré/Su-fixes définis_: Cette règle permet d'extraire des éléments dont la liste des valeurs possible est pré-définie depuis le début ou la fin d'un champ.

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-6.webp"/>

<div width="876" class="alert alert-info">Vous pouvez définir plusieurs règles d'extractions de différents types, y compris sur un même champ</div>

#### Règles d'enrichissement

Les règles d'enrichissement permettent d'utiliser les éléments précédents afin de définir les valeurs de certains champs. Tels que la référence parente afin d'identifier les variants par exemple, mais aussi de configurer les catégories Yuzer à partir des catégories fournisseur etc.

Trois possibilités d'enrichissement existent:

- _Association conditionelle_: Permet de définir une valeur si la condition est satisfaite.

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-7.webp"/>

- _Association valeur à valeur_: Permet de définir une valeur en fonction de la valeur d'origine.

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-8.webp"/>

- _Copier la valeur_: Permet de copier la valeur d'un autre champ. Cette dernière règle n'est possible que dans le cadre de champs dit libres, c'est à dire dont la liste des valeurs n'est pas contrainte par Yuzer.

<img width="876" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/enrichment-9.webp"/>

Comme vous pouvez le constater les champs extraits dans les règles précédentes deviennent disponible pour l'enrichissement des données du produit.

<div class="alert alert-info">
Les prochaines versions de Yuzer vous permettront également d'enrichir les propriétés des produits telles que la taille ou les couleurs.
</div>

## Comptabilité et analytiques

### Écritures comptables des caisses

Nous avons ajouté la possibilité d'agréger les écritures de caisse par moyen de paiement.

Pour ce faire, allez dans le menu `Comptabilité > Configurer` pour activer l'option:

<div class="text-center" style="text-align: 'center';">
  <img width="364" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/aggregate-cashdesk-by-payment-mean.webp"/>
</div>

<div class="alert alert-warning">
A noter que Yuzer effectue une validation en fonction de la configuration d'agrégation avant d'écrire dans le journal.
En conséquence, si vous changez la configuration alors que vous avez des écritures en attentes, ces dernières ne passeront plus la validation.

Dans ce cas, vous avez 2 solutions:

- Soit vous validez les écritures avant de mettre à jour la configuration d'agrégation.
- Soit vous rejetez les écritures en attentes pour les repasser en comptabilité avec la nouvelle configuration d'agrégation.
</div>

### Gestion des factures d'achat en comptabilité

Certains d'entre vous utilisent les factures d'achat dans Yuzer afin de valider les prix d'achat des réceptions mais les enregistrent dans leur logiciel comptable par d'autres biais. Dans ce cadre nous avons ajouté une option dans les paramètres de comptabilité afin de définir le comportement souhaité pour le passage en comptabilité des factures d'achat.

Trois options sont possibles:

<img width="600" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.14.0/purchase-invoice-accountancy.webp"/>

### Remises totales en analytique

Désormais, si vous avez configuré Yuzer pour qu'une ligne totalement remisée soit considérée comme une cession _cadeau client_ dans vos paramètres de comptabilité, l'analytique les considèrera également comme tel. Les marges ne seront donc plus impactées par celles-ci si vous n'incluez pas les cessions.

## Corrections

- Sur une cession de préparation véhicule le PAMP n'était pas correctement renseigné pour les produits consommés. Les produits montés sont eux bien assignés à un prix de zéro dans ce cadre puisque ceux-ci ne sortent pas du stock.
- Dans le cadre de livraisons partielles de stock à la facturation, un message d'avertissement sur l'impossibilité de réserver du stock à la facturation était affiché à tort pouvant causer une confusion.
- Le statut stock de certaines lignes de panier suite à une facturation pouvait ne plus être correctement affiché lors du retour immédiat sur le panier.
