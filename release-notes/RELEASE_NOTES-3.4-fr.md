# Mai 2024 - Version 3.4.x

yuzSection Dossiers et ventes produits identifiés

## Nouveau CERFA

Nous avons ajouté le CERFA 13749-05 à la liste des CERFAs supportés dans le cadre d'une vente de véhicule neuf.

## Dossiers véhicules

Vous pouvez désormais configurer des seuils afin d'afficher des indicateurs dans la liste de véhicules.

TODO

## Expertises et galleries

Nous avons effectué une migration des photo-expertises vers le système de gallerie de documents déjà utilisé entre autre sur la fiche de contact et sur la fiche dossier.

L'expérience utilisateur se retrouve unifiée et cela permet de bénéficier de temps de chargements améliorés à la lecture.

## Traduction des catégories editeur

Si Yuzer normalise les catégories des produits vers une arborescence unique, les catégories transmise par l'éditeur du catalogue sont bien conservées. Si la plupart des fournisseurs utilisent des catégories lisibles par un humain, ce n'est pas le cas de BIHR par exemple qui utilise un système de codes catégories.

Cela engendrait des difficulté de lisibilité de celles-ci. Nous supportons désormais la transcription de ces codes vers une traduction (qui doit aussi être fournie par l'éditeur).

yuzSection Gestion des tâches et prêts

## Nouvelle vue des tâches

Une nouvelle vue est disponible pour l'affichage des tâches. Cette vue n'est pas actuellement interractive et va continuer de s'améliorer dans les versions à venir.

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

## Nouveaux catalogues

Les catalogues suivants ont été ajoutés depuis la dernière version

- ZBR Hohl
- VESPA
