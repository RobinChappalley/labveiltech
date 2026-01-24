+++
date = '2026-01-24T16:48:16+01:00'
draft = false
title = 'À propos'
summary = "Des trucs sur moi"
+++

# 🗺️ Fiche de domaine : DevOps

## 📍 Domaine

**Ingénierie DevOps & automatisation des infrastructures**

Le DevOps (contraction de _Development_ et _Operations_) n'est pas seulement un ensemble d'outils, mais une culture et une méthodologie visant à unifier le développement logiciel et l'administration des systèmes. Ce domaine englobe l'ensemble du cycle de vie des applications, de la conception au déploiement et à la maintenance en production.

Il repose sur des piliers technologiques forts comme le **Cloud Computing**, la **Conteneurisation** et l'**Infrastructure as Code (IaC)**.

## 🔑 Mots-clés

_Lexique essentiel du domaine_

- **CI/CD** (Intégration Continue / Déploiement Continu)
- **Infrastructure as Code** (Terraform, Ansible)
- **Conteneurisation & Orchestration** (Docker, Kubernetes)
- **Monitoring & Observabilité** (Prometheus, Grafana, ELK)
- **Cloud Computing** (AWS, Azure, GCP)
- **Scalabilité & Haute Disponibilité**
- **Automatisation & Scripting** (Python, Bash)
- **GitOps**

## 🧩 Sous-domaines

_Division en sous-thèmes et domaines apparentés_

- **DevSecOps :** Intégration de la sécurité dès la phase de développement.
- **SRE (Site Reliability Engineering) :** Approche axée sur la fiabilité et la stabilité des services en production.
- **Cloud Architecture :** Conception d'infrastructures dématérialisées.
- **Platform Engineering :** Création de plateformes internes pour faciliter le travail des développeurs.
- **FinOps :** Optimisation des coûts liés au Cloud.
- **MLOps :** Application des principes DevOps aux projets de Machine Learning.

## 🎯 Pourquoi ?

_Alignement avec mon projet professionnel et mon Ikigai_

J'ai choisi le DevOps car c'est un domaine pivot qui réconcilie deux mondes souvent cloisonnés. Il correspond parfaitement à mon **Ikigai** pour les raisons suivantes :

{{< img src="images/ikigai.png" alt="Mon Ikigai" caption="Mon Ikigai personnel" >}}

1.  **Vision Transversale :** Il fait appel à ma capacité à _"voir les problèmes sous différents angles"_ et à _"penser à tous les cas possibles"_, en anticipant à la fois les besoins fonctionnels et les contraintes techniques.
2.  **Rigueur & Disponibilité :** Il satisfait mon besoin de structure et d'exigence. Assurer la fiabilité d'un système demande une grande rigueur, une valeur clé identifiée dans mon profil.
3.  **Communication & Faire :** C'est un métier d'action (_"faire"_, _"automatiser"_) qui nécessite impérativement de _"communiquer"_ pour briser les silos entre les équipes.

En résumé, le DevOps me permet d'être **l'architecte de solutions fiables**, transformant du code brut en produits finis utilisables par tous.

## L'organisation : mes 3 niveaux de taxonomies

Pour éviter que ma base de données ne devienne un fourre-tout inutilisable, j'ai défini une structure de classement précise. Chaque ressource capturée est qualifiée selon trois critères essentiels :

### 1. La thématique (Le sujet)

C'est le critère principal pour retrouver l'information. J'utilise un système de tags qui est le **miroir exact des catégories de mon blog**.

- **Objectif :** Si je veux écrire un article sur Docker, je filtre simplement sur ce tag pour voir toutes mes ressources accumulées.
- _Exemples :_ `🐳 Containerisation`, `☁️ Cloud`, `🛡️ Sécurité`, `⚒️ Outil` .

### 2. Le statut (Le workflow)

Ce champ définit l'état de vie de l'information et guide ma routine hebdomadaire. Il transforme la base de données en une file d'attente actionnable.

- 📥 **Inbox (À trier) :** Le statut par défaut assigné automatiquement par les robots (Make/Web Clipper).
- 🧠 **À lire / À voir :** L'intérêt est validé, mais je n'ai pas le temps de consommer le contenu immédiatement.
- ⭐ **Pépite (À exploiter) :** Contenu consommé et très pertinent, à utiliser comme source pour un futur article.
- ✅ **Archivé :** Lu et stocké pour référence future.

### 3. Le type (L'angle)

Une classification optionnelle qui m'aide à décider du format de mes futurs articles.

- _Exemples :_ `📰 News` (pour un article d'actualité), `🎓 Tutoriel` (pour un guide pratique), `🛠️ Outil` (pour une liste de ressources).

### Résumé visuel

Concrètement, voici à quoi ressemble une entrée dans mon système :

| Titre de la ressource           | Thématique          | Statut    | Type        |
| :------------------------------ | :------------------ | :-------- | :---------- |
| _Comprendre les volumes Docker_ | 🐳 Containerisation | ⭐ Pépite | 🎓 Tutoriel |
| _Nouveautés AWS re:Invent_      | ☁️ Cloud            | 📥 Inbox  | 📰 News     |

## Pourquoi Hugo ? (Le choix technique)

Si l'utilisation de **Hugo** m'a initialement été suggérée dans le cadre pédagogique de ce projet, ce générateur de site statique (SSG) s'est rapidement révélé être le candidat idéal pour mon architecture, pour trois raisons :

1.  **La rapidité (Go) :** Codé en Go, Hugo est l'un des moteurs les plus rapides du marché. La génération des pages est quasi-instantanée, ce qui fluidifie les déploiements.
2.  **La compatibilité Markdown :** Tout mon système de veille (Notion) est basé sur le texte. Hugo gérant nativement le Markdown, le passage de la prise de note à la publication est naturel.
3.  **La simplicité et sécurité :** En générant des fichiers HTML statiques, je m'affranchis des lourdeurs d'une base de données (comme sur WordPress) et réduis drastiquement les failles de sécurité.
