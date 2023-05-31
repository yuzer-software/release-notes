# Juin 2023 - Version 2.12.1

<div class="alert alert-info">La version 2.12.0 est disponible dès le 30/05/2023 en démo. La version 2.12.1 sera disponible le 01/06/2023</div>

## Gestion des cessions fournisseurs dans un dossier véhicule

<div class="alert alert-warning">Changement impactant</div>

Dans les versions précédentes, les cessions de garantie fournisseurs sur un dossier véhicule impactaient les coûts opérationels au même titre que les autres cessions. Depuis la version 2.12.1 ceci n'est plus le cas.

Par ailleurs nous avons rendu plus simple la création d'une cession de garantie fourninisseur depuis le dossier du véhicule en ajoutant le choix aux cessions de préparation ou maintenance.

<div class="text-center" style="text-align: 'center';">
  <img width="850" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.11.0/new_file_cessions.webp"/>
</div>

## Transfers de produits identifiés

Il est désormais possible d'effectuer un transfer d'un produit identifié. Celui-ci se fait à travers un panier intra-groupe et suit le même cheminement qu'un transfer de produit.

La réception dans ce contexte précis permet d'effectuer la réception du produit identifié et de définir quels sont les produits effectivement montés sur le produit identifié.

## Corrections et Améliorations

- Si vous laissez votre curseur de souris pendant une demi seconde sur la référence dans une ligne de panier, celle-ci sera affichée dans une info-bulle. Cela permet de visualiser de longues références. Souvenez vous que vous pouvez copier la référence par un simple click.

<img width="256" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.11.0/ref_tooltip.webp"/>

# Juin 2023 - Version 2.12.0

## Analytiques

Nous avons amélioré le temps de chargement de l'analytique en améliorant la gestion du cache local. A noter que les données journalière ne seront mise à jour que dans un interval de 30 minutes.

Il est désormais possible de modifier les entités, la période d'analyse, et même les groupes des sources de données d'un tableau de bord sans avoir à modifier sa configuration. Ces modifications sont également plus rapides que dans les versions précédentent qui forcaient un rechargement intégral du tableau de bord.

La sélection des assignés (mécaniciens, vendeurs) dans le cadre de tableaux de bord multi-entités est désormais correctement supporté.

Les liens pour accéder au contact ou au dossier/fiche véhicule dans l'analytique sont désormais correctement fonctionnels.

## Import de produits

Il est désormais possible de fermer un import de catalogue de produits et retrouver les résultats d'executions pendant une durée d'une semaine.

Le mapping des catégories fournisseurs a été amélioré et est désormais accessible directement depuis l'import de catalogue.

## Corrections et Améliorations

- Il est désormais possible de choisir une identité visuelle sur les documents de prêt de véhicule comme sur les autres documents.
- Correction d'une erreur de traduction sur le PV HT qui s'affichait en PA HT dans les en-têtes des lignes d'un panier.
- Correction d'une erreur pouvant impacter le montant consommé et perdu sur une fiche produit.
