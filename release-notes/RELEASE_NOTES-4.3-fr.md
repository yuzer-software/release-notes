# October 2025 - Version 4.3

yuzSection Gestion des contacts

## Distinction des organisations gouvernementales

Les organisations gouvernementales (mairies etc.) ont désormais un type de contact spécifique.

## Champs spécifiques par pays

yuzLeft

De nouveaux champs spécifiques par pays sont désormais disponibles. Cela permet de mieux remplir les informations d'entreprises qui sont spécifiques pour chaque pays.

Nous avons également continué à améliorer la lisibilité de la fiche contact, les données de pièces d'identité sont désormais plus lisibles, la galerie est désormais par défaut minimisée.
N'hésitez pas à revenir vers nous pour nous faire part de vos retours.

yuzRight

![Contact specific fields](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/country_fields.webp?w=400px)

yuzEnd

## Recherche de contacts

Un service de recherche et autocomplétion des informations d'un contact est désormais proposé pour les entreprises et organisations gouvernementales Françaises.

![Enterprise search 1](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/enterprise_search_1.webp?w=400px)

||| Attention, comme indiqué ce service implique un coût au click de _0,08_ euros (au 1er octobre 2025) par recherche.

![Enterprise search 2](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/enterprise_search_2.webp?w=400px)

## Exonérations de TVA

Il est désormais possible d'indiquer une raison à l'exonération de TVA qui sera indiquée sur les documents (factures etc.).

YUZER vous assiste pour définir l'exonération ainsi que la mention légale dans le cas d'une vente intra-communautaire ou internationale.

- À la création d'un contact
- À l'édition de celui-ci
- À l'ouverture de tout panier

Si le contact n'est pas exonéré alors que l'adresse de votre société et celle du contact indiquent clairement une vente soumise à exonération, une fenêtre est proposée permettant de mettre à jour directement et rapidement le contact.

![Exoneration suggestion](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/exonerated_1.webp?w=400px)

|| Ce procédé n'est pas appliqué pour les contacts qui sont déjà spécifiés comme exonérés car YUZER n'a pas moyen de contrôler si une raison tierce pousse à la non-exonération.

La raison d'exonération est affichée sur les documents générés.

![Exoneration reason](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/exonerated_2.webp?w=400px)

yuzSection Import de Panier

## Import de contenu dans un panier

Les améliorations permettent d'apporter plus de fluidité dans l'import des fichiers de type _EPC Honda_ et propose un format spécifique pour les fichiers _EPC Kawazaki_ qui ne respectent aucun format proposé.

- Le format de fichier sélectionné est conservé même lorsque celui-ci n'est pas cohérent avec l'extension du fichier (Honda EPC expose en effet des csv avec une extension txt).
- Il est désormais possible d'entrer facilement un séparateur `Tab`
- Les colonnes affichées pour la configuration du mapping des fichiers csv prennent désormais en compte la ligne ayant le plus de colonnes parmi les 10 premières lignes du fichier.

Vous pouvez aussi désormais configurer des références comme main d'œuvre dans ce type d'imports:

- Entrez la référence de la M.O. et appuyez sur +

![Import paniers Ajout M.O.](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/basket-content-import.webp?w=400px)

- Configurez la correspondance sur la M.O. YUZER

![Import paniers Correspondance M.O.](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/basket-content-import-2.webp?w=400px)

## Import multiple de paniers

||| Attention cette fonctionalité ne propose aujourd'hui qu'un format spécifique.

Vous pouvez désormais importer un fichier excel contenant le contenu d'un ou de plusieurs paniers qui seront créés automatiquement.

### Format

TODO / explication du format pris en compte

### Association du client

TODO / explication du matching client (par tags aujourd'hui)

yuzSection Analytiques

yuzSection Intégrations

## Ringover

Un connecteur Ringover premium est désormais disponible. Lorsque celui-ci est activé, vous pouvez afficher les transcriptions et écouter les appels directement depuis YUZER.

Sur une fiche contact, les activités liées à Ringover disposent désormais de boutons pour lire l'enregistrement de l'appel et charger la transcription.

La transcription du premier appel est automatiquement chargée.

![Ringover Premium](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/ringover_premium.webp?w=400px)

Une fois la lecture lancée vous pouvez controller celle-ci depuis YUZER.

![Ringover Premium 2](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/4.3/ringover_premium_2.webp?w=400px)

## Suzuki

- Le catalogue suzuki est désormais synchronisé avec une source officielle chaque jour.
- Le placement automatique de commandes est implémenté et attend la mise en place du service en production par les équipes informatiques Suzuki.

## CUBE

Le catalogue CUBE actuel devient déprécié. En effet les références CUBE ne sont pas unique dans le temps. Pour éviter qu'un produit de votre "vieux" stock ne change de désignation dans YUZER au gré d'un recyclage de référence par le constructeur nous avons introduit une nouvelle référence, affichée en plus de la référence réelle.

Un nouveau catalogue est disponible, utilisant cette nouvelle fonctionalité afin de garantir une utilisation et un affichage sur base de la référence usuelle tout en garantissant l'unicité d'une référence interne fournie par Planet'Fun.

## Honda

- Une intégration avec la technologie de réception AutoVHC sélectionnée par Honda a été implémentée et sera mise à l'essai chez les concessionaires concernés.

yuzSection Général

## Améliorations

- Vous pouvez désormais sélectionner les domaines sur lesquels vos entités sont affectés. Ainsi si votre licenses vous donne accès aux marchés vélo et moto mais qu'une de vos boutique travaille sur le marché vélo uniquement et une autre sur le marché moto uniquement cela peut-être configuré.

Les catalogues accessibles dans la recherche de catalogues à ajouter prennent en compte le marché du catalogue et celui auquel vous avez accès pour ne proposer que les éléments qui vous intéressent.

- Un nouveau marché _Énergie du bâtiment_, proposant de nouvelles catégories spécifiques, est désormais disponible pour les vendeurs de cheminées et poêles à bois.

## Corrections
