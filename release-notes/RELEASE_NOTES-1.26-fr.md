# Juin 2022 - Version 1.26.0

## Cessions: internes et garantie fournisseur

Nous avons complété les types de cessions disponibles avec l'ajout des cessions internes et garanties fournisseurs.

### Configuration des ventilations comptables:

Dans la configuration de comptabilité l'onglet _Configuration des comptes_ est renommé _Ventilations_ pour plus de clarté. Rendez vous dans celui-ci puis dans _Ventilation des ventes > Cessions_ pour configurer les règles permettant de ventiler les cessions de garantie fournisseurs.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/cessions.png" width="100%"/>

<div class="m-2 alert alert-warning">
Contraiement aux autres cessions une _garantie fournisseur_ peut avoir un tiers (le fournisseur) spécifié. Les fournisseurs disponibles nécessitent d'avoir été associés à un numéro de contact. Cette opération doit-être effecutée au préalable dans la configuration des fournisseurs.
</div>

<div class="m-2 alert alert-warning">
Pensez à bien ajouter une règle plus spécifique **avant** une règle moins spécifique.
</div>

### Création d'une session fournisseur

Désormais depuis une fiche client liée à un fournisseur lorsque vous créez un panier vous est proposé la création d'une garantie fournisseur ou un panier classique à facturer.

Vous pouvez toujours modifier la cible de n'importe quel groupe de facturation d'un panier vers une autre cible dont une cession de garantie fournisseur.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/cession_switch_1.png" width="380px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/cession_switch_2.png" width="380px"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/cession_switch_3.png" width="380px"/>

Dans ce cas la sélection du fournisseur tiers vous est demandée. Seuls les contacts liés à un fournisseur sont alors proposés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/cession_switch_4.png" width="600px"/>

Le nom du fournisseur apparait alors sur la cible du groupe de facturation.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/cession_switch_5.png" width="600px"/>

## Exports de stock automatisés

Vous pouvez désormais configurer un export automatisé de votre stock au format CSV. Ils permettent de synchroniser votre stock avec un fournisseur externe (constructeur, site web, etc.).

Rendez vous pour ceci dans la section _Administration > Automates > Stock_

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/stock_export.png" width="100%"/>

Comme vous pouvez le constater un export vers le constructeur possède une configuration particulière. En effet le serveur d'export est commun à l'ensemble des clients Yuzer dans ce cas et la configuration est par conséquent simplifiée.

Dans le cas d'un export personalisé cliquez sur le bouton _Nouveau_ afin de faire apparaitre la configuration d'export.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/stock_export_modal_0.png" width="380px"/>

Aprés avoir défini le nom de la configuration et la description, vous devez configurer trois aspects:

- Le format d'export.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/stock_export_modal_1.png" width="380px"/>

- La configuration du serveur vers lequel effectuer l'export.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/stock_export_modal_2.png" width="380px"/>

- Les fitres de ce qui doit-être exporté.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/stock_export_modal_3.png" width="380px"/>

<div class="m-2 alert alert-warning">Seules deux configurations d'export peuvent être définies par concession.</div>

### Rapport d'executions

Les rapports d'executions des exports peuvent-être consultés dans l'onglet \_Résultat d'éxecution.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.26.0/exec_report.png" width="100%"/>

## Améliorations diverses

- Nous avons généralisé la possibilité de mettre à jour le status d'un dossier neuf avec les valeurs: `Neuf`, `Employé`, `Courtoisie` ou `Démo`.
- La recherche des modèles de panier permet de rechercher indiférament avec ou sans accent.
- Le statut de paiement d'une cession est désormais toujours Payé. Ceci permet d'éviter de polluer les recherches de paniers.
- Vous pouvez désormais afficher toutes les étiquettes d'un sous ensemble filtré du stock.
- Lors de l'impression des étiquettes seules les opérations commerciales actives sont désormais affichées.

## C'est corrigé

- Les mots avec accents et apostrophes sont maintenant correctement gérés dans la recherche de modèle de panier.
- L'import de fichiers textes dans un panier ne nécessite plus de re-définir les colonnes à chaque fois.
- Les étiquettes d'emplacement de stock n'affichent plus les numéros d'emplacement en grisé. Ceci posait des problèmes d'impression sur plusieurs imprimantes etiquette.
