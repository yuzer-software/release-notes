# Mai 2025 - Version 4

yuzSection Horaires de travail

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
Désormais, vous pouvez annuler une avance de paiement sans avoir l'obligation d'annuler la facture. Yuzer calcul le montant de l'avance sur TVA à chaque édition d'un reçu de paiement.
Chaque reçu de paiement porte maintenant le montant de TVA à collecter en fonction du contenu du panier et du montant total payé au moment de l'édition, lorsque la facture n'est pas établie.

Concrètement:

- L'edition d'une avance collecte de l'avance sur TVA.
- L'édition d'une facture collecte le restant de la TVA.
- L'annulation d'une avance lorsqu'une facture a été édité n'annule pas de TVA.
- L'annulation d'une facture, l'annulation d'un paiement ou un remboursement entraîne l'annulation de la TVA correspondante dans la limite du montant des paiements restants.

Les reçus comportant une avance sur TVA possèdent un statut de passage en comptabilité. Ils doivent être traités individuellement afin d'enregistrer les écritures relatives à la TVA pré-collectée.
A noter que la validation peut être automatisée en activant la validation automatique des écritures dans vos paramètres de comptabilité.

yuzSection Général

## Rappels SMS

Les tâches de réception et livraison ont maintenant les tags respectifs `Réception` et `Livraison` lorsqu'ils sont créés à partir d'un panier. Il est également possible configurer ces tags à partir du planning de réception.
Ces tags peuvent être utilisés pour configurer les rappels afin de n'envoyer des messages que pour un certain type de rendez-vous.
