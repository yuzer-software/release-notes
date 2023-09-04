# Aout 2023 - Version 2.15.0

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


## Annulation de facture

Quand on annule une facture, les éventuelles réservations clientes liées au panier changent aussi d'état. Dorénavant on peut choisir si l'on souhaite leur annulation ou bien si l'on préfère qu'elles retournent dans l'état PRÉPARÉES, avec le déplacement de stock idoine.


## Réception

Quand on réceptionne plusieurs unités d'un même produit, Yuzer ajuste automatiquement la quantité reçue plutôt que de créer une nouvelle ligne de réception à chaque lecture de code barre. Ceci permet d'avoir une description de la réception plus concise.
Cependant il existe quelques cas où l'on peut préférer dupliquer une ligne de réception, par exemple lorsque toutes les unités n'ont pas le même prix. À cette fin, un nouveau bouton a été ajouté pour pouvoir changer le comportement.

<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/reception/add_to_new_line_before.png"/>
<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/reception/add_to_new_line_result.png"/>

## Enrichissement des produits

Les travaux concernant l'enrichissement des produits commencés dans la version précédente ont été complétés afin de pouvoir extraire des propriétés des produits depuis des champs tel que leur identifiant.

Afin d'activer cette possibilité il faut qu'une des règles d'enrichissement ait un filtre afin d'être appliquée à une catégorie spécifique de produits (par exemple aux vêtements hauts uniquement). En effet les propriétés des produits sont liées à leur catégorie.

Nous allons enrichir petit à petit certains de nos catalogues automatisés afin d'exploiter ces enrichissement lorsque cela est possible. N'hésitez pas, si vous connaissez des règles permettant d'extraire des couleurs ou tailles depuis des identifiants de produits, à les communiquer à notre équipe support.


## Corrections
