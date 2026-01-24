+++
date = '2026-01-15T10:49:38+01:00'
draft = "false"
title = "Les LLM dans l'apprentissage"
summary = "Quel impact des LLM sur la formation dans le DevOps ?"
tags = [ "LLM", "continuous-improvement"]
+++

## Introduction

Dans le domaine DevOps, les LLM sont devenus des outils efficaces pour se former et résoudre des problèmes. Cependant, comme tous les outils, ils ne permettent pas de résoudre tous les problèmes et présentent des avantages comme des inconvénients.

## Le défi du contexte insuffisant

Les LLM marchent mieux lorsqu'on leur donne plus de contexte. Or, pour débuguer un problème par exemple, il est compliqué de donner l'intégralité du contexte : les outils utilisés, la configuration mise en place, les dépendances entre les systèmes, etc.

Cela implique souvent plusieurs prompts successifs pour construire progressivement la compréhension du problème. Heureusement, des outils spécialisés comme [xDevOps](https://xdevops.ai/) commencent à adresser ce défi. Ces systèmes autonomes ont accès à toutes les informations de configuration et peuvent itérer jusqu'à identifier la source du problème, puis le résoudre automatiquement.

## Expliquer pour mieux comprendre

Un grand avantage réside dans la capacité à donner des fichiers de configuration (docker-compose, terraform, ansible, etc.) et recevoir des explications détaillées sur leur fonctionnement. Cela m'a permis de mieux comprendre comment architecturer un système.

### Pourquoi c'est plus efficace que la documentation

- La documentation officielle est rarement digeste et facile d'accès
- Discuter avec une IA est plus agréable et permet de mieux retenir les connaissances
- On obtient du contenu spécifique à notre contexte, pas des exemples génériques
- Les forums et documentations sont souvent flous sur les interactions entre les différents composants

### Une approche gagnante

Donner un problème à une IA en lui demandant de poser les questions nécessaires pour comprendre votre configuration permet de résoudre les problèmes rapidement et efficacement, même si on ne comprend pas immédiatement le lien entre tous les composants.

## La surcharge d'informations

Une problématique majeure : **l'IA génère beaucoup de contenu**. Souvent trop. ChatGPT en est un excellent exemple : il crée presque toujours trop de contenu, ouvre plusieurs pistes différentes et peut devenir confus.

On se retrouve facilement avec 3 ou 4 pages de texte pour une question simple, avec l'impression que la quantité équivaut à la qualité.

### Comment résoudre ce problème ?

Depuis que j'ajoute à mes prompts des instructions spécifiques, j'obtiens de meilleurs résultats :

- **Établir un plan clair** avant la réponse
- **Lister les avantages et inconvénients** des solutions proposées
- **Justifier la solution la plus pertinente** et expliquer pourquoi

Certes, cela prend un peu plus de temps, mais les résultats sont bien plus pertinents et consommables qu'extraire une information utile d'un texte de 4 pages.

## L'IA intégrée dans les IDE

Pour ce qui concerne l'IA directement dans les IDE, c'est très pratique pour :

- Corriger les erreurs de syntaxe
- Ajouter les points-virgules manquants
- Compléter les patterns répétitifs

C'est probablement l'une des applications **les plus concrètes et immédiates** de l'IA dans le DevOps actuel.

## Conclusion

Les LLM sont des outils puissants pour l'apprentissage en DevOps, à condition de les utiliser efficacement. Le secret réside dans la structuration des demandes et la conscience de leurs limitations liées au contexte.
