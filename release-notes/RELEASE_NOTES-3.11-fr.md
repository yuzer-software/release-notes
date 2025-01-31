# Février 2025 - Version 3.11.x

yuzSection Forfaits

La gestion des modèles de panier par catalogue est désormais parfaitement fonctionnelle. Si seule l'entité éditrice peut effectuer des modifications sur ceux-ci (y compris au sein d'un même compte) tout les abonnés au catalogue peuvent désormais les utiliser.

Pour cela il faudra cependant préciser les correspondances de M.O. (dont les identifiants internes sont spécifiques aux entités) et éventuellement de produits.

# Configurer les correspondances

Vous pouvez configurer des correspondances de produits qui seront à remplacer lors du chargement des modèles.

- En tant qu'éditeur cela permet de guider vos utilisateurs si vous n'imposez pas de référence spécifique.
  Par exemple si vous utilisez dans vos forfaits de l'huile mais n'imposez pas le choix de la marque, vous pouvez créer un produit d'huile générique au litre dans le catalogue, l'utiliser dans vos forfaits puis configurer un remplacement depuis les correspondances catalogue.
  Ce remplacement sera automatiquement proposé (et non complété) à vos utilisateurs lors de leur configuration.

![Editor replacement configuration](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/editor-replacement.webp?w=100%)

- En tant qu'utilisateur vous pouvez configurer vos correspondances. Cela vous permet:
  - de remplacer les références génériques que l'éditeur aurait spécifié.
  - de configurer d'autres remplacements à votre guise.

![Consumer replacement configuration](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/consumer-replacement.webp?w=100%)

Pour éditer une valeur cliquez sur le bouton d'édition puis remplissez les valeurs dans le champ qui s'affiche:

![Replacement edit](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/add-replacement.webp?w=368px)

Très important, pensez également à configurer le remplacement de la M.O. car les identifiants ne correspondent pas.

||| Attention n'oubliez pas de sauver! Sur cet écran il n'y a pas de sauvegarde automatique des changements.

yuzSection Général

# Améliorations

## Liste des contacts

La liste des contacts est devenue plus compacte pour une meilleure utilisabilité:

- Le pays de l'addresse n'est plus affichée sur cet écran. L'information est en général inutile et peut-être déduite du contexte.
- Seule une addresse, deux numéros de téléphonne, deux emails et deux entités chez qui le contact est client sont désormais affichés pour éviter que cela nuise à la lisibilité globale de la liste.
  Dans le cas ou certaines de ces données sont cachées vous pouvez visualiser des points de suspension "...". Passez alors votre souris sur la colonne en question pour afficher les informations masquées.

![Contact list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/contact-list.webp?w=100%)

## Listes

Le composant de tableau de yuzer évolue et va petit à petit remplacer l'existant sur de nombreux écrans.

- Dans le cas de liste 'drill-down' (en analytique ou dans les inventaires par exemple) les colonnes sur lesquelles les données sont grouppés apparaissent désormais clairement.
- Il est désormais plus simple d'ajouter une colonne sur les listes équipées du nouveau composant.
  Positionnez vous sur la colonne suite à laquelle vous désirez placer la nouvelle colonne, déplacez votre cuseur sur la limite droite de celle-ci jusqu'à ce qu'un bouton avec un icone d'oeil apparaisse.
  Vous pouvez alors sélectionner une colonne à ajouter, ou supprimer la colonne actuelle de l'affichage.

| A noter: En analytique, cela permet de modifier la visualisation immédiate mais n'impacte pas la configuration du tableau. De même sur les vues d'inventaire ou les changement de colonnes ne sont pas aujourd'hui sauvegardés.

Ce qui est visible aujourd'hui n'est qu'une partie des évolutions sur ce composant qui permettra à terme de nouvelles possibilités d'affichages dans YUZER.

## Divers

- Nombreuses mises à jour techniques sur cette version pour garantir une sécurité et performance optimale ainsi que préparer les évolutions à venir.

Comme toujours n'hésitez pas à exprimer auprès de nos équipes support, en toute courtoisie
