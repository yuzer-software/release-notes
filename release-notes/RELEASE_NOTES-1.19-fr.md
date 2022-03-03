# Mars 2022 - Version 1.19.0

# Comptabilité des cessions

La comptabilité des cessions a été revue totalement afin de pouvoir spécifier

- Un journal de cession
- La définition de comptes de contreparties souple et non plus un compte client affecté à la société.

## Configuration du journal de cession

Vous pouvez aller configurer le journal de cession dans l'onglet _Paramètres de comptabilité_ de la configuration comptable.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/accountancy-settings-cession-journal.png" width="900"/>

## Configuration des comptes de contreparties des cessions

Votre configuration du mapping de cession doit être mise à jour afin de définir pour chaque règle la contrepartie à ventiler.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/cession-mapping-config.png" width="900"/>

# Stock

## Export

Les colonnes _Marque_ et _Fournisseur_ sont disponibles à l'export de stock.

# C'est corrigé

- Le nom du fourniseur n'était pas affiché sur les dossiers de produits identifiés (vélo, etc.)
- L'identifiant du produit identifié n'était pas affiché sur l'entête du dossier juste après l'avoir saisie via le bouton _Réceptionner_ pour passer de l'état _Commandé_ à _Neuf_.
- La mise à jour des prix est maintenant fonctionnelle pour un modèle de panier.
- Les informations du véhicule du panier sont maintenant correctement mis à jour lorsqu'on l'associe depuis le bouton _Vendre_ d'un dossier.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/fix-vehicle-basket-line-refresh.gif" width="800"/>
- Sur un panier de vente véhicule, le formulaire d'ajout rapide garde maintenant le focus du dernier groupe sélectionné quand on revient sur le groupe de _Préparation et ventes additionnelles_.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/fix-basker-quick-add.gif" width="800"/>
- Il est possible de supprimer les inventaires _en cours d'ouverture_ 24h après leur création : un inventaire peut arriver dans cet état lorsque l'initialization de l'inventaire s'est mal passée.
