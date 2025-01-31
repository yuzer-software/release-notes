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

La liste des contacts est devenue plus compacte pour une meilleure utilisabilité :

- Le pays de l'adresse n'est plus affichée sur cet écran. L'information est en général inutile et peut-être déduite du contexte.
- Seule une adresse, deux numéros de téléphone, deux emails et deux entités chez qui le contact est client sont désormais affichés pour éviter que cela nuise à la lisibilité globale de la liste.
  Dans le cas ou certaines de ces données sont cachées vous pouvez visualiser des points de suspension "...". Passez alors votre souris sur la colonne en question pour afficher les informations masquées.

![Contact list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/contact-list.webp?w=100%)

## Listes

Le composant de tableau de Yuzer évolue et va petit à petit remplacer l'existant sur de nombreux écrans.

- Dans le cas de liste 'drill-down' (en analytique ou dans les inventaires par exemple) les colonnes sur lesquelles les données sont groupés apparaissent désormais clairement.
- Il est désormais plus simple d'ajouter une colonne sur les listes équipées du nouveau composant.
  Positionnez vous sur la colonne suite à laquelle vous désirez placer la nouvelle colonne, déplacez votre curseur sur la limite droite de celle-ci jusqu'à ce qu'un bouton avec un icône d'oeil apparaisse.
  Vous pouvez alors sélectionner une colonne à ajouter, ou supprimer la colonne actuelle de l'affichage.

| A noter: En analytique, cela permet de modifier la visualisation immédiate mais n'impacte pas la configuration du tableau. De même sur les vues d'inventaire ou les changement de colonnes ne sont pas aujourd'hui sauvegardés.

Ce qui est visible aujourd'hui n'est qu'une partie des évolutions sur ce composant qui permettra à terme de nouvelles possibilités d'affichages dans YUZER.

## Divers

- Nombreuses mises à jour techniques sur cette version pour garantir une sécurité et performance optimale ainsi que préparer les évolutions à venir.

Comme toujours n'hésitez pas à exprimer auprès de nos équipes support, en toute courtoisie

yuzSection App mobile

## Tâches

yuzLeft

- Sur l'écran d'accueil, votre _tâche actuelle_ est mise à jour quand vous _revenez_ sur l'écran d'accueil
- (1) Sur le détail d'une tâche avec produit identifié, deux identifiants sont désormais affichés, de manière plus visible qu'auparavant
- Meilleur rafraichissement du statut des tâches filles
- Photo expertises:
  - (2) Cliquer sur l'icône "appareil photo" lorsqu'aucune photo expertise n'est liée au panier vous propose directement d'en créer une (plus besoin de passer par le menu "photo expertises"). Si l'expertise existait déjà, le comportement est inchangé: vous naviguez vers l'expertise existante.
  - (3) Amélioration visuelle du menu
  - Correction d'un bug bloquant les actions si on annulait la création d'une photo expertise
  - Correction d'un bug empêchant de créer plusieurs photos expertises pour le même IDP

yuzRight

1. ![Set catalog priority](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/mobile-task-detail-head.webp?w=300px)

2. ![Set catalog priority](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/mobile-task-defail-actions.webp?w=300px)

3. ![Set catalog priority](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/mobile-photo-expertise.webp?w=300px)

yuzEnd

## Inventaires

yuzLeft

- L'édition de la quantité a été améliorée (ci-contre):
  - la quantité déjà comptée est affichée comme "décompte précédent"
  - la nouvelle quantité est désormais toujours vide (ce qui permet de la rentrer directement, sans effacer la quantité)
  - utiliser les boutons `-` ou `+` partira du décompte précédent si aucune quantité n'a été rentrée (comportement inchangé)

- Lorsqu'un _emplacement_ est scanné, un son (différent de celui pour les produits) est joué

yuzRight

![Set catalog priority](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/mobile-edit-quantity.webp?w=300px)

yuzEnd


## Paniers

- Le mode de comptage des produits persiste (avec le scanner ou à la main)
- Amélioration des sons et correction de leur occurrences
- Corrections diverses

## Réceptions

- Correction de l'affichage de la liste des réceptions d'un début d'année
- Seules les réceptions de l'entrepôt courant sont affichées

## Améliorations et corrections diverses

yuzLeft

- Lorsqu'un produit est connu dans plusieurs catalogues, les produits sont ordonnés par la priorité donnée au catalogue. Pour rappel, nous pouvez définir la priorité d'un catalogue depuis l'édition du catalogue. Plus la priorité est petite, plus le catalogue est prioritaire.

yuzRight

![Set catalog priority](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.11.0/set-catalog-priority.webp?w=800px)

yuzEnd

- Amélioration mineure de l'affichage des propriétés des produits identifiés
- Un inventaire _En cours d'ouverture_ ne peut plus être ouvert, il faut attendre qu'il soit _Ouvert_
- Lorsque la connexion se fait par OTP, le téléphone se souvient des informations de connexion
- Correction d'affichage de la sélection manuelle d'emplacements
- Vérifications de l'entrepôt: si l'entrepôt d'une réception ou d'un inventaire auquel vous cherchez à accéder n'est pas l'entrepôt courant (par exemple navigation depuis les derniers travaux), l'application vous demandera si vous voulez annuler ou changer d'entrepôt.
