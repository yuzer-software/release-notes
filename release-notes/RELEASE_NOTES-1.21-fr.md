# Avril 2022 - Version 1.21.2

## Catalogues

### Partage de catalogues entre entités

Vous pouvez désormais partager un de vos catalogues fournisseur avec d'autres entités du groupe.

<div class="m-2 alert alert-warning">
Attention, une fois partagé le catalogue du fournisseur pourra être modifié aussi bien par l'entité ayant effectué le partage que par celle à qui le catalogue est partagé. Il ne sera pas possible de définir par exemple un prix différent pour une entité ou l'autre sauf usage de règles de tarifications spécifiques.
</div>

Depuis votre liste de fournisseurs (_Administration_ / _Fournisseurs_) un bouton _Partager_ fait son apparition en face de vos catalogues locaux.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/share-supplier-list.png" width="100%"/>
<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/share-supplier.png" width="100%"/>

Une fois actionné une modal s'ouvre alors vous permettant de visualiser:

- Avec qui le catalogue est déjà partagé
- Avec qui le catalogue peut-être partagé

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/share-supplier-modal.png" width="700"/>

Une fois une cible sélectionnée, Yuzer vérifie que le préfixe n'est pas déjà utilisé dans la cible. Si tel est le cas, vous devez spécifier un autre préfixe afin de pouvoir partager le catalogue.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/share-supplier-modal-prefix.png" width="320"/>

Dans l'exemple ci-dessus nous allons utiliser le préfixe _ART_ car le fournisseur _Aratech_ est déjà dupliqué dans notre entité cible _Sullust Shipyard_.

<div class="m-2 alert alert-info">
Le partage doit se faire aujourd'hui cible par cible et il n'est pas possible de sélectionner plusieurs cibles d'un coup; ce point sera amélioré dans le futur.
</div>

Une fois partagé, le fournisseur devient visible dans la liste des fournisseurs en tant que catalogue communautaire.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/target-supplier-list.png" width="100%"/>

Pour rappel il existe trois icônes qui vous permettent de visualiser les types de syncronisation et mise à jour sur les catalogues:

<div>
<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/catalog-local.png" width="32"/>
<span>Calogue local que vous avez créé. Vous pouvez éditer les produits à votre convenance.</span>
</div>
<div>
<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/catalog-community.png" width="32"/>
<span>Calogue communautaire qui a été partagé avec vous. Vous pouvez éditer les produits et toute modification sera répercutée sur l'ensemble des autres utilisateurs du catalogue.</span>
<div>
<div>
<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/catalog-automatic.png" width="32"/><span>Catalogue managé dans lequel vous ne pouvez effectuer de modifications.</span>
<div>

Dans l'exemple ci-dessus le fournisseur _Aratech_ avait été créé en local avant que _Gallactic Empire_ ne nous partage son catalogue _Aratech_, c'est pourquoi celui-ci apparait deux fois, en local et en communautaire.

### Fusion de fournisseurs/catalogues

Une fois les catalogues partagé il est probable que vous souhaitiez vous débarasser de catalogues existant en doublons.

Il est possible pour cela d'utiliser la fonction de fusion de fournisseurs. Cette fonction vous permet de controler la consistence du catalogue cible mais également migrer

- votre stock vers les nouvelles références catalogue
- vos réservations en cours
- vos commandes en cours

<div class="m-2 alert alert-warning">Attention, les références des éventuels transferts ne seront pas migrées. Nous vous recommandons donc de les résoudre avant d'effectuer la fusion.</div>

<div class="m-2 alert alert-danger">Attention, il est important d'effectuer la fusion alors que personne ne travaille (en fin de journée par exemple). Ceci afin d'éviter que des nouvelles réservations/ commandes /entrées ou sorties en stock ne soient effectuées pendant le processus.</div>

Afin d'effectuer une fusion rendez-vous dans _Administration_ / _Fournisseurs_ puis cliquez sur le bouton d'édition _Gérer les fournisseurs_. Utilisez alors le bouton _Fusionner_ sur le fournisseur que vous souhaitez fusionner (celui amené à disparaitre).

Dans notre cas nous souhaitons fusionner le catalogue local _Aratech_ afin de ne garder que le catalogue communautaire partagé par _Gallactic Empire_. Faites bien attention lorsque, comme ici, le nom du fournisseur est dupliqué à bien choisir le catalogue que vous souhaitez conserver à l'aide de l'icône _Communautaire_ ou _Local_ (comme ci-dessous).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-supplier-start.png" width="100%"/>

Une fois la fusion lancée une boite de dialogue s'affiche et vous permet de sélectionner le fournisseur cible. Dans notre cas nous souhaitons fusionner dans le catalogue _Aratech_ communautaire (là encore faites bien attention à l'icône et au préfixe pour différencier les fournisseurs).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-supplier-select-target.png" width="100%"/>

Yuzer recherche alors les produits manquants dans le catalogue cible et qu'il faut éventuellement créer.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/
merge-resolve-missing.png" width="100%"/>

Chaque ligne de vous permet de visualiser un produit manquant dans le catalogue cible ainsi que le nombre de ses réservations (par status) commandes, ou présent en stock. Passez votre souris sur un nombre afin de d'avoir le détail du status, dont la couleur suit le code couleur de l'application.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-tooltip-booked.png" width="160"/>

Vous pouvez, en cliquant sur le bouton loupe de la ligne accéder également au détail des Réservations, Commandes et Stock qui seront fusionnés.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-product-detail-btn.png" width="160"/>

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-product-detail.png" width="100%"/>

Vous pouvez également accéder depuis cet écran aux deux catalogues pour effecuter un comparatif en cliquant sur la loupe se situant en sous-titre:

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-catalog-compare-btn.png" width="260"/>

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-catalog-compare.png" width="100%"/>

Re-cliquez sur la loupe en haut afin de revenir à la liste des produits manquants.

Plusieurs actions vous sont proposées pour chaque produit:

- Créer: le produit sera créé dans le catalogue cible avec la référence indiquée et sera accessible dans le cas d'un catalogue communautaire tant par vous même que par les autres utilisateurs du catalogue.
- Remplacer: rechercher une référence équivalente déjà présente dans le catalogue cible.
- Ignorer: disponible uniquement si vous n'avez ni stock, ni réservations.

Une fois toutes les actions choisies vous pouvez cliquer sur suivant afin d'accéder au récapitulatif des actions à mener:

Un onglet vous détaille les produits à créer
<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-preview-create.png" width="100%"/>

Et l'autre les produits à fusionner
<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-preview-merge.png" width="100%"/>

Vous pouvez alors lancer la fusion.

<div class="m-2 alert alert-danger">
Attendez bien que la fusion soit complétée avant de fermer la boite de dialogue ou Yuzer.
</div>

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/merge-complete.png" width="100%"/>

Une fois complétée Yuzer aura effecuté la migration vers les nouvelles référence:

- Du stock
- Des réservations client actives ainsi que les lignes de panier associées à celle-ci (mais uniquement les lignes de panier associées à ces réservations)
- Les commandes actives.

### Supprimer mon ancien fournisseur et modifier le préfixe du nouveau

Une fois le fournisseur correctement migré vous pouvez le supprimer (icône poubelle).

<div class="m-2 alert alert-danger">
ATTENTION de bien sélectionner le fournisseur que vous venez de fusionner et non celui dans lequel vous avez effectué la fusion.
</div>

Finalement vous souhaiterez probablement, dans le cas ou le fournisseur a été créé avec un autre préfixe, comme dans notre exemple, modifier le préfixe du fournisseur dans lequel les produits ont été migrés afin de ne pas perturber vos utilisateurs. Il vous suffit alors de l'éditer:

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/update-prefix.png" width="100%"/>

### Lignes de panier non migrées

Comme expliqué ci-dessus les lignes de panier qui n'avaient pas de réservations ne sont pas migrées automatiquement. N'ayez crainte cependant, elles sont clairement indiquées sur le panier et modifier les référence se fait très facilement.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/replace-ref-basket.png" width="100%"/>

Il suffit pour cela de cliquer sur le bouton de remplacement de la référence:

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/replace-ref-button.png" width="180"/>

La sélection de produit s'ouvre alors en effecuant une recherche par défaut avec la référence du produit:

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/replace-ref-modal.png" width="100%"/>

## Tableau de bord

### Widget de M.O.

Le widget de main d'oeuvre vous permet désormais d'afficher en plus des heures facturés et C.A. facturé les informations extraites de l'atelier que sont:

- La durée estimée: C'est le temps indiqué à la création d'une tâche atelier (à l'evoi à l'atelier lorsque la tâche est créée depuis un panier)
- La durée planifiée: C'est la durée de la tâche modifiée soit à l'édition du panier soit depuis l'atelier et qui est visible sur le calendrier.
- La durée de résolution qui est calculée à lorsqu'une tache est démarrée, mise en pause depuis l'application mobile et finalement marquée comme faite.

De plus la configuration du widget a été déportée dans une boite de dialogue afin de simplifier celle-ci. L'ensemble des widgets suivront cette évolution dans le futur.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/work-widget-cfg-1.png" width="700"/>

Certaines propriétés du graphique sont désormais disponibles par série de donnée affichée ce qui permet de mélanger sur le même graphique des courbes et histogrammes, pour des types de données différents par exemple.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/work-widget-cfg-2.png" width="700"/>

A noter que les statistiques atelier ne permettent pas de filtrer par type de panier ou type de cession actuellement, ces filtres disparaissent donc lorsqu'un de ces Types de données est sélectionné.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/work-widget-cfg-3.png" width="700"/>

Le graphique ci-dessous affiche à la fois le chiffre d'affaire en courbe et avec des labels (l'échelle de C.A. étant placée à gauche) et des durées (l'échelle de temps étant placée à droite).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/work-widget.png" width="100%"/>

### Utilisations de filtres personnalisés

Les filtres personnalisés qui seraient incompatibles avec le widget de chiffre d'affaires sont clairement exhibés.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/custom-filter-in-turnover-widget.png" width="500"/>

## Panier

Nous indiquons désormais clairement pourquoi une ligne avec préparations ne peut pas être supprimée.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/delete-line-with-preparations.png" width="500"/>

Depuis la version précédente (mais cela n'avait pas été noté dans la release note) vous pouvez accéder rapidement aux modèles depuis la bare d'édition.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/basket-template-quick-add.png" width="100%"/>

## Export des dossiers de produits

Il n'est plus possible d'exporter les dossiers de véhicules ou de produits identifiés qu'en CSV.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/dealer-file-export-button.png" width="350"/>

En revanche, beaucoup de champs ont été rajoutés et il est même possible d'y associer des informations croisées (frais, factures, contact).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/dealer-file-enhanced-export.png" width="650"/>

## Réceptions

Les lignes des réceptions sont triées par date d'ajout mais toutefois groupées par identifiant de produit, ce qui est généralement désirable. En conséquence, il est possible que des lignes soient réordonnées sur des opérations d'ajout ou de suppression de lignes, ce qui était parfois déconcertant pour l'utilisateur qui pouvait croire que davantage de produit avait été ajouté que ce qu'il n'avait demandé ou, lors d'une suppression, que plusieurs lignes avaient été supprimées. Par exemple, si un produit 890479 a été ajouté à la réception, puis une dizaine d'autres lignes, puis à nouveau du 890479 et que cela crée une nouvelle ligne, alors toutes les lignes de 890479 seront groupées ensemble en tête de liste. Si cette dernière ligne venait à être supprimée, les autres lignes retrouveraient leurs place en fin de liste, donnant l'impression qu'elles ont été supprimées.

Nous avons donc ajouté un message indiquant lorsque des lignes sont réordonnées avec la possibilité de filtrer les lignes impactées (comme illustré ci-dessous).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/warn-reception.png" width="600"/>

### Améliorations ergonomiques

- Lorsqu'une ligne contient une quantité supérieure à 1 et qu'un emplacement est choisi l'intégralité de la quantité est désormais affectée à l'emplacement choisi.

- La navigation entres les vues de détails de la réception, des produits en commandes ou du catalogue est désormais plus simple et claire. Elle s'effectue à l'aide des boutons _Détails_, _Commandes_ et _Catalogue_. situés juste en dessous des boutons pricipaux _Supprimer_, _Quitter l'édition_ et _Clôturer la réception_ lorsque la réception est en cours d'édition.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/reception-views.png" width="100%"/>

Ce type d'affichage est également appliqué sur les inventaires et transferts.

## Modèle de panier: import Honda

Honda fournit des modèles de panier au format CSV qu'il est désormais possible d'importer dans Yuzer.

- Vous devez au préalable avoir Honda comme fournisseur.
- Depuis la page des modèles, cliquez sur "Importer Honda".

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/new-honda-import.png" width="300"/>

- Suivez les instructions: téléchargez les fichiers fournis par Honda, puis remplissez les champs comme indiqué.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/honda-import.png" width="800"/>

- Cliquez sur "Charger": tous les modèles importés seront créés.

## Comptabilité

### TVA déductible à l'achat par taux de TVA

Il est maintenant possible de configurer les comptes de TVA déductible à l'achat par taux de TVA.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/vat-config.png" width="700"/>

## Améliorations diverses

- Lorsque vous créez un ordre de réparation à partir d'une tâche d'atelier, le panier est maintenant nommé à partir du libellé de la tâche.

## C'est corrigé

- Dans la boite de dialogue de sélection d'un contact, vous n'être maintenant plus redirigé vers la page de détails lors de la sélection d'un véhicule.
- La tâche de l'atelier n'était pas synchronisée lors de l'ajout d'un modèle de panier qui contient de la main d'oeuvre.
- Lors d'une réception de plus de 50 lignes changer un emplacement sur une ligne en page 2 ne fait plus revenir à la première page.
