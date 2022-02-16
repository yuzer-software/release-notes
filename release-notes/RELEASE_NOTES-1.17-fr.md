# Février 2022 - Version 1.17.3

## Améliorations diverses

- Vous pouvez désormais changer la taille du texte et la police dans les commentaires et CGV.

## Améliorations sur comptabilité

### Comptabilité de la TVA

Il est désormais possible de définir un compte différent pour chaque taux de TVA collecté. Nous avons effectué une migration des données qui utilise le compte que vous aviez défini pour chaque taux. Pensez à modifier cette configuration si vous souhaitez modifier ce comportement.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/vat-accounts.png" height="180"/>

### Aggrégation

Yuzer aujourd'hui expose en comptabilité le détail de la facturation en écrivant pour chaque ligne de la facture le détail. Certains d'entre vous ne désirent pas de détail en comptabilité mais souhaitaient voir s'aggréger les différents enregistrements sur les ventes et achats.

C'est désormais possible en choisissant l'option ci-dessous dans vos paramètres de comptabilité.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/accountancy-aggregation.png" height="180"/>

Attention cette option n'impactera pas les enregistrement existant pour des raisons évidentes de légalité et une fois activée les enregistrements passés seront agrégés et ne pourront être détaillés à nouveau.

## Disponibilité du stock dans les autres sociétés

Il est désormais possible de consulter la disponibilité du stock dans les autres sociétés du groupe en cliquant sur le petit icone ajouté sur les informations stock. Ceci est disponible depuis l'ensemble des vues proposant cette visualisation (panier, liste des produits, détail produit).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/stock-availability-btn.png" height="90"/>

S'affiche alors la liste des autres entités du groupe ayant le produit en stock ainsi que le nombre en stock (avec éventuellement les réservations liées).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/stock-availability-modal.png" height="90"/>

## Gestion des produits identifiés commandés (vélos, moto-marines etc.)

La gestion de l'évolution des statuts de commandes d'un produit identifié a été complétée afin de bien pouvoir passer un dossier de _A commander_ en _Commandé_ puis de _Commandé_ en _Neuf_

### Mise en commande d'un dossier _A commander_

Pour celà il suffit désormais d'utiliser le bouton _Commander_

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/mark-order.png" height="180"/>

Puis de compléter les informations de commande

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/mark-order-modal.png" height="260"/>

### Réception du dossier _Commandé_

Pour celà il suffit désormais d'utiliser le bouton _Réceptionner_

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/mark-new.png" height="180"/>

Puis de compléter les informations de réception et d'ajouter l'(es) identifiant(s) du produit.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.17.0/mark-new-modal.png" height="260"/>

## C'est corrigé
