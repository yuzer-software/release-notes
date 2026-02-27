# Novembre 2025 - Version 5.0

yuzSection Authentification

# Principes

Vous pouvez désormais configurer des moyens de connexion sécurisés pour vous et vos collaborateurs, et, si vous le souhaitez, forcer ceux-ci afin de garantir que les accès à vos données et celles de vos clients sont protégées comme il se doit.

## Modes de connextion

En plus de la connexion historique par mot de passe vous pouvez activer une sécurité robuste pour vous et vos collaborateurs en activant les facteurs d'authentification suivants:

- TOTP (Time based One Time Password): Permet l'enregistrement de YUZER dans l'application Authenticator de votre choix.
- WebAuthn: Permet une connexion fortement sécurisée à l'aide d'une clé de sécurité (Windows Hello, MacOS Passwords, Clé externe type Yubikey)

## Les stratégies de connexion

- Mot de passse uniquement: mode de connexion historique, ce mode de connexion a une sécurité faible. Trop d'utilisateurs enregistrent des mots de passes peu sécurisés, voir connus par différents membre d'équipes.
- WebAuthn: Permet une connexion basée sur une clé de sécurité stockée physiquement sur un matériel donné (ordinateur, clé externe, etc.).
- Mot de passe + TOTP: mode de connexion multifacteur permettant d'ajouter une application d'authentification générant un code d'authentification.
- Mot de passe + WebAuthn: mode de connexion multifacteur permettant d'ajouter une application clé de sécurité en plus du mot de passe.
- WebAuthn + TOTP: Le mode de connexion le plus sécurisé, imposant l'utilisation d'une clé de sécurité et d'une application d'authentification.

Seuls les modes activés peuvent-être utilisés par vos collaborateurs pour s'identifier, en fonction de ceux qu'ils ont configuré, et ce à l'exception des deux cas suivants:

- L'utilisateur n'a que sont mot de passe configuré. C'est le **mode dégradé** (voir ci-dessous).
- Vous n'avez configuré que la connexion par mot de passe mais un utilisateur a configuré un moyen de connexion plus sécurisé. C'est le **mode augmenté** (voir ci-dessous).

Note: Certaines politiques comme celles basées sur des clés d'accès peuvent nécessiter du temps et des moyens pour être implémentées. C'est pour cela que nous permettons des politiques différentes en fonction de vos entités/magasins.
Cependant nous recommandons qu'un administrateur de compte, soit responsable de cette configuration afin de valider que celle-ci soit uniforme sur l'ensemble des entités si cela est votre souhait.

### Mode dégradé

Un utilisateur qui n'a qu'un mot de passe alors qu'un mode plus avancé est obligatoire peut quand même se connecter à son compte mais uniquement si son mot de passe a été renouvellé dans les 15 minutes précédent la connexion. Cela est utile pour:

- Permettre à un nouvel utilisateur de se connecter.
- Permettre à un utilisateur n'ayant pas encore configuré de nouveau moyen d'authentification de se connecter.

Si le mot de passe n'a pas été renouvellé dans les 15 minutes précédentes la connexion échouera. Rendez-vous ci-dessous à la section _Comment Récupérer mon compte_ pour plus d'informations.

### Mode augmenté

Si une entité n'a configuré qu'une connexion par mot de passe mais qu'un utilisateur a défini un mode de connexion plus sécurisé alors celui-ci ne peut plus se connecter qu'avec son mot de passe uniquement. Son compte est devenu, de par son action, automatiquement plus sécurisé.

# Configuration

## Configurer les modes de connexion de l'entité:

|| Vous devez être administrateur ou administrateur du compte afin de configurer les modes de connexion. Nous recommandons qu'un administratuer de compte effectue ces configurations.

Rendez-vous dans **administration / utilisateurs**.

Le bouton _Authentification_ vous permet de visualiser la configuration actuelle de la sécurité de l'entité.

- Si le bouton est _jaune_ c'est que l'authentification par mot de passe est configurée et que vos utilisateurs peuvent éventuellement se connecter de manière non-sécurisée s'ils n'ont pas activé d'autres moyens sur leurs comptes.
- Si le bouton affiche le message _(Configuration héritée de)_ c'est que l'entité ne défini aucun moyen de configuration spécifique et que la configuration est alors récupérée depuis une entitée parente.

En cliquant sur le bouton vous pouvez visualiser et modifier les schémas d'authentifications autorisés pour l'entité:

- une coche verte indique que le moyen de connexion est activé
- une étoile indique qu'en cas de moyen multiples celui-ci sera proposé par défaut à l'utilisateur.

![auth_schemes](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.0/auth_schemes.webp?w=415px)

Sur ce même écran, vous pouvez visualiser pour chacun de vos utilisateurs un icone indiquant:

- ![user-secured](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.0/user-secured.webp?w=23px): L'utilisateur a configuré une authentification 2 facteur ou une clé de sécurité
- ![user-weak](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.0/user-weak.webp?w=22px): L'entité autorise la connexion par mot de passe et l'utilisateur n'a qu'un mot de passe configuré
- ![user-invalid](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.0/user-invalid.webp?w=22px)
  : L'utilisateur n'a pas défini les identifiants requis par l'entité pour se connecter de manière sécurisée.

## Configurer la connexion à mon compte

Clickez sur votre photo de profil puis _Informations du compte_ dans le menu déroulant.

![account_info_btn](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.0/account_info_btn.webp?w=231px)

Rendez vous alors dans l'onglet _Sécurtié et connexion_

![account_info_sec](https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/5.0/account_info_sec.webp?w=1098px)

Vous pouvez ici ajouter une sécurité par TOTP à l'aide de votre application d'authentification, ou configurer une clé de sécurité.

Si vous devez toujours conserver un mot de passe, vous pouvez également depuis cet écran révoquer votre application de sécurité ou vos clés de sécurité.

**Note**: La mise en place et la connexion par clé de sécurité se fait à travers une redirection vers une page web. Cette méthode nous permet d'accéder de manière sécurisée à votre trousseau d'accès à travers les fonctionalités de votre système d'exploitation.

## Comment Récupérer mon compte

||| Les agents support YUZER ne peuvent pas vous aider à la récupération de votre compte. Cela est en effet le seul moyen d'éviter une attaque par ingénérie sociale. En tant qu'administrateur vous devez faire preuve de la même vigilence lorsque vous reconfiguez un mot de passe. Cela ne doit-être effectué qu'en présence physique du collaborateur.

### Si vous avez défini des moyens de connexion sécurisés

Lorsque vous configurez des moyens de connexion nous vous recommandons de configurer des moyens de connexion alternatifs (par exemple plusieurs clés de sécurité, ou une authentification par mot de passe et TOTP ainsi que mot de passe et clé de sécurité).

Cela vous permet de récupérer votre compte à travers un autre moyen d'authentification.

Si malgré ces précautions vous perdez l'accès à votre compte, vous pouvez demander à votre administrateur de révoquer tous vos moyens de connexions (TOTP et clé de sécurité).

### Enregistrer un nouveau mot de passe

- Depuis la page de connexion, utilisez _Mot de passe oublié ?_ (celle-ci nécessite que vous ayez un email personnel configuré sur votre compte).
- Soit lui demander de mettre à jour votre mot de passe si vous n'avez pas d'email personel associé à votre compte.

Si votre entité ne permet pas la connexion par mot de passe, vous devez vous connecter dans les **15 minutes** suite à la configuration du nouveau mot de passe pour vous connecter et re-configurer vos moyens de connexion sécurisés.

## Comment mettre en place une authentification par clé de sécurité

Les clés de sécurité proposent un mode de sécurité basé sur l'accès physique à un objet et son, en ce sens un des moyens de sécurité les plus avancés, similaires au clés de votre maison.

Il en existe deux types:

- Biométriques: En plus d'un accès physique, une validation biométrique protège la clé. C'est les plus sécurisés puisque leur accès (perte, vol, accès temporaire discret) ne suffit pas à l'attaquant de l'utiliser. C'est le cas des clés de sécurité du trousseau de sécurité macOs ou de Windows Hello par exemple.
- Physiques: Elles fonctionnent comme les clés de votre maison. Elles sont particulièrement sécurisées (et ne peuvent pas être copiées) mais leur perte ou vol permet à l'attaquant de l'utiliser, un tel scenario doit conduire à la révocation immédiate de la clé par vous même ou l'un de vos administrateurs si vous ne pouvez pas récupérer votre clé.

yuzSection Comptabilité

Nous avons revu et amélioré notre service de comptabilité.

##

## Analytiques

Nous avons amélioré la redescente du _type de panier_ dans le cas des cessions, qui étaient auparavant toujours catégorisés en "Vente de pièces" ou "Ordre de réparation". Le type de cession n'a pas changé.

yuzSection Général

## Améliorations

## Corrections
