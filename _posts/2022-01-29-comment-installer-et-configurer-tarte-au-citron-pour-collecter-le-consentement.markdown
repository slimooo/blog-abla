---
layout: post
title:  Comment configurer Tarte au Citron pour recueillir le consentement ?
authors: Slim TOUHAMI, Charly R.
date:   2022-01-28 15:01:35 +0300
image:  '/images/15.jpg'
tags:   [cookies, RGPD, CNIL]
---

Lorsqu'on souhaite connaître le trafic sur son site, que l'on ajoute des bannières publicitaires ou des vidéos, il arrive souvent que l'on fasse appel à des services tiers déposants des traceurs appelés cookies. Sauf exemption, l'éditeur du site a l'obligation de collecter le consentement du visiteur puisque l'utilisation de ces traceurs implique souvent la collecte de données personnelles.

Pour ce faire, il existe aujourd'hui sur le marché plusieurs solutions pour l'affichage d'une "bannière cookies" à la première connexion du visiteur. Certaines sont proposées moyennant finance par des éditeurs (ex : Didomi ou Axeptio), et d'autres sont des solutions libres et gratuites. 

Tarte au Citron fait partie des solutions libres les plus utilisées. Bien que très facile à configurer, elle présente toutefois quelques lacunes :
- pas de gestion en natif de la preuve de consentement;
- pas de support des langues étrangères;
- pas de possibilité de faire du A/B testing facilement;
- pas de mise à jour automatique.

Il existe aussi une version payante (15€ par mois) qui permet de  résoudre une partie de ces problématiques.

Malgré un design pas au top de la modernité, Tarte au Citron est une solution que nous recommandons pour les sites avec un trafic peu élevé, les sites des administrations ou les petits budgets.

## La configuration de tarte au citron en quelques étapes

La procédure d’installation de tarteaucitron est plutôt bien [documentée](https://tarteaucitron.io/fr/install/).

Cette installation nécessite l’ajout du code suivant au début du bandeau `<head>` de l’ensemble des pages des sites des agences de l’eau :

`<script type="text/javascript" src="/tarteaucitron/tarteaucitron.js"></script>`
`<script type="text/javascript">`
`tarteaucitron.init({`
`"privacyUrl": "", /* Privacy policy url */`
`"hashtag": "#tarteaucitron", /* Open the panel with this hashtag */`
`"cookieName": "tarteaucitron", /* Cookie name */`    
`"orientation": "middle", /* Banner position (top - bottom) */`       
`"groupServices": false, /* Group services by category */`                           
`"showAlertSmall": false, /* Show the small banner on bottom right */`
`"cookieslist": false, /* Show the cookie list */`                           
`"closePopup": false, /* Show a close X on the banner */`
`"showIcon": true, /* Show cookie icon to manage cookies */`
`//"iconSrc": "", /* Optionnal: URL or base64 encoded image */`
`"iconPosition": "BottomRight", /* BottomRight, BottomLeft, TopRight and TopLeft */`
`"adblocker": false, /* Show a Warning if an adblocker is detected */`                           
`"DenyAllCta" : true, /* Show the deny all button */`
`"AcceptAllCta" : true, /* Show the accept all button when highPrivacy on */`
`"highPrivacy": true, /* HIGHLY RECOMMANDED Disable auto consent */`                           
`"handleBrowserDNTRequest": false, /* If Do Not Track == 1, disallow all */`
`"removeCredit": false, /* Remove credit link */`
`"moreInfoLink": true, /* Show more info link */`
`"useExternalCss": false, /* If false, the tarteaucitron.css file will be loaded */`
`"useExternalJs": false, /* If false, the tarteaucitron.js file will be loaded */`
`//"cookieDomain": ".my-multisite-domaine.fr", /* Shared cookie for multisite */`  
`"readmoreLink": "", /* Change the default readmore link */`
`"mandatory": true, /* Show a message about mandatory cookies */`
`});`
`</script>`

Une fois la solution tarteaucitron installée, il convient, pour chaque service nécessitant le consentement, d’ajouter un morceau de code spécifique au service. Ce code est fourni par tarteaucitron. Un moteur de recherche est présent dans la [documentation d’installation de tarteaucitron](https://tarteaucitron.io/fr/install/) pour obtenir la procédure d’installation de chaque service.

![Etape 3 Tarte au Citron](https://astraporta.com/assets/images/2.PNG)

Pour l’installation de Google Analytics par exemple, la documentation de tarteaucitron fournit le code suivant à ajouter à votre site web en remplacement du code de Google Analytics :

`<script type="text/javascript">`
`tarteaucitron.user.gajsUa = 'UA-XXXXXXXX-X';`
`tarteaucitron.user.gajsMore = function () { /* add here your optionnal _ga.push() */ };`
`(tarteaucitron.job = tarteaucitron.job || []).push('gajs');`
`</script>`

Certains services nécessitent une modification plus importante. Par exemple, pour le recueil du consentement pour l’utilisation de vidéos YouTube, la documentation de tarteaucitron explique qu’il est nécessaire pour chaque vidéo YouTube d’ajouter une balise spécifique :

`<div class="youtube_player" videoID="video_id" width="width" height="height" theme="theme (dark | light)" rel="rel (1 | 0)" controls="controls (1 | 0)" showinfo="showinfo (1 | 0)" autoplay="autoplay (0 | 1)" mute="mute (0 | 1)" srcdoc="srcdoc" loop="loop (0 | 1)" loading="loading (0 | 1)"></div>`