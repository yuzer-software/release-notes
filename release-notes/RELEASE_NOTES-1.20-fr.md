# Mars 2022 - Version 1.20.1

# Balances et crédit

## Visibilité des balances d'un client sur le groupe

La balance d'un client est désormais visible par les autres entités du groupe.

## Partage de crédit client entre entités logiques

Si plusieurs de vos entités sont des subdivisions logiques d'une même société il est désormais possible d'utiliser le crédit d'une entité dans une autre.

Le transfert peut-être fait directement lorsqu'un paiement avec du crédit est effectué.

# Extraction d'un trop payé sur un panier

Il est désormais possible d'extraire un trop payé sur un panier en crédit disponible pour achats futurs. Depuis la modale de paiement vous pouvez

# Recherche de contacts

Il est désormais possible de filtrer les contacts par date de dernières ventes sur les vélos, moto-marines et autres types de produits identifiés en plus des véhicules terrestres à moteurs.

# Recherche de modèles

Vous pouvez désormais ajouter des tags sur vos modèles et utiliser ceux-ci lors de la recherche.

# Améliorations diverses

- Le nom du tiers est conservé sur chaque ligne dans l'export en comptabilité (ne numéro de tiers n'est conservé que sur la ligne du tiers).

# C'est corrigé

- Le status de paiement d'un panier se solde bien lorsqu'un trop payé est reversé en crédit.
- Lorsqu'une reprise est effecutée le prix de revente estimé s'il est défini est utilisé comme prix de vente à la place de 99999
- Il pouvait y avoir un soucis suivant un certain ordre de navigation dans la gestion des prêts de vélos/moto-marines ayant pour conséquence l'affichage des employés au lieu des véhicules dans la fenêtre de prêt.
