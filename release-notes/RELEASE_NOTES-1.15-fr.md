# Décembre 2021 - Version 1.15.4

## Sélection centralisée de la caisse

La sélection de la caisse active s'effectue désormais directement depuis la barre de navigation principale à côté de la sélection de l'entrepôt:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/top-navbar.png" />

Cette sélection permet de mieux comprendre sur quelle caisse l'utilisateur travaille et remplace la sélection dans la pop-up de paiement ou dans la clôture de caisse.

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

## Améliorations du widget de main d'oeuvre

Les options de configuration du widget de main d'oeuvre ont été améliorées et permettent:

- d'afficher le temps disponible en plus du temps facturé.
- d'afficher le graphique ligne en cumulatif ou non (l'affichage était toujours cumulatif dans la version précédente pour ce type de graphique)
- de filtrer sur une période de l'année donnée.

Mais aussi d'afficher une nouvelle visualisation sous forme de jauge:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/workforce-gauge.png" />

## Améliorations du widget de chiffre d'affaires

- Il est désormais possible d'éditer le titre du widget.
- l'affichage du graphique ligne peut-être cumulatif ou non

## Exposition d'API externe

Vous pouvez désormais exposer votre liste de stock véhicules à un exploitant externe tel que Winteam. Il faut pour cela créer une clé d'API depuis la nouvelle section de votre espace administration.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/api-key-menu.png" />

Clickez sur _Ajouter_ puis configurez les différents paramètres de la clé d'API.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/api-key-new.png" />

Vous pouvez alors communiquer à votre exploitant les instructions qui s'affichent:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/api-key-instructions.png" />

## Gestion des factures d'achat

Il est désormais possible d'enregistrer ses factures d'achat dans Yuzer et d'associer les réceptions et dossiers de produit identifiés à celles-ci.

<div class="alert alert-info">Le support du lien des dossiers véhicules au factures d'achat est prévu pour le premier trimestre 2022 suite à une harmonisation de leur gestion avec celles des autres produits identifiables.</div>

### Paramètres de comptabilité lié aux achats

De nouveaux paramètres de comptabilité ont été ajoutés afin de pouvoir gérer vos factures d'achat.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/accountancy-settings-menu.png" />

Ces nouveaux paramètres vous permettent de configurer les numéros de comptes fournisseurs ainsi que les comptes TVA liés aux achats.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/accountancy-settings-new-params.png" />

Vous devrez également définir les règles d'association de votre comptabilité à l'achat et pour les remises à l'achat.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/accountancy-mapping-purchase.png" />

### Liste des factures d'achat

Les factures d'achat sont disponibles depuis l'onglet comptabilité

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/purchase-invoice-list.png" />

### Ajout d'une nouvelle facture d'achat

L'ajout d'une nouvelle facture d'achat se fait à l'aide du bouton depuis la liste.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/new-purchase-invoice.png" />

Notez que l'ajout d'une facture d'achat pour un fournisseur nécessite au préalable d'avoir associé un contact avec un numéro fournisseur à celui-ci. Le numéro de fournisseur est en effet utilisé comme numéro du tiers en comptabilité.

Yuzer vous permet de définir

- une facture avec TVA, vous devrez alors enregistrer vous même les prix HT et TTC de chaque ligne (en effet les règles d'arrondi pouvant être propre à votre fournisseurs c'est bien à vous de valider ceux-ci).
- une facture sans TVA apparente mais avec gestion de la TVA intra-communautaire, vous devez alors entrer ou valider pour chaque ligne le taux de TVA qui sera appliqué par Yuzer afin de calculer et enregistrer comptablement les TVA due et déductible intra-communautaires.
- une facture sans TVA apparente et sans gestion de TVA intra-communautaire. Peu recommandé mais possible, aucune TVA ne sera enregistré en comptabilité sur une telle facture.

Vous devez également spécifier le total de la facture. Yuzer effectuera une vérification lors du passage en comptabilité.

La plupart des informations peuvent être modifiés sur l'écran de détails.

### Edition d'une facture d'achat

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.15.0/purchase-invoice-edit.png" />

## Integration with Suzuki

Les concessionaires suzuki peuvent désormais utiliser le service lié pour rechercher des véhicules de la marque.

## Integration SADEM

Si vous êtes un adhérent SADEM vous pouvez désormais consulter les catalogues associés.

## C'est corrigé

- Plusieurs navigations ont été corrigées, il est par exemple désormais possible de revenir à la liste des réceptions lorsque l'on est sur le détail d'une d'entre elle en cliquant directement dans le menu.