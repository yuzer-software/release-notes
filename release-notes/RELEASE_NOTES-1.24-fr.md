# Mai 2022 - Version 1.24.2

Nous avons corrigé les exportations CSV et XLSX.

# Mai 2022 - Version 1.24.1

Nous avons corrigé l'ajout d'une carte cadeau à un panier ! (Bug introduit lors du déplacement de la catégorie "Carte cadeau".)

# Mai 2022 - Version 1.24.0

## Catégories

De nouvelles catégories ont été créées, quelques catégories ont été déplacées.

Catégories renommées :

- Lunettes de protections : Masques
- Accessoires lunettes de protections : Accessoires lunettes et masques
- Services et taxes : Services, taxes & primes

Nouvelles catégories :

- Dans *Pièces > Cadre* : Cadre, Boucle AR, Bras Oscillant, Cale Pied, Repose Pied, Carénage, Béquille
- Dans *Pièces > Moteur* : Moteur, Culasse, Carter, Joints, Durites, Boite
- Dans *Pièces > Électrique* : Bougies, Faisceau, Batterie, Feu, AV AR Compteur
- Dans *Pièces > Filtres* : Filtre à Huile, Filtre à Air, Filtre à Carburant
- Dans *Accessoires > Poste de pilotage > Cintre / guidon* : Guidon moto
- Dans *Accessoires > Bagagerie* : Valises, Top Cases
- Dans *Vêtements et équipement* : Hauts, Bas, Protections
- Dans *Vêtements et équipement > Autres* : Bijoux
- Dans *Vêtements et équipement > Autres > Lunettes* : Lunettes de style
- Dans *Partie cycle > Pneus* : Pneus Vélo, Pneus Quad / ORV, Pneus Auto, Pneus Remorque, Pneus Camion, Pneus Engins, Petits Pneus
- Dans *Partie cycle > Pneus > Pneus Moto* : Pneus Route, Pneus Cross, Pneus Scooter
- Dans *Partie cycle > Pneus > Petits Pneus* : Trottinettes, Tondeuses
- À la racine : Jouet
- Dans _Jouet_: Autres jouets
- Dans Services, taxes & primes : Taxes, Frais, Refacturation, Commissions, Recyclage, Carburant, Primes
- Dans Services, taxes & primes > Taxes : Malus

Catégories supprimées :

- Vêtements et équipement > Tops (_déplacé dans_ Vêtements et équipement > Hauts > T-shirts / Tops / Maillots)
- Vêtements et équipement > Autres > Bonnets (_déplacé dans_ Vêtements et équipement > Autres > Casquettes / Bonnets / Cache cou)
- Vêtements et équipement > Autres > Accessoires casque (_déplacé dans_ Casques > Accessoires casque)

Catégories déplacées :

- De _Vêtements et équipement_ dans *Vêtements et équipement > Hauts* : Vestes, T-shirts > Tops > Maillots, Chemise, Ponchos, Polos, Sweats
- De _Vêtements et équipement_ dans *Vêtements et équipement > Bas* : Pantalons, Short, Sous-vêtements
- De _Vêtements et équipement_ dans *Vêtements et équipement > Protections* : Jambières & Manchettes, Genouillères & Coudières
- _Vêtements et équipement > Autres > Protections_ → _Vêtements et équipement > Protections_
- De _Vêtements et équipement > Autres_ dans *Vêtements et équipement > Autres > Lunettes* : Masques, Accessoires lunettes et masques
- _Vélo enfant_ → _Jouet > Vélo enfant_
- De _Services, taxes & primes_ dans *Services, taxes & primes > Taxes* : Carte grise, Autres taxes
- De _Services, taxes & primes_ dans *Services, taxes & primes > Frais* : Frais postaux, Frais de port, Frais de gestion administrative, Frais publicitaires, Frais de mise en route
- De _Services, taxes & primes_ dans *Services, taxes & primes > Refacturation* : Refacturation de loyer, Refacturation location gérance,
  Refacturation de RFA, Refacturation de Personnel, Frais d'opération commerciale externe (chèques etc.)
- De _Services, taxes & primes_ dans *Services, taxes & primes > Commissions* : Comissions exonérées, Comissions soumises à TVA
- _Services, taxes & primes > Carte cadeau_ → _Produit non stockable > Carte cadeau_

Ceci vient compléter les mises à jour 1.22.7 et 1.23.3 qui ajoutaient les catégories

- Services et taxes > Location > Location courte durée
- Services et taxes > Location > Location longue durée
- Produit non stockable > Petites fournitures
- Produit non stockable > Bon d’achat

Nous avons fait aussi une passe pour vérifier la correction de toutes les catégories en base. Vous risquez donc de mieux trouver certains produits !

## Stock

### Réceptions

Les réceptions sont désormais affichées par mois, ce qui simplifie à la fois la recherche et la navigation.

### Factures d'achat

Amélioration de la recherche et de la navigation lors d'ajout de produits réceptionnés:
- possibilité de filtrer les réceptions par produit réceptionné (image ci-dessous).
- la fenêtre d'ajout ne se ferme pas après avoir ajouté une ligne (ce qui permet d'ajouter des lignes de plusieurs réceptions).
- ajout d'un bouton pour revenir du détail d'une réception à la liste des réceptions.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.24.0/purchase-invoice-filtering.png" width="650px"/>

## Export de données en XLSX

La plupart des écrans proposant d'exporter des données au format CSV supportent désormais l'export XLSX.

## Widgets

La configuration du widget de chiffre d'affaires a été rendue plus claire, notamment sur les interactions des différentes options: des messages vous expliquent pourquoi certaines options entre en contradiction, etc.

## C'est corrigé

- Un panier **vide** n'était pas correctement remis à jour lors d'un changement de contact d'un groupe de facturation.
- La synchronisation de prix d'achat entre dossier véhicule et panier pouvait afficher une erreur.
- Nous ne permettons plus de créer un OR depuis un dossier véhicule qui n'a pas de VIN (dossier commandé ou en attente de réception).
