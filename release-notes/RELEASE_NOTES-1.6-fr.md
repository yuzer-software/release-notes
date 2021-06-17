# Juin 2021 - Version 1.6.0

- Possibilité de modifier le libellé d'un produit dans un panier.
- Le taux de marge est maintenant affiché dans l'encadré _Résumé_ du panier de vente véhicule lorsque le filtre d'affichage des prix d'achats et marges est désactivé.

## Nouvelles fonctionalités sur la réception

### Ré-ouverture

Il est maintenant possible de ré-ouvrir une réception clôturée pour y ajouter de nouvelles lignes.
Les lignes traitées ne sont pas modifiable.

### Annulation

L'annulation d'une réception est maintenant possible. Vous pouvez choisir d'annuler seulement quelque ligne ou toutes les lignes de la réception.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-new-menu.png" width="320"/>

Une ligne annulée est affichée avec un texte grisé avec l'icône <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-ban-icon.png" width="16" />, comme ci-dessous.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-canceled-line.png" width="1024"/>

Lors de l'annulation, les différentes actions suivantes sont exécutées pour chacune des lignes pour essayer de revenir à l'état avant clôture:

- Annulation des quantités de stock sur l'emplacement de réception
- Annulation des prix de stock pour le produit (prix FIFO, prix moyen)
- Si existant, annulation de la ligne de commande associée
- Si existant, annulation de la réservation/préparation pour un client

Il se peut que les emplacements spécifiés lors de la réception aient été mis à jour entre la clôture et l'annulation.
Dans le cas où la quantité est trop faible (_quantité de l'emplacement < quantité reçue_), une fenêtre sera affichée pour vous demander de résoudre et spécifier les emplacements à impacter pour l'annulation.

L'image suivante montre la fenêtre de validation.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-cancellation-modal-1.png" width="1024"/>
Nous constatons qu'une ligne avait été clôturé avec 4 quantités reçues, toutes stockées à l'emplacement: _Showroom/Étagère 1/ Planche 1/ Paquet 1_.
Cependant, l'emplacement ne contient plus que 2 unités du produit.

Pour l'exemple, nous choisissons d'ajouter l'annulation de 2 quantités sur l'_Emplacement inconnu_.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-cancellation-modal-2.png" width="1024"/>

A noter que le nombre d'articles et le total du prix incluant remises sont calculés en ignorant les lignes annulées.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-infos.png" width="384"/>

### Filtrage des lignes

Des filtres ont été ajouter pour pouvoir cacher les lignes traitées ou annulées.
Cela devrait facilité la lisibilité en particulier sur la modification d'une relative grosse réception qui aurait été ré-ouverte.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/reception-new-filters.png" width="896"/>
