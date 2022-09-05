# Sept 2022 - Version 1.30.5

## Corrections

- La date des paiements de chèque différé s'affichait avec un mois de décalage dans le fichier d'export de compta.

# Aout 2022 - Version 1.30.0

## Post-its sur les contacts

Vous pouvez désormais ajouter des post-its sur les contacts. Ceux-ci peuvent-être visible pour l'intégralité des entités du compte ou uniquement pour l'entité sur laquelle l'utilisateur est connecté.

Seuls les administrateurs ou comptables peuvent ajouter des notes visibles pour l'intégralité du compte.

Depuis la fiche contact cliquez sur le nouveau bouton _Post-it_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/contact-sticky-notes-1.png" width="360px"/>

Si votre droit ne vous permet que de créer des notes locales à l'entité sur laquelle vous êtes connectés la boite de dialogue suivante s'ouvre automatiquement sans sélection du type de note à créer.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/contact-sticky-notes-2.png" width="480px"/>

Vous pouvez choisir un style de note ainsi que définir son message.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/contact-sticky-notes-3.png" width="420px"/>

La note globale apparait avec un icône spécifique. Vous pouvez bien entendu éditer ou supprimer une note à l'aide des boutons disponibles.

## Affichage des paniers du client

Le statut de paiement ainsi que le montant total du panier ont été ajoutés à l'affichage d'un panier dans la liste.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/contact-baskets-1.png" width="400px"/>

Les paniers sont désormais filtrés par défaut afin de simplifier leur lisibilité et n'afficher que les paniers les plus utiles: Les panier non facturés, non annulés ou non soldés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/contact-baskets-2.png" width="420px"/>

Yuzer charge désormais les premiers paniers du client et vous propose, si celui-ci a d'autres paniers, de charger plus de paniers.

<div class="alert alert-info">
Les paniers sont récupérés en fonction de leur date de création et vous affiche dates du premier et dernier panier ainsi que le nombre de paniers filtrés.
</div>

Pour afficher les autres paniers vous pouvez cliquer sur l'icône de filtre et modifier la sélection par défaut.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/contact-baskets-3.png" width="420px"/>

## Gestion des paiements sur les paniers de reprises

Les paniers de reprises ont désormais, comme les autres paniers un statut de paiement permettant d'indiquer si un remboursement a été effectué auprès du client et de l'enregistrer.

<div class="alert alert-warning">
Lisez attentivement les informations suivantes qui décrivent la migration opérée afin de solder les reprises pré-1.30
</div>

Dans les versions précédentes de Yuzer les remboursement client sur les reprises sèches n'étaient pas liés au panier de reprise. Vous avez donc dans la plupart des cas:

- soit remboursé le client par un paiement négatif sur la fiche client.
- soit extrait le montant en crédit pour utiliser celui-ci sur un autre panier.

Afin de bien noter le panier comme soldé et étant donné qu'il pouvait-être complexe de retrouver les opération sus-mentionnées nous avons effectué les opérations suivantes:

- Génération d'une extraction en crédit de la valeur de la reprise avec le message suivant:
  - Correction système: Paiement de la reprise au client par génération de crédit.
- Puis une remise dans la balance de ce crédit afin que la migration n'ait aucun impact sur les opérations que vous auriez déjà effectué:
  - Correction système: Mise en balance du crédit pour annuler le paiement automatique par crédit (release note v1.30).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.30.0/credit-payment-1.png" width="100%"/>

Ces deux opérations n'ont aucune implication comptable et permettent, sans aucun impact sur la balance, de solder tous les paniers de reprises sèche dont le bon d'achat a été édité avant la version 1.30.

Dans le cas ou vous n'auriez pas déjà remboursé le client sur une reprise pré-1.30 (ni en paiement négatif, ni via crédit) vous devrez effectuer les opérations manuelles décrites ci-dessous.

Pour les reprises effectuées par la suite vous pourrez utiliser les paiements sur le panier directement afin de rembourser votre client ou de générer du crédit pour une utilisation sur un autre panier de vente.

## Gestion des paiements depuis la fiche de contact

Les paiements effectués sur une fiche de contact peuvent désormais être affectés simplement sur un ou plusieurs paniers.

L'ouverture de la boite de dialogue effectue un chargement de tous les paniers non-payés du contact et les affiche dans deux colonnes distinctes:

- Les paniers déjà facturés (qui devraient donc être prioritaire dans l'affectation du paiement)
- Les paniers non-facturés sur lesquels des avances peuvent-être versées.

Lors du paiement vous pouvez visualiser et modifier:

- Le montant qui sera affecté sur la balance
- Le montant qui sera automatiquement transféré en crédit
- Le montant qui sera affecté sur certains paniers.

Le fonctionnement interne va effectuer un paiement classique en impactant la balance, puis déplacer tout ou partie du montant en crédit et enfin utiliser ce crédit en affectation sur différents paniers.

L'historique des ces opérations sera visible sur l'écran de balance client.

<div class="alert alert-info">
Cet écran sera amélioré dans la prochaine version afin de vous permettre de laisser Yuzer effectuer une répartition automatique des montants afin
<ul>
  <li>De solder une éventuelle balance négative externe</li>
  <li>D'assigner les montants en priorité aux plus vieux paniers facturés non-soldés puis sur les autres paniers non-soldés</li>
  <li>D'affecter le reste au crédit</li>
  <li>Tout en préservant le montant versé sur les paniers non-facturé (qui correspond à un montant séquestré dans le cadre de ceux-ci)</li>
</ul>
</div>

## Améliorations diverses

- Le montant de TVA est désormais affiché dans le bandeau de totaux du panier.

## Corrections

- La facturation d'un panier d'un montant de 0€ est désormais bien affichée comme payée.
- Lors de la génération d'un bon de commande de véhicule depuis un élément du catalogue le modèle est désormais bien affiché dans l'encadré.
