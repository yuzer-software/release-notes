# Août 2024 - Version 3.7.x

yuzSection Facturation et autres documents

|| Attention lors de la génération de documents un champ a désormais été clairement ajouté pour l'envoi ou non de celui-ci au client par email.

Dans les versions précédentes le fait qu'un email soit défini suffisait à l'envoi du document.

Il faut désormais clairement valider l'envoi (activé par défaut)

yuzSection Analytiques

- Les identifiants d'un produit sont désormais visibles en analytique dans le cadre d'un ordre de réparation et non uniquement dans le cadre d'une vente de véhicule.

- Il est désormais possible de définir des périodes d'analyse fixe. En effet l'ensemble des périodes définies jusque là étaient des périodes glissantes qui dépendaient de la date actuelle.

- Dans une analyse de stock il est désormais possible d'exclure les produits qui ont une quantité de stock négative. Cela est recommandé pour les analyse ABC car ces stock invalides par naturent ont un impact négatif sur celle-ci.

- Il est désormais possible de configurer une colonne de tri par défaut sur une table analytique. La configuration doit bien entendu être effectuée pour chaque niveau d'analyse.

yuzSection APIs

- Une API permettant de récupérer les stocks de produits identifiées (véhicules) est désormais disponible.
- Plusieurs APIs orientées e-commerce et permettant de créer des paniers et d'enregistrer des paiements externes sont désormais disponibles.
- Il est désormais possible de définir un filtre par marque et catalogue sur les données accessibles par API dans le cadre des endpoints de Facture et Dossiers véhicules (stock/fermetures à date)

yuzSection Général

## Améliorations

- Les transfers internes entre 2 entités de la même société ont désormais un statut terminal (Transféré).
- En mode vue client les âges de stock et dates de réception dans la vue de liste des dossiers véhicules sont désormais cachés.
- Et comme souvent de nombreuses améliorations qui ne sont pas visibles mais améliorent la stabilité et performance du logiciel!

## Corrections

- Un groupe de facturation dans panier peut être annulé sans annuler l'ensemble du panier.
- Correction d'une erreur qui empêchait le passage automatique d'une cession contenant un forfait en comptabilité. L'écriture était bloquée dans les "écritures à valider" même si celle-ci était bien valide.
- Il n'est plus possible d'annuler un panier ayant un transfer qui n'aurait pas été retourné.
- Lors d'une réception d'un produit en quantité négative (retour) une erreur est affichée si une ligne de commande est associée. Ce comportement n'est en effet pas supporté aujourd'hui.
- Sur une réception les commandes de produits identifiés sont désormais automatiquement liées.

## Nouveaux catalogues

Les catalogues suivants ont été ajoutés depuis la dernière version

- CGN
