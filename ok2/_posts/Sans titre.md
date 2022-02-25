---
layout: post
title:  XXXX
authors: Slim TOUHAMI, Charly R.
date:   2022-01-12 15:01:35 +0300
image:  '/images/22.png'
tags:   [consentement CNIL]
---

Pour simplifier la configuration de la solution Tarte au Citron, il peut être envisagé d’utiliser un gestionnaire de tags afin de permettre la configuration de la solution tarteaucitron directement dans le gestionnaire de Tag pour ne pas avoir à solliciter les équipes chargées du développement des applications des agences de l’eau.

Cette approche comporte cependant les inconvénients suivants :
-	Dans son fonctionnement actuel, la solution tarteaucitron ne peut pas être installée directement via le gestionnaire de tags. Elle doit être installée en première position entre les balises `<head>` de l’application web.
-	Certains services gérés par tarteaucitron ne peuvent pas être configurés entièrement via la gestionnaire de tags, par exemple, pour ajouter des vidéos YouTube, il est nécessaire pour chaque vidéo d’ajouter une balise propre à tarte au citron. Cette balise ne peut pas être ajoutée via un gestionnaire de tags.
-	Le gestionnaire de tags ne doit pas déposer des cookies et nécessiter le consentement des visiteurs de l’application.

Malgré ces inconvénients, il peut être pertinent d’utiliser un gestionnaire de tags. Nous vous proposons un exemple d’installation et d’utilisation de tarteaucitron avec le gestionnaire de tag Google Tag Manager et les services Google Analytics et YouTube. L’utilisation d’un autre gestionnaire de tags ne devrait pas modifier de manière significative cette procédure d'installation.

Dans sa version actuelle et son utilisation par défaut, Google Tag Manager ne nécessite pas le consentement des utilisateurs, en effet, il ne dépose pas de cookies sur le navigateur des utilisateurs et ne récolte pas de données personnelles. Attention cependant, la modification de la configuration de Google Tag Manager et l’ajout de certaines balises peuvent rendre l’application non conforme. Dans notre exemple, nous utilisons uniquement les « balises HTML personnalisées » pour ajouter les éléments de configuration de tarteaucitron. Cette approche ne nécessite pas le consentement et est conforme au RGPD.

![capture 5](https://astraporta.com/assets/images/5.PNG)

Afin de fonctionner, l’application Tarte au citron doit être installée entre les balises `head` de l’application en première position (il n’est pas possible d’installer tarteaucitron depuis un gestionnaire de tags).

![capture 6](https://astraporta.com/assets/images/6.png)

À la suite de l’installation de tarteaucitron, il est nécessaire d’ajouter le code du gestionnaire de tags. Dans notre exemple, nous utilisons Google Tag Manager.

![capture 7](https://astraporta.com/assets/images/7.png)

Dans le gestionnaire de tags, il est possible maintenant de paramétrer tarteaucitron pour exiger le consentement des utilisateurs pour les différents services présents sur l’application. Par exemple, nous avons ajouté le code suivant dans Google Tag Manager pour le support de Google Analytics par tarteaucitron :

![capture 8](https://astraporta.com/assets/images/8.PNG)

Pour le support des vidéos YouTube, il est possible d’informer Tarte au citron de l’utilisation de ce service via Google Tag Manager. Nous avons ajouté la balise suivante dans le gestionnaire de tags :

![capture 9](https://astraporta.com/assets/images/9.PNG)

Il est également nécessaire d’ajouter dans le code source (donc en dehors de Google Tag Manager), la balise tarteaucitron qui permet de respecter le consentement pour une vidéo YouTube :

![capture 10](https://astraporta.com/assets/images/10.PNG)

Dans notre exemple, lors d’une première visite de notre application de démonstration, le service Google Analytics et la vidéo YouTube ne sont pas chargés. L’application tarteaucitron fonctionne normalement avec l’utilisation d’un gestionnaire de tags. Ceci est conforme au RGPD :

![capture 11](https://astraporta.com/assets/images/11.PNG)