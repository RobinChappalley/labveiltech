# labveiltech

Blog personnel construit avec [Hugo](https://gohugo.io/) et le thème [github-style](https://github.com/MeiK2333/github-style).

## Prérequis

- Hugo v0.154.5 ou supérieur

## Installation

1. Clonez le projet :

```bash
git clone https://github.com/RobinChappalley/labveiltech.git
cd labveiltech
```

## Build en local

### Démarrer le serveur de développement

```bash
hugo server
```

Le site sera accessible à `http://localhost:1313`

### Build pour la production

```bash
hugo --minify
```

Les fichiers générés seront dans le dossier `public/`

## Structure du projet

```
.
├── content/          # Contenu des articles (markdown)
├── layouts/          # Templates personnalisés
├── static/           # Fichiers statiques (images, CSS, JS)
├── themes/           # Thèmes Hugo
├── public/           # Sortie de compilation (généré automatiquement)
└── hugo.toml         # Configuration Hugo
```

## Ajouter un nouvel article

1. Créez un nouveau fichier dans `content/post/` :

```bash
hugo new post/mon-article.md
```

2. Éditez le fichier avec le contenu souhaité

3. Démarrez le serveur pour voir l'aperçu en direct

## Déploiement

Le site est automatiquement déployé sur GitHub Pages via GitHub Actions lors d'un push sur la branche `main`.

Voir [`.github/workflows/static.yml`](.github/workflows/static.yml) pour les détails du workflow.
