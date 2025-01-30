# Octobre 2024 - Version 3.9.x

yuzSection Modèles et Rappels SMS

## Modèles SMS

Vous pouvez désormais configurer des modèles SMS depuis l'écran _Administration / Communication Hub / Téléphonie / Modèles_.

![SMS templates](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-1.webp?w=100%)

Pour ajouter un nouveau modèle cliquez sur _Ajouter_. Une boite de dialogue s'ouvre alors dans laquelle vous pouvez entrer le nom du modèle.

![SMS template new](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-2.webp?w=480px)

Le modèle est alors ouvert en édition. Entrez le texte du message en utilisant au besoin les variables choisies.

![SMS template edit](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-3.webp?w=968px)

||| Attention certaines variables ne sont disponible que dans le contexte d'une tâche, donc depuis un rappel (voir ci-dessous).

Si vous cliquez sur Annuler le modèle ne sera pas créé. Si vous cliquez sur Sauvegarder le modèle sera enregistré en tant que brouillon. Il ne sera pas utilisable tant que non publié.

Une fois l'édition terminée vous pouvez donc publier le modèle, mais aussi le supprimer ou l'éditer à nouveau.

![SMS template saved](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-4.webp?w=968px)

Lorsque le modèle est publié il peut-être utilisé dans le cadre de rappel ou par vos équipes depuis la boite de dialogue d'envoi de SMS.
Un indicateur dans la liste (coche verte) vous indique que le modèle est publié. Par ailleurs un bouton vous permet changer l'affichage entre le modèle publié et le modèle en brouillon.

![SMS template published](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-5.webp?w=968px)

Vous pouvez dé-publier un modèle publié.
Si vous faîtes des modifications au brouillon, celle-ci ne seront prises en compte que lorsque vous publiez celles-ci.
Pour annuler les modification effectuées au brouillon et revenir à la dernière version publiée vous pouvez utiliser le bouton _Revenir_

![SMS template view published](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-6.webp?w=968px)

## Utilisation d'un modèle SMS

Lorsque vous envoyez un message à un utilisateur (depuis sa fiche contact ou le module de réception par exemple), vous pouvez désormais choisir un modèle:

![SMS template send normal](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-send-1.webp?w=480px)

||| Attention, si le modèle contient des variables liées à une tâche, celles-ci seront remplacées par un texte vide

![SMS template send task variables](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/sms-tpl-send-2.webp?w=480px)

## Configuration des rappels SMS

Vous pouvez configurer désormais des rappels SMS, pour cela rendez-vous sur l'écran _Administration / Communication Hub / Rappels_ et cliquez sur _Ajouter_.

![Reminder](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/3.9.0/reminder.webp?w=100%)

Les rappels sont effectués par rapport à des tâches dans n'importe lequel de vos espaces de travail. Vous pouvez filtrer les tâches sur lesquelles envoyer un rappel en fonction:

- De l'espace de travail
- De l'état de la tâche

Vous devez ensuite sélectionner un modèle de message (voir ci-dessus).

Finalement vous devez configurer une, ou plusieurs planification pour le rappel du message. Sélectionnez en premier l'heure d'envoi du message. Celle-ci peut-être soit à heure fixe (par exemple à 19h environ) soit basée sur l'heure du rendez-vous.

Si l'heure d'envoi du message est à heure fixe, vous pouvez configurer un rappel un nombre de jours avant la tâche. Ce nombre de jour doit-être 1 jour au minimum.
Si l'heure d'envoi du message est à l'heure du rendez-vous vous configurez également un rappel un nombre de jours avant la tâche mais nous permettons alors de configurer un rappel le jour même (0 jours avant le rendez-vous), vous devrez alors sélectionner un nombre d'heures avant le rendez-vous pour le rappel.

yuzEnd

yuzSection Général

## Améliorations

- Amélioration de l'écran de licences qui affiche désormais le nom de l'employé et la possibilité de modifier les licences directement depuis cette page lorsque le mois sélectionné est le mois courant.
- Améliorations de stabilité et performance
