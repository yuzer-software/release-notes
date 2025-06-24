# Juin 2025 - Version 4.1

yuzSection Arrondis de TVA

## Arrondis de TVA

||| ATTENTION, merci de bien lire cette section et de bien informer vos collaborateurs en cas de changements de paramétrage. Nous vous recommandons d'effectuer le changement en dehors des horaires d'ouverture et de valider que tous vos collaborateurs relancent bien YUZER pour éviter tout effet de bord lié à au cache.

### Contexte

Il existe plusieurs manières d'arrondir la TVA dans le cadre d'une vente.

L'arrondi de la somme ou la somme des arrondis.

YUZER fonctionne suivant la logique de somme des arrondis. Cela permet en effet de collecter la même TVA quelle que soit la manière de vendre une quantité donnée de produit.

Par exemple, prenons un produit donc le prix HT est 7,22 avec une TVA de 20%.

- Le montant de TVA sur ce produit est _1,444_, ce montant doit bien entendu être arrondi au centime ce qui donne _1,44_.
- Le prix unitaire TTC du produit est donc _8,66_

Si nous vendons une quantité de 2 le prix HT total devient _14,44_.
Suivant la stratégie de somme des arrondis nous allons calculer le PV TTC en faisant la somme des arrondis donc _8,66 \* 2_ ce qui donne _17,32_.
Si l'on utilise l'arrondi de la somme, le PV TTC est re-calculé en appliquant le taux de TVA à la somme des PV HT. Si l'on applique une TVA de 20% à _14,44_ le prix total du produit est alors _2,888_ ce qui une fois arrondi au centime donne _2,89_. Le prix TTC dans ce cas est alors _17,33_.

Comme nous l'avons dit, YUZER applique la stratégie de la somme des arrondis, mais notez qu'elle est utilisée dans YUZER de manière totale, tant au niveau d'une ligne en appliquant sa quantité, que sur la somme des lignes.

Cela garantit que la TVA collectée reste la même quelle que soit la manière dont la vente est construite. En effet, avec la stratégie ci-dessus la TVA collectée est identique dans les cas :

- Le produit est vendu dans deux factures différentes avec une quantité de 1
- Le produit est vendu dans une facture unique sous deux lignes différentes avec une quantité de 1
- Le produit est vendu dans une facture unique avec une ligne unique dont la quantité est 2

Si la stratégie de la somme des arrondis est communément appliquée, il est beaucoup plus rare qu'elle soit utilisée sur une ligne unique. Ainsi il est beaucoup plus commun de voir les différents logiciels appliquer la TVA sur le prix total HT d'une ligne puis la somme des arrondis sur l'ensemble des différentes lignes.

Cette différence de comportement peut complexifier la compréhension du traitement des arrondis par certains consommateurs peu habitués à un tel fonctionnement.

Nous avons donc introduit un nouveau paramètre permettant de modifier le comportement de YUZER au niveau d'une ligne unique.

Attention actuellement la somme des arrondis reste la stratégie utilisée pour le calcul de la TVA totale sur une facture (somme des lignes) quel que soit la stratégie à la ligne choisie.

### Modification du paramètre

Afin de modifier le paramètre rendez-vous dans vos paramètres de comptabilité :

![Lines Vat Policy](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/lines-vat-policy.webp?w=100%)

### Impacts

#### Factures établies

Les factures établies ne changent bien évidemment pas. Leur annulation est totalement consistante et utilise la même stratégie que la facture d'origine afin de garantir une annulation égale de la TVA collectée.

#### Nouvelle factures

Toutes les nouvelles factures doivent-être établies avec la stratégie configurée.

Si un groupe de facturation a été créé avec une stratégie différente, YUZER vous oblige de mettre celle-ci à jour au niveau du panier avant de pouvoir éditer de nouveaux documents.

L'erreur suivante est alors affichée avant l'édition d'un document :

![Lines Vat Policy error](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/lines-vat-policy-error.webp?w=450px)

L'opérateur doit alors appliquer le changement de stratégie au panier (seuls les groupes non-facturés sont impactés)

![Lines Vat Policy update](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/lines-vat-policy-update.webp?w=450px)

|| Dans certains cas le changement de stratégie peut impacter de quelques centimes le prix total de votre panier.

#### Affichage du panier

La position de la colonne TVA dans le panier est fonction du paramètre d'application de la TVA afin bien refléter son application.
Ainsi

- lorsque l'arrondi est appliqué sur le prix unitaire puis multiplié par la quantité la colonne TVA apparait après le prix unitaire et avant la quantité.

![Lines Vat Policy basket unit](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/lines-vat-policy-vat-unit.webp?w=450px)

- lorsque l'arrondi est appliqué sur le prix total la colonne de TVA apparait après les colonnes de quantité et remises et juste avant la colonne indiquant le prix total TTC

![Lines Vat Policy basket total](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/lines-vat-policy-vat-total.webp?w=450px)

yuzSection Remises et affichage du panier

## Remises

YUZER vous permet désormais d'appliquer une remise non sur le prix unitaire du produit (la remise était alors multipliée par la quantité) mais bien sur le prix total de la ligne.
Si cela n'a que très peu d'impacts dans le cadre de remises en pourcentages (cela peut-être le cas dans de rare cas d'arrondis) cela est particulièrement important dans le cadre de remises en montant.

Il existe désormais 6 options de remises qui se composent de deux éléments :

- Type de remise (Pourcentage du prix, Montant HT, Montant TTC)
- Prix sur lequel la remise est appliquée (Prix Unitaire, Prix Total)

Le changement de type de remise s'effectue depuis le panier en cliquant sur les symboles permettant d'identifier le type de remise :

![Discount type selector](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/discount-select.webp?w=450px)

| En cas de remises le prix total hors remises est désormais affiché barré en dessous du prix total appliqué.

## Affichage du panier

Vous pouvez désormais cacher certaines colonnes dans la vue panier. Cela peut-être particulièrement utile pour les magasins d'accessoires qui souhaitent une vue plus épurée.

Rendez-vous dans la configuration POS (_Administration_/_Configuration POS_) et dé-cochez les colonnes que vous ne souhaitez plus voir apparaitre dans la vue de panier :

![Lines Vat Policy](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/basket-display.webp?w=100%)

yuzSection Intégrations

## Eldowallet

Vous pouvez désormais créer une wallet pour votre client directement depuis sa fiche client.

## Pennylane

Pennylane : vous pouvez désormais activer l'intégration de vos écritures comptables dans Pennylane.

yuzSection Affiliés

## Enregistrement des commandes

Si vous appartenez à un réseau qui prend en charge l'enregistrement de vos commandes client, vous pouvez désormais les déclarer dans Yuzer.

### Yuzer full

Si vous avez une license Yuzer complète, l'enregistrement de la commande client auprès de votre fournisseur vous sera automatiquement proposée après l'édition du bon de commande du panier client.

![Register order with Yuzer full](](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/register-order-yuzer-full.webp?w=600px)

Pour rappel, vous pouvez de la même manière enregistrer vos ventes et vos démarrages de garanties au moment où vous éditez une facture. Petite amélioration de ce côté : le choix de remise déclaré à la vente ou à la garantie sera pré-rempli si une commande client a été enregistrée.

### Yuzer link

L'enregistrement de la commande client se fait au choix:
- depuis un dossier véhicule
![Register customer order from dealer file detail](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/register-order-link-df-button.webp?w=400px)
- ou depuis la liste des dossiers véhicules
![Register customer order from dealer file list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/register-order-link-list-button.webp?w=400px)

Dans le second cas, vous devrez commencé par choisir un dossier existant ou par créer un nouveau dossier (à commander).

![Select dealer file](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/register-order-link-1-select-df.webp?w=500px)

Puis, vous devrez remplir le formulaire. En particulier, vous devez attacher le document justificatif à la galerie de documents du dossier véhicule et le sélectionner.

![Select dealer file](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.1/register-order-link-2-modal.webp?w=500px)

Une fois les données remplies, vous pouvez, avant d'enregistrer, choisir de passer effectivement la commande à votre fournisseur, en quel cas la modale de commande s'affichera. La coche est sélectionnée par défaut si le dossier est _à commander_.

yuzSection Général

## Améliorations

- La clôture de caisse vous permet désormais de charger plus de paiements en attente. Cela vous permet de valider des paiements à venir directement depuis cet écran.
- L'amélioration précédente est automatiquement utilisée lorsqu'un paiement en attente (caution) YUZER pay a eu lieu dans la journée afin que nous n'oubliez pas si besoin de la restituer au client.
- Les vues de paiement et transactions de YUZER pay sont désormais paginées pour supporter une charge accrue.

## Corrections

- Les montants d'ouverture précédente sur une clôture de caisse ont été rajoutés, ils avaient disparus en version 4.
- La visualisation des accès de redistribution YUZER affiche désormais le nom du partenaire associé.
- Lorsqu'un accès peut-être enregistré plusieurs fois, comme le connecteur e-commerce par exemple, vous pouvez le renommer.
