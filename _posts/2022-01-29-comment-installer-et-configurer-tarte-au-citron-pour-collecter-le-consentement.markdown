---
layout: post
title:  Comment installer et configurer Tarte au Citron pour recueillir le consentement ?
authors: ["Charly"]
description: Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative a...
date:   2022-01-28 15:01:35 +0300
image:  '/images/15.jpg'
tags:   [cookies, RGPD, CNIL]
---

Pour recueillir et gérer le consentement des visiteurs des applications des agences de l’eau, nous recommandons l’utilisation de la solution [tarteaucitron](https://tarteaucitron.io/fr/).

Cette solution possède de nombreux avantages, elle est open source, gratuite, utilisée par de nombreuses applications et facile à configurer dans une installation « standard ».

En comparaison avec une solution payante de gestion du consentement, les inconvénients sont que tarteaucitron ne gère pas la preuve du consentement. C’est pour cela que nous proposons une sauvegarde du code de l’application sur l'Internet Archive pour pallier ce manquement.

En complément, la version gratuite de tarteaucitron ne supporte pas les langues étrangères et les mises à jour ne sont pas automatiques. Pour pallier ce problème, une version payante à 15 euros par mois pour l’ensemble des sites des agences de l’eau est proposée par l’éditeur de la solution.

La procédure d’installation de tarteaucitron est décrite à l’adresse [https://tarteaucitron.io/fr/install/](https://tarteaucitron.io/fr/install/).

Cette installation nécessite l’ajout du code suivant au début du bandeau `<head>` de l’ensemble des pages des sites des agences de l’eau :

![capture 1](https://astraporta.com/assets/images/1.PNG)

Une fois la solution tarteaucitron installée, il convient, pour chaque service nécessitant le consentement, d’ajouter un morceau de code spécifique au service. Ce code est fourni par tarteaucitron. Un moteur de recherche est présent dans la documentation d’installation de tarteaucitron (étape 3 : [https://tarteaucitron.io/fr/install/](https://tarteaucitron.io/fr/install/)) pour obtenir la procédure d’installation de chaque service.

![capture 2](https://astraporta.com/assets/images/2.PNG)

Pour l’installation de Google Analytics par exemple, la documentation de tarteaucitron fournit le code suivant à ajouter à votre site web en remplacement du code de Google Analytics :

![capture 3](https://astraporta.com/assets/images/3.PNG)

Certains services nécessitent une modification plus importante des applications des agences de l’eau. Par exemple, pour le recueil du consentement pour l’utilisation de vidéos YouTube, la documentation de tarteaucitron explique qu’il est nécessaire pour chaque vidéo YouTube d’ajouter une balise spécifique :

![capture 4](https://astraporta.com/assets/images/4.PNG)