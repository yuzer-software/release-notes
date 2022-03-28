# Avril 2022 - Version 1.21.0

# Tableau de bord

Les filtres personnalisés qui seraient incompatibles avec le widget de chiffre d'affaires sont clairement exhibés.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/custom-filter-in-turnover-widget.png" width="500"/>

# Modèle de panier: import Honda

Honda fournit des modèles de panier au format CSV qu'il est désormais possible d'importer dans Yuzer.

- Vous devez au préalable avoir Honda comme fournisseur.
- Depuis la page des modèles, cliquez sur "Importer Honda".

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/new-honda-import.png" width="300"/>

- Suivez les instructions: téléchargez les fichiers fournis par Honda, puis remplissez les champs comme indiqué.

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/honda-import.png" width="800"/>

- Cliquez sur "Charger": tous les modèles importés seront créés.

<div *dmsHasAnyAuth="['ROLE_ACCOUNTANT']">

# Réceptions

Les lignes des réceptions sont réceptions sont triées par date d'ajout mais toutefois groupées par identifiant de produit, ce qui est généralement désirable. En conséquence, il est possible que des lignes soient réordonnées sur des opérations d'ajout ou de suppression de lignes, ce qui était parfois déconcertant pour l'utilisateur qui pouvait croire que davantage de produit avait été ajouté que ce qu'il n'avait demandé ou, lors d'une suppression, que plusieurs lignes avaient été supprimées. Par exemple, si un produit 890479 a été ajouté à la réception, puis une dizaine d'autres lignes, puis à nouveau du 890479 et que cela crée une nouvelle ligne, alors toutes les lignes de 890479 seront groupées ensemble en tête de liste. Si cette dernière ligne venait à être supprimée, les autres lignes retrouveraient leurs place en fin de liste, donnant l'impression qu'elles ont été supprimées.

Nous avons donc ajouté un message indiquant lorsque des lignes sont réordonnées avec la possibilité de filtrer les lignes impactées (comme illustré ci-dessous).

<img class="ml-5" src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/warn-reception.png" width="900"/>

# Comptabilité

## TVA déductible à l'achat par taux de TVA

Il est maintenant possible de configurer les comptes de TVA déductible à l'achat par taux de TVA.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.21.0/vat-config.png" width="500"/>

</div>
