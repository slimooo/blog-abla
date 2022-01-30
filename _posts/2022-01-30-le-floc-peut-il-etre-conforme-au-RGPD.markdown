---
layout: post
title:  Le FloC est-il conforme au RGPD ?
authors: ["Caroline"]
description: Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative a...
date:   2022-01-28 15:01:35 +0300
image:  '/images/15.jpg'
tags:   [cookies, RGPD, CNIL]
---
Google prévoit d’utiliser sur son navigateur Chrome la technologie FloC, ou Federated Learning of Cohorts. Il s’agit d’une technologie open source permettant de suivre la navigation de l’utilisateur sur internet pour lui proposer de la publicité ciblée. Son utilisation soulève toutefois de nombreuses critiques car elle n’est pas respectueuse de la vie privée de la personne. 

## A quoi sert le FloC ?
Les sites internet ont souvent recours au dépôt de micro-logiciels, appelés cookies tiers. Les cookies tiers s’avèrent pourtant être peu respectueux de la vie privée de l’utilisateur. Non seulement ils sont utilisés pour tracer son activité sur internet et lui proposer de la publicité ciblée, mais ils sont aussi souvent déposés sans son accord. 

Le RGPD et les lignes directrices de la CNIL ont par conséquent limité l’utilisation de ce type de cookies. La réglementation prévoit désormais l’obligation de recueillir le consentement de l’utilisateur avant leur dépôt, et la possibilité pour lui de les refuser. Cette évolution réglementaire est problématique pour Google puisque son modèle économique repose en grande partie sur la publicité personnalisée.

De plus, la firme de mountain view doit s’adapter aux nouvelles préoccupations des consommateurs qui exigent une protection effective de leur vie privée. Le groupe doit également s’adapter à la concurrence, notamment celle d’Apple et de son navigateur Safari qui bloque les cookies tiers par défaut.
Le FloC développé par Google est une solution permettant justement de se passer de ces cookies. Il marque la fin du pistage individuel, mais pas du ciblage publicitaire.

## Comment fonctionne le FloC ?
Chaque utilisateur va générer des données pendant sa navigation. Le navigateur va recueillir ces données (ex: sujet de la page consultée, le nombre de fois qu’elle a été consultée, ou encore la durée de la navigation) et utiliser le FloC afin de classer l’utilisateur dans un groupe, ou cohorte, selon ses habitudes de navigation. 

Chaque cohorte va ainsi regrouper des utilisateurs avec des comportements de navigation similaires. Ces groupes pourront par exemple rassembler des personnes avec les mêmes goûts musicaux, la même orientation sexuelle, ou le même âge. Le navigateur attribuera alors à l’utilisateur un “identifiant de cohorte”, c’est-à-dire un identifiant propre à son groupe et partagé avec d’autres utilisateurs. Les annonceurs pourront ensuite se baser sur cet identifiant pour proposer de la publicité.

## Pourquoi le FloC n’est-il pas respectueux de la vie privée ?
Si en théorie cette technologie vise à protéger l’utilisateur contre le profilage individualisé, elle n’est en pratique pas totalement respectueuse de sa vie privée.

Le premier problème n’est pas directement propre au FloC mais dans la manière dont Google a opéré ses tests. Il a été testé sur 0.5% des utilisateurs de Chrome sans les informer préalablement. Les données sont regroupées et anonymisées donc il n’y a pas d’obligation d’informer et de recueillir le consentement de l’utilisateur. Ce dernier a tout de même la possibilité de savoir s’il fait partie des personnes testées en allant sur le site créé par l'Electronic Frontier Foundation (EFF). La France n’est pour le moment pas concernée par ces tests.  

Le deuxième problème soulevé par le FloC est son rapport avec la pratique du fingerprinting. Il est normalement impossible avec le FloC de distinguer l’utilisateur car cette technologie le place dans un groupe composé de plusieurs autres milliers d’utilisateurs. Mais que se passe-t-il lorsque le FloC est combiné avec le fingerprinting ? Avec cette technique le navigateur va collecter plusieurs informations, comme le type de navigateur utilisé sur l’appareil, son adresse IP, sa version, ou encore son système d’exploitation. Cela sert ensuite à créer une empreinte (fingerprint), qui sera différente pour chaque utilisateur.  Les trackers pourront donc combiner l'identité de cohorte de la personne avec les informations récupérées grâce au fingerprinting. Il sera alors tout à fait possible d’obtenir l’empreinte unique de l’utilisateur. Ce dernier pourra donc être parfaitement identifiable et différencié des autres utilisateurs. L’association du FloC et du fingerprinting constitue ainsi un risque pour la vie privée de la personne.

Enfin, le FloC met à disposition des sites internet un résumé complet de l’activité de l’utilisateur. Concrètement, cela signifie qu’un site va obtenir l’identifiant de l’utilisateur qui indique que ce dernier est intéressé par son produit. Mais cela signifie aussi, et surtout, que le site sera également au courant que l’utilisateur appartient au groupe de personnes intéressées par d’autres types de produits ou de services, disponibles sur d’autres sites. Connaître l’activité complète de l’utilisateur sur internet n’est pourtant pas essentiel pour proposer de la publicité ciblée.

## Est-il possible de bloquer le FloC ?
Il est possible de désactiver l’utilisation du FloC sur Chrome en allant dans le menu Paramètres, en cliquant sur Confidentialité et sécurité, puis cookies et autres données du site, et enfin bloquer les cookies tiers. 

L’utilisateur peut aussi installer des extensions sur le navigateur de Google. Parmi ces extensions on retrouve par exemple AdBlock, Ghostery, Disconnect, ou encore Privacy Badger. 

L’extension du moteur de recherche DuckDuckGo bloque également automatiquement le FloC. 

Une autre solution est de ne plus utiliser Google Chrome et de privilégier des navigateurs plus respectueux de la vie privée. Apple Safari, Microsoft Edge, Firefox et Opera ont indiqué ne pas vouloir utiliser le FloC pour le moment. C’est également le cas des navigateurs Brave, Vivaldi, et Tor.