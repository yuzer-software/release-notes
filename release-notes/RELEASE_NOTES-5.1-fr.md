# Mai 2026 - Version 5.1

yuzSection Panier

## Groupe de facturation

### Changement de contact ou de contact de facturation

Lors du changement de contact d'un groupe de facturation, si le nouveau contact a un programme de fidélité applicable automatiquement, alors celui-ci est bien ajouté au groupe de facturation. Si un programme de fidélité était déjà en place, vous avez la possibilité le supprimer.

![basket-contact-change-loyalty-modal](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/basket-contact-change-loyalty-modal.webp?w=502px)

Par ailleurs, les règles sur l'exonération de TVA du contact sont aussi bien appliquées.

### Exonération de TVA

Le groupe de facturation est désormais doté d'un statut d'exonération de TVA.

![billing-group-ex-vat-status](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/bg-ex-vat-status.webp?w=132px)

Si le statut d'exonération du contact change (ou sur les paniers existants), vous pourrez mettre à jour celui du groupe de facturation, ce qui aura pour effet de recalculer les prix.

![billing-group-ex-vat-mismatch](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/bg-ex-vat-mismatch.webp?w=375px)

Un warning vous informe si une ligne ne semble pas correspondre à ce statut.

![billing-group-ex-vat-warning](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/bg-ex-vat-warning.webp?w=248px)


Le statut d'exonération est utilisé par la fonction _rafraîchir les prix_ : les taux de TVA sont réécrits à partir du catalogue.

## Reprises

Le résumé de la vente d'un panier de produit identifié avec reprises inclus une ligne explicite _financement des reprises_ (somme des Soldes restant dûs aux organismes de financement).

![trade-in-summary](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/trade-in-summary.webp?w=339px)


yuzSection Général

## Améliorations

- Amélioration de la recherche des dossiers véhicules : les résultats n'étaient pas toujours triés par pertinence mais par date de création du dossier.
- Sur l'écran de paiement des paniers par la fiche contact, le total TTC des paniers tient compte des reprises.

## Corrections

- Possibilité de retirer un dossier _annulé_ d'un panier
- Possibilité de payer le rachat de crédit d'une reprise sur un panier de pur reprise
- Statut de paiement d'un pur panier de reprise
- Analyse de stock
