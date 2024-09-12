# Septembre 2024 - Version 3.7.x

yuzSection Documents

## Envoi par email

||| Attention lors de la génération de documents un champ a désormais été clairement ajouté pour l'envoi ou non de celui-ci au client par email.

Dans les versions précédentes le fait qu'un email soit défini suffisait à l'envoi du document. Désormais une case à cocher détermine l'envoi ou non du document (celui-ci est activé par défaut).

![document email](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.7.0/document_mail.webp?w=500px)

## Recherche de documents

Vous pouvez désormais chercher un document directement depuis son identifiant dans la barre de recherche principale.

![document search](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.7.0/document_search.webp?w=800px)

Yuzer vous propose tous les type de documents générés sous le numéro donné.

||| Attention pour les identifiants de documents versionnés ne contiennent pas l'année ni le mois actuellement. Seule les deux dernières années sont alors recherchées dans ce cas. Les versions futures de Yuzer feront évoluer cet aspect.

Depuis le document vous pouvez accéder au panier en utilisant le bouton _retour_.

![document back to basket](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.7.0/document_back_to_basket.webp?w=500px)

yuzSection Analytiques

## Définition des périodes de références

Il est désormais possible de définir des périodes d'analyse fixe. En effet l'ensemble des périodes définies jusque là étaient des périodes glissantes qui dépendaient de la date actuelle.

![analytics periods](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.7.0/analytics_periods.webp?w=100%)

Le choix des dates n'est désormais possibles que lorsque qu'une période personalisée est choisie. Dans ce cas vous devez au préalable déterminer si la période est:

- **glissante** elle pourra se décaller chaque jour ou mois en fonction des dates choisies.
- **glissante à l'année** elle se décallera d'une année sur l'autre uniquement.
- **fixe** les dates resteront inchangée dans le temps.

## Tri par défaut

Il est désormais possible de configurer une colonne de tri par défaut sur une table analytique.

||| La configuration doit être effectuée pour chaque niveau d'analyse.

![analytics periods](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.7.0/analytics_sort.webp?w=800px)

Ce point est particulièrement utile dans les analyses de stock et stock et ventes ABC pour une meilleure lecture des données.

## Autres améliorations analytiques

- Les identifiants d'un produit sont désormais visibles en analytique dans le cadre d'un ordre de réparation et non uniquement dans le cadre d'une vente de véhicule.

- Dans une analyse de stock il est désormais possible d'exclure les produits qui ont une quantité de stock négative. Cela est recommandé pour les analyse ABC car ces stock invalides par naturent ont un impact négatif sur celle-ci.

yuzSection APIs

- Une API permettant de récupérer les stocks de produits identifiées (véhicules) est désormais disponible.
- Une API permettant de requêter un véhicule par VIN/Immat est désormais disponible. Attention cette API peut engendrer des coûts SIV qui vous seront facturés. Ne donnez pas son accès à n'importe qui.
- Plusieurs APIs orientées e-commerce et permettant de créer des paniers et d'enregistrer des paiements externes sont désormais disponibles.
- Il est désormais possible de définir un filtre par marque et catalogue sur les données accessibles par API dans le cadre des endpoints de Facture et Dossiers véhicules (stock/fermetures à date)

yuzSection Général

## Support des Mac ARM64

Une version spécifique est désormais disponible pour les Mac ARM64. En effet la version précédente utilisait la surcouche rosetta entrainant une pénalité de performance importante.

Pour installer celle-ci vous devez réinstaller yuzer. Rendez vous sur la page de la [documentation yuzer](https://yuzer.crisp.help/fr/article/installation-de-yuzer-hhoo2e/)

## Améliorations

- Les transfers internes entre 2 entités de la même société ont désormais un statut terminal (Transféré).
- En mode vue client les âges de stock et dates de réception dans la vue de liste des dossiers véhicules sont désormais cachés.
- Améliorations mineures sur la boite de dialogue d'envoi SMS.
- Et comme souvent de nombreuses améliorations invisibles pour une meilleure stabilité et performance du logiciel!

## Corrections

- Un groupe de facturation dans panier peut être annulé sans annuler l'ensemble du panier.
- Correction d'une erreur qui empêchait le passage automatique d'une cession contenant un forfait en comptabilité. L'écriture était bloquée dans les "écritures à valider" même si celle-ci était bien valide.
- Il n'est plus possible d'annuler un panier ayant un transfer qui n'aurait pas été retourné.
- Lors d'une réception d'un produit en quantité négative (retour) une erreur est affichée si une ligne de commande est associée. Ce comportement n'est en effet pas supporté aujourd'hui.
- Sur une réception les commandes de produits identifiés sont désormais automatiquement liées.
- La configuration des couleurs d'age de stock dossiers par fournisseur est désormais possible.
- Lorsqu'un prix était entré, l'utilisation du point pouvait dans certains cas réinitialiser le champ.

## Nouveaux catalogues

Les catalogues suivants ont été ajoutés depuis la dernière version

- CGN
