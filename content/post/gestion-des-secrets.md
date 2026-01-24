+++
date = '2026-01-15T10:49:38+01:00'
draft = "false"
title = "La gestion des secrets et des variables d'environnement en intégration continue sur github"
summary = "Comment gérer les secrets et les variables d'environnement"
tags = ["devops","tool"]

+++

## Introduction

Dans l'univers du DevOps et de l'intégration continue (CI/CD), la gestion sécurisée et flexible des configurations est primordiale. Si vous utilisez GitHub Actions, vous vous êtes sûrement déjà demandé comment éviter de coder en dur des informations sensibles ou comment rendre vos workflows plus dynamiques.

Cet article résume les bonnes pratiques pour utiliser les variables d'environnement et les secrets dans vos pipelines GitHub Actions.

## Pourquoi utiliser des variables d'environnement ?

Les développeurs sont souvent tentés de coder en dur des chaînes de connexion, des clés d'API ou des configurations spécifiques directement dans le code ou les fichiers YAML. C'est une pratique dangereuse et peu flexible.

Les variables d'environnement permettent de :

- **Réutiliser des valeurs** à plusieurs endroits du workflow
- **Configurer le comportement** des scripts sans changer le code
- **Sécuriser les données sensibles** via les secrets

## Les 3 niveaux de portée des variables

Dans GitHub Actions, la définition des variables dépend de l'endroit où elles doivent être accessibles. Il existe trois niveaux de portée définis par le mot-clé `env` :

### 1. Portée Workflow (Globale)

Définies à la racine du fichier YAML, ces variables sont accessibles par tous les jobs et toutes les étapes du workflow.

```yaml
name: Mon Workflow
env:
  APP_NAME: "Snyk Demo" # Accessible partout

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Print Name
        run: echo "Hello ${{ env.APP_NAME }}"
```

### 2. Portée Job (Job Level)

Définies à l'intérieur d'un job spécifique. Ces variables ne sont accessibles que par les étapes de ce job précis.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    env:
      JAVA_VERSION: "21" # Accessible uniquement dans le job 'build'
    steps:
      - uses: actions/setup-java@v3
        with:
          java-version: ${{ env.JAVA_VERSION }}
```

### 3. Portée Étape (Step Level)

Définies au sein d'une étape unique. Elles ne sont visibles que pendant l'exécution de cette étape.

```yaml
steps:
  - name: Run Build
    env:
      BUILD_CONTEXT: "Production"
    run: echo "Building for ${{ env.BUILD_CONTEXT }}"
```

## Les variables par défaut de GitHub

En plus de vos variables personnalisées, GitHub fournit une liste de variables par défaut prêtes à l'emploi. Elles sont très utiles pour conditionner l'exécution de vos scripts selon le contexte.

### Exemples courants

- **GITHUB_ACTOR** : Le nom de la personne ou de l'app qui a déclenché le workflow
- **GITHUB_RUN_ID** : Un identifiant unique pour l'exécution du workflow
- **RUNNER_OS** : Le système d'exploitation du runner (ex: Linux, Windows)

Pour la liste complète, référez-vous à la [documentation officielle](https://docs.github.com).

## Gestion sécurisée avec les GitHub Secrets

C'est le point critique de la sécurité. Vous ne devez jamais stocker de clés API, de mots de passe ou de chaînes de connexion en clair dans vos fichiers YAML.

### Comment créer un secret ?

1. Allez dans votre dépôt GitHub
2. Cliquez sur **Settings > Security > Secrets and variables > Actions**
3. Cliquez sur **New repository secret**
4. Ajoutez votre clé (ex: `API_KEY`) et sa valeur

### Utiliser un secret dans le workflow

La syntaxe change légèrement. Au lieu d'utiliser le contexte `env`, on utilise le contexte `secrets`.

```yaml
steps:
  - name: Connect to Database
    run: ./connect-db.sh
    env:
      DB_PASSWORD: ${{ secrets.DB_PASSWORD }} # Injection sécurisée
```

**Note importante** : GitHub Actions masque automatiquement les secrets dans les logs. Si vous tentez d'afficher un secret avec un `echo`, la sortie sera remplacée par des astérisques (`****`).

## Cas pratique : Intégration de Snyk pour la sécurité

Pour illustrer l'utilisation d'un secret tiers, prenons l'exemple de l'intégration de Snyk (outil de détection de vulnérabilités).

### Étapes d'intégration

**1. Récupération du Token**
Créez un compte sur Snyk.io et récupérez votre Auth Token dans les paramètres du compte.

**2. Création du Secret**
Ajoutez ce token dans les secrets GitHub sous le nom `SNYK_TOKEN`.

**3. Configuration du Workflow**

Utilisez une Action pré-configurée (disponible sur la marketplace) et passez-lui le token via une variable d'environnement au niveau du job.

```yaml
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run Snyk to check for vulnerabilities
        uses: snyk/actions/maven@master
        env:
          SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}
```

Cela permet de scanner votre code à chaque push sans jamais exposer votre clé d'API Snyk publiquement.

## Conclusion

L'utilisation correcte des variables d'environnement et des secrets est essentielle pour maintenir des pipelines CI/CD propres, maintenables et sécurisés.

**Points clés à retenir :**

- Utilisez les scopes pour limiter la portée des variables au strict nécessaire
- Appuyez-vous sur les variables par défaut pour le contexte d'exécution
- Utilisez toujours les GitHub Secrets pour vos données sensibles

En adoptant ces pratiques, vous évitez les fuites de données accidentelles et facilitez la collaboration sur vos projets.

Sources :
[Stéphane Robert](https://blog.stephane-robert.info/docs/pipeline-cicd/github/fondations/secrets/) -
[Snyk](https://www.youtube.com/watch?v=5xngh29yx9A)
