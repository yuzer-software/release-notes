# Juillet 2022 - Version 1.28.3

## Améliorations diverses

- La sélection de fournisseurs dans les filtres personalisés impliquaient de rentrer l'identifiant Yuzer interne et non le nom du fournisseur. Un sélecteur a été ajouté pour permette le bon usage de la fonction.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.29.0/analytics-supplier-filter.png" width="600px"/>

# Juillet 2022 - Version 1.28.1

## Améliorations diverses

- Le temps disponible sur le widget de M.O. prends désormais bien en compte les pourcentages de non-affectation.

# Juillet 2022 - Version 1.28.0

## Gestion des dates d'échéances pour les chèques

Vous pouvez désormais configurer un moyen de paiement de type chèque pour qu'il soit ou non possible de définir une date d'encaissement différée.

### Configuration du moyen de paiement

Rendez vous dans un premier temps dans _Comptabilité / Configurer / Moyens de paiements_. Vous pouvez alors modifier ou créer un moyen de paiement de type chèque et permettre l'autorisation des encaissements différés.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/payment-mean-new.png" width="640px"/>

<div class="alert alert-warning">
Attention il n'est pas possible pour l'instant de modifier un moyen de paiement de type chèque pour ne plus autoriser un encaissement différé. Il vous faudra, si vous avez activé celui-ci et souhaitez annuler ceci, désactiver le moyen de paiement et en créer un nouveau.
</div>

Lors de la configuration vous pouvez configurer le comportement de paiement différé, si le paiement doit impacter la balance client immédiatement ou au moment de l'encaissement ainsi que le nombre de jours de délai maximum autorisés pour spécifier la date d'encaissement (vos collaborateurs ne pourront pas alors saisir une date ultérieure).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/payment-mean-new-2.png" width="640px"/>

### Encaissement d'un chèque

A l'encaissement si le moyen de paiement autorise une date d'encaissement différée il est possible de définir celle-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/payment-register-due-2.png" width="740px"/>

Qui sera alors rappelée sur le ticket de caisse ou reçu généré.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/payment-receipt-due.png" width="280px"/>

### Paiements en attente de d'encaissement

Les paiements en attente d'encaissement peuvent-être consultés depuis le nouvel écran ajouté à l'onglet de comptabilité.

Vous pouvez depuis cet écran enregistré le paiement comme collecté ce qui aura pour impact de supprimer celui-ci de l'écran mais également, dans le cas ou la balance client n'est impactée qu'au moment de la collecte de mouvementer celle-ci.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/payment-reclaim.png" width="100%"/>

### Gestion comptable

Comptablement et en gestion de caisse le paiement est comptabilité dans la clôture de caisse à sa date d'enregistrement. Il sera de même passé dans le journal dans la clôture de caisse du jour. Cependant une date d'échéance sera associée et exportée au jour d'encaisssement défini.

## Analytics

### Drill down

Les tables "Drill Down" arrivent dans analytics!

Une table "Drill Down" est constituée de plusieurs niveaux et permet de "zoomer" du premier niveau vers les niveaux inférieurs.
Chaque niveau regroupe des lignes de données selon certaines colonnes, et affiche d'autres colonnes de façon agglomérées.

Dans l'exemple suivant, on souhaite afficher la marge et le prix de vente HT par semaine.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/drilldown-level1.png" width="100%"/>

Il est ensuite possible de zoomer sur une semaine donnée, pour connaitre le détail des ventes en cliquant sur une des lignes.
On accède alors au niveau 2, qui affiche la marge, le prix de vente HT et la quantité, par catégorie.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/drilldown-level2.png" width="100%"/>

Il est possible d'ajouter autant de niveaux que souhaité.

#### Configuration

La table se configure dans "Affichage".

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/drilldown-config.png" width="820px"/>

Pour chaque niveau, on sélectionne les colonnes qui permettront de regrouper les données dans "Grouper par", et les colonnes qui seront agrégées dans "Colonnes visibles".

### Filter

Il est ensuite possible de filtrer les tables selon différents critères, que vous trouverez dans "Filtres".

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.28.0/analytics-filter.png" width="820px" />

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

- Les numéros de client sont désormais indiqués sur les factures et autres documents générés par l'application.
