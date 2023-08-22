# Juillet 2023 - Version 2.13.7

## Corrections et Améliorations

- Nouvelle autorité de produit identifié: plaques d'immatriculations autrichiennes.

<div class="text-center" style="text-align: 'center';">
  <img width="240" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.13.0/austrian-registration.webp"/>
</div>

# Juillet 2023 - Version 2.13.6

## Corrections et Améliorations

- Corrections de calcul et de vérification de calcul d'arrondis.

# Juillet 2023 - Version 2.13.2

## Corrections et Améliorations

- Le dossier produit n'est plus requis pour l'édition d'une facture proforma.
- Correction de l'affichage de la fenêtre de "Champs requis" lors de la création d'un nouveau contact.

# Juillet 2023 - Version 2.13.1

## Honda: amélioration de la remontée d'information sur commandes et envois

Suite à une commande passée via Yuzer, les statuts de prise en charge de la commande par Honda sont désormais remontés dans Yuzer.

De plus, lorsque Honda effectue un envoi une réception est automatiquement crée avec le contenu de l'envoi. Vous n'avez alors plus qu'à valider que tout est bien reçu comme prévu et à clôturer la réception une fois le contrôle effectué.

## Compteur SIV

Nous avons ajouté un onglet dans `Administration > Automates > SIV` permettant de consulter le compteur et l'historique des requêtes vers MiSIV.

<div class="text-center" style="text-align: 'center';">
  <img width="840" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.13.0/siv-count.webp"/>
</div>

## Corrections et Améliorations

- Correction de l'affichage du compteur de documents dans l'analytique

# Juin 2023 - Version 2.13.0

## Rafraîchissement des données analytiques

Les données d'analytiques sont désormais automatiquement rafraîchies:

- lors de mises à jour de coûts et bonus ou cessions liées aux dossiers de véhicules.
- lors d'édition de catégories de ventes depuis les listes de documents.

Afin de pleinement bénéficier de cette fonctionnalité et garantir que vos données sont bien à jour il est recommandé de réinitialiser vos données.

## Gestion du stock monté sur véhicule

Le stock monté sur véhicule est désormais traité comme non-disponible dans le cadre des propositions de commande automatisées.

Cet aspect est désormais clairement explicité dans la vue produit et dans les résumés de contenu de stock.

## Gestion des références équivalentes et modèles

Lorsqu'un modèle est ajouté à un panier, si celui-ci contient une référence A qui est une référence d'une référence B définie comme principale, c'est bien la référence B qui sera ajoutée dans le panier.

## Les programmes de fidélités peuvent désormais être appliqués sur les produits identifiés (véhicules etc.)

## Commandes & prix d'achat

- Lors de la commande, Yuzer s'assure de la mise à jour des prix d'achat de chaque produit et affiche désormais le coût total estimé dans la fenêtre de `Récapitulatif des produits à commander`.

<div class="text-center" style="text-align: 'center';">
  <img width="840" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.13.0/orders-estimated-costs.webp"/>
</div>

- Il est possible rafraîchir ou de mettre à jours ces prix d'achats si ce n'est renseigné sur les lignes en attente de commande

<div class="text-center" style="text-align: 'center';">
  <img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.13.0/orders-refresh-prices.webp"/>
</div>

- Nous avons également ajouter les informations de prix d'achat sur l'écran de commandes

<div class="text-center" style="text-align: 'center';">
  <img width="840" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.13.0/orders-purchase-prices.webp"/>
</div>

`Coût total estimé` : Prix d'achat calculé à partir du catalogue.
`Total prix d'achat` : Prix d'achat donné par le fournisseur (si disponible).

## Statut de dossiers

Il arrivait que le statut d'un dossier ne se mette pas correctement à jour, particulièrement lors de l'annulation d'une facture où le dossier restait parfois à `Facturé et soldé`, bloquant ainsi certaines actions autour du panier.
Désormais, Yuzer vérifie que les statuts du dossier et du panier sont consistants et corrige automatique le statut du dossier si nécessaire.

De plus, Yuzer marque désormais automatiquement le dossier à `Facturé et soldé` si le panier est soldé au moment de la facturation. La boîte de dialogue demandant à l'utilisateur s'il souhaite ou non clôturer le dossier disparait donc.

## Nouvelles configurations

Nous avons ajouté la possibilité de restreindre les actions suivantes aux administrateurs seulement:

- La possibilité de délivrer les produits d'un panier sans impacter le stock.
- La possibilité d'initialiser le stock depuis la fiche produit.

Pour ce faire, allez dans le menu `Administration > Gestion commerciale > Configurer > Configuration commerciale`

<div class="text-center" style="text-align: 'center';">
  <img width="1536" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.13.0/new-trade-configurations.webp"/>
</div>

## Corrections et Améliorations

- La clôture d'inventaire ne remontait plus correctement le statut de clôture et ni les erreurs éventuelles.
- Un catalogue ne pouvait pas toujours être supprimé même lorsque tout le stock a été fusionné.
- Améliorations internes du module comptabilité.
