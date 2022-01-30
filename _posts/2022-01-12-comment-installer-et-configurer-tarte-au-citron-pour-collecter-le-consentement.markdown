---
layout: post
title:  Comment configurer Tarte au Citron pour recueillir le consentement ?
authors: Slim TOUHAMI, Charly R.
date:   2022-01-12 15:01:35 +0300
image:  '/images/22.png'
tags:   [consentement CNIL]
---

Lorsqu'on souhaite connaître le trafic sur son site, que l'on ajoute des bannières publicitaires ou des vidéos, il arrive souvent que l'on fasse appel à des services tiers déposants des traceurs appelés cookies. Sauf exemption, l'éditeur du site a l'obligation de collecter le consentement du visiteur puisque l'utilisation de ces traceurs implique souvent la collecte de données personnelles.

Pour ce faire, il existe aujourd'hui sur le marché plusieurs solutions pour l'affichage d'une "bannière cookies" à la première connexion du visiteur. Certaines sont proposées moyennant finance par des éditeurs (ex : [Didomi](https://support.didomi.io/fr/analytics) ou [Axeptio](https://www.axeptio.eu/post/les-cookies-google-analytics-sont-ils-soumis-au-consentement)), et d'autres sont des solutions libres et gratuites. 

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

![](https://astraporta.com/assets/images/1.PNG)

Une fois la solution tarteaucitron installée, il convient, pour chaque service nécessitant le consentement, d’ajouter un morceau de code spécifique au service. Ce code est fourni par tarteaucitron. Un moteur de recherche est présent dans la [documentation d’installation de tarteaucitron](https://tarteaucitron.io/fr/install/) pour obtenir la procédure d’installation de chaque service.

![](https://astraporta.com/assets/images/2.PNG)

Pour l’installation de Google Analytics par exemple, la documentation de tarteaucitron fournit le code suivant à ajouter à votre site web en remplacement du code de Google Analytics :

![](https://astraporta.com/assets/images/3.PNG)

Certains services nécessitent une modification plus importante. Par exemple, pour le recueil du consentement pour l’utilisation de vidéos YouTube, la documentation de tarteaucitron explique qu’il est nécessaire pour chaque vidéo YouTube d’ajouter une balise spécifique :

![](https://astraporta.com/assets/images/4.PNG)