# Mars 2024 - Version 3.2.x

yuzSection Produits

## Recherche de produits

La recherche de produtis a été améliorée afin d'afficher dans l'ordre:

- Les produits correspondant le mieux à la requête et parmis ceux-ci:
  - Les produits en stock et indiqués comme obsolètes (1)
  - Les produits en stock
  - Les produits qui ne sont pas en stock mais indiqués comme disponible par le fournisseur
  - Les produits qui ne sont pas en stock mais indiqués comme disponible sous peu par le fournisseur
  - Les produits qui ne sont pas en stock mais dont la disponibilité n'est pas connue
  - Le produits obsolètes
- Les produits correspondant moins bien à la requête avec les même règles que précédamment pour le tri interne

![Liste produits](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/products/product-list.webp?w=100%)

1 Un produit est obsolète s'il n'existe plus dans la dernière mise à jour du catalogue ou s'il est indiqué comme tel par l'éditeur du catalogue.

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

Nous avons ajouté la notion de gallerie partagée sur un dossier.

Une gallerie partagée est une gallerie dont les documents seront accessibles à l'acheteur du véhicule. Cette fonctionalité est aujourd'hui réservée aux clients utilisateurs de Yuzer (via la fonctionalité de transfer).

- Votre gallerie privée, reste toujours à la même place et tous les documents qui sont insérés dedans sont bien visible par votre entité uniquement.

![Gallerie dossier](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/gallery/gallery_private.webp?w=480px)

- Une nouvelle gallerie est ajoutée dans l'encadré de vente du véhicule. Celle-ci sera, dans le cas d'un transfer de véhicule par Yuzer, partagée avec l'entité à qui le véhicule sera transféré.

![Gallerie de vente](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/gallery/gallery_sale.webp?w=480px)

- Finalement, si vous avez acheté un véhicule transféré via Yuzer, vous pouvez retrouver la gallerie partagée par le vendeur dans l'onglet d'achat.

![Gallerie d'achat](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/gallery/gallery_purchase.webp?w=480px)

Cette dernière est en lecture seule. Votre fournisseur peut supprimer ou modifier les documents qu'il y a mis, vous ne pouvez pas en ajouter ni en supprimer.
Il est cependant possible de copier les documents de la gallerie d'origine dans votre propre gallerie de dossier.

yuzSection Analytiques

L'acceuil et la gestion des différents tableaux de bord en analytique a été revue afin de

- vous permettre d'organiser ceux-ci dans une arborescence.
- augmenter le nombre de configurations à votre disposition.

![Analytiques configurations](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/analytics/dashboards-list.webp?w=100%)

Vous pouvez naviguer dans l'arborescence des configurations, gérer vos onglets ou voire les configurations héritées (en lecture seule) comme avant.

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

Nous avons ajouté une nouvelle fonctionalité de _réseaux_ afin de permettre un partage des disponibilités produits dans un réseau donné en temps réel.

yuzSection Général

## Action par défaut pour les transferts

Vous pouvez configurer les actions possibles pour vos transferts: Livrer et envoyer, Livrer, ou avoir le choix. Dans `Administration > Gestion commerciale > Configurer > Configuration Commerciale`, configurez "Action lors de la livraison d'un transfert" :

| Action                     | Conséquence sur la fenêtre de stock                                                                                                                  |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Emballer et envoyer        | ![Emballer et envoyer](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/general/transfer-send.webp?w=330px) |
| Emballer                   | ![Emballer](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/general/transfer-deliver.webp?w=330px)         |
| Toujours poser la question | ![Au choix](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/general/transfer-choose.webp?w=330px)          |

yuzSection Abonnement Yuzer et licenses

Nous nous rapprochons de la mise en place de la facturation et prélèvement mensuel automatiques pour la souscription à votre abonnement Yuzer.

Afin que cette mise en place se passe le plus simplement possible nous avons mis à jour la page de gestion de contact afin de vous permettre de configurer les licenses actives pour vos différents utilisateurs.

Seul un administrateur peut ajouter ou supprimer une license pour un utilisateur.

Les licenses disponibles sur votre compte seront configurées par un de nos commerciaux qui ajoutera les différents éléments d'engagement.

- Votre engagement de licenses compte comme un nombre minimal de licenses.
- Vous pouvez à tout moment ajouter une license à un nouvel utilisateur sans limite maximale.
- Toute license ajoutée à un utilisateur sur un mois donnée est configurée sans limite de temps.
- Vous pouvez à tout moment supprimer la license d'un utilisateur. Celle-ci reste alors active jusqu'à la fin du mois commencé.

## Visualiser les licenses d'un utilisateur

Depuis la page de détail d'un utilisateur vous pouvez visualiser ses licenses:

![Licenses](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/licenses/licenses-user-page.webp?w=100%)

Cliquez sur Editer pour ouvrir la page de configuration des licenses:

![Licenses update](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/licenses/licenses-update.webp?w=100%)

||| Attention sauvegarder mettra a jour les licenses et entrainera une modification de la facturation à tout ajout de license.

## Départ d'un employé

Au départ d'un employé vous devez toujours désactiver l'utilisateur afin que celui-ci ne puisse plus se connecter. Désactiver les licenses de celui-ci ne l'empêcheront pas de se connecter avant la fin du mois.

## Mise en place de la validation de license et facturation automatique

La mise en place de l'automatisation de facturation de votre abonnement ainsi que les vérifications de licenses à la connexion d'un utilisateur seront activées à partir du 22 avril. Pensez à bien valider que chacun de vos utilisateur a ses licenses correctements configurées avant cette date.

La facture d'abonnement sera établie à chaque début de mois et portera sur le mois précédent elle incluera:

- Les facturation de licenses actives sur le mois précédent (une license désactivée en cours de mois sera donc facturée)
- Les éventuelles consommations au click (SMS, SIV)
