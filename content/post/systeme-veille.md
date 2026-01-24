+++
date = '2026-01-23T10:49:38+01:00'
draft = "false"
title = "Mon système de veille autour du DevOps"
summary = "Comment mettre en place une stratégie de veille efficace en DevOps ?"
tags = ["devops", "veille", "autonomous-system"]
+++

## Introduction

En tant que passionné de tech, la veille est un mal nécessaire. D'un côté, c'est le carburant de ce blog ; de l'autre, c'est une source inépuisable de distraction et de charge mentale.

Pendant longtemps, j'ai eu des onglets ouverts partout, des liens "à lire plus tard" qui moisissaient dans mes favoris, et des newsletters noyées dans ma boîte de réception. Résultat ? Beaucoup de bruit, peu de signal, et une difficulté énorme à retrouver l'information au moment de rédiger un article.

J'ai décidé de tout remettre à plat. Aujourd'hui, je vous présente mon "Second Cerveau" : **un système automatisé qui centralise tout dans Notion**, pour que je puisse me concentrer sur l'essentiel : créer.

## L'architecture : Une base unique pour les gouverner toutes

Le cœur du système est simple mais radical : **tout est centralisé dans une seule Base de Données Notion**.

Fini la dispersion entre Pocket, les favoris du navigateur et les dossiers d'emails. Que l'info vienne d'une vidéo, d'un article ou d'une newsletter, elle atterrit au même endroit. Cela me permet d'avoir une vue unifiée et consultable instantanément.

Mais la vraie magie réside dans la façon dont cette base se remplit. Voici mes **3 sources d'entrée principales**.

### 1. YouTube : La curation automatisée

Je consomme beaucoup de contenu vidéo pour ma veille. Mais je ne veux pas interrompre mon visionnage pour prendre des notes.

**Le déclencheur :** Dès que je tombe sur une vidéo pertinente, je l'ajoute simplement à une playlist YouTube privée nommée "Veille".

**L'automatisation :** Une fois par semaine, un scénario Make (ex-Integromat) scanne cette playlist.

**Le résultat :** Make crée automatiquement une nouvelle entrée dans ma base Notion avec le titre de la vidéo, le lien direct et la miniature.

### 2. Newsletters : La fin du chaos dans la Inbox

Les newsletters techniques sont des mines d'or, mais elles polluent ma boîte mail principale.

**Le tri :** J'ai configuré une règle dans ma messagerie : tout ce qui est newsletter technique part directement dans un dossier "DevOps", sans passer par la boîte de réception.

**L'automatisation :** Là encore, Make entre en jeu. Une fois par semaine, il récupère les mails non lus de ce dossier, extrait le contenu (le corps du mail) et génère une page Notion pour chaque newsletter.

**L'avantage :** Je ne subis plus l'arrivée des mails. Ils m'attendent sagement dans Notion pour le moment où j'ai décidé de les lire.

### 3. Le Web : La capture ciblée

Pour les articles de blog et la documentation que je croise lors de ma navigation quotidienne, je reste sur une méthode manuelle mais optimisée.

**L'outil :** J'utilise l'extension **Notion Web Clipper**.

**L'action :** En un clic, l'extension capture non seulement le lien, mais aussi tout le contenu de la page. Cela me permet de sauvegarder l'article pour une lecture hors-ligne ou archivée, au cas où le site disparaîtrait.

## L'organisation et le workflow : De la collecte à la création

Avoir de l'information, c'est bien. Pouvoir l'utiliser, c'est mieux. Pour éviter que ma base Notion ne devienne un cimetière d'articles, j'ai mis en place une routine stricte.

### Le système de Tags "Miroir"

Dans Notion, chaque entrée doit être taguée. J'ai fait le choix de créer un système de tags qui est le miroir exact des catégories de mon blog.

Si je tague un article CI/CD ou Kubernetes dans ma veille, je sais que dans 3 semaines, quand je voudrai écrire un article sur ce sujet, je n'aurai qu'à filtrer ma base pour retrouver toutes mes sources prêtes à l'emploi.

### La routine hebdomadaire

Le secret de ce système, c'est qu'il tourne tout seul **90% du temps**.

Le lundi matin, je me connecte à mon tableau de bord Notion. J'utilise une vue filtrée "Derniers 7 jours". Mon travail est alors balisé :

- Je passe en revue ce que le robot a collecté
- Je lis ce qui est pertinent immédiatement
- J'archive ce qui n'est finalement pas intéressant
- Je tague ce qui servira pour un futur contenu

## Pourquoi ça change tout : Les bénéfices

Après quelques semaines d'utilisation, je ne pourrais plus revenir en arrière. Voici pourquoi :

### Charge mentale réduite

Je ne ressens plus le besoin de vérifier mes mails ou YouTube tous les jours de peur de rater une info. Je sais que le système capture tout pour moi. J'ai arrêté de subir le flux, je le contrôle.

### Centralisation de la connaissance

Tout est consultable via la recherche Notion. Une idée lue il y a 6 mois est retrouvée en 3 secondes.

### Gain de temps rédactionnel

C'est le plus gros ROI. Quand je commence à rédiger un article de blog, je ne pars plus d'une page blanche. J'ai déjà sous les yeux une liste de sources qualifiées et triées.

## Conclusion

Mettre en place ce système de veille a transformé ma façon de produire du contenu. Ce n'est pas seulement de l'automatisation, c'est une façon de construire un actif durable de connaissances.

Si vous souhaitez mettre en place un système similaire, **commencez petit** : centralisez d'abord une source (comme YouTube), puis étendez votre système.

Et vous, quels outils utilisez-vous pour ne pas vous noyer sous l'information ?
