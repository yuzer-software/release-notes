# Août 2021 - Version 1.9.0

- Lorsque vous créez un nouveau rendez-vous à l'aide de la fonction de _prise de rendez-vous rapide_, le titre du panier créé est désormais celui du modèle choisi, ou, dans le cas d'une description libre, la première ligne de cette description.
- Le nom de modèle d'un véhicule est maintenant éditable.
- Il est désormais possible de générer un export avec les produits du stock dans un fichier **csv**, **excel** ou **txt**.
- Il est maintenant possible de convertir de la balance en crédit même quand cela engendre une balance négative.
- Un administrateur peut maintenant choisir d’ignorer d’impacter le stock des produits pour tous les types de panier lors de la facturation (initialement possible uniquement pour les paniers de type _préparation de véhicule_).
- Il est désormais possible d'encaisser un paiement avec un montant supérieur à celui du panier.

## Modification des catégories de produit

Nous avons séparé la catégorie "Autres services et taxes" en "Autres services" d'une part et "Autres taxes" d'autre part afin d'automatiser, dans le futur, l'application de la TVA à ces catégories. Toutefois, le processus de renommage ne peut pas être totalement automatisé et requiert votre attention.

Nous avons renommé la catégorie _Autres services et taxes_ en _Autres services_ dans tous les catalogues, mais nous n'avons pas effectué de renommage ailleurs, et en particulier dans les règles de comptabilité. Nous vous demandons donc :

<div class="alert alert-danger">
  <ul>
    <li>
      de bien vérifier vos règles de comptabilité (Comptabilité > Configuration des comptes)<br/>
      Dans le cas ou vous aviez spécifié une règle spécifique telle que celle-ci:
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/accountancy-rule.png" width="100%"/>
      Si toute les factures et tickets de caisses n'ont pas encore été passés en comptabilité nous vous suggérons de garder la règle obsolète et d'ajouter au dessus les règles correspondant aux nouvelles catégories de services et de taxes. N'hésitez pas à contacter notre support si vous avez besoin d'assistance.
    </li>
    <li>de bien vérifier que les catégories des produits dans les paniers ouverts existants sont correctes</li>
    <li>
      de bien vérifier que les produits désormais dans "Autres services" ne devraient pas être dans "Autres taxes" (vous pouvez utiliser le filtre comme ci-dessous)<br/>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/search-for-other-services.png" height="160"/>
    </li>
  </ul>
</div>

## Contacts

### Numéro d'immatriculation des véhicules

- Le numéro d'immatriculation des véhicules du client sont désormais affichés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/vehicle-registration.png" height="140"/>

### Exonération de TVA

Lors de la création ou modification d'un client, il est maintenant possible de sélectionner "Exonéré de TVA" si vous avez un rôle de type "ACCOUNTANT", "ADMIN" ou "SALES_MANAGER".
Un client exonéré de TVA aura sa TVA mise à 0% par défaut lors de l'ajout d'élément à un panier.

A noter que la création de modèles à partir d'un panier appartenant à un contact étant exonéré de TVA a temporairement été désactivé.
En effet, lorsque nous créons un modèle de panier, nous sauvegardons actuellement le prix des produits tel qu'il a été renseigné dans le panier source. De ce fait, lorsque le modèle est ré-appliqué sur un nouveau panier, il est possible que les prix se retrouvent sans TVA. Nous avons prévu de revoir le fonctionnement pour éviter ce genre de problème dans le futur.

## Stock négatif

Dans Stock -> Onglet Stock, il y a maintenant un nouveau bouton "Stock négatif" permettant d'afficher tous les produits ayant un stock négatif dans au moins un de ses emplacements. A noter que vous pouvez imprimer la page affichée avec la liste des produits.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/negative-stock.png" height="160"/>

## Surcharge de prix d'un véhicule dans le catalogue

Il est désormais possible de surcharger le prix d'un vehicule dans le catalogue, même si le catalogue n'est pas géré par la concession.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/override_prices.gif" width="100%"/>

## Filtrer les véhicules réservés

Il est désormais possible de filtrer les véhicules réservés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/dealer-file-reserved-filter.png" width="475"/>

## Date de facture d'achat

Dans la fiche de véhicule, vous pouvez dorénavant retrouver et modifier la date de facture d'achat.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/purchase-invoice-date.png" height="160"/>

## Impression de réceptions

Vous pouvez désormais utiliser le bouton _Imprimer_ sur une réception clôturée afin d'en imprimer le listing.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/reception-print.png" width="100%"/>

## Sélection dans les listes de produits et véhicules

La navigation dans les listes de produits et véhicules a été améliorée: vous pouvez cliquer à n'importe quel endroit de la ligne pour accéder au détail. La sélection de texte (description, référence) reste possible soit par double clic soit en sélectionnant une sous-partie de celui-ci avec la souris.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/line-select.gif" width="100%"/>

## Améliorations sur la barre de recherche globale

La recherche globale a été améliorée pour plus de confort. La recherche est désormais effectuée à travers:

- Les dossiers véhicules
- Les contacts
- Les produits

Nous avons également apporté les améliorations ergonomiques suivantes:

- Le résultat le plus probable est affiché en haut de liste et est surligné; vous pouvez y accéder immédiatement en appuyant sur la touche _entrée_ du clavier.
- Vous pouvez naviguer entre les résultats à l'aide des touches de navigation du clavier (et utiliser la touche _entrée_ pour accéder au résultat en surbrillance).
- Vous pouvez accéder à l'écran de recherche des dossiers/contacts/produits incluant la recherche entrée en utilisant les fonctions _Recherche avancée_ et bénéficier ainsi de fonctions de recherche plus avancées.

Notez que la recherche d'un véhicule dans les systèmes des constructeurs ou par plaque d'immatriculation n'est activée qu'avec un minimum de 6 caractères mais:

- Seul Triumph supporte actuellement la recherche de VIN avec les 6 derniers caractères.
- Une immatriculation ou un VIN pour les autres constructeurs doivent être obligatoirement entrés en entier.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/top-search.gif" width="100%"/>

## Renommage du label 'En attente de livraison'

- Le label 'En attente de livraison' a été renommé par le label 'En attente du fournisseur' dans l'écran d'affichage du calendrier en vue kanban et dans la modale d'édition d'une tâche.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/kanban_fr.png" width="100%"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/status_fr.png" width="100%"/>

## Configuration des couleurs des tâches

Les couleurs des tâches peuvent désormais être modifiées selon vos souhaits. Elles peuvent-être configurées pour la société/entité (ou héritées de la société parente si aucune configuration n'est définie sur une société fille), ou surchargées par utilisateur.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/task-color-config.gif" width="100%"/>

A noter que chaque utilisateur peut avoir sa propre configuration de couleurs en le configurant dans _Informations du compte > Espaces de travail_

# C'est corrigé

- Correction d'un problème de focus lors de l'édition d'un libellé sur une ligne du panier.
- Correction d'un problème lorsqu'on duplique une règle dans la configuration des comptes.
- Correction du filtre de recherche sur les catégories de produit qui ne retournait pas toujours les bons résultats.
- Correction d'une erreur lorsqu'on crée un groupe de facturation lorsqu'il n'y en a aucun dans le panier.
- Ajout d'une traduction manquante pour le message d'erreur de l'édition d'une facture de cession avec des remises.
- Diverses corrections lors de la suppression ou annulation d'un groupe de facturation.
- La TVA est maintenant correctement mise à jour lors qu'on déplace un produit non stockable dans ou en dehors d'un groupe de cession.
- Correction de la page indéfiniment en attente lorsqu'on essaie d'éditer un bon d'achat à partir d'un dossier de véhicule.
- Erreur lors de l'ajout d'une ligne à un panier de type O.R. converti en PG&A avec une tâche d'atelier annulée.
- Correction de problèmes de _drag and drop_ à l'intérieur d'un sous-groupe et à travers certains groupes de facturation.
- Résolution de l'affichage du statut de stock à l'ajout d'une nouvelle ligne dans un panier.
- Le passage en comptabilité des cessions avec auto-écriture en cas de succès s'inscrivait bien dans le journal mais restait en statut envoyé et non validé.

Note: _La plupart de ces corrections ont été incluses dans les versions 1.8.3 et 1.8.4_

# Application mobile

- Certains codes barres sont préfixés ou suffixés par des espaces. Ils sont désormais automatiquement supprimés lors d'un scan.
- Les tâches sont colorisées comme sur l'application de bureau.
- Après la création d'une réception ou d'un transfert, l'application navigue automatiquement vers l'ajout de nouveaux produits.
- Lors de l'ouverture d'une réception ou d'un transfert vide, l'application navigue automatiquement vers l'ajout de nouveaux produits.
- Lorsqu’un modèle de véhicule est mis à jour, le résultat de la recherche sur le catalogue est maintenant mise à jour afin d’afficher des résultats à jour.
- Correction d’un problème de rafraichissement avec la fenêtre d’annulation de panier.
- Correction des boutons _total_ et _acompte_ de la fenêtre de paiement qui n’étaient pas affichés pour les paniers PG&A et O.R.
