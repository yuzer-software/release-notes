# Juin 2023 - Version 2.12.1

<div class="alert alert-info">La version 2.12.0 est disponible dès le 30/05/2023 en démo. La version 2.12.1 sera disponible le 01/06/2023</div>

## Gestion des cessions fournisseurs dans un dossier véhicule

<div class="alert alert-warning">Changement impactant</div>

Dans les versions précédentes, les cessions de garantie fournisseurs sur un dossier véhicule impactaient les coûts opérationnels au même titre que les autres cessions. Depuis la version 2.12.1 ceci n'est plus le cas.

Par ailleurs, nous avons rendu plus simple la création d'une cession de garantie fournisseur depuis le dossier du véhicule en ajoutant le choix aux cessions de préparation ou maintenance.

<div class="text-center" style="text-align: 'center';">
  <img width="850" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.12.0/new_file_cessions.webp"/>
</div>

## Transferts de produits identifiés

Il est désormais possible d'effectuer un transfert d'un produit identifié. Celui-ci se fait à travers un panier intra-groupe et suit le même cheminement qu'un transfert de produit.

La réception dans ce contexte précis permet d'effectuer la réception du produit identifié et de définir quels sont les produits effectivement montés sur le produit identifié.

### Transfert intra-entité (changement d'entrepôt)

Le transfert d'un produit identifié au sein de la même entité n'est pas possible par le flux des transferts. Il n'y a donc pas de changement sur ce point : il faut et il suffit de passer par la fiche du dossier véhicule et de changer l'entrepôt comme ci-dessous.

<div class="text-center" style="text-align: 'center';">
  <img width="220" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.12.0/0-change-idp-warehouse.webp"/>
</div>

### Création et édition du panier

Le transfert de produit identifié suit le même flux que celui d'une vente de produit identifié.

<div class="text-center" style="text-align: 'center';">
  <img width="400" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.12.0/1-new_idp_transfer.webp"/>
</div>

Jusqu'à l'édition des documents, il n'y a aucune différence d'avec une vente client. En particulier, les produits "montés sur le produit identifié" seront transférés en même temps que le véhicule, exactement comme lors d'une vente classique (un groupe de cession peut être fait pour démonter les produits à ne pas transférer, etc.).

### Transfert du panier

Comme pour les transferts de pièces, il vous faudra éditer un bon de livraison ou une facture (réservé aux transferts inter-société). Pour rappel :

- _Livrer_ crée un transfert sans l'envoyer (vous devrez le faire depuis la page des transferts),
- _Livrer en envoyer le transfert_ crée un transfert et l'envoie directement.

<div class="text-center" style="text-align: 'center';">
  <img width="250" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.12.0/3-deliver-with-transfer.webp"/>
</div>

**Note** : Comme pour les transferts de pièces, si les pièces du panier proviennent de plusieurs entrepôts différents, un transfert par entrepôt sera créé. Un seul panier peut donc se retrouver dans 2 transferts différents. Le produit identifié et les pièces montées dessus proviennent de l'entrepôt dans lequel le produit identifié est entreposé.

### Statut du dossier véhicule après le Transfert

Dans le cas d'un transfert entre deux sociétés distinctes (maisons mères ou filiales), il y a facturation : le dossier est traité comme une vente standard, il aura donc les statuts **Délivré** ou **Facturé et soldé** selon l'état du panier.

Dans le cadre d'un transfert intra-société (même entité logique ou succursale), il n'y a pas de facturation : le dossier est **annulé** lors de la génération du bon de livraison avec le message _Transfert intra-société vers xxxxx_.

### Retour

Si vous retournez le transfert, une réception est créée. Le dossier du produit identifié apparaît sur une ligne particulière. Il n'est pas possible de le changer.

À la clôture de la réception, le dossier est réouvert et le stock est rétablit. Vous devrez encore annuler les documents au niveau de panier pour faire correspondre les documents et le stock.

### Réception du produit identifié

Lorsque le destinataire reçoit le transfert de produit identifié, une réception est créée avec une ligne particulière pour le produit identifié et une ligne pour chaque produit "monté sur" ce produit.

Deux comportements sont possible pour la ligne de produit identifié.

- Par défaut, la ligne n'est liée à aucun dossier ouvert et un nouveau dossier sera créé à la clôture de la réception.
- En éditant l'entrée en stock, vous pouvez choisir un dossier ouvert déjà existant référençant le même produit identifié (attention, pas le même _modèle_, mais exactement le même _produit identifié_).

À la clôture, le nouveau dossier ou le dossier sélectionné sera mis à jour ainsi :

- les coûts et bonus (dont paniers de cession) transférés sont recopiés dans le nouveau dossier de l'entité cible en tant que coût opérationnels.
- les produits "montés sur" le produit identifié seront effectivement montés dessus.

### Réception des autres produits et produits montés

Sur les lignes de produits, un nouvel emplacement est disponible : celui du produit identifié. Au moment de la création de la réception, tout correspond à l'état du panier. À la clôture de la réception, les produits "montés sur" un produit identifié seront déplacés dans le stock correspondant à ce produit identifié.

Toutefois, il est possible de changer à loisir l'emplacement de ces produits au cas où l'expéditeur aurait fait une erreur (vous vous apercevez par exemple qu'un produit n'est pas monté sur le produit identifié).

### Facture d'achat

Lors d'un transfert intra-société, il n'y a pas de facturation et le statut comptable du transfert est considéré comme validé (aucun changement par rapport aux transferts de pièces).

Lors d'un transfert inter-société, la facture d'achat est générée à partir de la facture émise (lors de l'édition du panier) par Yuzer. La nouveauté principale sur les factures d'achat est qu'une ligne de facture peut maintenant référencer à la fois un dossier _et_ une ligne de réception.

## Corrections et Améliorations

- Si vous laissez votre curseur de souris pendant une demi seconde sur la référence dans une ligne de panier, celle-ci sera affichée dans une info-bulle. Cela permet de visualiser de longues références. Souvenez vous que vous pouvez copier la référence par un simple click.

<img width="256" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.12.0/ref_tooltip.webp"/>

# Juin 2023 - Version 2.12.0

## Analytiques

Nous avons amélioré le temps de chargement de l'analytique en améliorant la gestion du cache local. A noter que les données journalière ne seront mise à jour que dans un intervalle de 30 minutes.

Il est désormais possible de modifier les entités, la période d'analyse, et même les groupes des sources de données d'un tableau de bord sans avoir à modifier sa configuration. Ces modifications sont également plus rapides que dans les versions précédentes qui forçaient un rechargement intégral du tableau de bord.

La sélection des assignés (mécaniciens, vendeurs) dans le cadre de tableaux de bord multi-entités est désormais correctement supporté.

Les liens pour accéder au contact ou au dossier/fiche véhicule dans l'analytique sont désormais correctement fonctionnels.

## Import de produits

Il est désormais possible de fermer un import de catalogue de produits et retrouver les résultats d'exécutions pendant une durée d'une semaine.

Le mapping des catégories fournisseurs a été amélioré et est désormais accessible directement depuis l'import de catalogue.

## Corrections et Améliorations

- Il est désormais possible de choisir une identité visuelle sur les documents de prêt de véhicule comme sur les autres documents.
- Correction d'une erreur de traduction sur le PV HT qui s'affichait en PA HT dans les en-têtes des lignes d'un panier.
- Correction d'une erreur pouvant impacter le montant consommé et perdu sur une fiche produit.
