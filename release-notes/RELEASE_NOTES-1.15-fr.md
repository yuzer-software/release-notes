# Décembre 2021 - Version 1.15.0

Améliorations diverses:

-

## Impression rapide des étiquettes de produit

Nous avons ajouté un bouton en haut à droite de la fiche de détails d'un produit afin d'imprimer directement ses étiquettes.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/quick-price-tag-printing.png" />

## Configuration des imprimantes par défaut

Il est maintenant possible de choisir une imprimante par défaut pour éditer les tickets de caisse et les étiquettes de produits dans Yuzer.
Vous avez la possibilité de définir des options d'impression usuelles (nombre de copies, couleur ou noir et blanc, etc).
A noter que si vous activez le **mode silencieux**, la fenêtre de paramètre de l'imprimante ne s'ouvrira pas lorsque vous cliquez sur le bouton "_imprimer_".
Aussi, en activant l'option **impression automatique** pour l'imprimante ticket de caisse, une requête d'impression sera automatiquement envoyer à l'imprimante de votre choix lorsque vous éditez un ticket de caisse, un accompte ou un reçu de paiement.

La configuration est spécifique sur chaque poste.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/default-printer-configuration.png" />

## Imprimer les étiquettes de produits de tout mon stock

Nous avons ajouté une fonctionnalité, accessible depuis le menu **Stock**, pour pouvoir imprimer les étiquettes de tous les produits du stock.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/print-all-stock-labels-01.png" />
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/print-all-stock-labels-02.png" />
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/print-all-stock-labels-03.png" />

Description des options:

- **Commencer au produit (0 pour le premier produit)**
  Indique l'index du produit à partir duquel l'impression doit commencer.
  Concrètement, avant impression nous récupérons tous les produits du stock puis les trions par fournisseurs et identifiants, si vous saisissez le nombre _12_, l'impression commencera après le 12ème produit.

- **Taille des groupes de produits**
  Indique le nombre de produits à envoyer à l'imprimante par requête d'impression.

- **Nombre de groupes après lesquels pauser**
  Met en pause les requêtes d'envoie d'impression tous les X requêtes.
  Une fois en pause, cliquez sur le bouton _Reprendre_ pour continuer.

- **Imprimer la quantité en stock**
  Si coché, imprime autant d'étiquettes que de quantité en stock pour chacun des produits.

- **Imprimer 1 seule étiquette si quantité supérieure à**
  Cette option est disponible si l'option **Imprimer la quantité en stock** est cochée.
  Si le seuil défini est atteint, seulement une seule étiquette sera imprimé.
  _Cette option est utile afin d'éviter d'imprimer 200 étiquettes pour un bidon d'huile avec une quantité de 200L._

# C'est corrigé

-
