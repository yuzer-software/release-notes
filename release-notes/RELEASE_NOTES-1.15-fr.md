# Janvier 2022 - Version 1.15.16

La chargement des paniers et de certaines pages a été amélioré.

# Janvier 2022 - Version 1.15.15

## Produits en attente de commande par marque

Nous avons ajouté une colonne _marque_ à la liste des produits en attente de commande. Il est donc possible, comme illustré ci-dessous, de grouper par fournisseur puis marque. Cette fonctionnalité est particulièrement utile lorsqu'un fournisseur de catalogue possède plusieurs marques et que les commandes doivent être passées directement aux marques en question.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/waiting-order-by-brand.png" height="350"/>

## C'est corrigé

- Dans le cas d'un panier vide (ou d'un panier _véhicule_ sans autre ligne de panier), lors de l'ajout d'une remise fixe, la TVA n'était pas automatiquement remplie: le remplissage du prix TTC n'impactait pas le prix HT et il en résultat une ligne avec 0€ HT, 0% TVA mais le prix TTC rentré. La facture éditée était donc fausse. Il est maintenant impossible de rentrer un prix sans TVA.
- Il est à nouveau possible de sauvegarder les modèles commentaires.

# Janvier 2022 - Version 1.15.14

## Inventaires

### Inventorier les zones réservées

Il est désormais possible de créer un inventaire partiel pour les zones réservées (préparation panier, produits identifiés, etc.).

### Scinder un inventaire

De même qu'il était possible de déplacer les lignes avec des références inconnues dans un nouvel inventaire reliquat, il est maintenant possible de déplacer des lignes par emplacement de stockage dans un nouvel inventaire reliquat.

Le bouton "Extraire les produits inconnus dans un nouvel inventaire reliquat" devient "Scinder l'inventaire".

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/split-inventory-button.png" height="90"/>

Il ouvre une fenêtre où vous pouvez choisir entre :

- déplacer les lignes de produits inconnus dans un nouvel inventaire (ancienne fonctionnalité),
- déplacer les lignes de certaines zones dans un nouvel inventaire (nouvelle fonctionnalité).

La description du nouvel inventaire est pré-remplie dans les deux cas mais peut être personnalisée.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/split-inventory-modal.png" height="500"/>

# Janvier 2022 - Version 1.15.13

Il est possible de définir un préfixe pour les numéros de documents édités (factures, bons de commandes, etc). Cette fonctionnalité est particulièrement important si vous avez des entités logiques (sous-entité d'une même entité légale) pour éviter des conflits entre vos numéros de factures, chaque entité ayant sa propre séquence.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/document_id_prefix_conf.png" height="400"/>

# Janvier 2022 - Version 1.15.12

- Ajoute d'un sélecteur pour allez directement sur une page d'inventaire donnée.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/inventory-page-selector.png" height="150"/>

## C'est corrigé

- Dans un inventaire, la vue ne se réinitialise plus sur la première page lorsqu'on active/désactive la vue catalogue ou qu'on ajoute ou supprime une ligne.

# Janvier 2022 - Version 1.15.11

Nous avons ajouté sur les lignes d'inventaire:

- l'avatar de l'utilisateur qui l'a modifié en dernier
- le prix moyen pondéré du produit
- et une case à cocher pour aider à la validation et à la vérification de l'inventaire. A noter que ces valeurs sont stockées localement sur votre machine pour l'instant.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/inventory-lines-more-columns.png" height="150"/>

## C'est corrigé

- Sur les lignes d'inventaire, l'icône de balance de stock pouvait s'afficher avec un status incorrect lorsque la quantité est indéfinie.

# Janvier 2022 - Version 1.15.10

## Amélioration sur l'inventaire

- Ajout d'un bouton pour pouvoir filtrer et ne voir que les lignes d'inventaire qui ont une balance de stock incorrecte.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/inventory-balance-filter.png" height="150"/>

- Ajout d'un bouton pour ajouter rapidement un produit par référence. A noter que vous devez activer le filtre par emplacement pour que le bouton apparaisse.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/inventory-quick-add.png" height="80"/>

- Les zones de préparation de panier et emplacement véhicules ont été ajouté dans le filtre par emplacement.

## C'est corrigé

- Il est maintenant possible de naviguer entre les pages de l'inventaire lorsque le filtre par emplacement est activé.
- Il est désormais possible facturer un panier véhicule alors que la cession associée au dossier du véhicule est facturée avec un montant de 0.

# Janvier 2022 - Version 1.15.9

## C'est corrigé

- Dans certaines situations la selection de caisse dans la barre de navigation principale pouvait ne pas se charger correctement.

# Janvier 2022 - Version 1.15.8

## Sélection centralisée de la caisse

La sélection de la caisse active s'effectue désormais directement depuis la barre de navigation principale à côté de la sélection de l'entrepôt:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/top-navbar.png" />

Cette sélection permet de mieux comprendre sur quelle caisse l'utilisateur travaille et remplace la sélection dans la pop-up de paiement ou dans la clôture de caisse.

## Impression rapide des étiquettes de produit

Nous avons ajouté un bouton en haut à droite de la fiche de détails d'un produit afin d'imprimer directement ses étiquettes.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/quick-price-tag-printing.png" />

## Configuration des imprimantes par défaut

Il est maintenant possible de choisir une imprimante par défaut pour éditer les tickets de caisse et les étiquettes de produits dans Yuzer.
Vous avez la possibilité de définir des options d'impression usuelles (nombre de copies, couleur ou noir et blanc, etc).
A noter que si vous activez le **mode silencieux**, la fenêtre de paramètres de l'imprimante ne s'ouvrira pas lorsque vous cliquez sur le bouton "_imprimer_".
Aussi, en activant l'option **impression automatique** pour l'imprimante ticket de caisse, une requête d'impression sera automatiquement envoyée à l'imprimante de votre choix lorsque vous éditez un ticket de caisse, un acompte ou un reçu de paiement.

La configuration est spécifique sur chaque poste.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/default-printer-configuration.png" />

## Imprimer les étiquettes de produits de tout mon stock

Nous avons ajouté une fonctionnalité, accessible depuis le menu **Stock**, pour pouvoir imprimer les étiquettes de tous les produits du stock.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/print-all-stock-labels-01.png" />
<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/print-all-stock-labels-02.png" />
<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/print-all-stock-labels-03.png" />

Description des options:

- **Commencer au produit (0 pour le premier produit)**
  Indique l'index du produit à partir duquel l'impression doit commencer.
  Concrètement, avant impression nous récupérons tous les produits du stock puis les trions par fournisseurs et identifiants, si vous saisissez le nombre _12_, l'impression commencera après le 12ème produit.

- **Taille des groupes de produits**
  Indique le nombre de produits à envoyer à l'imprimante par requête d'impression.

- **Nombre de groupes après lesquels suspendre**
  Met en pause les requêtes d'envoi d'impression toutes les X requêtes.
  Une fois en pause, cliquez sur le bouton _Reprendre_ pour continuer.

- **Imprimer la quantité en stock**
  Si coché, imprime autant d'étiquettes que de quantité en stock pour chacun des produits.

- **Imprimer 1 seule étiquette si quantité supérieure à**
  Cette option est disponible si l'option **Imprimer la quantité en stock** est cochée.
  Si le seuil défini est atteint, seulement une étiquette sera imprimée.
  _Cette option est utile afin d'éviter d'imprimer 200 étiquettes pour un bidon d'huile avec une quantité de 200L._

## Bêta de gestion du TPE

Cette version introduit un support en bêta de la connexion TPE. Il est développé chez nous à l'aide d'un Ingenico Move 5000.

Cette fonctionnalité n'est pas considérée comme stable. Elle peut-être utilisée épisodiquement à vos risque et périls afin de tester le support de votre terminal.
Notez qu'il n'est pas actuellement possible d'enregistrer deux paiements cartes dans la même session de paiement (même boite de dialogue paiement) avec la connexion TPE.

## Améliorations du widget de main-d'œuvre

Les options de configuration du widget de main-d'œuvre ont été améliorées et permettent:

- d'afficher le temps disponible en plus du temps facturé (attention cette valeur est une estimation basée sur la capacité actuelle de l'atelier - ce point sera amélioré dans le futur).
- d'afficher le graphique ligne en cumulatif ou non (l'affichage était toujours cumulatif dans la version précédente pour ce type de graphique)
- de filtrer sur une période de l'année donnée.

Mais aussi d'afficher une nouvelle visualisation sous forme de jauge:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/workforce-gauge.png" height="350"/>

## Améliorations du widget de chiffre d'affaires

- Il est désormais possible d'éditer le titre du widget.
- l'affichage du graphique ligne peut-être cumulatif ou non

## Exposition d'API externe

Vous pouvez désormais exposer votre liste de stock véhicules à un exploitant externe tel que Winteam. Il faut pour cela créer une clé d'API depuis la nouvelle section de votre espace administration.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/api-key-menu.png" height="100"/>

Cliquez sur _Ajouter_ puis configurez les différents paramètres de la clé d'API.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/api-key-new.png" height="300" />

Vous pouvez alors communiquer à votre exploitant les instructions qui s'affichent:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/api-key-instructions.png"  height="100" />

## Gestion des factures d'achat

Il est désormais possible d'enregistrer ses factures d'achat dans Yuzer et d'associer les réceptions et dossiers de produit identifiés à celles-ci.

<div class="alert alert-info">Le support du lien des dossiers véhicules aux factures d'achat est prévu pour le premier trimestre 2022 suite à une harmonisation de leur gestion avec celles des autres produits identifiables.</div>

### Paramètres de comptabilité lié aux achats

De nouveaux paramètres de comptabilité ont été ajoutés afin de pouvoir gérer vos factures d'achat.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/accountancy-settings-menu.png" height="80" />

Ces nouveaux paramètres vous permettent de configurer les numéros de comptes fournisseurs ainsi que les comptes TVA liés aux achats.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/accountancy-settings-new-params.png" height="150" />

Vous devrez également définir les règles d'association de votre comptabilité à l'achat et pour les remises à l'achat.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/accountancy-mapping-purchase.png" height="200" />

<div class="alert alert-info">
Plusieurs améliorations seront développées sur ce sujet courant janvier, incluant la possibilité de créer une configuration à l'achat spécifique pour les achats intra-communautaires.
</div>

### Liste des factures d'achat

Les factures d'achat sont disponibles depuis l'onglet comptabilité

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/purchase-invoice-list.png" height="400"/>

### Ajout d'une nouvelle facture d'achat

L'ajout d'une nouvelle facture d'achat se fait à l'aide du bouton depuis la liste.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/new-purchase-invoice.png" height="350"/>

Notez que l'ajout d'une facture d'achat pour un fournisseur nécessite au préalable d'avoir associé un contact avec un numéro fournisseur à celui-ci. Le numéro de fournisseur est en effet utilisé comme numéro du tiers en comptabilité.

Yuzer vous permet de définir

- une facture avec TVA, vous devrez alors enregistrer vous même les prix HT et TTC de chaque ligne (en effet les règles d'arrondi pouvant être propre à votre fournisseurs c'est bien à vous de valider ceux-ci).
- une facture sans TVA apparente mais avec gestion de la TVA intra-communautaire, vous devez alors entrer ou valider pour chaque ligne le taux de TVA qui sera appliqué par Yuzer afin de calculer et enregistrer comptablement les TVA due et déductible intra-communautaires.
- une facture sans TVA apparente et sans gestion de TVA intra-communautaire. Peu recommandé mais possible, aucune TVA ne sera enregistré en comptabilité sur une telle facture.

Vous devez également spécifier le total de la facture. Yuzer effectuera une vérification lors du passage en comptabilité.

La plupart des informations peuvent être modifiées sur l'écran de détails.

### Edition d'une facture d'achat

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/purchase-invoice-edit.png" height="100"/>

### Lien avec un dossier

Pour une ligne de facture d'achat associée à un produit identifié, vous pouvez lier celle ci au dossier du/des produit(s) en utilisant l'icône d'ajout de dossier.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/purchase-invoice-dealerfile-link.png" height="100"/>

Il est aussi possible de générer une ligne à partir du dossier produit en cliquant sur le bouton ci-dessous:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.15.0/create-purchase-line-from-dealerfile.png" height="100"/>

## Integration with Suzuki

Les concessionaires Suzuki peuvent désormais utiliser le service lié pour rechercher des véhicules de la marque.

## Integration SADEM

Si vous êtes un adhérent SADEM vous pouvez désormais consulter les catalogues associés.

<div class="alert alert-info">
Pour configurer l'export de vos stock SADEM merci de nous contacter.
</div>

## C'est corrigé

- Plusieurs navigations ont été corrigées, il est par exemple désormais possible de revenir à la liste des réceptions lorsque l'on est sur le détail d'une d'entre elle en cliquant directement dans le menu.
- Le taux de TVA exporté en comptabilité n'est plus calculé sur la valeur totale (et donc impacté par la somme des arrondis) mais est bien celui des lignes agrégées au taux.
