---
layout: post
title:  Comment rendre Google Analytics conforme au RGPD ?
authors: ["Caroline"]
description: Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative a...
date:   2021-03-26 12:30:00 +0300
image:  '/images/15.jpg'
tags:   [cookies, RGPD, CNIL]
---

Google Analytics est la solution de mesure d’audience la plus utilisée sur le marché. La mise en place de cet outil conduit à la collecte de données personnelles dont l’adresse IP et l’identifiant du navigateur (ou user-agent). Son utilisation nécessite par conséquent de respecter la réglementation sur la protection des données personnelles (RGPD et ePrivacy). Or, par défaut, la solution du géant de Mountain View n’est pas conforme au RGPD.

## Est-il possible d’anonymiser les données sur Google Analytics pour rendre la solution conforme au RGPD ?

L’éditeur du site peut faire le choix d’anonymiser les données afin de ne pas tomber sous le régime de la réglementation sur les données personnelles.

Par défaut, Google Analytics n’anonymise pas les données collectées. L’éditeur devra donc configurer l’outil dans le but de rendre les données de l’utilisateur anonymes, et ce avant même de les transmettre à Google. Se limiter à envoyer les données personnelles à Google pour ensuite les rendre anonymes n’est pas suffisant pour respecter les exigences européennes de protection des données personnelles.

Dans les faits, un développement sera nécessaire pour bloquer le transfert de données depuis navigateur du visiteur vers Google, et installer une librairie qui sera chargée d’anonymiser les données avant communication à Analytics. Cette procédure est complexe à mettre en œuvre et nécessite des compétences techniques.

Si l’anonymisation est impossible, ou si l’éditeur du site n’a pas les moyens d’y procéder, l’outil de mesure d’audience sera soumis au respect de la réglementation sur les données personnelles. L’éditeur devra alors informer le visiteur sur le mécanisme de suivi et recueillir valablement son consentement.

## Quelles sont les informations à communiquer à l’utilisateur ?

L’éditeur devra alors mettre en place un bandeau cookies visible qui s’affiche sur la page d'accueil du site. Cette fenêtre cookie devra ainsi renseigner l’utilisateur, de façon claire et compréhensible, sur plusieurs éléments.

Parmi ces éléments, on compte tout d’abord l’identité du ou des responsable(s) de traitements, les catégories de données collectées, la finalité de cette collecte (à savoir ici le profilage et la publicité), ainsi que des possibilités qui lui sont offertes pour consentir ou non au traitement des données.

Enfin, l’utilisateur doit pouvoir accéder à un lien hypertexte renvoyant vers la politique de confidentialité. Ce texte détaillera alors les informations précitées, le cas échéant les coordonnées du délégué à la protection des données, ainsi que l’existence d’éventuels transferts de cookies hors de l’Union européenne (les données de Google Analytics sont transférées aux Etats-Unis). Aussi, il est nécessaire que cette politique de confidentialité rappelle les droits des utilisateurs et leur possibilité d’introduire une plainte auprès de la CNIL.

## Comment recueillir le consentement de l’utilisateur ?

L’éditeur sera aussi tenu de mettre en place un système permettant le recueillement du consentement de l’utilisateur. Plus spécifiquement, il devra ajouter dans le bandeau cookie trois boutons permettant à l’utilisateur de faire un choix. Il pourra être en mesure d’accepter tous les cookies, de les refuser, ou de n’accepter que certaines catégories de cookies.

L’acceptation implicite via une poursuite de navigation ou une case précochée, ne peut être considérée comme valide. Le clic de l’utilisateur sur le bouton “Oui j’accepte” est le seul moyen valable de recueillir le consentement.

Les conséquences pour l’utilisateur en cas de refus des cookies doivent être portées également à sa connaissance, tout comme la possibilité de retirer son consentement, et ce à n’importe quel moment, de façon aussi simple que lorsqu’il l’avait donné.

## Est-il nécessaire de configurer dans Google Analytics la durée de conservation des cookies ?

Google Analytics conserve par défaut les données collectées deux ans à compter de la dernière visite. Cette durée semble être excessive par rapport à la finalité du traitement. Pour être plus respectueux de la vie privée de l'utilisateur, il est donc conseillé de configurer cette durée à treize mois.

## Existe-t-il un autre moyen de mettre en conformité son outil de mesure d’audience ?

Abla Analytics est notre solution de mesure d'audience répondant aux lacunes de Google Analytics en matière de respect de la vie privée des visiteurs.

Non seulement son utilisation est aisée, mais elle est aussi, et surtout, en mesure de garantir un traitement juste et protecteur des données des utilisateurs.

Là où les autres solutions d’analyse nécessitent une configuration pour traiter les données collectées de façon conforme à la réglementation européenne, Abla Analytics offre une anonymisation automatique et par défaut des données. Il n’est pas non plus obligatoire de recueillir le consentement de l’utilisateur pour que la solution soit conforme au RGPD.

Abla Analytics n’opère de plus aucun profilage, et rend impossible le suivi de la navigation des utilisateurs sur plusieurs sites.
