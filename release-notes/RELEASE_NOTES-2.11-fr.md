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

- Les lignes de réception comportant des erreurs sont marquées d'un warning rouge pour rapidement les identifier:

<div class="text-center" style="text-align: 'center';">
  <img width="300" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.11.0/mobile-reception-line-with-error.webp"/>
</div>

- Sur le détail d'une ligne de réception, les rapports d'erreurs sont améliorés.

Corrections:

- Dans certaines conditions, certaines valeurs décimales ne pouvaient pas être correctement rentrées.
