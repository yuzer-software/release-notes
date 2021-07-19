# Juillet 2021 - Version 1.7.0

- Les réservations et commandes de stock d'un contact sont désormais affichés sur sa page. Vous pouvez aggrandir la section comme les autres en cliquant sur son titre.
- Nous avons remplacé les _#_ par _Ref._ pour indiquer les références produit dans plusieurs écrans de l'application.
- Nous avons améliorés quelques confirmations d'annulations qui proposaient les choix _annuler_ pour annuler l'opération et _annuler_ pour confirmer l'annulation.
- La performance de plusieurs écrans tels que les écrans de justificatifs comptables ansi que certaines opérations de panier a été améliorée.

## Moyens de paiement

### Assossiation aux types de panier

Les moyens de paiements sont maintenant associés aux types de panier : lors de l'encaissement d'un paiement, seuls les moyens de paiements correspondant au type du panier seront disponibles.

## Configuration des entités — analyse automatique de mails

Il est désormais possible d'activer l'analyse automatique de vos mails. Cette option requiert votre consentement et n'est pas activée par défaut. Vous devez l'activer sur la page de configuration du mail de votre entité.

## Prise de rendez-vous

Nous avons apporté plusieurs améliorations à la prise de rendez-vous afin d'améliorer sa fluidité.

- Si vous avez configuré des vues pour différencier les temps mécanicien entre réparations et préparation véhicule la vue de réparation est sélectionnée par défaut.

Une fois le client, le véhicule et le travail défini (soit par template soit en précisant un détail et une durée) vous sélectionnez l'emplacement de la tâche atelier.

- Afin de sélectionner celle-ci vous pouvez cliquer sur le calendrier dans la vue semaine, mais aussi accéder rapidement à la vue jour en cliquant sur le titre du jour choisi. Ceci vous permettra de rapidement définir le mécanicien à assigner, ou d'avoir une meilleure visibilité sur le choix du moment de la journée ou placer le rendez-vous.

Lorsque le rendez-vous est placé à l'atelier Yuzer bascule le calendrier sur le calendrier des réceptions/livraisons véhicule et vous pourrez alors définir le rendez vous de réception du véhicule client, puis celui de livraison.

Vous pouvez ensuite comme avant sélectionner éventuellement un prêt de véhicule de courtoisie.

Une fois que les information sont complétées vous pouvez:

- Soit créer le panier mais ne pas l'envoyer à l'atelier; ceci vous permet éventuellement de compléter les détails de la réparation, tant en ajoutant les pièces qu'en détaillant la main d'oeuvre avant de l'envoyer à l'atelier.
- Soit créer rapidement le panier en l'envoyant directement à l'atelier (auquel cas la tâche atelier est créer telle qu'elle a été définie et placée dans le calendrier).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/booking-modal.gif" width="100%"/>

## Correction de bugs

- La charge atelier sur la vue jour du calendrier n'était pas bien mise à jour lors du changement de date.
- La sélection de dates sur la vue du journal en comptabilité ne fonctionnait plus.
