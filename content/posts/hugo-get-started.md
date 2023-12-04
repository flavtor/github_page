---
title: "Débutez Hugo"
date: 2023-11-25
categories: ["Coding", "Coding Tools"]
tags: ["Web", "Frontend", "Tutorial"]
author: "flavtor"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Fait ton premier site web en hugo"
canonicalURL: "https://flavtor.github.io/hugo-blog/posts/hugo-get-started"
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
  image: "images/hugo.png" # image path/url
  alt: "Hugo Logo" # alt text
  # caption: "<text>" # display caption under cover
  relative: false # when using page bundles set this to true
  hidden: true # only hide on current single page
---

Bien sûr, voici la version traduite en français que tu pourrais copier-coller :

---

# Démarrer avec Hugo : Créer votre premier site web

Dans ce tutoriel, nous allons vous guider à travers le processus de configuration de Hugo et la création de votre premier site web.

Que vous soyez un développeur expérimenté ou que vous débutiez tout juste en développement web, Hugo est un excellent choix pour créer des sites web rapides et efficaces.

## Qu'est-ce que Hugo ?

[Hugo](https://gohugo.io/) est un générateur de site statique open-source qui vous permet de créer des sites web avec des performances ultra-rapides. Il est écrit en Go, un langage de programmation compilé à haute performance souvent utilisé pour développer des applications web, entre autres.

Contrairement aux systèmes de gestion de contenu dynamique (CMS), Hugo génère l'intégralité de votre site web sous forme de fichiers statiques, le rendant hautement efficace et sécurisé.

> _"La simplicité est la sophistication suprême."_ — Léonard de Vinci

## Prérequis

1. **Installer Hugo** : Assurez-vous d'avoir Hugo installé sur votre ordinateur. Si vous ne l'avez pas encore installé, vous pouvez suivre les instructions d'installation sur le [site officiel de Hugo](https://gohugo.io/getting-started/installing/).

2. **Connaissance de base de Markdown** : Hugo utilise Markdown pour la création de contenu. Si vous n'êtes pas familier avec Markdown, ne vous inquiétez pas ; c'est facile à apprendre et c'est un langage de balisage léger pour formater du texte.

3. **Éditeur de texte** : Vous aurez besoin d'un éditeur de texte pour créer et modifier les fichiers de contenu de votre site Hugo. Des choix populaires incluent Visual Studio Code, Sublime Text, ou tout éditeur de texte que vous préférez.

## Configuration de votre projet Hugo

Commençons par la création de votre premier site Hugo :

**Créer un nouveau site Hugo** :

```bash
hugo new site mon-site-hugo
```

Remplacez `mon-site-hugo` par le nom de projet que vous préférez.

**Accéder au dossier de votre projet** :

```bash
cd mon-site-hugo
git init
```

**Choisir un thème Hugo** :

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
echo "theme = 'ananke'" >> hugo.toml
```

**Démarrer le serveur de développement de Hugo pour visualiser le site** :

```bash
hugo server
```

Rendez-vous sur [http://localhost:1313/](http://localhost:1313/) dans votre navigateur web pour voir votre site en action.

Maintenant, vous êtes prêt, vous avez un site web tout comme le thème que vous avez choisi ! Il vous reste à remplir le site avec du contenu !

## Ajout de contenu

Créons votre première page :

**Créer une nouvelle page de contenu** :

```bash
hugo new content posts/mon-premier-article.md
```

Cela créera un nouveau fichier Markdown pour votre premier article dans le répertoire "content/posts".

```
---
title: "Mon premier article"
date: 2023-11-25
draft: true
---
```

```bash
hugo server -D
```

Vous pouvez maintenant commencer à écrire votre contenu en [Markdown](https://commonmark.org/help/).

## Comprendre la structure de répertoires de Hugo
- Front Matter : Métadonnées en haut de chaque fichier de contenu (YAML, TOML, JSON). Réglez `draft: false` pour publier.
- Dossier Statique : Stockez les fichiers statiques tels que les images ou les CSS.
- Dossier Modèles : Contient les modèles pour l'apparence des pages.
- Dossier Thèmes : Stockez et personnalisez les thèmes.
- Dossier Données : Contient les fichiers de données de configuration.
- Dossier Archétypes : Modèles pour un nouveau contenu avec des métadonnées par défaut.
- Dossier Ressources : Stocke les fichiers de ressources transformées comme les CSS post-traités.
- Fichier de Configuration : Le fichier de configuration principal (hugo.toml/hugo.yaml/hugo.json) définit les paramètres du site.

## Générer votre site

```bash
hugo
```

Cette commande génère les fichiers statiques dans le répertoire "public".

## Déploiement de votre site

Avec votre site généré, vous êtes prêt à le déployer sur un service d'hébergement web ou un réseau de diffusion de contenu (CDN). Vous pouvez simplement télécharger le contenu du répertoire "public" sur votre fournisseur d'hébergement.

Félicitations ! Vous avez réussi à configurer Hugo et à créer votre premier site web. Explorez la documentation et les thèmes de Hugo pour personnaliser et améliorer davantage votre site. Bonne construction !

---

Cela devrait être prêt à être copié-collé pour votre usage !

---