# Septembre 2021 - Version 1.10.0

- Nous avons amélioré la fonction de filtrage des produits en stock. Cela devrait vous fournir de meilleurs résultats.

# Tableau de bord

La configuration du _widget_ "Chiffre d'affaires" a été rendue plus évidente et dispose d'une nouvelle fonctionnalité: filter ou grouper par type de panier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/turnover.png" height="320"/>

# Calendrier

Vous pouvez désormais afficher plusieurs espaces de travail sur le même calendrier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/multiple-workspaces.png" height="140"/>

Lorsque plusieurs espaces de travails sont affichés:

- La charge est affichée comme inconnue étant donnée qu'elle ne peut prendre en compte que les tâches atelier et n'aurait pas de sens avec d'autres espaces de travail.
- Les couleurs des tâches sont chargées depuis la configuration "espaces de travail multiples".

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

L'option _Obligation d'estimation des prix de vente et de réparation lors d'une reprise_ vous permet de définir si, au moment de la reprise d'un véhicule, l'estimation du prix de revente ainsi que l'estimation du coût des réparations est obligatoire et devra bloquer l'édition des documents et donc la finalisation de la reprise.

Si l'on coche "Non", les valeurs pourront être renseignées, mais ne bloqueront pas la finalisation de la reprise.

Vous pouvez également définir la marge recommandée qui permet d'afficher un prix de reprise recommandé basé sur l'estimation du prix de revente et des réparations.

# C'est corrigé

- Lors de l'édition du prix d'achat un véhicule sur une machine windows en Français, entrer un "." plutôt qu'une virgule causait un comportement erroné (complétion curieuse des décimales).
- Lorsque vous passez en comptabilité une cloture de caisse sans évènement et que votre configuration requiers une validation manuelle le statut de comptabilité restait en _Traité_ et non _Validé_ (il ne pouvait l'être dans l'interface).
