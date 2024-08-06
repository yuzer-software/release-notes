# Août 2024 - Version 3.6.x

yuzSection Version 3.6.4 et suivantes

# 6 Août 2024 - Versions 3.6.4 et 3.6.5

- Correction du chargement des données analytiques
- Correction du lien vers le panier depuis un transfert
- Correction du lien vers une commande depuis une ligne de réception
- Amélioration de la sélection de nouvelles adresses à l'édition d'un document
- Amélioration du filtrage des contacts depuis la liste des paniers

yuzSection Licences

# Validation des licences

Les licences de l'utilisateur actif sont désormais validées lors de l'accès à certains écrans. En cas d'apparition du message suivant

![license check](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/license-check.webp?w=80%)

Demandez à votre administrateur de vous ajouter une licence DESKTOP. Il peut suivre la notice ci-dessous afin de vous ajouter la licence.

# Ajout d'une licence à un utilisateur

Pour ajouter une licence à un de vos utilisateurs, rendez-vous dans le menu _Administration/Utilisateurs_ puis cliquez sur le bouton _Éditer_ en face de l'utilisateur concerné.

Vous pouvez alors visualiser ses licences :

![licences](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/licenses/licenses-user-page.webp?w=100%)

Cliquez sur Éditer pour ouvrir la page de configuration des licences:

![licences update](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.2.0/licenses/licenses-update.webp?w=100%)

||| Attention : sauvegarder mettra à jour les licences et entrainera une modification de la facturation à tout ajout de licence.

yuzSection Édition de documents

En plus de pouvoir sélectionner les emails et adresses du contact, il est désormais possible de définir directement dans la modale d'édition de documents une nouvelle adresse ou email.

![edit contact select](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/doc-edit-contact-select.webp?w=80%)

Cela est particulièrement utile lorsque votre contact ne dispose pas d'adresse au moment où vous souhaitez le facturer.

De plus, vous pouvez désormais éditer les informations d'un contact directement depuis cette même modale.

![edit contact update](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/doc-edit-contact-update.webp?w=80%)

|| Attention : l'édition met à jour la fiche du contact et une modification d'une adresse (email ou postale) existante remplacera de manière effective celle-ci sur la fiche du contact.

yuzSection Dossiers produits

Nous avons amélioré l'affichage d'un dossier produit ainsi que des informations d'une fiche véhicule.

![dealer file](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/dealer-file.webp?w=100%)

Cet affichage permet d'accéder plus rapidement aux actions importantes, O.R. ou expertises diverses.

![idp](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/idp.webp?w=100%)

yuzSection Yuzer Pour les franchisés (LINK)

| Cette section s'adresse aux utilisateurs franchisés détenteurs d'une licence YUZER LINK

|| Cette documentation sera étoffée !

# Commandes de véhicules

Vous pouvez utiliser les fonctions de commandes habituelles pour commandez vos véhicules chez vos fournisseurs hébergés par Yuzer.

- Soit via la section `En attente de commande`
  - Sélectionnez votre fournisseur
  - Cliquez sur `Commandes dossiers`: vous pouvez voir vos commandes et ajouter des produits à la commande par référence, vous pouvez créer des dossiers pour vos produits déjà commandés qui n'ont pas de dossier.
- Allez dans la section `Commandes` pour créer une commande manuelle.
  - Cliquez sur `Ajouter une commande manuelle`
  - Ajoutez ce que vous voulez commander
  - Cliquez sur `Valider`, puis, dans la fenêtre qui apparaît sur `Commander` pour créer une nouvelle commande chez votre fournisseur.

![create order for link](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/link-make-order.webp?w=60%)

Lorsque votre fournisseur aura expédié votre commande, vous la retrouverez dans vos `Transferts` depuis lesquels vous pourrez faire votre réception.

# Garantie et vente

## Démarrage de garantie d'un véhicule de démo ou de courtoisie

Vous pouvez démarrer la garantie depuis les actions de la fiche produit.

![start warranty](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/start-warranty.webp?w=60%)

## Enregistrement de la vente et démarrage de la garantie d'un véhicule

Vous pouvez désormais clôturer un dossier véhicule et ainsi transmettre l'information de livraison ainsi que le démarrage de garantie.

yuzSection Yuzer pour les importateurs

# Évènements de vente et garantie

Si vous êtes importateur et êtes responsable de la garantie des produits, vous pouvez désormais visualiser les évènements de vente et d'enregistrement de garantie de votre réseau depuis l'onglet `Évènements` du menu concernant vos produits identifiés.

![list events](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/idp-supplier-list-events.webp?w=60%)

# Enregistrement des informations de contact

yuzSection Général

## Améliorations

- Nous avons ajouté des filigranes aux documents générés dans le cas d'un aperçu ou dans les environnements de démo.
- La sélection d'un dossier véhicule depuis un panier pré-filtre désormais sur les dossiers ouverts, même si le dernier écran consulté concernait les dossiers clos.
- Vous pouvez désormais configurer un thème pour toute votre entité (version beta).
  ![theme configuration](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/theme-configuration.webp?w=60%)
- Un QR code a été rajouté sur les galeries de document permettant à la fonctionnalité de revenir suite à la migration des expertises vers celles-ci.
- La liste des paniers peut désormais être filtrée par client.
  ![filter basket by contact](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/search-basket-by-contact.webp?w=60%)
- Nous avons ajouté le support des filtres personnalisés dans l'analytique.
- Il est maintenant possible d'éditer l'adresse postal et mail du client dans la fenêtre d'édition de facture.
  ![invoice modal](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.6.0/invoice-billing-modal.webp?w=60%)

## Corrections

- Correction de l'affichage de la date d'achat sur un dossier véhicule.
- La création d'une nouvelle catégorie de produit identifié ne nécessite plus le choix d'un fournisseur.
