# Aout 2023 - Version 2.15.0

## Espaces de travail

Dans le cas où vous gérer un seul atelier physique partagé entre plusieurs entités, vous pouvez désormais relier ces espaces de travail dans Yuzer.

<img width="896" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/workspace-config.webp"/>

Lier les espaces de travail permet de visualiser les tâches de tous les espaces ainsi reliés.
Les tâches provenant d'une autre entité apparaîtront grisées. Il faudra vous connecter sur l'entité où la tâche été créer pour pouvoir la modifié.

<img width="640" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/calendar-shared-tasks.webp"/>

<div class="alert alert-info">
La barre de pourcentage dans la vue calendrier représente la charge pour l'entité courante.
</div>

<div class="alert alert-warning">
Assurez-vous d'avoir les mêmes horaires d'ouverture sur les espaces de travail relié. Dans le cas contraire, les pourcentages d'occupations du calendrier peuvent être erronés.
</div>

## Gestion des calendriers et ressources

La configuration du **temps de d'occupation** et de leurs **indisponibilités** des ressources sont maintenant partagées entre toutes les entités du compte.
Ainsi, vous devez commencer par définir le pourcentage de temps alloué à chaque entité et ensuite définir le pourcentage de temps pour chaque type de tâches pour une entité donnée.

**Exemple de configuration**:
<img width="1024" src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/2.15.0/resource-limit-config.webp"/>

**Droid DUM** a une charge journalière de 40% sur _Bespin_ et 40% sur _Gallactic Empire_ et 20% pour n'importe quelle tâche (<span class="text-info">en bleu</span>).
Pour _Bespin_, il doit partager son temps entre les tâches de `Réparation et maintenance` et `Préparation véhicule`.
Pour _Gallactic Empire_, il consacre 100% de son temps sur n'importe quelle tâche.

**Testeur T** a une charge journalière de 50% sur _Bespin_.
Vous pouvez remarquer qu'il a une configuration avec une règle de 15% de son temps pour des tâches sans tags et le reste pour n'importe quelle tâche.
Cette configuration ne fait pas vraiment de sens et revient au même que s'il avait simplement 100% sur n'importe quelle tâche.

<div class="alert alert-warning">
Pour des raisons de simplification, les règles possédant des tags vides comme ci-dessus seront ignorées lors de la sauvegarde.
Nous vous invitons à corriger votre configuration si vous rencontrez le message d'alerte.
</div>

## Corrections
