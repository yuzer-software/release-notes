# Décembre 2021 - Version 1.14.0

Améliorations diverses:

## Les caisses

Diverses améliorations ont été apportées sur la gestion des caisses.

### Caisse par défaut

Dorénavant, lors de la navigation entre les différents écrans de configuration des caisses, 
ainsi que dans la modal de paiement, la dernière caisse utilisée est sauvegardée et affichée par défaut.
Cette sauvegarde est valable pour un utilisateur donné, sur un poste physique donné.

### Alerte sur l'écran de paiement lors de l'utilisation d'une caisse fermée

Dans l'écran de paiement, une alerte apparait maintenant si la caisse sélectionnée est fermée et les boutons sont invalidés.

### Mémoire des billets rentrés lors de la fermeture d'une caisse

Au moment de la fermeture d'une caisse et tout particulièrement du comptage des billets, les billets déjà comptés sont gardés en mémoire.
Ainsi, si vous êtes amené à changer d'écran pendant le comptage, les billets rentrés seront récupérés lorsque vous reprendrez la clôture.

### Nouvelle configuration "Ouverture d'une caisse avec les billets de la veille"

Une nouvelle configuration est maintenant possible dans le paramètrage des caisses.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.14.0/cashdesk-openWithClosingAmount.png" height="100"/>

Cette nouvelle option permet d'avoir comme montant et billets à l'ouverture de la caisse, les valeurs à la clôture précédente. 
Cette option remplace donc le "Montant d'ouverture souhaité".

Il est à noté que dans cette configuration, il n'est plus possible d'ouvrir une nouvelle caisse avant d'avoir finalisé la clôture de la caisse courante, 
le compte de billet étant nécessaire pour connaitre le contenu de la nouvelle caisse.

### Remaniement du processus de clôture de caisse

Lors de la clôture de la caisse, le comptage des billets se fait maintenant directement à la validation. 
Les étapes sont donc dorénavant:
- Initialisation de la clôture
  
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.14.0/cashdesk-initiateClosing.png" height="100"/>

- Comptage des billets et vérification des tickets
- Validation de la clôture

# C'est corrigé

- Les fonction d’alignement du texte dans les lignes de commentaires du panier ont été corrigées.

# Application mobile

## Tâches

Lorsqu'une tâche est liée à un produit, les détails de ce produit apparaissent désormais. Il est possible d'aller vers les détails du produit en question avec l'icône correspondant (en bas à gauche).

Dans le cas d'un véhicule immatriculé, la plaque d'immatriculation est affichée entre parenthèses.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.14.0/task-with-motorcycle.png" height="100"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.14.0/task-with-bike.png" height="100"/>

<img src="./1.14.0/task-with-motorcycle.png" height="400"/>
<img src="./1.14.0/task-with-bike.png" height="400"/>

## Détails d'un produit

La page des détails de véhicules et produit a été révisée et étoffée. De nombreuses informations y ont été ajoutées et vous pouvez désormais consulter toutes les photos expertises liées à ce produit et en créer de nouvelles.

<img src="./1.14.0/motorcycle-details.png" height="400"/>
<img src="./1.14.0/bike-details.png" height="400"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.14.0/motorcycle-details.png" height="100"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.14.0/bike-details.png" height="100"/>

## C'est corrigé

- Sur iOS, il est possible d'exporter beaucoup de photos simultanément.
