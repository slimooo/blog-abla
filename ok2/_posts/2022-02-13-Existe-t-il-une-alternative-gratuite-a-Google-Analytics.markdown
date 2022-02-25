---
layout: post
title:  Existe-t-il une alternative gratuite à Google Analytics ?
authors: Slim TOUHAMI
date:   2022-02-13 16:09:00 +0300
image:  '/images/15.jpg'
tags:   [analytics, RGPD]
---

La [CNIL a sanctionnée en février 2022](https://www.cnil.fr/fr/utilisation-de-google-analytics-et-transferts-de-donnees-vers-les-etats-unis-la-cnil-met-en-demeure) un site internet français pour son utilisation de Google Analytics. L'outil serait non conforme au RGPD car transférant des données personnelles vers les États-Unis sans protection suffisante.

Nombreuses sont donc les personnes à la recherche d'une alternative gratuite à Google Analytics.

En avant-propos, nous souhaitions souligner que Google Analytics n'est pas totalement gratuit. S'il est effectivement mis à disposition gratuitement des éditeurs de sites internet, en contrepartie Google exploite les données à des fins de profilage des visiteurs. In fine, le coût réel de son utilisation est à retrouver sur les tarifs de sa plateforme publicitaire Google Ads.

## Matomo la solution open source gratuite ?

Depuis plus d'une quinzaine d'années, Matomo (anciennement Piwik) se positionne comme une solution alternative et libre de Google Analytics. L'outil est puissant, riche en fonctionnalités, et est plutôt bien adapté pour une utilisation avancée.

L'application peut se [télécharger gratuitement et s'installer sur son propre serveur](https://fr.matomo.org/docs/installation/).

Toutefois, le tarif d'une application ne se résume pas seulement à son accès. Il est aussi nécessaire de prendre en compte :
- L'hébergement de l'application, et Matomo est plutôt [une solution gourmande en ressources](https://fr.matomo.org/docs/requirements/)
- Le temps nécessaire pour les développeurs pour l'installation et la configuration de l'application (notamment la prise en compte du [guide de configuration de la CNIL](https://www.cnil.fr/sites/default/files/atoms/files/matomo_analytics_-_exemption_-_guide_de_configuration.pdf))
- Le temps à consacrer pour les mises à jour et les vérifications de sécurité informatique

Matomo est une solution gratuite si vous avez déjà des serveurs performants et du temps à y consacrer.

L'application de mesure d'audience est aussi proposée en version cloud, mais aucune version gratuite n'est disponible. Et en termes de tarifs, ce n'est pas donné. À titre d'exemple pour 2 millions de pages vues mensuelles Matomo Cloud est proposé à 309 euros, contre seulement 44 euros chez Abla Analytics.

## Les logs du serveur sont-ils suffisants pour des analyses d'audience ?

Les logs permettent d'avoir un aperçu sur l'activité réalisée sur un site internet. Il est possible d'installer des solutions comme [AWStats](https://github.com/eldy/awstats) pour avoir une visualisation des données. Certains hébergeurs proposent même cette fonctionnalité par défaut.

Toutefois, ces solutions ne permettent pas d'obtenir des données aussi précises que celle d'un outil de mesure d'audience :
- les visites générées par les robots ne sont pas exclues des résultats
- les sources de trafic ne sont agglomérées (ex: fb.com et facebool.com seront considérés comme deux sources distinctes)
- les visites uniques ne sont pas calculées aussi précisément

Nous vous invitons à comparer les résultats obtenus entre une solution d'analyse d'audience et une solution d'analyse de logs.

Avec ces outils vous pouvez également oublier l'expérience utilisateur adaptée, le travail collaboratif ou encore la mise à disposition d'une API.

## Abla Analytics propose-t-elle une version gratuite ?

Abla Analytics propose une solution totalement gratuite et à vie pour les sites générant moins de 5000 pages vues par mois.

Pour les autres sites, nous proposons une période d'essai de 30 jours sans engagement. Nos tarifs sont des plus compétitifs et débutent à partir de 6€ par mois. Si vous trouvez moins chers ailleurs n'existez pas à nous envoyer un mail!

En résumé, une solution gratuite, aussi avancée que Google Analytics et conforme au RGPD, est un mouton à 5 pattes. 