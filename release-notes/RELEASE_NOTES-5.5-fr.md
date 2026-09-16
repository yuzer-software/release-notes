# Septembre 2026 - Version 5.5

yuzSection Général

## Catalogue produits

### Parents, variants et discriminants

Le support de variants est amélioré avec une auto-détection des discriminant et leur exploitation dans l'affichage et la sélection de ceux-ci sur une fiche produit.

L'auto-détection compare les propriétés des produits et, lorsque des propriétés diffèrent sur des variants les indiques comme discriminants.

<!-- ![variant-display](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.5/variant-display.webp?w=896px) -->

La recherche des variants par code barre permet de retrouver le parent correctement.

## Signature électronique

|| Fonctionalité bêta disponible avec coût au click.

Vous pouvez désormais envoyer un document pour signature électonique. Actuellement il faut d'abord éditer le document sans signature puis l'envoyer pour signature électronique.
Disponible actuellement sur les bon de commande, ordres de réparations, bon de livraisons et formulaires de prêt véhicule.

## Internationalisation

### Support des DROM

Nous avons apporté plusieurs modifications pour supporter les Départements et régions d'outre-mer, plus particulièrement de la Réunion, Martinique et Guadeloupe.

Nous avons également ajouté le support des surcharges de TVA spécifiques aux échanges métropoles-drom en plus des exonérations.

### Support international

Vous pouvez désormais configurer la devise de l'entité, permettant ainsi l'utilisation de YUZER hors zone euro.

## Améliorations Diverses

- Vous pouvez désormais exporter puis ré-importer les locations d'un entrepôt pour une édition simplifiée dans excel par exemple.
- Amélioration de la synchronisation pennylane.
- Amélioration du contrôle de duplicat d'une facture d'achat pour un même fournisseur (le contrôle était appliqué à la création et non à la modification).
- Amélioration de la performance des imports de données.

## Corrections

- Sur client de passage il est désormais possible d'assigner un client pour génération d'une facture. Attention ce changement est définitif.
- Il est désormais possible d'annuler des produits non stockable lors d'une annulation partielle.
- Nous avons amélioré la validation de l'utilisation d'une carte cadeau en ajoutant un niveau de vérification supérieur.
- Nous avons corrigé un problème de changement de client d'un client intra-entité (transfer seulement) vers extra-entité (sans transfer).
- Le support des variants dans l'intégration e-commerce a été corrigé. De même les codes barres des produits sont désormais exportés par l'intégration e-commerce.
- Nous avons corrigé l'affichage des demi-journées d'indisponibilité dans le planning.
- Plusieurs cas de désynchronisations de status dans l'affichage ont été résolus.
- Amélioration de certains libellés dans les exports comptables.
