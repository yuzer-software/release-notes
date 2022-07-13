# Juin 2022 - Version 1.28.0

## Analytics

### Drill down

Les tables "Drill Down" arrivent dans analytics! 

Une table "Drill Down" est constituée de plusieurs niveaux et permet de "zoomer" du premier niveau vers les niveaux inférieurs. 
Chaque niveau regroupe des lignes de données selon certaines colonnes, et affiche d'autres colonnes de façon agglomérées.

Dans l'exemple suivant, on souhaite afficher la marge et le prix de vente HT par semaine.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/drilldown-level1.png" />

Il est ensuite possible de zoomer sur une semaine donnée, pour connaitre le détail des ventes en cliquant sur une des lignes. 
On accède alors au niveau 2, qui affiche la marge, le prix de vente HT et la quantité, par catégorie.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/drilldown-level2.png" />

Il est possible d'ajouter autant de niveaux que souhaité.

#### Configuration
La table se configure dans "Affichage".

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/drilldown-config.png" />

Pour chaque niveau, on sélectionne les colonnes qui permettront de regrouper les données dans "Grouper par", et les colonnes qui seront agrégées dans "Colonnes visibles". 

### Filter

Il est ensuite possible de filtrer les tables selon différents critères, que vous trouverez dans "Filtres".  

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/analytics-filter.png" />

## Améliorations diverses

- Sur l'écran de liste de paniers, nous affichons désormais le montant dû, le total HT, le total TTC, ainsi que le total de paiements.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/bsk-list.png" width="600px"/>

- Il est maintenant possible de filtrer les justificatifs de cession par type de cession.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/cession-type-filter.png" width="600px"/>
  
- Il est maintenant possible de filtrer en sélectionnant plusieurs catégories sur la vue de catalogue produits.
- Le filtre de catégories a également été ajouté sur l'écran _En attente de commande_

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/category-filter.png" width="350px"/>
  
- Amélioration de l'affichage de la colonne de quantity. Des `…` apparaissent lorsque tous les chiffres du champs ne s'affichent pas à l'écran. Aussi, la quantity ne déborde plus sur le prix d'achat.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/bsk-time-qty-column.png" width="225px"/>
