# Juin 2023 - Version 2.13.0

## Commandes & prix d'achat

- Lors de la commande, Yuzer s'assure de la mise à jour des prix d'achat de chaque produit et affiche désormais le coût total estimé dans la fenêtre de `Récapitulatif des produits à commander`.

<div class="text-center" style="text-align: 'center';">
  <img width="840" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.13.0/orders-estimated-costs.webp"/>
</div>

- Il est possible rafraîchir ou de mettre à jours ces prix d'achats si ce n'est renseigné sur les lignes en attente de commande

<div class="text-center" style="text-align: 'center';">
  <img width="300" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.13.0/orders-refresh-prices.webp"/>
</div>

- Nous avons également ajouter les informations de prix d'achat sur l'écran de commandes

<div class="text-center" style="text-align: 'center';">
  <img width="840" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.13.0/orders-purchase-prices.webp"/>
</div>

<div class="alert alert-info">
`Coût total estimé` : Prix d'achat calculé à partir du catalogue.
`Total prix d'achat` : Prix d'achat donné par le fournisseur (si disponible).
</div>

## Statut de dossiers

Il arrivait que le statut d'un dossier ne se mette pas correctement à jour, particulièrement lors de l'annulation d'une facture où le dossier restait parfois à `Facturé et soldé`, bloquant ainsi certaines actions autour du panier.
Désormais, Yuzer vérifie que les statuts du dossier et du panier sont consistants et corrige automatique le statut du dossier si nécessaire.

Aussi, Yuzer marque désormais automatiquement le dossier à `Facturé et soldé` si le panier est soldé au moment de la facturation.

## Nouvelles configurations

Nous avons ajouté la possibilité de restreindre les actions suivantes aux administrateurs seulement:

- La possibilité de délivrer les produits d'un panier sans impacter le stock.
- La possibilité d'initialiser le stock depuis la fiche produit.

Pour ce faire, allez dans le menu `Administration > Gestion commerciale > Configurer > Configuration commerciale`

<div class="text-center" style="text-align: 'center';">
  <img width="1536" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.13.0/new-trade-configurations.webp"/>
</div>

## Corrections et Améliorations

- Un modèle de panier sera maintenant importer avec les références principales des produits si vous avez activé l'option des équivalences (`Administration > Gestion du stock`).
- La clôture d'inventaire ne remontait plus correctement le statut de clôture et ni les erreurs éventuelles.
- Un catalogue ne pouvait pas toujours être supprimé même lorsque tout le stock a été fusionné.
