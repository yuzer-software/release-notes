# Octobre 2024 - Version 3.10.x

yuzSection Forfaits

Les forfaits sont désormais liés à des catalogues (comme les produits). Ils bénéficient des mêmes capacités de partage que ceux-ci et peuvent être utilisés désormais par l'ensemble des entités de votre groupe.

À là création d'un nouveau forfait vous devez désormais choisir le catalogue de celui-ci.

||| Attention aujourd'hui seul l'entité éditrice du catalogue peut éditer le contenu d'un forfait/modèle.

yuzSection Vente véhicules

La sélection d'un dossier dont la référence produit n'est pas celle du panier a été simplifiée.

yuzSection Inventaires

- Il est désormais possible de sélectionner les colonnes affichées dans les tables de la vue inventaire. Celles-ci ne sont pas aujourd'hui sauvegardées.
- Les vues de résumé (par marque etc.) restent disponibles en mode édition.

## Fusion des décomptes

||| Attention cette fonctionnalité est dangereuse et correspond à un cas d'utilisation très particulier. Elle doit-être utilisée avec attention.

|| Cette fonctionalité n'est active que sur les comptes en ayant effecuté la demande, suite à formation spécifique et validation de la compréhenssion de ses impacts.

Cas d'utilisation:

- Votre entrepôt n'est pas segmenté en plusieurs emplacements pour simplifier des mouvements très fréquents d'emplacements de vos produits dans celui-ci.
- Vos produits peuvent-être situés à plusieurs emplacements dans celui-ci (rayon et tête de gondole par exemple)

|| Avoir des produits dans plusieurs 'endroits' non représentés dans YUZER n'est pas une pratique idéale car ils complexifient l'inventaire et la localisation des produits.

- Plusieurs personnes effectuent des décomptes sur cet emplacement unique alors que le même produit dans le même emplacement.
  Par exemple Luc compte 3 (en rayon) puis Matthieu 2 (en tête de gondole). Yuzer afficher alors une quantité inventoriée de 2.

- Une fois les décomptes terminés une fusion de ceux-ci est lancée par un opérateur (magasinier ou administrateur).
  Sur l'exemple précédent YUZER va ajouter un nouveau compte de 5 correspondant à la fusion des deux décomptes précédents. Ce décompte sera assigné dans l'historique à l'opérateur.

yuzSection Général

## Améliorations
