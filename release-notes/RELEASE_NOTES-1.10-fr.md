# Septembre 2021 - Version 1.10.0

- Nous avons amélioré la fonction de filtrage des produits en stock. Cela devrait vous fournir de meilleurs résultats.

# Calendrier

Vous pouvez désormais afficher plusieurs espaces de travail sur le même calendrier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/multiple-workspaces.png" height="140"/>

Lorsque plusieurs espaces de travails sont affichés:

- La charge est affichée comme inconnue étant donnée qu'elle ne peut prendre en compte que les tâches atelier et n'aurait pas de sens avec d'autres espaces de travail.
- Les couleurs des tâches sont chargées depuis la configuration "espaces de travail multiples".

# Configuration commerciale

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

### Obligation d'estimation des prix de vente et de réparation lors d'une reprise.

Cette nouvelle option permet de définir si, au moment de la reprise d'un véhicule, l'estimation du prix de revente ainsi que l'estimation du coût des réparations est obligatoire et devra bloquer l'édition des documents et donc la finalisation de la reprise.
Si l'on coche "Non", les valeurs pourront être renseignées, mais ne bloqueront pas la finalisation de la reprise.

# C'est corrigé

- Lors de l'édition du prix d'achat un véhicule sur une machine windows en Français, entrer un "." plutôt qu'une virgule causait un comportement erroné (complétion curieuse des décimales).
