---
title: "Comprendre git et github"
date: 2023-11-23
categories: ["Version Control", "Coding Tools"]
tags: ["Git", "GitHub", "Tutorial"]
author: "Flavien Thel"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Guide pour les débutants sur Git et Github."
canonicalURL: "https://flavtor.github.io/hugo-blog/posts/git-github-guide"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "images/github.png" # image path/url
    alt: "GitHub globe" # alt text
    # caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---
Découvez les fondamentaux de Git et GitHub, en passant par la génération d'un site static avec Hugo et la mise en ligne avec Github pages.

<!--more-->
# Les fondamentaux de Git et GitHub


## Introduction

Lorsqu'un projet d'application ou de site est en pleine phase de développement, surtout avec la participation de plusieurs collaborateurs, l'adoption de Git devient incontournable. Cela permet de résoudre de manière significative les problèmes liés au versioning du code, en offrant une traçabilité, une collaboration et une gestion des modifications bien plus efficaces. Git devient ainsi l'outil essentiel pour garantir la cohérence et la stabilité du projet, en facilitant la gestion harmonieuse des contributions, la résolution des conflits, et le suivi minutieux des évolutions du code au fil du temps.

## Définitions

- **Git :** Un système de gestion de version qui permet de suivre les changements dans votre code.
- **GitHub :** Une plateforme d'hébergement de code qui utilise Git pour la gestion de version collaborative.

## Pourquoi Git est pratique

Git offre plusieurs avantages pratiques pour les développeurs :

1. **Suivi des Modifications :** Git garde un historique détaillé des modifications apportées au code, facilitant le suivi des changements au fil du temps.
2. **Collaboration Facilitée :** GitHub permet une collaboration fluide entre plusieurs contributeurs. Les fonctionnalités telles que les pull requests simplifient le processus de fusion des contributions.
3. **Gestion des Branches :** La gestion des branches dans Git permet de travailler sur des fonctionnalités ou des correctifs de manière isolée avant de les fusionner dans la branche principale.
4. **Revenir à des Versions Antérieures :** En cas d'erreur ou de problème, Git permet de revenir à des versions antérieures du code, assurant ainsi la stabilité du projet.

## Les commandes Git de bases

##### Initialisation du Projet avec Git
Pour commencer à utiliser Git dans votre projet, vous devez d'abord initialiser un référentiel Git. Voici la première commande que vous devrez utiliser :

`
git init
`

##### Connexion à un Repository distant
Avant de pouvoir pousser vos modifications sur GitHub, vous devez connecter votre référentiel local à un référentiel distant sur GitHub. Avant de faire cela, il faut s'assurer d'avoir d'abord créé un nouveau référentiel sur GitHub.
`
git remote add origin URL_du_repo_GitHub
`

##### Cloner un Référentiel
Pour cloner un référentiel distant depuis GitHub vers votre machine locale, utilisez la commande suivante :
`
git clone URL_du_repo_GitHub
`

Cette commande crée une copie exacte du référentiel distant sur votre machine locale. Assurez-vous de remplacer URL_du_repo_GitHub par l'URL du référentiel GitHub que vous souhaitez cloner.

##### Mettre à Jour votre Projet Cloné

Si d'autres contributeurs apportent des modifications au référentiel distant, vous pouvez mettre à jour votre copie locale avec la dernière version en utilisant la commande :
`
git pull origin master
`

##### Vérifier les Modifications en Attente
En exécutant la commande suivante, Git vous fournira des informations sur les modifications qui ont été faites dans votre répertoire de travail par rapport au dernier push. Vous verrez les fichiers qui ont été modifiés, ajoutés ou supprimés.

`
git status
`

##### Ajouter des fichiers au suivi de Git

Afin d'ajouter des fichiers au suivi de Git vous pouvez effectuer la commande : 
`
git add nom_du_fichier
`

en remplaçant nom_du_fichier par un fichier qui contient des modifications (et donc remonter par le git status)

Pour ajouter tous les fichiers modifiés ou nouveaux au suivi de Git, utilisez la commande :
`
git add .
`

{{< admonition info >}}
Il est important de faire preuve de prudence lors de l'utilisation de cette commande, car elle ajoute tous les fichiers, y compris ceux que vous pourriez ne pas vouloir inclure dans votre prochain commit. S'il y a des fichiers que vous souhaitez excluse du git add, vous pouvez les renseigner dans un fichier `.gitignore`
{{< /admonition >}}

##### Enregistrer les modifications
Une fois que vous avez ajouté les fichiers que vous souhaitez suivre, enregistrez les modifications avec la commande :
`
git commit -m "Message de commit descriptif"
`

Il est important de fournir un message de commit descriptif pour expliquer les modifications apportées. Vous pouvez vous rendre sur
[https://www.conventionalcommits.org/](https://www.conventionalcommits.org/en/v1.0.0/) afin d'en savoir plus sur les commit conventionels.

{{< admonition >}}
A ce niveau là, les commits sont uniquement local et ne sont pas encore sur le repository distant
{{< /admonition >}}

##### Pousser les modifications sur GitHub

Une fois que vous avez ajouté des fichiers et effectué des commits localement, poussez les modifications vers votre référentiel GitHub avec la commande :

`
git push -u origin master
`

# Génération de Site Statique avec Hugo

[Hugo](https://gohugo.io/) est un générateur de sites statiques open source, rapide et flexible, écrit en langage de programmation Go. Il offre une manière simple de créer des sites web rapides, sécurisés et faciles à maintenir.

## Pourquoi Choisir Hugo ?

1. **Rapidité :** Hugo est connu pour sa vitesse de génération exceptionnelle. La génération d'un site avec Hugo est souvent quasi-instantanée, ce qui en fait un choix idéal pour les sites web de toutes tailles.

2. **Facilité d'utilisation :** Hugo est facile à prendre en main, même pour les débutants. Sa structure simple et sa documentation claire facilitent le processus de création de sites web.

3. **Thèmes Flexibles :** Hugo prend en charge une variété de thèmes prêts à l'emploi, ce qui permet aux utilisateurs de personnaliser facilement l'apparence de leur site.

## Configuration de Hugo

Avant de pouvoir générer votre site statique avec Hugo, vous devez effectuer quelques étapes de configuration.

#### Installation 
Vous pouvez télécharger la dernière version de Hugo sur le [site officiel de Hugo](https://gohugo.io/installation/). Suivez les instructions d'installation pour votre système d'exploitation.

#### Création d'un nouveau site 

Une fois Hugo installé, créez un nouveau site avec la commande suivante :


`
hugo new site nom_de_votre_site
`

#### Sélection d'un Thème

 Choisissez un thème pour votre site en ajoutant le thème de votre choix dans le répertoire themes. Vous pouvez explorer les thèmes disponibles sur l[le site des thèmes Hugo](https://themes.gohugo.io/).


`
git submodule add URL_du_theme themes/nom_du_theme
`

#### Configuration du Fichier de Paramètres

Personnalisez les paramètres de votre site en éditant le fichier config.toml à la racine de votre site.



# Exemple de configuration config.toml
```bash
baseURL = "https://votresite.com/"
languageCode = "fr-fr"
title = "Mon Super Site"
theme = "nom_du_theme"
```

#### Lancement du serveur
Maintenant que l'installation et la configuation est faite, vous pouvez lancer votre site static avec la commande 

`
hugo server
`

#### Commencer à créer du contenu

Vous pouvez maintenant créer du contenu très simplement et rapidement en Markdown dans vos articles 

`
hugo new content posts/my-first-post.md
`

# Mise en Ligne avec GitHub Pages

La dernière étape pour partager votre site Hugo avec le monde est de le mettre en ligne sur GitHub Pages. Suivez ces étapes pour publier votre site statique :

## Qu'est-ce que Github Pages ?

GitHub Pages est un service offert par GitHub qui permet aux utilisateurs de créer et héberger des sites web directement depuis leurs dépôts GitHub. C'est une fonctionnalité gratuite qui simplifie le processus de publication en permettant aux utilisateurs de partager leur travail, documentation, projets personnels, portfolios, ou tout autre contenu statique de manière simple et accessible.

## Configuration de GitHub Pages

##### Créez une Branche gh-pages
Créez une nouvelle branche gh-pages qui contiendra le contenu généré par Hugo.

`
git checkout -b gh-pages
`
#####  Génération de Site avec Hugo
Générez votre site Hugo dans le dossier public.

`
hugo -D
`
Le répertoire public contient maintenant les fichiers HTML, CSS et autres nécessaires pour votre site.

##### Poussez le Contenu vers gh-pages
Poussez le contenu du dossier public vers la branche gh-pages.

```bash
cd public/`
git add .
git commit -m "Add generated files for GitHub Pages"
git push origin gh-pages
```

# Configuration des Actions GitHub (Optionnel)

Automatisez le processus de génération de votre site Hugo avec GitHub Actions. Créez un fichier `.github/workflows/build.yml` dans votre repository avec le contenu suivant :

```bash
name: Deploy Hugo site to Pages

on:
  push:
    branches:
      - main
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

defaults:
  run:
    shell: bash

jobs:
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.120.2
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: Install Dart Sass
        run: sudo snap install dart-sass
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v3
      - name: Install Node.js dependencies
        run: "[[ -f package-lock.json || -f npm-shrinkwrap.json ]] && npm ci || true"
      - name: Build with Hugo
        env:
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --gc \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          path: ./public

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2

```


# Félicitations ! Votre site static Hugo sera maintenant deployé à chaque push sur votre repository GitHub !