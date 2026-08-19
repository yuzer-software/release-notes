# Septembre 2026 - Version 5.4

yuzSection Cartes de fidélité Adelya

Nous avons développé l'intégration pour les cartes de fidélités Adelya.

Vous devez avoir un accès à `MOTO AXXE - Fidélité` ou `MAXXESS - Fidélité` sur votre entité (`Administration > Accès et réseaux > Mes accès`), puis vous pourrez créer une adhésion pour un contact.
Sur le panier, depuis la section d'ajout de lignes, vous verrez apparaitre une sélection de bons de fidélités que votre client peut bénéficier.

yuzSection Général

## Nouveautés

### Catalogue produits

- Il est maintenant possible de faire un import de produits à blanc.

### Comptabilité

- L'historique des fermetures de caisse sont maintenant triés par la date de l'ouverture.

### Panier

- Il est maintenant possible d'ajouter des tags sur les groupes de facturation de panier.

## Corrections

### Panier

- Correction de la mise à jour du solde dans l'encadré `Résumé` d'un panier de produit identifié.
- Le statut de stock du panier est désormais marqué comme "Transféré" lorsque le transfert a été effectué.
- Correction d'un problème avec l'annulation de facture contenant un pack de produits.
- Dans la fenêtre de paiement, correction pour ne pas afficher le montant de l'acompte restant quand cela n'a pas de sens (ex: annulation, etc.)

### Produits identifiés

- Correction de l'affectation du produit identifié aux tâches d'atelier lors de la création du panier.
- Correction de la mise à jour des états de dossier de produit identifié après l'édition d'une facture ou l'enregistrement d'un paiement.
- Le véhicule est maintenant bien rattaché à l'utilisateur/locataire lors de la clôture d'un dossier.

### Divers

- Dans l'analytique, correction du calcul des montants de remises sur les documents d'annulation.
- Correction pour afficher le libellé de l'emplacement de stock pour les entrepôts non configurés (inconnu, etc.)
- Correction permettant d'ouvrir l'application Yuzer en mode "Se souvenir de moi" lors d'une connextion via WebAuthn.
