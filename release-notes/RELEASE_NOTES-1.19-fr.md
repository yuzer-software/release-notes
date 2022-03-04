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

<div class="alert alert-danger">
Ces configurations sont nécessaires afin que vos cessions passent en comptabilité et nous vous invitons à effectuer celles-ci au plus vite.
</div>

# Recherche des clients

De nouveaux filtres ont été ajoutés sur la recherche de client et vous permettent de trouver les clients à l'aide de leur cycle de prospection ou par date de la dernière vente réalisée.

## Recherche par cycle de prospection du contact

Depuis une fiche contact, vous pouvez éditer le cycle de prospection d'un contact:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/contact-edit-state.png" width="480"/>

- **Client à contacter**: Ce statut permet d'indiquer un contact intéressé par une vente mais dont la qualification et proposition commerciale n'a pas été effectuée ou finalisée.
- **Proposition effectuée**: Une proposition commerciale a été effectuée et il n’y a pas eu de bon de commande ou facture depuis.
- **Vente effectuée**: Un bon de commande ou une facture ont été édités pour le contact.
- **Annulé**: Une proposition commerciale a expirée.

Les états sont mis à jour automatiquement par Yuzer à l'exception de l'état _Client à contacter_. Vous pouvez les mettre à jour manuellement quoi qu'il arrive.

Depuis la liste des clients, un nouveau filtre vous permet de rechercher les contacts à l'aide de ces états:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/contact-state-filter.png" width="360"/>

## Recherche par date de dernière vente

Lorsqu'une facture est éditée yuzer conserve la date de la dernière vente en fonction de son type. Vous pouvez alors utiliser cette information afin de filtrer les clients par date de dernière vente.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/contact-sale-date-filter.png" width="360"/>

Des racourcis rapide vous permettent de définir des périodes rapidement, vous pouvez également définir votre propre période manuellement à l'aide du bouton calendrier.

<div class="alert alert-warning">
Les ventes de vélo, moto-marines et autres produits identifiés ne sont pas encore proposées à la recherche.
L'implémentation de cette évolution est en cours mais non-finalisées et sera disponible sur la prochaine version.
</div>

# Améliorations diverses

- Les colonnes _Marque_ et _Fournisseur_ sont disponibles à l'export de stock.

# C'est corrigé

- Le nom du fourniseur n'était pas affiché sur les dossiers de produits identifiés (vélo, etc.)
- L'identifiant du produit identifié n'était pas affiché sur l'entête du dossier juste après l'avoir saisie via le bouton _Réceptionner_ pour passer de l'état _Commandé_ à _Neuf_.
- La mise à jour des prix est maintenant fonctionnelle pour un modèle de panier.
- Les informations du véhicule du panier sont maintenant correctement mis à jour lorsqu'on l'associe depuis le bouton _Vendre_ d'un dossier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/fix-vehicle-basket-line-refresh.gif" width="800"/>

- Sur un panier de vente véhicule, le formulaire d'ajout rapide garde maintenant le focus du dernier groupe sélectionné quand on revient sur le groupe de _Préparation et ventes additionnelles_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.19.0/fix-basker-quick-add.gif" width="800"/>

- Il est possible de supprimer les inventaires _en cours d'ouverture_ 24h après leur création : un inventaire peut arriver dans cet état lorsque l'initialization de l'inventaire s'est mal passée.
