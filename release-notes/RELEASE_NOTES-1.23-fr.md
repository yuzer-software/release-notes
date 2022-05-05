# Mai 2022 - Version 1.23.4

## C’est corrigé

- Nous avons corrigé une erreur d'arrondi qui pouvait intervenir sur les prix de reprises de véhicules.
- Lors d'un export commande au format Harley Davidson la boite de dialogue se ferme désormais correctement.

# Mai 2022 - Version 1.23.3

## Export des dossiers

- Renommage de 'Commercial du produit phare' en 'Ajouté par' et de 'Éditeur' en 'Facturé par'.
- Correction du champ 'Ajouté par'.

## Nouvelles catégories

Ajout des catégories "location" dans services et taxes:

- Services et taxes
  - Location
    - Location courte durée
    - Location longue durée

# Mai 2022 - Version 1.23.1

## Support BIHR

Les tarifs BIHR n'étaient pas correct pour votre concession. Il est en effet nécessaire pour cela d'obtenir de la part de BIHR des codes spécifiques qui vous permettent de récupérer vos tarifs.
Vous pouvez les demander à BIHR à l'aide d'un email à _customercare.france@mybihr.com_ ou en vous rapprochant de votre commercial BIHR.

Une fois ces codes récupérés vous pourrez les enregistrer dans l'interface Yuzer dans _Administration/Fournisseurs_ en éditant le fournisseur BIHR. Vos tarifs spécifiques seront alors récupérés chaque nuit (il faut attendre une journée afin que la mise à jour soit appliquée).

Vos prix de vente restent définis même si vous ne faites pas cette opération mais la marge catalogue sera assignée à 0 tant que vos tarifs d'achat spécifiques n'auront pas été récupérés. Ceci nous a semblé être un meilleur choix que de vous afficher une donnée erronée.

Notez que vos marges sur PAMP restent bien entendu non-impactées par les changements ci-dessus.

## Produits identifiés

Il est désormais possible de:

- modifier le produit catalogue lié à un produit identifié (vélo, moto-marine)
- mettre à jour les informations principales (modèle, libellé etc.) de celui-ci
- supprimer un identifiant d'un produit identifié

Les informations se retrouvent correctement synchronisées avec le panier de vente.

## Consommation SMS

Votre consommation SMS est désormais visible dans la section _Administration/Téléphonie/SMS_.

## Améliorations diverses

- Vous pouvez désormais copier/coller à la souris en utilisant le menu contextuel "bouton droit".
- Le libellé du tiers est exporté sur chaque ligne dans un export comptable (le numéro de compte ne l'est que sur la ligne du tiers).
- Vous pouvez exporter vos commandes dans un format spécifique Harley Davidson.
- Les configurations des différents widgets sont désormais accessibles depuis une modal sur le modèle de la configuration du widget de Main d'oeuvre.
- Vous pouvez désormais visualiser les pdf depuis les galeries de documents.
- L'affichage de la vue stock a été amélioré et rendu plus réactif.

## C’est corrigé

- Lorsque vous accédez en changeant d'entité à un dossier qui n'existe plus vous pouvez désormais correctement revenir à la liste des dossiers.
- Lors de la création d'un transfert il était possible dans certaines conditions de ne pas correctement changer l'entrepôt cible empêchant par la suite la réception de celui-ci. Ceci a été corrigé.
