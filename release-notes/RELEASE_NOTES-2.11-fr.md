# Mai 2023 - Version 2.11.x

## Réceptions

- L'ajout d'un produit inconnu au catalogue ne génère plus d'erreurs, mais il crée une ligne:
  - Il vous faudra faire son entrée en stock dans un produit du catalogue
  - Vous devrez ensuite faire manuellement le lien vers les réservations
  - Il n'est pas encore possible de les lier à une commande car les commandes sont liées aux produits catalogue

<div class="text-center" style="text-align: 'center';">
  <img width="850" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.11.0/unknown-item-reception-line.webp"/>
</div>

Des vérifications ont été ajoutées à la fenêtre de décomposition avec des messages explicatifs en cas de mauvaise correspondance.

## Application mobile

### Oubli sur la release précédente

Tout d'abord, un oubli sur la release note précédente : il est possible de choisir l'action de réception par défaut en cliquant sur le bouton de configuration en haut à droite sur la page d'ajout de produits (voir ci-dessous). Choisissez ensuite l'action par défaut souhaitée.

<div class="text-center" style="text-align: 'center';">
  <img width="300" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.11.0/mobile-select-reception-action.webp"/>
</div>

### Remontée d'erreurs sur les réceptions

- Les lignes de réception comportant des erreurs sont marquées d'un warning rouge pour rapidement les identifier:

<div class="text-center" style="text-align: 'center';">
  <img width="300" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.11.0/mobile-reception-line-with-error.webp"/>
</div>

- Les rapports d'erreurs sont améliorés sur le détail d'une ligne de réception et sur l'écran de conversion des produits.

### Corrections

- Dans certaines conditions, certaines valeurs décimales ne pouvaient pas être correctement rentrées.
