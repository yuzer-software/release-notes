# Aout 2023 - Version 2.15.0

## Opérations entre différents comptes

Auparavant vous pouviez déjà effectuer des opérations de commandes, facturations et livraisons à une autre entité de votre groupe (ou compte Yuzer).
Dorénavant vous pouvez effectuer ces opérations avec une entité Yuzer qui n'est pas de votre groupe, à la condition que les deux entités aient préalablement autoriser cette collaboration.

### Lier un contact à une entité externe

En tant que fournisseur, pour accepter qu'une entité commande des pièces chez
vous (c'est-à-dire créent des paniers, etc.), vous devez d'abord leur donner
la permission de le faire. Pour cela, allez dans le nouveau menu
`Administration/Codes d'association` et cliquez sur `Ajouter`. Choisissez une
date d'expiration, et validez. Notez qu'une fois que la date d'expiration est
atteinte, vous devrez soit la repousser soit re-générer un code (si vous ne
souhaitez pas d'expiration, vous pouvez configurer une date très loin dans le futur).

<img width="400" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-1-admin.webp"/>

Vous verrez le détail du code généré. Vous pouvez :

- l'envoyer par mail (bouton `enveloppe`) ou par tout autre moyen de
  votre choix en le copiant (bouton `copier`)
- ajouter un libellé personnalisé pour vous rappeler son objet ou son destinataire,
- voir le nom de l'entité Yuzer qui a utilisé ce code
- voir la date d'expiration du code
- révoquer le code pour cesser de travailler avec l'entité sus-mentionnée,
  ou le réactiver.

<img width="500" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-2-detail.webp"/>

En tant qu'entité cliente du fournisseur :

- assurez-vous d'abord que votre fournisseur est lié à une fiche client:

<img width="700" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-3-supplier-is-linked-to-contact.webp"/>

- sur la fiche client, cliquez sur le bouton "lien". Une modale s'ouvre.

<img width="300" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-4-pair-button.webp"/>

- Copiez/collez le code envoyé par votre fournisseur et validez (tapez `Entrée`).

<img width="500" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-5-enter-code.webp"/>

- L'entité de votre fournisseur est désormais liée à votre fiche contact.

<img width="330" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/pairing-code-6-is-linked.webp"/>

## Espaces de travail

Dans le cas où vous gérer un seul atelier physique partagé entre plusieurs entités, vous pouvez désormais relier ces espaces de travail dans Yuzer.

<img width="896" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/workspace-config.webp"/>

Lier les espaces de travail permet de visualiser les tâches de tous les espaces ainsi reliés.
Les tâches provenant d'une autre entité apparaîtront grisées. Il faudra vous connecter sur l'entité où la tâche été créer pour pouvoir la modifier.

<img width="640" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/calendar-shared-tasks.webp"/>

<div class="alert alert-info">
La barre de pourcentage dans la vue calendrier représente la charge pour l'entité courante.
</div>

<div class="alert alert-warning">
Assurez-vous d'avoir les mêmes horaires d'ouverture sur les espaces de travail relié. Dans le cas contraire, les pourcentages d'occupations du calendrier peuvent être erronés.
</div>

## Gestion des calendriers et ressources

Les configurations du **temps de d'occupation** et des **indisponibilités** de leurs ressources sont maintenant partagées entre toutes les entités du compte.
Ainsi, vous devez commencer par définir le pourcentage de temps alloué à chaque entité et ensuite définir le pourcentage de temps pour chaque type de tâches pour une entité donnée.

**Exemple de configuration**:
<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/resource-limit-config.webp"/>

**Droid DUM** a une charge journalière de 40% sur _Bespin_ et 40% sur _Gallactic Empire_ et 20% pour n'importe quelle tâche (<span class="text-info">en bleu</span>).
Pour _Bespin_, il doit partager son temps entre les tâches de `Réparation et maintenance` et `Préparation véhicule`.
Pour _Gallactic Empire_, il consacre 100% de son temps sur n'importe quelle tâche.

**Testeur T** a une charge journalière de 50% sur _Bespin_.
Vous pouvez remarquer qu'il a une configuration avec une règle de 15% de son temps pour des tâches sans tags et le reste pour n'importe quelle tâche.
Cette configuration ne fait pas vraiment de sens : elle est équivalente à une règle de 100% du temps pour n'importe quelle tâche.

<div class="alert alert-warning">
Pour des raisons de simplification, les règles possédant des tags vides comme ci-dessus seront ignorées lors de la sauvegarde.
Nous vous invitons à corriger votre configuration si vous rencontrez un message d'alerte à ce sujet.
</div>

## Corrections
