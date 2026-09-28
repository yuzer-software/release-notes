# Septembre 2026 - Version 5.5

yuzSection API

## Intégration e-commerce

Nous avons légèrement modifié l'API e-commerce.

Un champ a été modifié :
- `imageUrls: string[]` pour le support de plusieurs images. Ce champ remplace `imageUrl`.

Un champ a été renommé :
- `supplierCategory` s'appelle désormais `editorCategory`

Les précédents champs sont encore remplis pour permettre une transition douce, mais sont appelés à être supprimés.
