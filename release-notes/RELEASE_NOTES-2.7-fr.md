# Février 2022 - Version 2.7.x

Cette version 2.7 marque enfin le grand retour des release notes détaillées! Nous espérons que celle-ci vous permettra de vous approprier les dernières nouveautés de Yuzer de la meilleure manière possible.

# Contact: Adresses, emails et numéros de téléphones

## Clés personnalisées

Nous avons supprimé la limitation sur les descriptions des libellés des adresses, emails et numéros de téléphones qui sont par ailleurs traduits en français.

Afin d'ajouter votre libellé personnalisé si les libellés pré-définis ne vous suffisent pas, sélectionnez _Personnaliser_ dans la liste puis cliquez sur le bouton Ajouter.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/default_key_add.png" width="400px"/>

Vous pouvez alors renseigner une clé personnalisée pour le numéro, l'email ou l'adresse:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/custom_key_modal.png" width="460px"/>

Puis définir la valeur associée:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/custom_key_val_edit.png" width="400px"/>

## Définition des valeurs par défaut

En plus de définir vos clés personnalisée vous pouvez définir, à l'édition du contact, les adresses, numéros de téléphone et email à utiliser par défaut à la facturation:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/default_invoicing_phone.png" width="312px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/default_invoicing_email.png" width="312px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/default_invoicing.png" width="312px"/>

À noter que vous pouvez également dès maintenant définir une adresse de livraison par défaut. Cette adresse n'est pas actuellement exploitée dans Yuzer mais le sera plus tard dans l'année.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/defaut_shipment.png" width="312px"/>

# Simplification des transferts inter-groupe

Dans le cas où le contact est un contact intra-groupe, vous pouvez définir l'entrepôt de livraison par défaut, ainsi que le nom du transport utilisé. Ces informations seront alors pré-remplies dans le cas de transferts entre deux entités correspondant à des sociétés différentes du groupe. Donc, lorsqu'une facture doit-être éditée entre les deux sociétés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/entity_shipment.png" width="312px"/>

Pour rappel ce type de transfert s'effectue en créant un panier de vente classique depuis la société à qui transférer les produits. Lors de la facturation à l'étape de gestion stock la boite de dialogue vous permet de livrer les produits à travers un transfert PGNA.

Nous avons ajouté une option permettant d'emballer et envoyer immédiatement le transfert.

Cela permet de ne pas avoir à traiter les étapes de colisage et d'envoi du transfert. Car ces étapes peuvent être superflues dans le cas où le transfert ne nécessite pas de passer par un transporteur.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/transfer_basket_ship_modal.png" width="100%"/>

# Exports FTP des informations de ventes

Il est désormais possible d'effectuer un export automatisé sur un serveur (S)FTP(S) des différents contenus des documents.
Celui-ci se configure directement dans la section automates qui vous permet déjà de configurer vos exports de stocks (Pièces ou véhicules).

# Ajout de frais de carte grise hors d'un panier de vente

Vous pouvez désormais accéder à l'ajout des frais de carte grise dans un panier de vente PGNA ou de réparation. Pour cela le véhicule à immatriculer doit-être renseigné comme véhicule de contexte dans le panier.

Le plus simple est de le pré-sélectionner depuis la fiche du client, vous pouvez également l'ajouter dans un panier déjà créé comme suit:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/set_vehicle.png" width="512px"/>

Ensuite rendez-vous dans le menu contextuel du groupe de facturation souhaité afin d'ajouter les frais de carte grise.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/add_registration.png" width="100%"/>

# Intégration Triumph

L'intégration Triumph nous permet de vous faciliter la vie avec l'enregistrement automatique des O.R. dans AMP depuis Yuzer.

À la facturation Yuzer utilise les informations remontées par Triumph pour proposer les différents forfaits applicables sur le véhicule.

Si la réparation ne doit pas être transmise à AMP contentez-vous de cliquer sur annuler. Sinon remplissez le formulaire et validez.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.7.0/triumph_register.png" width="512px"/>

<div class="alert alert-warning">
Attention, vous êtes responsables des informations remontées à Triumph, merci de bien valider celles-ci.
</div>

# Nouvelles automatisations de catalogues

Nous continuons à travailler activement à une meilleure synchronisation des tarifs avec les fournisseurs qui disposent de points d'intégration.

# Analyses des ventes - beta 2

Le module d'analyse des ventes a été réécrit afin d'offrir plus de capacités de personnalisations. Les anciennes configurations ont été fusionnées dans ce nouveau module.

<div class="alert alert-info">
Cette fonctionnalité est encore en bêta et nous continuons d'améliorer celle-ci ainsi que sa performance.

Le principal objectif de cette itération était de fournir un ensemble de fonctionnalité d'analyse. Afin de fournir une première version rapidement nous avons décidé de différer la prise en compte d'un ensemble d'optimisations de performances qui seront livrées petit à petit dans les versions futures de Yuzer.

</div>

## Tableaux de bords

La nouvelle fonction d'analyse vous permet de définir un ou plusieurs tableaux de bord.

Vous pouvez également réutiliser des tableaux de bords pré-définis par Yuzer. Ceux-ci sont en cours d'élaboration et nous vous invitons à contacter notre support dans le cas où vous ne trouverez pas ceux que vous recherchez.

## Créer un tableau de bord

### Période d'analyse

Les périodes d'analyse sont aujourd'hui toutes glissantes. Les périodes les plus courantes, de la journée au mois sont définies par défaut.

<div class="alert alert-info">
Les périodes non-glissantes, permettant d'adresser des problématiques de visions par trimestres, ou de période de soldes ou activité commerciales spécifiques, seront livrées dans les versions futures.
</div>

Lors du choix de la période d'analyse, Yuzer vous propose d'ajouter deux ensembles de données connexes:

- celles de la période précédente (par exemple semaine passée si vous avez choisi comme période la semaine en cours)
- celles de la même période à l'année précédente (par exemple la même semaine l'année dernière)

Bien entendu dans le cas où le choix de période concerne l'année en cours, alors «la période précédente» et «la même période de l'année précédente» désignent la même période et une seule sélection doit alors être effectuée.

### Définition des filtres généraux

Vous pouvez en plus de la définition de la période d'analyse, définir un ensemble de filtres généraux qui sont appliqués aux données affichées dans le tableau de bords. L'ensemble des données de la période sont donc pré-filtrées à l'aide de ceux-ci avant le rendu.

### Définition des sources de données

Un tableau de bord dans l'analyse Yuzer peut utiliser une ou plusieurs sources de données basées sur les données des périodes et pré-filtrées à l'aide des filtres généraux.

Chaque source de donnée peut être utilisée par un ou plusieurs graphiques ou tableaux. Il est donc possible de définir une source de donnée unique, et plusieurs visualisations comme un tableau et un graphique par exemple.

Il est aussi possible de définir plusieurs sources de données pour afficher, par exemple, un tableau des ventes véhicules et un tableau des ventes de produits sur un même dashboard.

Les sources de données définissent un ensemble de filtres spécifiques à la source de donnée ainsi que les différents niveaux d'agrégations.

### Visualisation des données et définition des widgets

Une fois les données

# Utilisation des catalogues

Lorsque vous êtes éditeur d'un catalogue vous pouvez désormais visualiser qui utilise celui-ci.
