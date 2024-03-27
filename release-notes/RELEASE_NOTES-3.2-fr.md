# Mars 2024 - Version 3.2.x

yuzSection Application mobile

Il est maintenant possible d'utiliser un scanner externe pour scanner des QR-codes de navigation (depuis la page principale ou le menu latéral).

Corrections :

- du choix de produit de même référence sur la page des paniers
- du choix d'assigné à une tâche (lorsqu'il y a beaucoup d'utilisateurs)
- de l'affichage des tâches en retard

yuzSection Produits

## Recherche de produits

La recherche de produits a été améliorée afin d'afficher dans l'ordre:

- Les produits correspondant le mieux à la requête et parmi ceux-ci:
  - Les produits en stock et indiqués comme obsolètes (1)
  - Les produits en stock
  - Les produits qui ne sont pas en stock mais indiqués comme disponible par le fournisseur
  - Les produits qui ne sont pas en stock mais indiqués comme disponible sous peu par le fournisseur
  - Les produits qui ne sont pas en stock mais dont la disponibilité n'est pas connue
  - Les produits obsolètes
- Les produits correspondant moins bien à la requête avec les même règles que précédemment pour le tri interne

![Liste produits](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/product-list.webp?w=100%)

(1) Un produit est obsolète s'il n'existe plus dans la dernière mise à jour du catalogue ou s'il est indiqué comme tel par l'éditeur du catalogue.

## Disponibilité réseau

Vous pouvez consulter la disponibilité réseau d'un produit directement depuis la recherche produit:

- Icône vert: le produit est disponible dans une autre entité de votre groupe (réseau interne)

![Icône vert](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/icon-green.webp?w=100%)

En cliquant sur le détail, vous pouvez consulter quelle entité de votre groupe possède du stock sur le produit en question.

![Dispo interne](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/avail-internal.webp?w=480px)

- Icône jaune: le produit est disponible dans une entité de votre réseau de redistribution (fournisseur interne Yuzer)

![Icône jaune](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/icon-yellow.webp?w=100%)

En cliquant sur le détail, vous pouvez consulter quelle entité de votre réseau de redistribution possède du stock. L'indicateur ne fourni pas de valeur précise dans ce cas.

![Dispo distribution](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/avail-distri.webp?w=480px)

- Icône orange: le produit est disponible dans une entité d'un de vos réseaux globaux (voir l'onglet Réseaux)

![Icône orange](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/icon-orange.webp?w=100%)

En cliquant sur le détail, vous pouvez consulter quelle entité de votre réseau de redistribution possède du stock. L'indicateur ne fourni pas de valeur précise dans ce cas.

![Dispo globale](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/avail-global.webp?w=480px)

yuzSection Dossiers

## Galeries de documents des dossiers

Nous avons ajouté la notion de galerie partagée sur un dossier.

Une galerie partagée est une galerie dont les documents seront accessibles à l'acheteur du véhicule. Cette fonctionnalité est aujourd'hui réservée aux clients utilisateurs de Yuzer (via la fonctionnalité de transfert).

- Votre galerie privée, reste toujours à la même place et tous les documents qui sont insérés dedans sont bien visible par votre entité uniquement.

![Galerie dossier](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/gallery/gallery_private.webp?w=480px)

- Une nouvelle galerie est ajoutée dans l'encadré de vente du véhicule. Celle-ci sera, dans le cas d'un transfert de véhicule par Yuzer, partagée avec l'entité à qui le véhicule sera transféré.

![Galerie de vente](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/gallery/gallery_sale.webp?w=480px)

- Finalement, si vous avez acheté un véhicule transféré via Yuzer, vous pouvez retrouver la galerie partagée par le vendeur dans l'onglet d'achat.

![Galerie d'achat](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/gallery/gallery_purchase.webp?w=480px)

Cette dernière est en lecture seule. Votre fournisseur peut supprimer ou modifier les documents qu'il y a mis, vous ne pouvez pas en ajouter ni en supprimer.
Il est cependant possible de copier les documents de la galerie d'origine dans votre propre galerie de dossier.

yuzSection Analytiques

L'accueil et la gestion des différents tableaux de bord en analytique a été revue afin de

- vous permettre d'organiser ceux-ci dans une arborescence.
- augmenter le nombre de configurations à votre disposition.

![Analytiques configurations](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/dashboards-list.webp?w=100%)

Vous pouvez naviguer dans l'arborescence des configurations, gérer vos onglets ou voir les configurations héritées (en lecture seule) comme avant.

## Créer un dossier

Pour créer un nouveau dossier il vous suffit de cliquer sur le bouton suivant

![Ajouter un dossier](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/add-folder.webp?w=64px)

|| La création d'un nouveau dossier ne peut se faire que dans la configuration de l'entité actuelle.

## Créer un nouveau tableau de bord

Pour créer un nouveau tableau de bord, dans le dossier en cours, il vous suffit de cliquer sur le bouton suivant

![Ajouter un tableau de bord](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/add-dashboard.webp?w=64px)

|| La création d'un nouveau tableau de bord ne peut se faire que dans la configuration de l'entité actuelle.

## Dupliquer un tableau de bord

Vous pouvez dupliquer un tableau de bord, de votre entité ou d'une entité héritée, à travers le bouton suivant

![Dupliquer ](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/duplicate-dashboard.webp?w=48px)

|| La création d'un nouveau tableau de bord ne peut se faire que dans la configuration de l'entité actuelle.

## Déplacer un tableau de bord

En plus de cela il est possible de réorganiser les onglets ou tableaux de bord en drag and drop. Afin de déplacer un tableau de bord d'un dossier à un autre, vous devez afficher le navigateur parallèle à l'aide du bouton suivant

![Ouvrir la navigation parallèle](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/move-dashboards.webp?w=48px)

Vous pouvez alors naviguer dans le dossier de destination puis glisser/déposer un tableau de bord d'une liste à l'autre.

![Déplacer un tableau de bord](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/move-dashboard-list.webp?w=680px)

yuzSection Réseaux

Nous avons ajouté une nouvelle fonctionnalité de _réseaux_ afin de permettre un partage des disponibilités produits dans un réseau donné en temps réel.

yuzSection Commandes véhicules intra-Yuzer

Lorsque votre fournisseur utilise le réseau Yuzer afin de gérer ses prises de commandes de véhicules, ou pour passer vos commandes par le biais de votre réseau Yuzer (interne ou de distribution), vous pouvez désormais utiliser l'outil de synchronisation des dossiers et commandes.

![Déplacer un tableau de bord](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/dealer-file-order/waiting-order.webp?w=100%)
_Sélectionnez un fournisseur utilisant Yuzer afin de pouvoir accéder à la fonctionnalité._

Une fois ouvert, l'outil vous permet de

- valider que chaque dossier _A commander_ ou _Commandé_ a bien une ligne de commande correspondante dans le système de gestion de commande.
- créer de nouvelles commandes, soit déjà placées par un autre biais que Yuzer _Sans commande fournisseur_. Soit en créant un panier de commande directement chez votre fournisseur _Nouvelle commande au fournisseur_.

![Déplacer un tableau de bord](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/dealer-file-order/sync.webp?w=680px)

Des dossiers pourront alors être automatiquement mis à jour (leur statut passé de _A commander_ à _Commandé_) ou créés.

Une fois validé, un écran de résumé des actions est alors affiché.

![Déplacer un tableau de bord](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/dealer-file-order/summary.webp?w=680px)

Vous pouvez ensuite consulter vos commandes puis, une fois le véhicule transféré par votre fournisseur, le réceptionner directement par le module de transfert et réception. Cela vous permettra de bénéficier des galeries partagées si votre fournisseur en a attaché à la vente!

yuzSection Général

## Action par défaut pour les transferts

Vous pouvez configurer les actions possibles pour vos transferts: Livrer et envoyer, Livrer, ou avoir le choix. Dans `Administration > Gestion commerciale > Configurer > Configuration Commerciale`, configurez "Action lors de la livraison d'un transfert" :

| Action                     | Conséquence sur la fenêtre de stock                                                                                                                  |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Emballer et envoyer        | ![Emballer et envoyer](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/general/transfer-send.webp?w=330px) |
| Emballer                   | ![Emballer](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/general/transfer-deliver.webp?w=330px)         |
| Toujours poser la question | ![Au choix](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/general/transfer-choose.webp?w=330px)          |

## Améliorations diverses

- Durant les trois jours précédents l'anniversaire d'un contact, un icône de gâteau d'anniversaire sera affiché sur le détail d'un contact.
- Sur la page de détail d'un contact, les dates de création et modification sont désormais affichées à côté de la personne ayant effectué la création / dernière modification
- Sur l'historique des paiements d'un panier le moyen de paiement exact est désormais affiché.
- A la création d'un produit qui existe déjà, Yuzer vous redirige vers la page du produit existant.
- Amélioration de la fusion de catalogue concernant les produits qui ne sont plus en stock mais qui ont été en stock. Il est désormais plus simple de les ignorer.

## Corrections diverses

- Les marges sur l'impression d'un arrêté de caisse sont désormais corrigées.
- Correction des libellés de planche et étagère qui étaient inversés sur la page d'export du stock.

yuzSection Export facturation

L'automate d'export des données de facturation a été amélioré afin de permettre la configuration:

- L'agrégation des données par produit (total des quantités et CA au lieu du détail de facturation)

![Agrégation](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/invoice-export/aggregate.webp?w=330px)

- La planification d'exécution

![Planification](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/invoice-export/plan.webp?w=330px)

- Le format d'export (Il est désormais possible d'ajouter un export au format xlsx)

![Format](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/invoice-export/format.webp?w=330px)

yuzSection Abonnement Yuzer

Nous nous rapprochons de la mise en place de la facturation et prélèvement mensuel automatiques pour la souscription à votre abonnement Yuzer.

Afin que cette mise en place se passe le plus simplement possible nous avons mis à jour la page de gestion de contact afin de vous permettre de configurer les licences actives pour vos différents utilisateurs.

Seul un administrateur peut ajouter ou supprimer une licence pour un utilisateur.

Les licences disponibles sur votre compte seront configurées par un de nos commerciaux qui ajoutera les différents éléments d'engagement.

- Votre engagement de licences compte comme un nombre minimal de licences.
- Vous pouvez à tout moment ajouter une licence à un nouvel utilisateur sans limite maximale.
- Toute licence ajoutée à un utilisateur sur un mois donnée est configurée sans limite de temps.
- Vous pouvez à tout moment supprimer la licence d'un utilisateur. Celle-ci reste alors active jusqu'à la fin du mois commencé.

## Visualiser les licences d'un utilisateur

Depuis la page de détail d'un utilisateur vous pouvez visualiser ses licences:

![licences](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/licenses/licenses-user-page.webp?w=100%)

Cliquez sur Editer pour ouvrir la page de configuration des licences:

![licences update](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/licenses/licenses-update.webp?w=100%)

||| Attention sauvegarder mettra a jour les licences et entrainera une modification de la facturation à tout ajout de licence.

## Départ d'un employé

Au départ d'un employé vous devez toujours désactiver l'utilisateur afin que celui-ci ne puisse plus se connecter. Désactiver les licences de celui-ci ne l'empêcheront pas de se connecter avant la fin du mois.

## Mise en place de la validation de licence et facturation automatique

La mise en place de l'automatisation de facturation de votre abonnement ainsi que les vérifications de licences à la connexion d'un utilisateur seront activées à partir du 22 avril. Pensez à bien valider que chacun de vos utilisateur a ses licences correctement configurées avant cette date.

La facture d'abonnement sera établie à chaque début de mois et portera sur le mois précédent elle inclura:

- Les facturation de licences actives sur le mois précédent (une licence désactivée en cours de mois sera donc facturée)
- Les éventuelles consommations au click (SMS, SIV)
