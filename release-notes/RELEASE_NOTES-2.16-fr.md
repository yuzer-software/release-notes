# September 2023 - Version 2.16.0

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


## Corrections
