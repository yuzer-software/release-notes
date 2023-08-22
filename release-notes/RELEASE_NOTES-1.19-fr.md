# Mars 2022 - Version 1.19.0

# Comptabilité des cessions

La comptabilité des cessions a été revue totalement afin de pouvoir spécifier

- Un journal de cession
- La définition de comptes de contreparties souple et non plus un compte client affecté à la société.

## Configuration du journal de cession

Vous pouvez aller configurer le journal de cession dans l'onglet _Paramètres de comptabilité_ de la configuration comptable.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/accountancy-settings-cession-journal.png" width="900"/>

## Configuration des comptes de contreparties des cessions

Votre configuration du mapping de cession doit être mise à jour afin de définir pour chaque règle la contrepartie à ventiler.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/cession-mapping-config.png" width="900"/>

<div class="alert alert-danger">
Ces configurations sont nécessaires afin que vos cessions passent en comptabilité et nous vous invitons à effectuer celles-ci au plus vite.
</div>

# Recherche des clients

De nouveaux filtres ont été ajoutés sur la recherche de client et vous permettent de trouver les clients à l'aide de leur cycle de prospection ou par date de la dernière vente réalisée.

## Recherche par cycle de prospection du contact

Depuis une fiche contact, vous pouvez éditer le cycle de prospection d'un contact:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/contact-edit-state.png" width="480"/>

- **Client à contacter**: Ce statut permet d'indiquer un contact intéressé par une vente mais dont la qualification et proposition commerciale n'a pas été effectuée ou finalisée.
- **Proposition effectuée**: Une proposition commerciale a été effectuée et il n’y a pas eu de bon de commande ou facture depuis.
- **Vente effectuée**: Un bon de commande ou une facture ont été édités pour le contact.
- **Annulé**: Une proposition commerciale a expirée.

Les états sont mis à jour automatiquement par Yuzer à l'exception de l'état _Client à contacter_. Vous pouvez les mettre à jour manuellement quoi qu'il arrive.

Depuis la liste des clients, un nouveau filtre vous permet de rechercher les contacts à l'aide de ces états:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/contact-state-filter.png" width="360"/>

## Recherche par date de dernière vente

Lorsqu'une facture est éditée Yuzer conserve la date de la dernière vente en fonction de son type. Vous pouvez alors utiliser cette information afin de filtrer les clients par date de dernière vente.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/contact-sale-date-filter.png" width="360"/>

Des raccourcis rapide vous permettent de définir des périodes rapidement, vous pouvez également définir votre propre période manuellement à l'aide du bouton calendrier.

<div class="alert alert-info">
Les ventes de vélo, moto-marines et autres produits identifiés ne sont pas encore proposées à la recherche.
L'implémentation de cette évolution est en cours mais non-finalisés et sera disponible sur la prochaine version.
</div>

<div class="alert alert-warning">
Attention les filtres sont actuellement appliqués sur l'ensemble des entités du groupe. Ainsi si une vente a été faite pour le contact C dans l'entité A et qu'un employé de l'entité B recherche par date de dernière vente il verra le contact C apparaitre même si celui-ci n'a pas effectué d'achat dans l'entité B.

Ce point sera amélioré dans une prochaine version vous permettant de restreindre de manière optionnelle le filtre à l'entité de l'utilisateur.

</div>

# Visibilité des balances

Vous pouvez désormais configurer la visibilité des balances client entre plusieurs entités afin de partager une vision commune au sein d'un sous-ensemble

- d'entités logiques (même société mais structurée logiquement et non administrativement en sous-gestion)
- de succusalles / établissement (même SIRET mais SIREN différents)

Cette configuration est définie dans la partie _Administration / Configuration commerciale_

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/shared-balance-config.png" width="800"/>

<div class="alert alert-info">
Seule la vision est aujourd'hui partagée. L'utilisation d'un crédit disponible dans une autre entité n'est pas aujourd'hui possible.
Pour cette raison le montant disponible à l'utilisation en crédit depuis un panier client peut ne pas être égal à celui affiché sur la fiche du client dans le cas ou vous choisissez de définir une telle configuration.

Le transfert de crédit d'une entité à une autre sera disponible dans la prochaine version et automatiquement activé en cas de partage de visibilité.
Celui-ci sera effectué en direct sans opérations comptables exportées étant donné que la fonction de partage n'est possible que pour une société unique.

</div>

## Exposition d'API externe

Vous pouvez désormais exposer vos informations de facturations à des fins de statistiques ou commerciales pour un usage interne ou vers un exploitant externe tel que GarageScore.
Comme pour l'exposition des stocks véhicules, il faut pour cela créer une clé d'API dans le menu _Adminitration_.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/api-key-invoice-customer.png" height="400" />

Nous avons 2 types d'expositions de ressources disponible:

- _Factures contenant des données personnelles sensibles du client_: Toutes les factures seront exportées, que le client ait accepté ou non de recevoir de la publicité.
- _Factures uniquement des clients acceptant la publicité_: Seules les factures des clients ayant accepté de recevoir de la publicité seront exportées. C'est à dire que le champs _Autoriser la publicité_ a la valeur _Oui_ sur la fiche cliente.

<div class="alert alert-warning">
Attention, vous êtes responsable de la gestion et de la divulgation des secrets permettant l’accès à ce _endpoint_. Des informations personnelle de vos clients telles que leur noms, prénoms, numéros de téléphone, adresses et emails sont accessibles à travers ce _endpoint_ si vous l’activez.
La responsabilité de Yuzer, de même que lors d’un export de contacts en fichier, ne saurait être engagée en cas de non respect du RGPD.
Vous êtes responsable à ce titre de prévenir vos clients d’un éventuel partage de ses données à des tiers.
</div>

# Améliorations diverses

- Les colonnes _Marque_ et _Fournisseur_ sont disponibles à l'export de stock.

# C'est corrigé

- Le nom du fournisseur n'était pas affiché sur les dossiers de produits identifiés (vélo, etc.)
- L'identifiant du produit identifié n'était pas affiché sur l'entête du dossier juste après l'avoir saisie via le bouton _Réceptionner_ pour passer de l'état _Commandé_ à _Neuf_.
- La mise à jour des prix est maintenant fonctionnelle pour un modèle de panier.
- Les informations du véhicule du panier sont maintenant correctement mis à jour lorsqu'on l'associe depuis le bouton _Vendre_ d'un dossier.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/fix-vehicle-basket-line-refresh.gif" width="800"/>

- Sur un panier de vente véhicule, le formulaire d'ajout rapide garde maintenant le focus du dernier groupe sélectionné quand on revient sur le groupe de _Préparation et ventes additionnelles_.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/fix-basker-quick-add.gif" width="800"/>

- Il est possible de supprimer les inventaires _en cours d'ouverture_ 24h après leur création : un inventaire peut arriver dans cet état lorsque l'initialisation de l'inventaire s'est mal passée.
- La mise à jour du statut de paiement de panier n'était pas correctement effectuée lorsque la facture était éditée depuis la boite de dialogue de paiement.

## Comptabilité des achats de véhicule avec TVA

Les versions précédentes de Yuzer effectuaient la comptabilité d'un achat de véhicule avec TVA en prenant en compte que le montant HT de celui-ci de manière identique à un achat sans TVA (cas d'un achat à particulier).
Ce point a été résolu et Yuzer ventile désormais la TVA déductible à l'achat sur base du compte configuré dans vos paramètres de comptabilité.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.19.0/tradein-accountancy.png" width="800"/>
