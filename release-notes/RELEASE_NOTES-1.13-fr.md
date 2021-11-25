# Novembre 2021 - Version 1.13.0

Améliorations diverses:

- Lors de l'édition d'une facture la date de livraison est automatiquement configurée sur la date du jour.
- Dans les écrans de configuration de l'entité, amélioration de la configuration des **CVG** et des autres **messages** inclus dans les documents (factures, propositions commerciales, etc.)
- Vous pouvez désormais rechercher un produit dans la liste de produits à l'aide d'un code barre.
- Vous pouvez désormais ajouter une photo expertise à un panier de produits identifiés/vélos.
- Nous avons ajouté une nouvelle catégorie "vélo enfants (jouets)" pour les vélos enfant bas-age ne nécessitant pas d'identification (APIC).
- Dans un détail de réception, lorsqu'un produit est affecté à un client il est possible d'accéder rapidement à la fiche contact de celui-ci (icone personne).
- Nous avons ajouté la possiblité de renseigner l'IBAN ainsi que l'origine (moteur de recherche, salon etc.) sur une fiche contact.
- Il est désormais possible de sélectionner une période sur le widget de main d'oeuvre comme il était possible de le faire sur le widget de chiffre d'affaire.

# Facture Proforma

Yuzer gère maintenant un nouveau type de document : les factures **proforma**.

On peut éditer une facture **proforma** depuis un panier de vente, en cliquant sur le bouton "_éditer_" puis en choississant le document "_facture proforma_".

L'édition d'une facture **proforma** n'a aucun impact sur les numérotations des factures, ni sur la comptabilité de l'entreprise.

<div class="alert alert-warning">
Pensez à bien configurer les CGV et messages pour les factures proforma dans vos paramètres. Seul l'administrateur de la plateforme peut effectuer cette configuration.
</div>

# Carte cadeau

Il est désormais possible de gérer des cartes cadeaux dans Yuzer. Assurez vous au préalable de bien avoir configuré dans votre plan comptable un compte pour les cartes cadeaux (_46700000_ en général).

## Configuration d'une carte cadeau

La première étape pour accepter les cartes cadeaux est de configurer un moyen de paiement de type carte cadeau.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/gift-card-cfg.png" height="400"/>

Vous pouvez choisir de laisser yuzer générer les numéros de séquences des cartes, ou utiliser des cartes cadeaux existantes dont les numéros ne sont pas générés par yuzer.

Si vous n'avez pas de cartes existantes ou afin de renouveller votre stock de cartes il est recommandé de laisser Yuzer générer les numéros.
Notez que vous pouvez avoir plusieurs moyen de paiement de type carte cadeau, il est donc possible de définir un moyen de paiement permettant d'écouler votre stock de cartes existant puis de définir un nouveau moyen de paiement afin de générer de nouvelles cartes.

## Création d'un produit de carte cadeau

La vente de carte cadeau se fait à travers l'ajout d'un produit dont la catégorie est "Services et Taxes / Carte cadeau". La première étape consiste donc à créer ce produit dans le catalogue local de votre société depuis l'onglet magasin.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/add-product.png" height="140"/>

Lors de la création du produit les prix peuvent-être laissés à zero car la valeur de la carte cadeau sera quoi qu'il arrive définie lors de l'ajout de celle-ci au panier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/new-gift-card-product.png" height="140"/>

La création d'un produit de carte cadeau vous permet de mettre en magasin des pochettes de cartes cadeaux qui ne contiendraient pas la carte, ou ne laisseraient pas le code barre de la carte visible. Seule le code barre du produit étant visible sur celle-ci.

## Création d'un batch de cartes cadeau

Lorsque les numéros de cartes sont créés par Yuzer vous devrez créer un lot de cartes (opération qui peut-être effecutée plusieurs fois).

Dans l'onglet _administration_ le menu _Cartes fidélités_ est désormais _Cartes cadeaux et fidélités_ et dispose de deux sous-menus vous permettant de gérer chaque type de carte. Rendez vous donc dans le sous menu _Cartes cadeaux_.

Vous retrouvez ici la liste des cartes cadeaux configurées en moyen de paiement:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/gift-card-list.png" width="100%"/>

Sélectionnez la carte cadeau pour laquelle générer un lot de cartes et cliquez sur le bouton **+** à droite.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/gift-card-batches.png" width="100%"/>

Vous devez préciser le nombre de carte cadeau à générer ainsi qu'un montant optionnel sur la carte cadeau. Dans le cas ou le montant n'est pas précisé, celui sera affecté au moment de la vente de la carte avec le montant de celle-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/gift-card-new-batch.png" height="160"/>

La liste des cartes cadeaux générées est alors affichée. Vous pouvez l'exporter en csv ou xlsx afin de pouvoir, si vous le souhaitez, la transmettre à un service d'impression de cartes PVC.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/gift-card-batch-cards.png" width="100%"/>

Comme vous pouvez le constater les cartes générées ne sont pas activées et il est impossible de les utiliser comme moyen de paiement.

## Vente et activation d'une carte cadeau

Lors de la vente du produit carte cadeau (qui peut-être ajouté au panier par identifiant, en scannant son code barre, ou par le catalogue) une boite de dialogue s'ouvre afin que vous définissiez la carte cadeau à associer à la vente.
Les cartes cadeaux sont en effet désactivées lors de leur création et activées unitairement lors de la vente de celles-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/add-giftcard-to-basket-modal.png" height="240"/>

La première étape, dans le cas ou vous avez configuré plusieurs types de cartes cadeau dans les moyens de paiement, est de sélectionner celle que vous souhaitez. Ce cas et rare et cet selection n'est pas nécessaire dans la plupart des cas.

Vous pouvez ici scanner, ou entrer le numéro de la carte cadeau que vous souhaitez vendre, si celle-ci est sur un support physique. Dans l'optique d'une impression de la carte suite à la vente vous pouvez également demander à Yuzer d'automatiquement sélectionner le numéro d'une carte non-activée et non-invalidée à l'aide du bouton rafraichir.

Une fois la carte sélectionnée vous devez sélectionner le montant à lui affecter (si aucun montant initial n'a été configuré pour celle-ci).

Il est finalement possible de définir un client bénéficiaire de la carte cadeau si celle-ci est dès maintenant destinée à une personne en particulier. Ce champ est bien entendu disponible.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/add-giftcard-to-basket-modal-2.png" height="300"/>

Contrairement aux autres lignes, la modification d'une carte cadeau (pour la changer ou modifier le montant) se fait au niveau du bouton _éditer_ se trouvant sur la ligne (au niveau de la colonne stock).

Lors de l'édition de la facture ou du ticket de caisse la carte cadeau est activée.

## Utilisation d'une carte cadeau comme moyen de paiement

Pour utiliser une carte cadeau lors d'un paiement il suffit dans la boite de dialogue de paiement de sélectionner le moyen de paiement auquel est lié la carte cadeau, puis de scanner le code barre de la carte ou l'entrer manuellement.

Il est possible dans cet écran d'afficher le détail des opérations précédamment effectuées sur la carte.

Le reste du paiement suit le flux habituel.

## Annulation d'un paiement effectué avec une carte cadeau

L'annulation d'un paiement effectué avec une carte cadeau est effectué en assignant le montant en crédit client. Il est impossible de re-créditer une carte cadeau.

Si le paiement a été assigné au mauvais client il faudra qu'un administrateur ou qu'une personne ayant le droit de comptabilité effectue la correction sur les deux fiches client.

## Consultation des évènements (activation, paiement, etc.) d'une carte cadeau

Vous pouvez, à tout moment consulter l'ensemble des évènements de cadeau depuis l'écran d'administration des cartes cadeaux en sélectionnant la carte en question.

# Champs requis pour un contact

En tant qu'administrateur vous pouvez désormais configurer un ensemble de champs obligatoires lors de la création d'un contact.

# Re-synchronisation de la gestion des produits "montés" sur un dossier

Dans les versions précédentes Yuzer ne remettait pas à jour les produits "montés" sur un dossier. Ceci pouvait poser problème nottament dans le cadre de cessions finalisées en décallage par rapport à une vente.

Yuzer va désormais re-synchroniser ces produits vous permettant de les placer dans le groupe de facturation du client ou dans le groupe de facturation "à démonter".

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.13.0/basket-synch.png" height="340"/>

De la même façon, un produit démonté lors d'une session, verra son statut "Monté sur produit" mis à jour.

## Cas d'un panier clôturé

Dans le cas d'un panier déjà facturé et cessionné Yuzer va se contenter de vous avertir mais ne modifiera pas le panier.

Dans ce cas précis il peut y avoir un produit qui a été monté à postériori sur le dossier et qui n'a donc été ni démonté, ni facturé. Il a potentiellement été "perdu" du à la mauvaise séquence de clôture des cessions dans la concession et est parti gratuitement avec la moto du client.
Il vous faut dans ce cas effectuer un inventaire pour supprimer le produit en question et, si vous l'aviez démonté le remettre dans un autre emplacement de stock et s'il a bien été "perdu" lors de la transaction le déclarer en perte.

# Calcul de la TVA sur marge

Nous avons amélioré/corrigé le calcul de la TVA sur marge. Dans les version précédentes Yuzer appliquait une TVA sur l'ensemble de la marge de la vente, la déduisait du compte de produit et ajoutait une ligne de TVA correspondant à ce montant. Désormais Yuzer considère la marge de la vente comme étant une somme de la marge du concessionaire et de la TVA collectée.

Les lignes comptables reflettent ceci d'une meilleur façon. De plus, il est possible de configurer un compte différent pour la valeur de produit correspondant à la marge et celle correspondant au montant de l'achat (non-assujeti à TVA).

Vous aurez ainsi ce type d'enregistrement comptables:

```
Compte	    Libellé	                    Débit.   Crédit
41100000	Vente Mr X	                11 200
707240x0	Vente VO TTC Marque X	              10 000
707240x1	Marge sur vente VO 		               1 000
44571002	TVA Collectée sur marge		             200
```

Vous pouvez effectuer une demande de récupération de TVA trop payée sur vos précedentes reprises afin de compenser le trop versé dus à l'ancienne méthode de calcul. En effet dans l'exemple ci-dessus nous aurions considéré une marge de 1 200 euros (prix de vente de 11 200 moins prix d'achat 10 000) et aurions appliqué la création d'une TVA dessus soit un montant de 240 euros et non 200 euros.

# C'est corrigé

- Lorsque vous aviez des filtres sur la vue de liste de panier, alliez sur la liste de produits (magasin) reveniez les filtres étaient remis à zero.
- La lisibilité des propositions de duplicats de contacts n'étaient pas lisibles en thème sombre.
- Lors de la suppression du champ modèle de la liste des champ sur la table de dossier véhicule, il était impossible de le remettre.
- Il est désormais possible de trouver les vélos et autres produits identifiables à l'aide de la recherche principale.
- La création d'un nouvel inventaire complet pouvait dans certains cas afficher une erreur.
- L'arrondi effectué dans la conversion des unités sur les lignes de main d'oeuvre pouvait entrainer des montants ne correspondant pas au souhait de l'utilisateur. Nous avons augmenté la précision afin d'éviter ces problèmes.
- Lors de l'utilisation d'une douchette sur un panier, si le champ de reférence était sélectionné, ce qui est le cas par défaut, le produit était ajouté deux fois au panier.
- Lorsqu'on déplaçait un produit monté sur un produit identifié dans un groupe de cession pour démontage, la quantité n'était pas mis à jour avec sa valeur négative. Ce qui empêchait de le remettre en stock lors de la facturation.
- Lors de la création d'un contact depuis la boite de dialogue (lors d'un nouvel O.R. par exemple) un problème de dépassement rendait le formulaire illisible.
- Les coûts opérationnels par marque et la sélection du fournisseur sur les produits identifiés ne fonctionaient pas correctement.
- La description des tâches dans le contexte de produits identifiés pouvait être incorrecte lorsque crée depuis un panier.
- La catégorie d'une ligne hors catalogue n'était pas correctement mise à jour lors de la sélection du produit.

# Améliorations et corrections des versions 1.12.x

- La recherche par référence depuis l'ajout par référence dans le panier et dans l'application mobile permet d'ajouter un produit depuis son code barre et non simplement depuis son identifiant (Note: dans l'univers moto de nombreux produits ont pour code barre leur identifiant).
- Lorsqu'un produit existe avec la même référence/code barre dans divers fournisseur Yuzer vous permet de selectionner le produit sélectionné au lieu de ne rien faire.
- L'ajout d'un nouvel identifiant à un produit identifié est désormais possible.
- L'édition des attributs d'un vélo ou autre produit identifié est désormais possible.
- Il est désormais possible d'imprimer une étiquette d'un dossier vélo ou produit identifié.
- Amélioration de l'impression des codes barres qui utilisent désormais une taille fixe quelque soit le contenu du code.
- Amélioration de l'impression des codes barres qui peuvent désormais se fonder sur le champ code barre et non uniquement id du produit.
- Amélioration de l'impression des codes barres qui peuvent ne pas être centrés sur l'étiquette corrigeant un problème de compatibilité avec les imprimantes Zebra.
- Il est désormais possible de prendre un paiement pour un panier de passage déjà facturé (ticket de caisse) mais dont un paiement aurait été annulé. Ceci permettant d'effectuer une opération corrective sur le paiement sans annuler la vente.

### C'est corrigé

- Lors de l'édition de la facture avec paiement et annulation de la phase de stock puis réédition directe depuis l'apperçu (ce qui ouvre à nouveau la phase d'édition de stock) le paiement était enregistré à chaque nouvelle phase d'édition. Il fallait alors l'annuler.
- L'affichage des TVA était arrondu à l'unité entrainant l'affichage d'une TVA de 5,5% à 6%. Le calcul était correctement effectué sur 5,5%.

## Application mobile

### C'est corrigé

- La vue d'une tâche était mal affichée sur certaines tablettes.
