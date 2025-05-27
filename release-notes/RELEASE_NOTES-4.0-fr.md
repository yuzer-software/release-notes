# Mai 2025 - Version 4

yuzSection Horaires d'ouverture / travail

Yuzer 4 vous permet de définir vos horaires de travail et d'ouverture de manière plus précise.

Pour chaque définition d'horaires, vous pouvez définir :

- les horaires standard, appliqués à partir d'une certaine date et répétés tous les ans pour certaines périodes de l'année (par exemple horaires d'été et horaires d'hiver)
- les horaires exceptionnels, appliqués une seule fois entre deux dates bien précises

Les horaires sont partagés avec les entités filles.

Les horaires que vous aviez configurés pour vos espaces de travail ont été recréés dans des horaires standard contenant une seule période avec les plages horaires que vous aviez choisies. Un minimum d'horaires a été créé : si deux espaces de travail avaient les mêmes horaires, ces horaires ne seront définis qu'une seule fois et réutilisés pour les deux espaces de travail. Si ces deux entités appartiennent à des entités différentes ayant un lien de hiérarchie, les horaires seront définis dans l'entité parente et réutilisée dans l'entité fille. Si les deux espaces de travail n'ont pas de lien hiérarchique, deux horaires seront définis.

Toutes les définitions d'horaires sont accessibles depuis le menu d'administration `Espace de travail > Horaires`.

## Le menu `Horaires`

Ce menu vous permet de visualiser vos horaires sur une plage donnée (par défaut l'année courante) et de les définir. Vous pouvez choisir des horaires à modifier (1) ou en créer de nouveaux (2). Si vous modifiez des horaires, tous les espaces de travail utilisant ces horaires bénéficieront automatiquement du changement. Ne créez donc de nouveaux horaires que si nécessaire, c'est-à-dire si deux espaces de travail utilisant les mêmes horaires doivent désormais utiliser des horaires différents qui n'existent pas déjà.

Ce menu comporte trois partie :

- `Horaires` : vous permet de visualiser les horaires résultantes des horaires standard actuels et futurs, et des horaires exceptionnels. Un changement d'horaires est manifesté par un fin séparateur orange (3).
- `Horaires standard` : Vous permet de visualiser les horaires récurrents d'une année sur l'autre et de définir de nouveaux horaires pour une date fixée.
- `Horaires exceptionnels` : Vous permet de visualiser et de définir des horaires exceptionnels.

![Schedules](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/working-times.webp?w=100%)

## Définition des horaires standard

Les horaires standard se répètent chaque année par période de l'année (par exemple été / hiver). Vous pouvez planifier un changement d'horaires pour une date fixée. Pour cela, cliquez sur `Nouveaux horaires` à côté du titre `Horaires standards`.

![New working times](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/working-times-new-revision.webp?w=100%)

La fenêtre d'édition s'ouvre (Note : ouvrir la fenêtre d'édition en cliquant sur "éditer" alors que la date d'application des horaires est passée ne vous permettra que d'en changer le nom).

Définissez les informations générales :

- Nom des horaires : nouveau nom, visible lors de la sélection des horaires sur les espaces de travail
- Date d'application : date à laquelle les nouveaux horaires entrent en vigueur

Puis définissez les périodes. Vous pouvez demander à Yuzer d'arrondir le début de la période à partir d'une date spécifique. Dans l'exemple ci-dessous, notre période d'été commence le mardi 1er avril ou, si le 1er avril n'est pas un mardi, le mardi suivant le 1er avril.

![Period start](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/working-times-start-period.webp?w=100%)

Enfin, cliquez sur la ligne d'une journée pour ajouter une période de travail, ou cliquez sur une période définie pour la modifier. Lorsqu'une ligne est vide, vous pouvez copier les données de la ligne immédiatement supérieure pour aller plus vite.

![Period schedules](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/working-times-period-edit-range.webp?w=100%)

Enfin, pour définir une nouvelle période, vous pouvez cliquer sur "Ajouter" pour définir une période vide, ou sur "Dupliquer" pour copier la période précédente. Dans ce dernier cas, les boutons `-30 min` et `+30 min` peuvent être utilisés pour décaler tous les horaires de 30 minutes.

Une fois toutes vos périodes définies, vous n'avez plus qu'à valider. Si vous avez utilisé des arrondis, n'hésitez pas à changer d'année pour voir le résultat sur les années suivantes.

Note : dans le cas où vous voudriez créer (et non modifier) des horaires, le même menu s'ouvre. Vous ne devriez pas avoir à changer la date d'application pour pouvoir l'utiliser immédiatement.

## Définition des horaires exceptionnels

Pour définir un horaire exceptionnel, vous pouvez directement cliquer sur la vue pour sélectionner le début de la période. Vous pouvez aussi cliquer sur une définition d'horaires exceptionnels existante pour l'éditer.

![New exceptional schedules](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/working-times-exceptionnal-view.webp?w=100%)

Dans les deux cas, le menu d'édition s'ouvre. Vous aurez à configurer la date de fin et les horaires à appliquer pour cette période. La sélection des horaires est la même que pour une période d'horaires standard.

![New exceptional schedules](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/working-times-exceptionnal-edit.webp?w=100%)

yuzSection Comptabilité

## Avance sur TVA

Nous avons revu la gestion de l'avance sur TVA.
Désormais, vous pouvez annuler une avance de paiement sans avoir l'obligation d'annuler la facture. Yuzer calcule le montant de l'avance sur TVA à chaque édition d'un reçu de paiement.
Chaque reçu de paiement porte maintenant le montant de TVA à collecter en fonction du contenu du panier et du montant total payé au moment de l'édition, lorsque la facture n'est pas établie.

Concrètement:

- L'édition d'une avance collecte de l'avance sur TVA.
- L'édition d'une facture collecte le restant de la TVA.
- L'annulation d'une avance lorsqu'une facture a été éditée n'annule pas de TVA.
- L'annulation d'une facture, l'annulation d'un paiement ou un remboursement entraîne l'annulation de la TVA correspondante dans la limite du montant des paiements restants.

Pour rappel, les reçus comportant une avance sur TVA possèdent un statut de passage en comptabilité. En effet, si la partie paiement est traitée et passée en comptabilité à travers l'arrêté de caisse, la partie de déclaration de TVA est traitée par le flux classique (comme les factures). Si vous n'avez pas configuré la validation automatique des écritures dans vos paramètres de comptabilité, vous devez valider les écritures liées à ces enregistrements.

yuzSection Liste véhicules

L'écran de liste de véhicules évolue pour plus de simplicité d'utilisation et une meilleure performance d'affichage.

![Dealer file list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/df-list.webp?w=100%)

# Filtres

Première évolution majeure, les filtres ne sont désormais plus liés aux colonnes. Il devient donc possible de filtrer les données sans que la colonne liée soit obligatoirement affichée.
Cela est d'autant plus logique lorsque la vue 'fiches' est utilisée (en lieu et place de la vue 'table').

![Filter button](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/df-list-filter-1.webp?w=400px)

Une fois activé, l'ensemble des filtres disponibles s'affiche à gauche de la liste:

![Filter list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/df-list-filter-2.webp?w=400px)

# Édition de la vue

L'affichage est désormais fixe. Pour modifier la liste des colonnes, les ré-arranger ou grouper/dégrouper, vous devez désormais utiliser le bouton éditer.

## Regroupement

Afin de rendre l'interface plus simple pour l'ensemble des utilisateurs et quelles que soient les colonnes affichées, le regroupement n'est plus activé par drag and drop mais par sélection de colonnes dans la zone _Grouper par_.

![Filter list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.0/df-list-edit-group.webp?w=400px)

|| Vous pouvez toujours cependant réorganiser les colonnes de groupement par drag and drop.

## Ajout de colonnes

Pour ajouter une colonne, déplacez le curseur de la souris à l'extrémité gauche de la colonne après laquelle vous souhaitez ajouter la nouvelle colonne, juste après l'icône de tri. Un nouveau bouton avec l'icône œil apparait alors.

# Replier / Développer

Vous pouvez désormais facilement replier / développer l'ensemble des éléments de la liste.

|| Cette option n'est disponible que lorsque l'ensemble des données peut être affichée. Pour les concessions disposant d'un stock imposant de véhicules il faudra au préalable affiner la requête.

yuzSection Fournisseurs / Accès et services

La gestion des fournisseurs a été revue afin de bien dissocier les notions de fournisseurs et "d'accès / intégration".

- Les fournisseurs sont désormais uniquement dédiés à votre gestion des fournisseurs et restent liés à vos achats divers.
- La gestion de l'accès à des services tiers ou complémentaires est désormais externalisée.

Chaque accès correspond à une autorisation vous permettant d'exploiter un ou plusieurs services.

Par exemple, si un catalogue vous intéresse, il vous faut désormais une validation que vous y avez effectivement accès. En effet, les catalogues sont édités par des tiers et l'accès aux informations de ceux-ci sont donc liés à vos contrats avec ces tiers.
De même, pour accéder au service de commande de pièces que certains fournisseurs offrent, vous devez valider un accès à ce service, qui devra ensuite être lié à un fournisseur donné.
D'autres accès vous permettent de valider votre capacité à effectuer des enregistrements de données dans des services externes (constructeurs, APIC pour le vélo etc.)

La séparation des deux concepts permet par exemple d'ajouter à un fournisseur existant un nouveau service de commande: cela vous évite de devoir d'une part désactiver le fournisseur existant et d'autre part recréer un nouveau fournisseur... avec tous les problèmes liés aux numéros de fournisseurs.

# Évolutions fournisseurs

Pour gérer vos fournisseurs, rendez-vous comme avant dans le menu _fournisseurs_ de Yuzer.

Les fournisseurs sont désormais définis au niveau du compte : ils peuvent ensuite être ajoutés sur chaque entité. Cela permet de mieux gérer leur numéro en comptabilité.
Cette information peut être surchargée par entité.

## Ajouter un fournisseur

Nous avons simplifié l'ajout de fournisseur, permettant de réutiliser rapidement un fournisseur déjà défini au niveau groupe, de créer rapidement un nouveau fournisseur, d'ajouter un autre compte YUZER comme fournisseur (réseau de redistribution) ou d'en créer à partir d'un accès, tout cela depuis la même interface pour plus de clarté.

| La création depuis un accès permet le cas échéant de connecter le fournisseur à l'accès de gestion de commande. Si l'accès choisi ne propose pas de gestion de commande la sélection permet uniquement de pré-remplir un ensemble de champs automatiquement.

## Gestion des modalités de paiement

Les modalités de paiement des fournisseurs sont désormais gérées directement au niveau du fournisseur et non dans un menu externalisé.

Vous devez actuellement re-spécifier ces modalités pour chaque entité à cause du lien avec les moyens de paiements (qui sont définis au niveau de l'entité).

yuzSection Yuzer PAY

YUZER 4, c'est surtout l'arrivée de YUZER PAY, notre solution de paiement intégrée.

Cette solution sera mise en place progressivement, tout d'abord chez quelques beta-testeurs sélectionnés, puis progressivement à l'ensemble d'entre vous.

Nous vous tiendrons au courant des modalités d'accès lorsque celles-ci seront précisées.

yuzSection Général

## Rappels SMS

Les tâches de réception et de livraison ont maintenant les tags respectifs `Réception` et `Livraison` lorsqu'elles sont créés à partir d'un panier. Il est également possible de configurer ces tags à partir du planning de réception.
Ces tags peuvent être utilisés pour configurer les rappels afin de n'envoyer des messages que pour un certain type de rendez-vous.

## Intégrations

- Le marquage vélo APIC avec Auvray a été mis en place. Nous contactons les autres opérateurs afin de proposer d'autres fournisseurs.
- Une intégration Pennylane facilite votre synchronisation comptable avec l'outil mentionné. Celle-ci est disponible en alpha et sera ouverte à tous bientôt.
