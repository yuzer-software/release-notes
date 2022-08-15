# Aout 2022 - Version 1.30.0

## Post-its sur les contacts

Vous pouvez désormais ajouter des post-its sur les contacts. Ceux-ci peuvent-être visible pour l'intégralité des entités du compte ou uniquement pour l'entité sur laquelle l'utilisateur est connecté.

Seuls les administrateurs ou comptables peuvent ajouter des notes visibles pour l'intégralité du compte.

Depuis la fiche contact cliquez sur le nouveau bouton _Post-it_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/contact-sticky-notes-1.png" width="550px"/>

Si votre droit ne vous permet que de créer des notes locales à l'entité sur laquelle vous êtes connectés la boite de dialogue suivante s'ouvre automatiquement sans sélection du type de note à créer.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/contact-sticky-notes-2.png" width="550px"/>

Vous pouvez choisir un style de note ainsi que définir son message.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/contact-sticky-notes-3.png" width="550px"/>

La note globale apparait avec un icone spécifique. Vous pouvez bien entendu éditer ou supprimer une note à l'aide des boutons disponibles.

## Affichage des paniers du client

Le statut de paiement ainsi que le montant total du panier ont été ajoutés à l'affichage d'un panier dans la liste.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/contact-baskets-1.png" width="550px"/>

Les paniers sont désormais filtrés par défaut afin de simplifier leur lisibilité et n'afficher que les paniers les plus utiles: Les panier non facturés, non annulés ou non soldés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/contact-baskets-2.png" width="550px"/>

Yuzer charge désormais les premiers paniers du client et vous propose, si celui-ci a d'autres paniers, de charger plus de paniers.

<div class="alert alert-info">
Les paniers sont récupérés en fonction de leur date de création et vous affiche dates du premier et dernier panier ainsi que le nombre de paniers filtrés.
</div>

Pour afficher les autres paniers vous pouvez cliquer sur l'icone de filtre et modifier la sélection par défaut.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/contact-baskets-3.png" width="550px"/>

## Gestion des paiements sur les paniers de reprises

Les paniers de reprises ont désormais, comme les autres paniers un statut de paiement permettant d'indiquer si un remboursement a été effectué auprès du client et de l'enregistrer.

<div class="alert alert-warning">
Pour ne pas impacter l'existant de manière pénalisante en terme de gestion nous avons pour chaque panier de reprise soldé ceux-ci automatiquement à traver les opérations suivantes:
 - Déplacement de balance en crédit
 - Utilisation du crédit comme paiement pour le panier (ce qui le remet dans la balance à l'identique).

Ces deux opérations permettent de créer un paiement assigné au panier afin de le solder sans impacter la balance finale de l'utilisateur.

</div>

## Gestion des paiements despuis la fiche de contact

Les paiements effectués sur une fiche de contact peuvent désormais être affectés simplement sur un ou plusieurs paniers.

L'ouverture de la boite de dialogue effectue un chargement de tous les paniers non-payés du contact et les affiche dans deux colonnes distinctes:

- Les paniers déjà facturés (qui devraient donc être prioritaire dans l'affectation du paiement)
- Les paniers non-facturés sur lesquels des avancent peuvent-être versées.

Lors du paiement vous pouvez visualiser et modifier:

- Le montant qui sera affecté sur la balance
- Le montant qui sera automatiquement transféré en crédit
- Le montant qui sera affecté sur certains paniers.

Le fonctionnement interne va effecuter un paiement classique en impactant la balance, puis déplacer tout ou partie du montant en crédit et enfin utiliser ce crédit en affectation sur différents paniers.

L'historique des ces opétations sera visible sur l'écran de balance client.

<div class="alert alert-info">
Cet écran sera amélioré dans la prochaine version afin de vous permettre de laisser Yuzer effectuer une répartition automatique des montants afin
- De solder une éventuelle balance négative externe
- D'assigner les montants en priorité aux plus vieux paniers facturés non-soldés puis sur les autres paniers non-soldés
- Et d'affecter le reste au crédit
- Tout en préservant le montant versé sur les paniers non-facturé (qui correspond à un montant séquestré dans le cadre de ceux-ci)
</div>

## Améliorations diverses

- Le montant de TVA est désormais affiché dans le bandeau de totaux du panier.

## Corrections

- La facturation d'un panier d'un montant de 0€ est désormais bien affichée comme payée.
- Lors de la génération d'un bon de commande de véhicule depuis un élément du catalogue le modèle est désormais bien affiché dans l'encadré.
