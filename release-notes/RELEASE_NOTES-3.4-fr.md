# June 2024 - Version 3.4.x

yuzSection Dossiers et ventes produits identifiés

## Nouveau CERFA

Nous avons ajouté le CERFA 13749-05 à la liste des CERFAs supportés dans le cadre d'une vente de véhicule neuf.

## Dossiers véhicules

Vous pouvez désormais configurer des seuils afin d'afficher des indicateurs dans la liste de véhicules.

Rendez vous dans votre liste de produits identifiés puis _Configurer_ et _Tranche d’âge pour les nouveaux produits identifiés_ ou _Tranche d’âge pour les produits identifiés d'ocassion_ en fonction des seuils que vous souhaitez configurer.

![age display menu](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/df-age-menu.webp?w=100%)

Vous pouvez alors configurer des coloris en fonction de l'age des dossiers.

![age display settings](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/df-age-settings.webp?w=100%)

L'âge peut-être calculé depuis la date de facturation du fournisseur ou d'entrée dans votre stock du véhicule (nombre de jour depuis cette date), ou en fonction de la date limite de paiement au fournisseur (nombre de jours restants avant cette date).

| Nous avons choisi des couleurs mettant bien en valeur le sens de la fonctionnalité. Si vous ne souhaitez pas que vos clients, en regardant votre écran puissent visualisez des couleurs rouges ou jaunes par exemple vous pouvez librement modifier le code couleur.

Une fois configurés vous pourrez visualisez les indicateurs directement sur la liste de véhicules:

![age display settings](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/df-age-list.webp?w=360px)

Ainsi que dans le détail d'une fiche dossier:

![age display settings](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/df-age-detail.webp?w=400px)

## Expertises et galeries

Nous avons effectué une migration des photo-expertises vers le système de galerie de documents déjà utilisé entre autre sur la fiche de contact et sur la fiche dossier.

L'expérience utilisateur se retrouve unifiée et cela permet de bénéficier de temps de chargements améliorés à la lecture.

yuzSection Gestion des tâches et prêts

## Nouvelle vue des tâches

Une nouvelle vue de calendrier, _Timeline_ est disponible pour l'affichage des tâches. Elle vous permet de mieux planifier les tâches avec une vision sur une longue durée.
Afin de l'afficher choisissez la vue correspondante dans le menu:

![view choice](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/timeline-view-choice.webp?w=300px)

Vous pouvez choisir la période à afficher à l'aide du sélecteur de dates:

![date choice](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/timeline-date-choice.webp?w=400px)

La période sélectionnée peut alors être visualisée.

![vue](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.4.0/timeline-display.webp?w=100%)

|| Cette vue est proposée en beta et est actuellement non interractive. Si vous pouvez cliquer sur une tâche pour accéder à ses informtions vous ne pouvez pas ajouter de nouvelle tâche ou glisser-déposer des tâches existantes pour les planifier. Nous améliorerons ces éléments sur les version à venir.

||| Aujourd'hui le nombre de tâche affiché est limité à 1000. L'affichage d'une longue période sur laquelle de trop nombreuses tâches seraient à afficher peut entrainer ralentissements ou affichage partiel du contenu. Une amélioration est en cours de dévelopement pour résoudre ce type de problèmes.

yuzSection Général

## Améliorations

- Nous avons revu le poids donné aux disponibilité de stock pour que la recherche affiche le résultat le plus pertinent possible, nottament lors d'une recherche sur un identifiant produit.
- L'indicateur de disponibilité réseau des produits identifiés est désormais visibles dans la vue de catalogue, et non uniquement dans la vue de dossiers par produits.
- Vous pouvez désormais filtrer les paniers qui ont été créé automatiquement par Yuzer. Dans le cadre d'une commande effectuée par une autre entité connectée par exemple.
- Les groupes de cessions dans le cadre d'une vente de véhicule ne sont plus affichés par défaut sur une proposition commerciale ou bon de commande. Vous pouvez toujours les rajouter si vous le souhaitez.
- L'édition de stock a vu sa performance légèrement améliorée.

## Corrections

- La création d'un nouveau modèle depuis un panier fonctionne que le panier soit facturé ou non et redirige bien sur le modèle créé.
- La conversion d'un surplus de paiement vers un crédit client sur la boite de dialogue de paiements du panier met désormais bien à jour le montant restant.

yuzSection Catalogues produits et interconnexions

## Améliorations et corrections

- Les statuts des disponibilités produits chez BIHR ont été corrigées et sont désormais mise à jour chaque nuit.
- Nous avons ré-adapté notre code de connexion aux systèmes KTM suite à des changements non communiqués ni planifiés de leur part. Les éclatés et catalogues véhicules sont à nouveau mis à jour.

## Traduction des catégories editeur

Si Yuzer normalise les catégories des produits vers une arborescence unique, les catégories transmise par l'éditeur du catalogue sont bien conservées. Si la plupart des fournisseurs utilisent des catégories lisibles par un humain, ce n'est pas le cas de BIHR par exemple qui utilise un système de codes catégories.

Cela engendrait des difficulté de lisibilité de celles-ci. Nous supportons désormais la transcription de ces codes vers une traduction (qui doit aussi être fournie par l'éditeur).

## Nouveaux catalogues

Les catalogues suivants ont été ajoutés depuis la dernière version

- ZBR Hohl
- VESPA
- BRP
  - Seadoo
  - Can-am
