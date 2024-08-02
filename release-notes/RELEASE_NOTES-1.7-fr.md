# Juillet 2021 - Version 1.7.0

- Les réservations et commandes de stock d'un contact sont désormais affichés sur sa page. Vous pouvez aggrandir la section comme les autres en cliquant sur son titre.
- Nous avons remplacé les _#_ par _Ref._ pour indiquer les références produit dans plusieurs écrans de l'application.
- Nous avons améliorés quelques confirmations d'annulations qui proposaient les choix _annuler_ pour annuler l'opération et _annuler_ pour confirmer l'annulation.
- La performance de plusieurs écrans tels que les écrans de justificatifs comptables ansi que certaines opérations de panier a été améliorée.
- Le numéro du dossier de véhicule n'est plus affiché au niveau de la liste de produits sur les documents (factures, bon de commande, etc.).
- Vous pouvez désormais filtrer les tâches annulées dans les vues de calendrier.
- La lisibilité de l'écran contact a été améliorée.
- Le numéro de dossier du véhicule n'apparâit plus sur la ligne dans les documents (factures etc.)

## Les acomptes

Dans Comptabilité -> Configurer, il est maintenant possible de configurer des acomptes par défaut, pour les différents types d'opérations.

Il est possible de choisir soit un montant fixe, soit un pourcentage du prix, arrondi selon la stratégie selectionnée.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/deposit-config.png"/>

## Moyens de paiement

### Assossiation aux types de panier

Les moyens de paiements sont maintenant associés aux types de panier : lors de l'encaissement d'un paiement, seuls les moyens de paiements correspondant au type du panier seront disponibles.

### Association des moyens de paiements aux caisses

Dans Comptabilité -> Configurer, les caisses sont maintenant créées et configurées depuis un nouvel onglet.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/cashdesk-config.png"/>

La grande nouveauté est qu'il faut maintenant associer les moyens de paiements aux caisses afin d'avoir des choix plus pertinent lors du paiement. Il est à noté qu'une caisse ne peut avoir qu'un seul moyen de paiement de type "Espèce".

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/cashdesk-modal.gif"/>

### Les paiements rapides

Afin de fluidifier la saisie des lors des paiements, l'écran de saisie à été amélioré. Il est dorénavant possible de remplir les montants avec un seul click.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/payment-modal.gif"/>

Dans le cas ou un acompte par défaut aurait été configuré, il est possible de choisir "Acompte" afin de remplir automatiquement les champs avec le montant de l'acompte.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/payment-deposit-modal.gif"/>

Comme vous pouvez le constater, dans le cas d'un paiement espèce Yuzer vous permet de rentrer le montant reçu du client et vous indique le montant à lui rendre.

## Prise de rendez-vous

Nous avons apporté plusieurs améliorations à la prise de rendez-vous afin d'améliorer sa fluidité.

- Si vous avez configuré des vues pour différencier la disponibilité des mécaniciens entre temps de réparation et préparation véhicule, la vue de réparation est sélectionnée par défaut.

Une fois le client, le véhicule et le travail défini (soit par template soit en précisant un détail et une durée) vous sélectionnez l'emplacement de la tâche atelier.

- Afin de sélectionner celle-ci vous pouvez cliquer sur le calendrier dans la vue semaine, mais aussi accéder rapidement à la vue jour en cliquant sur le titre du jour choisi. Ceci vous permettra de rapidement définir le mécanicien à assigner, ou d'avoir une meilleure visibilité sur le choix du moment de la journée ou placer le rendez-vous.

Lorsque le rendez-vous est placé à l'atelier Yuzer bascule le calendrier sur le calendrier des réceptions/livraisons véhicule et vous pourrez alors définir le rendez vous de réception du véhicule client, puis celui de livraison.

Vous pouvez ensuite comme avant sélectionner éventuellement un prêt de véhicule de courtoisie.

Une fois que les information sont complétées vous pouvez:

- Soit créer le panier mais ne pas l'envoyer à l'atelier; ceci vous permet éventuellement de compléter les détails de la réparation, tant en ajoutant les pièces qu'en détaillant la main d'oeuvre avant de l'envoyer à l'atelier.
- Soit créer rapidement le panier en l'envoyant directement à l'atelier (auquel cas la tâche atelier est créer telle qu'elle a été définie et placée dans le calendrier).

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/booking-modal.gif" width="100%"/>

## C'est corrigé!

- La charge atelier sur la vue jour du calendrier n'était pas bien mise à jour lors du changement de date.
- La charge atelier incluait les tâches annulées.
- La sélection de dates sur la vue du journal en comptabilité ne fonctionnait plus.
- Les rachats de crédits ne peuvent plus être réservés en stock.
- Les utilisateurs non-administrateurs pouvaient rencontrer un problème avec les notifications Ringover. Cela causait aussi l'apparition d'un message d'erreur au lancement de Yuzer.
- Dans certains cas, lors de l'édition d'un bon de commande de véhicule, la boite de dialogue demandant les informations pouvait être affichée deux fois.
- Les lignes de rachat de crédit étaient réservées en stock. Cela n'avait pas lieu d'être et elles sont bien ignorées dans la gestion de stock désormais.

## Auto-création de tâches sur email - Beta

Il est désormais possible d'activer l'analyse automatique de vos mails. Cette option requiert votre consentement et n'est pas activée par défaut. Vous devez l'activer sur la page de configuration du mail de votre entité.

<div class="alert alert-info">
Cette fonctionnalité est disponible en beta elle peut-être utilisée dès maintenant et sera améliorée dans les versions futures. N'hésitez pas à nous apporter vos retours.
</div>

<div class="alert alert-warning">
Attention, en bêta, la désactivation de la fonctionnalité peut mettre du temps à être effective. Merci de contacter notre support si vous l'avez activé puis souhaitez que Yuzer stoppe la récupération des emails.
</div>

Vous pouvez désormais créer automatiquement des tâches sur réception de certains emails pré-formattés.

Pour cela rendez-vous dans la configuration des emails pour activer la fonctionnalité en cochant la case _Souscrire à l'analyse automatique des emails_.
Notez que vous devez entrer vos mots de passes à nouveau afin de sauvegarder la configuration.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/emailfetch-setup.gif" width="100%"/>

Une fois activé vous devez initialiser votre boite email depuis l'écran _boite de réception_. Notez qu'une fois lancée il vous faudra attendre quelques minutes pour que Yuzer complète la récupération de vos emails.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/emailfetch-init.gif" width="100%"/>

La dernière étape consiste à créer vos templates d'email pour que le robot puisse extraire et créer les tâches en fonction de vos emails reçus.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/emailfetch-create-template.gif" width="100%"/>

Vous retrouverez alors vos tâches dans la liste des tâches du groupe associé.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.7.0/emailfetch-task.png" width="100%"/>
