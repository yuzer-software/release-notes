# 6 Novembre 2022 - Version 2.0.0

<div class="alert alert-danger">
Nous invitons nos utilisateurs concessionnaires moto à lire la release note avec attention. Celle-ci explique les modifications induites par les changements sur cette nouvelle version.
</div>

Yuzer 2 uniformise la gestion des dossiers et ventes véhicules avec celle des vélos et autres produits possédant un identifiant unique (VIN, Immatriculation pour les véhicules; numéro APIC pour les vélos).

Cela entraine la disparition de plusieurs éléments spécifiques au véhicules (motos) tels que:

- Le catalogue de modèles de véhicules qui rejoint le catalogue de produits standard sous une nouvelle catégorie _Véhicules terrestres à moteurs_.
- L'écran de détail véhicule disparait et est remplacé par un détail de produit standard.
- Les _Paniers de ventes véhicules_ sont remplacés par les _Paniers de vente de produit sur dossier_ qui leur sont équivalent mais considèrent le véhicule comme une ligne spécifique du panier. L'onglet _Ventes et préparations additionelles_ disparait donc.
- L'écran de détail de dossier véhicule devient identique à celui de détail de dossier utilisé pour les vélos.

Nous avons effectué une migration de vos données et de vos paramètres de widget afin de refléter les différents changements opérés et que ceux-ci aient le moins d'impacts possible sur votre quotidien.

## Catalogue véhicule

Le catalogue véhicule présent dans le même onglet que les dossiers disparait

|                                                                 Yuzer 1.x                                                                  |                                                             Yuzer 2.x                                                              |
| :----------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file-list-catalog-1.x.png" width="512px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file-list-2.x.png" width="512px"/> |

Les modèles de véhicules sont désormais directement existant en tant que produit dans le même catalogue que ceux-ci la catégorie à sélectionner pour filtrer sur ceux-ci est _Véhicule terrestre à moteur_. Tous les véhicules possédant un VIN sont regroupés sous celle-ci dont les sous-catégories _Moto_, _Voiture_ etc.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/vehicle-catalog-2.x.png" width="1024px"/>

### Fiche détail produit véhicule

La fiche de détail du produit véhicule s'aligne sur la fiche de détail produit:

|                                                                Yuzer 1.x                                                                 |                                                                Yuzer 2.x                                                                 |
| :--------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/vehicle-detail-1.x.png" width="1024px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/vehicle-detail-2.x.png" width="1024px"/> |

## Véhicules et Dossiers véhicules

De la même manière que le catalogue véhicule est aligné sur les produits classiques, les fiches véhicules et dossiers véhicules s'alignent sur ceux existant pour les vélos, moto-marines et autre produit "identifiable".

Un _produit identifiable_ est un produit possédant un ou plusieurs numéro(s) d'identification unique (comme le VIN ou l'immatriculation pour un véhicule). La vente d'un certain produit ne peut-être substituée à un autre produit équivalent (le VIN apparait sur sa facture, est liée à l'immatriculation, la carte grise et donc à l'acheteur).

### Gestion des identifiants

La gestion des identifiants véhicules dans Yuzer s'aligne sur la gestion de ceux des vélos et autres moto-marines. Ils deviennent à la fois plus générique mais aussi plus stricts en terme de validation.

Ainsi là ou Yuzer permettait d'entrer un VIN qui n'en était pas un (un numéro de série ne possédant pas 17 caractères) ceci n'est plus possible. Certaines carte grise sur de vieille motos n'affichent pas de VIN et le véhicule ne le possède parfois pas. Dans ces cas vous devrez choisir comme identifiant le _Numéro dans la série du type_.

### Création d'un dossier véhicule

Quelques modifications à la création de dossier apportent plus de clarté et souplesse:

|                                                                Yuzer 1.x                                                                 |                                                              Yuzer 2.x                                                               |
| :--------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_step1_old.png" width="1024px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_step1.png" width="1024px"/> |

L'ajout d'un produit sans identifiant est désormais, bien que non recommandé, possible immédiatement à l'aide du bouton
<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_no_id.png" width="140px"/>
Vous pourrez associer un identifiant (VIN, Immatriculation etc.) ultérieurement.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_search.png" width="1024px"/>

La recherche de l'identifiant précise si l'information provient de données Yuzer ou de données d'un service extérieur (SIV, constructeur etc.).

Vous pouvez également choisir, en cas de plusieurs données correspondante, choisir le résultat que vous souhaitez.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_selected.png" width="1024px"/>

#### Identifiant inconnu

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_unknown_id_search.png" width="1024px"/>

Dans le cas ou l'identifiant sélectionné est inconnu du système ainsi que des systèmes connectés l'information vous ai clairement présentée. Si vous êtes certain de votre identifiant il est possible de créer le dossier avec un identifiant donné. Vous devez alors préciser le type d'identifiant spécifique que vous souhaitez enregister:

|                        Le bouton permettant cette action est grisé tant que le choix de l'identifiant n'a pas été effectué.                        |                                Pour choisir l'identifiant précisez le dans la zone de recherche à la place de _Tous_                                 |
| :------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_unknown_id_type_warn.png" width="256px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_unknown_id_type_select.png" width="256px"/> |

<div class="alert alert-warning">
Attention le format de l'identifiant doit-être correct. Dans le cas contraire la création du dossier échouera lors de la validation finale:
<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/file_new_wrong_id.png" width="256px"/>
</div>

### Dossier véhicule

|                                                               Yuzer 1.x                                                               |                                                               Yuzer 2.x                                                               |
| :-----------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-old.png" width="1024px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-new.png" width="1024px"/> |

Les informations principales restent affichées en haut mais sont complétées de plusieurs informations et liens:

- La marque et le libellé du produit

Ceux-ci peuvent être édités à l'aide du bouton d'édition principal:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-main-props.png" width="758px"/>

- Les informations de la fiche produit associée, la référence produit, le libellé catalogue ainsi que le fournisseur et catégorie du dossier. Contrairement aux véhicules, il est possible de modifier l'association à une référence en cas d'erreur:

|                                                               Aller au produit                                                                |                                                           Changer le produit associé                                                            |                                                    Supprimer l'assciation à la fiche produit                                                    |
| :-------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-product-goto.png" width="256px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-product-change.png" width="256px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-product-unlink.png" width="256px"/> |

Finalement vous pouvez consulter les attributs et propriétés du produit en bas de la fiche.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/dealer-file-props-and-attr.png" width="1024px"/>

_Note: Une propriété est présente sur la fiche produit également. Un attribut est spécifique au véhicule. Par exemple toutes les Duke 390 2021 ont le même type de moteur. Cependant le kilométrage est spécifique à chaque véhicule._

<div class="alert alert-info">
Il est désormais possible d'attacher un identifiant (VIN) à un véhicule commandé ou en attente de commande.
</div>

## Recherche de produits

La recherche de véhicule

## Liste de paniers

La liste de panier affiche plus clairement les informations des véhicules ou autres produits identifiés des paniers.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/basket-list.png" width="1024px"/>

De plus les icônes du type de vente deviennent dépendant du type de dossier contenu dans le panier mais également du type de reprises.

|                                                         vente de moto                                                         |                                                         vente de vélo                                                         |                                                          reprise de moto                                                           |                                                      vente et reprise de moto                                                      |                                                   vente vélo et reprise de moto                                                    |                                                produit vendu non sélectionné                                                 |
| :---------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/icon_moto.png" width="34px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/icon_bicy.png" width="34px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/icon_none_moto.png" width="34px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/icon_moto_moto.png" width="34px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/icon_bicy_moto.png" width="34px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/icon_idp.png" width="34px"/> |

## Liste de paniers du client

La liste des ventes de véhicules du client dispose des même changements. De plus, si votre concession vends plusieurs types de produits, vous avez la possibilité de facilement filtrer les paniers du client pour ne visualiser que ceux que vous souhaitez

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/contact-idp-baskets.png" width="512px"/>

La création de nouveau panier de vente sur dossier reste inchangée pour une concession moto uniquement, et se simplifie pour une concession vendant différent types de produits identifiés:

|                                                                Yuzer 1.x                                                                |                                                                Yuzer 2.x                                                                |
| :-------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: |
|   <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/old-sale-moto.png" width="256px"/>    |   <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/new-sale-moto.png" width="256px"/>    |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/old-sale-moto-bicy.png" width="256px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/new-sale-moto-bicy.png" width="256px"/> |

L'icône et le texte s'adapte à votre contexte, ainsi si vous vendez vélos, véhicules et moto-marines:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/new-sale-all.png" width="256px"/>

## Panier véhicules

|                                                             Yuzer 1.x                                                              |                                                             Yuzer 2.x                                                              |
| :--------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-old.png" width="1024px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-new.png" width="1024px"/> |

L'onglet Préparation et ventes additionelles disparait, tout se passe directement dans le panier désormais.

L'ajout de dossier se fait à partir du même endroit que l'ajout des autres produits, si vous vendez plusieurs type de produits vous devez sélectionner le type de dossier à ajouter:

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-select-new-1.png" width="256px"/>

La sélection du dossier s'ouvre alors:

|                                                                 Yuzer 1.x                                                                 |                                                                 Yuzer 2.x                                                                 |
| :---------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-select-old.png" width="1024px"/> | <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-select-new.png" width="1024px"/> |

<div class="alert alert-info">
Désormais la vue s'ouvre sur tous les dossiers. De plus un filtre pré-défini impose l'affichage des dossiers non-réservés uniquement. Celui-ci peut, bien entendu, être désactivé.
</div>

Comme avant les frais de carte grise pourront être ajoutés. Et la ligne sera ajoutée au panier. Celle-ci comme une ligne classique peut-être déplacée dans le panier. Les informations du dossier y sont également affichées.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-selected.png" width="1024px"/>

Vous pouvez comme avant créer vos Cerfa depuis le même menu qu'avant.

### Reprises

L'onglet reprise existe toujours et évolue légèrement pour permettre, si vous gérez plusieurs type de produits, le choix du produit à reprendre.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-trade-in.png" width="1024px"/>

La première étape d'une réception de reprise permet également de valider et compléter l'ensemble des informations liées.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.0.0/v-basket-trade-in-2.png" width="1024px"/>

## Changement de catégorie

Le déplacement de la catégorie des véhicules sous _Produits_ impliquée a des conséquences qui ne devraient pas poser de problèmes pour vous, les différentes configurations ayant été migrées automatiquement.

### Impact comptabilité

Notre outil de migration a modifié automatiquement vos règles comptables pour que vos règles sur véhicules soient bien appliquées sur la nouvelle catégorie. L'ensemble des données passées ayant également été migrées devrait-être transparent à moins que vous soyez dans le cas suivant.

- Si vos règles spécifiques véhicules se trouvaient après une règle générique regroupant tous les produits (Ce qui n'est pas recommandé quoi qu'il en soit et ne devrait pas être le cas). Vous devrez déplacer la règle générique en dessous des règles produit.

## Widgets et Analytiques

Les widgets et analytiques sont impactés par deux évolutions:

- La disparition du panier véhicule (qui est remplacé par le panier de vente sur dossier)
  - Si vous ne vendez qu'un type de produit cela n'a aucun impact pour vous.
  - Dans le cas ou vous vendez à la fois des motos et vélos ou moto-marines un nouveau paramètre _Type de produit_ dans les widgets vous permet de différencier les deux produits. Dans l'analytique un filtre sur la catégorie dans les lignes permet l'équivalent.
- L'évolution sur les catégories puisque les véhicules sont déplacés dans _Produits_ est immédiate. Pour disposer d'une métrique sur _Tous les autres produits_ vos configurations _Produits_ uniquemenet ont été migrées vers la sélection de l'ensemble des produits. Une catégorie virtuelle _Autres produits_ est ajoutée pour toutes les ventes dont le produit aurait été mal catégorisé.
