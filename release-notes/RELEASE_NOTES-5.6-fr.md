# Octobre 2026 - Version 5.6

yuzSection API

## Intégration e-commerce

|| Evolution des synchronisation du catalogue produit. Mettez à jour vos intégrations dès que possible.

Certains champs deviennent dépréciés à la faveur de nouveaux champs. Les anciens champs seront appelés à être supprimés.

Support d'images multiples :

- `imageUrl` de type `string` est désormais déprécié et est amené à disparaitre.
- `imageUrls` de type `string[]` permettant le support de plusieurs images fait son apparition, la première image si celle-ci existe est celle définie dans `imageUrl`.

Clarification des catégories :

- `supplierCategory` est désormais déprécié et est amené à disparaitre.
- `editorCategory` a été ajouté et contient le même contenu que `supplierCategory` mais clarifie la provenance des catégories qui sont celles fournies par l'éditeur du catalogue. Celui-ci peut-être mais n'est pas toujours le fournisseur des produits.
