# Mars 2025 - Version 3.12.x

yuzSection Export de catalogues

Yuzer permet aux éditeurs de catalogues (sous réserve d'activation de la fonctionnalité par le support) d'exporter ceux-ci automatiquement. Les catalogues exportés peuvent alors être téléchargés par les autres utilisateurs abonnés à celui-ci.

Depuis un catalogue dont vous êtes l'éditeur, rendez-vous dans l'onglet _Exportation_

![Catalog export](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-catalog.webp?w=100%)

Vous pouvez ici visualiser les jobs d'exportation existant ou en créer un nouveau avec le bouton _Nouveau_.

À la création d'un nouvel export, une fenêtre de configuration s'ouvre et vous permet de configurer

- le nom du catalogue exporté (il peut être différent du nom du catalogue en fonction du format ou des filtres que vous pourriez définir).
- une description
- Le format du fichier CSV exporté (dont le choix des colonnes)

![Catalog export format](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-modal-format.webp?w=800px)

- Et dans l'onglet `Filtres` la configuration des éléments à exporter

![Catalog export filter](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-modal-filter.webp?w=800px)

L'export est exécuté chaque nuit et vous pouvez alors lancer le téléchargement du catalogue depuis l'écran du catalogue dans YUZER à l'aide du bouton télécharger (cf. première capture d'écran ci-dessus).

||| Les exports de catalogues peuvent également être retrouvés depuis la section `Automates`.

![Catalog export automation list](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-automation.webp?w=100%)

Vous retrouverez les résultats de votre export dans l'onglet `Résultats d'exécution`.

![Catalog export results](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/catalog-export-results.webp?w=100%)

yuzSection Écran client et marketing

Vous pouvez désormais configurer un media à afficher sur votre écran déporté:

![Customer screen marketing configure](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/cust-screen-marketing.webp?w=100%)

- Quand aucun panier n'est actif
  ![Customer screen no basket](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/marketing-nobasket.webp?w=100%)

- Quant un panier est actif
  ![Customer screen basket](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/marketing-basket.webp?w=100%)

### Configuration d'une vidéo youtube

yuzLeft

Pour configurer une vidéo youtube, vous devez utiliser leur API d'intégration (https://support.google.com/youtube/answer/171780).

Voici les étapes recommandées :
- Aller sur la vidéo que vous voulez partager
- Clic droit puis `Copier le code d'intégration` (voir ci-contre)
- Coller le texte copié dans un éditeur de texte (bloc notes, mail, word, etc.)

  ```
  <iframe
    width="937" height="515"
    src="https://www.youtube.com/embed/Dagrn_9V4jE"
    title="Yehudi Menuhin plays Paganini"
    ...
    ></iframe>
  ```

- Extraire l'URL source: `https://www.youtube.com/embed/Dagrn_9V4jE` (effacer le reste)
- Paramétrer la source:
  - ajouter, avant les paramètres: `?`
  - ajouter les paramètres (voir ci-dessous les paramètres possibles) — paramètres recommandés:
    - `?&autoplay=1&loop=1&controls=0&mute=1&rel=0&modestbranding=1`
- Ce qui donne l'URL suivante:
  `https://www.youtube.com/embed/Dagrn_9V4jE?&autoplay=1&loop=1&controls=0&mute=1&cc_load_policy=1&rel=0&modestbranding=1`
- Utilisez cette URL dans Yuzer avec le type `iFrame`:

yuzRight

![Copy integration link](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/marketing-youtube-config.webp?w=400px)

yuzEnd

![Copy integration link](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/marketing-youtube-in-yuzer.webp?w=800px)


Voici les paramètres pour une URL youtube intégrée qui pourraient vous être utiles:

- `&autoplay=1` : La vidéo démarrera automatiquement dès le chargement de la page.
- `&loop=1` : La vidéo se mettra en boucle une fois qu'elle aura terminé.
- `&start=xx` : La vidéo commencera à partir d'un point spécifique, en secondes (par exemple, start=60 commencera à 1 minute).
- `&end=xx` : La vidéo s'arrêtera à un point spécifique, en secondes.
- `&controls=0` : Les contrôles du lecteur (play, pause, volume) seront masqués.
- `&mute=1` : La vidéo sera coupée (muet) au démarrage.
- `&rel=0` : Empêche l'affichage de vidéos connexes à la fin de la vidéo.
- `&modestbranding=1` : Réduit l'image de marque de YouTube (le logo YouTube est plus discret).
- `&cc_load_policy=1` : Affiche les sous-titres par défaut.
- `&iv_load_policy=3` : Masque les annotations sur la vidéo.


yuzSection Général

# Tâches commerciales

Vous pouvez désormais facilement créer une tâche de suivi depuis une tâche existante à J+2/4/7.

![Task follow up](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.12.0/task-follow-up.webp?w=100%)

## Divers

- Amélioration de la persistance des configurations calendrier sur les vues commercial et atelier.
- Amélioration de la réinitialisation de mot de passe (un email valide pour l'utilisateur reste requis).
- Amélioration mineure de l'affichage des variants sur le détail d'une fiche produit.

- Correction de rafraichissement sur l'écran de calendrier lors de l'accès à une date par le sélecteur de dates.
- Correction de la connexion lors de certains cas d'expiration de token aux limites.
- Correction de comportements de pré-sélection dans un panier multi-groupes (écran de paiement etc.).
- Correction de la configuration d'une catégorie de tarification dans une règle d'enrichissement de catalogue.
- Correction de la mise à jour des CGV sur 1 colonne.
- Les réservations de stock affichent désormais la référence produit et son label par défaut sur tous les écrans.

Comme toujours n'hésitez pas à exprimer vos demandes, en toute courtoisie, auprès de nos équipes support !
