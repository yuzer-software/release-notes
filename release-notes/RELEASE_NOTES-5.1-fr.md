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

Le statut d'exonération est utilisé par la fonction _rafraîchir les prix_: les taux de TVA sont réécrits à partir du catalogue.

## Reprises

Le résumé de la vente d'un panier de produit identifié avec reprises inclus une ligne explicite _financement des reprises_ (somme des Soldes restant dûs aux organismes de financement).

![trade-in-summary](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/trade-in-summary.webp?w=339px)

yuzSection Compabilité

# Mise en page de documents

En vue de la préparation de FactureX, nous avons mis à jour notre service de génération de PDF. A noter que la police du texte a légèrement changé. Par ailleur, nous avons améliorer de la mise en page en générale (alignements, etc) et nous avons également ajouter le libéllé de moyen de paiement sur les documents de factures.

# Annulation de factures d'acompte

Il est maintenant possible d'annuler les factures d'acompte.

yuzSection Général

## Améliorations

- Amélioration de la recherche des dossiers véhicules : les résultats n'étaient pas toujours triés par pertinence mais par date de création du dossier.
- Sur l'écran de paiement des paniers par la fiche contact, le total TTC des paniers tient compte des reprises.
- Ajout d'une aide à la saise du type de code-barres supporté dans l'édition de produit.
- Ajout d'un bouton pour copier la configuration des colonnes visibles du niveau précédent dans l'analytique.
  ![analytics-copy-config](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/analytics-copy-config.webp?w=984px)
- Simplification de la configuration des exports de journaux dans le menu `Comptabilité > Paramètres de comptabilité`. La configuration du format d'export et la saisie de la configuration ftp peuvent maintenant être sauvegardés séparément.
- Nous avons revu l'option de l'envoie d'email sur les formulaires de pré-édition de documents pour apporter plus de consistence entre l'édition des différents documents. L'option est maintenant toujours pré-cochée en fonction de l'email configuré par défaut sur la fiche cliente.
- Amélioration de la sélection automatique du numéro de téléphone par défaut: Lorsque le contact ne possède qu'un seul numéro de téléphone, celui-ci sera sélectionné par défaut lors de l'édition d'un document.
- Ajout de la possibilité de trier les lignes de réception par référence de produit.
- Ajout de la possibilité d'afficher le code-barres des produits dans l'analytique.
- Il est maintenant possible d'annuler une réception **RÉ-OUVERTE** quand toutes ses lignes sont annulées.
- Les lignes de factures d'achats sont maintenant ordonnées selon l'ordre d'insertion.

### Export de documents comptables

Vous pouviez paramétrer le nom du fichier en fonction de variables horaires, comme le numéro de la semaine. La date utilisée pour formatter le nom du fichier était le jour de l'export, c'est-à-dire le jour _suivant_ la période exportée. Si vous exportiez une semaine donnée, le nom du fichier avait donc le n° de la semaine _suivant_ la semaine exportée. Vous pouvez désormais choisir d'utiliser la date du début de la période exportée.

![billing-export-date](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.1/billing-export-date.webp?w=839px)

## Corrections

- Possibilité de retirer un dossier _annulé_ d'un panier
- Possibilité de payer le rachat de crédit d'une reprise sur un panier de pur reprise
- Statut de paiement d'un pur panier de reprise
- Correction du masquage du prix d'achat des équivalences dans la fiche produit.
- Correction de l'affichage du contact acheteur qui n'était pas toujours rafraichît après un changement.
- Correction d'un dysfonctionnement pouvant survenir sur l'écran du panier après la suppression de la dernière ligne d'un groupe.
- Affichage d'un message d'erreur dans le cas d'un échec de synchronisation lors de l'édition d'un reçu de vente.
- Les documents de panier n'était pas tous affichés dans le menu latérale après l'édition d'une annulation. C'est maintenant corrigé.
- Correction des bugs avec la configuration de filtres rapides dans la recherche de dossier de produits identifiés.
- Il est maintenant possible de supprimer les réservations de produits appartenant à un panier qui a été supprimé.
