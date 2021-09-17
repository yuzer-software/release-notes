# Septembre 2021 - Version 1.10.0

- Nous avons amélioré la fonction de filtrage des produits en stock. Cela devrait vous fournir de meilleurs résultats.

# Tableau de bord

La configuration du _widget_ "Chiffre d'affaires" a été rendue plus claire et dispose d'une nouvelle fonctionnalité: filter ou grouper par type de panier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/turnover.png" height="320"/>

Un nouveau _widget_ "Main-d'œuvre" a été ajouté et vous permet d'afficher le temps ou le chiffre d'affaire **facturé** de l'atelier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/workforce-widget.png" height="320"/>

# Calendrier

Vous pouvez désormais afficher plusieurs espaces de travail sur le même calendrier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/multiple-workspaces.png" height="140"/>

Lorsque plusieurs espaces de travails sont affichés:

- La charge est affichée comme inconnue étant donnée qu'elle ne peut prendre en compte que les tâches atelier et n'aurait pas de sens avec d'autres espaces de travail.
- Les couleurs des tâches sont chargées depuis la configuration "espaces de travail multiples".

# Création de tâches pour valider les cessions en cours

Lorsqu'un panier est facturé alors que des cessions (préparations / réparations) n'ont pas été terminées, une tâche est créée automatiquement dans le calendrier de gestion commerciale afin de rappeler la nécessité de clôturer celles-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/incomplete-cession-warn.png" height="140"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/incomplete-cession-create.png" height="140"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/incomplete-cession-task-cal" height="140"/>

# Estimation des reprises.

Lorsque vous effectuez une reprise vous pouvez désormais indiquer les prix estimés de revente et coûts de réparation estimés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/trade-in-estimate.png"/>

Ces champs sont optionnels par défaut mais peuvent être rendus obligatoire par l'administrateur dans la section _Configuration commerciale_ (voir ci-dessous).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/trade-in-estimate-mandatory.png"/>

Si une marge recommandée a été configurée dans les paramètres de gestion commerciale (voir ci-dessous) Yuzer affiche aussi une valeur de prix d'achat recommandée basée sur les prix de vente et coûts de réparations estimés ainsi que sur la marge recommandée.

# Export du stock

Des options ont été ajoutées à l'export de stock afin de pouvoir exporter le stock complet et non uniquement celui de l'entrepôt selectionné.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/stock-export.png"/>

Vous pouvez également chosir d'exporter l'intégralité du stock ou d'ignorer les valeurs positives ou négatives.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/stock-export-opts.png"/>

# Gestion commerciale

Un nouveau menu "Gestion commerciale" est disponible dans l'onglet "administration".
L'on pourra y retrouver les menus suivants:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/commercial_config.png"/>

La configuration des messages et CGV ainsi que la configuration des prêts de véhicules y ont donc été déplacés.

## Configuration commerciale

Un nouveau menu permet d'accéder à de nouvelles options de configuration.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/commercial_config_tab.png"/>

### Durée de validité par défaut des documents

Ce nouveau paramètre permet de définir une durée de validité par défaut des documents, en jours.

Les propositions commerciales ont une échéance. La date de fin de validité peut être choisie lors de chaque édition.
Choisir une valeur par défaut permet donc de pré-remplir la date de fin de validité.

### Paramètres d'estimation des reprises

L'option _Obligation d'estimation des prix de vente et de réparation lors d'une reprise_ vous permet de définir si, au moment de la reprise d'un véhicule, l'estimation du prix de revente ainsi que l'estimation du coût des réparations sont obligatoires et devront empêcher l'édition du document de reprise.

Si l'on coche "Non", les valeurs pourront toujours être renseignées, mais leur absence n'empêcheront pas la reprise.

Vous pouvez également définir la "marge recommandée pour les véhicules d'occasion". Celle-ci permet d'afficher un prix de reprise recommandé, calculé à partir de l'estimation des prix de revente et des réparations.

# Programmes de fidélité

Vous pouvez maintenant gérer des programmes de fidélité dans Yuzer.

## Configuration des programmes de fidélité

Les programmes de fidélité sont définis dans le menu "Administration", à la section "Programmes de fidélité". Vous pouvez définir autant de programmes de fidélité que vous le désirez. Dans l'exemple ci-dessous, vous pouvez voir deux programmes: Yuzer Premium et Yuzer Ultimate.

- Yuzer Premium offre une réduction immédiate de 10% sur tous les vêtements et une réduction immédiate de 5% sur tous les produits Blackbird fourni par Bihr.
- Yuzer Ultimate offre une réduction immédiate de 20% sur tout hormis les services et taxes.

Actuellement, quelques limitations demeurent: il n'est pas possible d'offrir des remises sur les véhicules ni sur la catégorie "services et taxes" (légalement les taxes ne peuvent bénéficier d'aucune réduction).

Notez que la marque doit être renseignée avec exactitude (majuscule, etc). Une valeur vide signifie que le programme de fidélité s'applique à toutes les marques.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/loyalty-config.png"/>

## Souscrire à un programme de fidélité

Vous pouvez inscrire un de vos clients à un programme de fidélité depuis sa page de contact ou directement depuis le panier. Ci-dessous, une cinématique montrant comment :

- Inscrire le client à un programme de fidélité depuis un panier de vente,
- Ajouter un programme de fidélité, dont le contact est membre, au groupe de facturation (remarque: un groupe de facturation ne peut être lié qu'à un seul programme de fidélité). Nous en décrirons les effets à la section "Appliquer un programme de fidélité".
- Supprimer le programme de fidélité d'un groupe de facturation.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/loyalty-subscription.gif"/>

## Appliquer un programme de fidélité

Vous pouvez voir ci-dessous le résultat de l'application du programme "Yuzer Premium" à un groupe de facturation de trois lignes. Le nom du programme fidélité est affiché en haut du groupe de facturation et de nouvelles lignes de remise ont été ajoutées au panier.

Les remises de fidélité sont regroupées par TVA. Dans notre exemple, tous les produits ayant une TVA de 20%, nous n'avons qu'une seule ligne de remise fidélité qui somme les remises et donne une description par produit :

- BIH-0040038 n'est ni un vêtement, ni un produit Blackbird : aucune remise n'est appliquée.
- BIH-01-142 est un vêtement : la première règle du programme de fidélité s'applique, ce qui donne 10% de remise.
- BIH-1003038 n'est pas un vêtement, mais c'est un produit Blackbird fourni par Bihr : la deuxième règle du programme de fidélité s'applique, ce qui donne 5% de remise.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/loyalty-basket.png"/>

# C'est corrigé

- Lors de l'édition du prix d'achat un véhicule sur une machine windows en Français, entrer un "." plutôt qu'une virgule causait un comportement erroné (complétion curieuse des décimales).
- Lorsque vous passez en comptabilité une clôture de caisse sans évènement et que votre configuration requiert une validation manuelle le statut de comptabilité restait en _Traité_ et non _Validé_ (il ne pouvait pas l'être dans l'interface).
- Il est possible d'enregistrer des paiements négatifs (remboursement).
- Correction de problèmes de droits qui empêchaient la modification des identifiants de connexion fournisseur.
