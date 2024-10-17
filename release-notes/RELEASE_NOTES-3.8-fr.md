# Octobre 2024 - Version 3.8.x

yuzSection Version 3.8.8 et suivantes

## Stocks dossiers (véhicules) à date

Vous pouvez désormais afficher, et exporter, vos listes de dossiers à date:

![Stock at date](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.8.0/stock_at_date.webp?w=300px)

Le stock à date peut-être établi sur base de:

- la date de création du dossier
- la date de facture d'achat du dossier
- la date de réception du dossier

## Améliorations

- Caching et Amélioration du chargement dossiers produits dans l'analytique (pour les tableaux de bords utilisant des colonnes d'identifiants). Visible sur le second chargement et les suivants.
- Correction des icones de téléphonie sur la fiche client suite à la mise à jour de la librairie d'icones.

yuzSection Application mobile

## Connexion OTP (sans votre mot de passe)

Il est désormais possible de se connecter avec un PIN plutôt qu'avec votre mot de passe utilisateur.

![select OTP](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.8.0/otp-1.webp?w=300px)

yuzLeft

![OTP popup](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.8.0/otp-2.webp?w=300px)

yuzRight

Depuis l'application de bureau, sélectionnez "Connexion sans mot de passe" et scannez le QR-code affiché avec votre téléphone.

Un code apparait alors sur votre téléphone: recopiez-le sur l'application de bureau: vous êtes connecté !

![OTP mobile](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.8.0/otp-mobile.webp?w=200px)

yuzEnd

yuzSection Général

## Améliorations

- Amélioration des messages d'erreurs techniques.
- Amélioration du time tracking des tâches.
- Possibilité d'ouvrir l'écran de release notes dans une nouvelle fenêtre.
- Ajout d'un menu pour que chaque utilisateur puisse changer son mot de passe, à partir du menu `Information du comptes`.
- Amélioration du workflow sur l'édition du bon d'achat d'une reprise. Aussi, le terme 'Occasion' est maintenant imprimé à la place de 'Occasion à réceptionner'.
- Ré-organisation du menu d'administration.
- Amélioration pour se rendre compte d'une éventuelle erreur lorsque l'on quitte le mode `édition` sur une réception.
- Fonctionnalité pour créer des templates de SMS: `Administration > Communication Hub > Téléphonie Modèles`.
