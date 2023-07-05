# Juillet 2023 - Version 2.14.0

## Écritures comptables des caisses

Nous avons ajouté la possibilité d'agréger les écritures de caisse par moyen de paiement.

Pour ce faire, allez dans le menu `Comptabilité > Configurer` pour activer l'option:

<div class="text-center" style="text-align: 'center';">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/2.14.0/aggregate-cashdesk-by-payment-mean.webp"/>
</div>

<div class="alert alert-warning">
A noter que Yuzer effectue quelque validation en fonction de la configuration d'aggrégation avant d'écrire dans le journal.
En conséquence, si vous changez la configuration alors que vous avez des écritures en attentes, ces dernières ne passeront plus la validation.

Dans ce cas, vous avez 2 solutions:

- Soit vous validez les écritures avant de mettre à jour la configuration d'agrégation.
- Soit vous rejetez les écritures en attentes pour les repasser en comptabilité avec la nouvelle configuration agrégation.
</div>
