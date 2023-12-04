---
title: "Hugo Get Started"
date: 2023-11-25
categories: ["Coding", "Coding Tools"]
tags: ["Web", "Frontend", "Tutorial"]
author: "Hakan"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Make your first website with Hugo!"
canonicalURL: "https://agahakan.github.io/hugo-blog/posts/hugo-get-started"
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

# Hugo Get Started: Creating Your First Website

In this tutorial, we'll guide you through the process of setting up Hugo and creating your first website.

Whether you're a seasoned developer or just getting started with web development, Hugo is a fantastic choice for building fast and efficient websites.

## What is Hugo?

[Hugo](https://gohugo.io/) is an open-source static site generator that allows you to create websites with lightning-fast performance. It's written in Go, a high-performance compiled programming language often used for developing web applications, among other things.

Unlike dynamic content management systems (CMS), Hugo generates your entire website as static files, making it highly efficient and secure.

> _"Simplicity is the ultimate sophistication."_ — Leonardo da Vinci

## Prerequisites

1. **Install Hugo**: Make sure you have Hugo installed on your computer. If you haven't installed it yet, you can follow the installation instructions on the [official Hugo website](https://gohugo.io/getting-started/installing/).

2. **Basic Knowledge of Markdown**: Hugo uses Markdown for content creation. If you're not familiar with Markdown, don't worry; it's easy to learn and is a lightweight markup language for formatting text.

3. **Text Editor**: You'll need a text editor to create and edit your Hugo website's content files. Popular choices include Visual Studio Code, Sublime Text, or any text editor you prefer.

## Setting Up Your Hugo Project

Let's start by creating your first Hugo website:

**Create a New Hugo Site**:

Open your terminal and run the following command to create a new Hugo site:

```bash
hugo new site my-hugo-site
```

Replace my-hugo-site with your preferred project name.

**Navigate to Your Project Folder**:

Change your working directory to the newly created project folder:

```bash
cd my-hugo-site
```

Initialize an empty Git repository in the current directory.

```bash
git init
```

**Choose a Hugo Theme**:

Hugo offers a variety of themes to choose from. You can find them on the [Hugo Themes website](https://themes.gohugo.io/). Once you've selected a theme, you can add it to your project using Git or download it manually.

For example, if you want to add the same theme as my blog (yes this blog was with Hugo!), you can use Git like this:

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

**Configure Your Hugo Site**:

Hugo's configuration is defined in a file named hugo.toml.

You need to append a line to that file to indicate the current theme.

```bash
echo "theme = 'ananke'" >> hugo.toml
```

Feel free to edit the hugo.toml file to customize your website's settings, including the theme, title, and other options.

**Start Hugo’s development server to view the site**:

```bash
hugo server
```

Visit [http://localhost:1313/](http://localhost:1313/) in your web browser to see your website in action.

Press Ctrl + C to stop Hugo’s development server.

Now you are all set up, you have a website just like the theme you choosed!
It is now your job to just populate the site with content!

## Adding Content

Now that you've set up your Hugo project, let's create your first page:

**Create a New Content Page**:

Run the following command to create a new content page (in Markdown format):

```bash
hugo new content posts/my-first-post.md
```

This will create a new Markdown file for your first post in the "content/posts" directory.

```
---
title: "My First Post"
date: 2023-11-25
draft: true
---
```

As you can see draft is set to true, so you won't see it on your website as it is still a draft. You can set it to false to see the new content on your site, or you can start your server like so:

```bash
hugo server -D
```

-D or --buildDrafts are optional flags you can include with the hugo server command. When you include the -D flag, Hugo will build and display draft content on the local server.

You can now start writing your content in [Markdown](https://commonmark.org/help/). You can use Markdown features like headings, lists, links, and more to format your content.

## Understanding Hugo's Directory Structure
- Front Matter: Metadata at the top of each content file (YAML, TOML, JSON). Set draft: false to publish.
- Static Folder: Store static files like images or CSS.
- Layouts Folder: Contains templates for page appearance.
- Themes Folder: Store and customize themes.
- Data Folder: Holds configuration data files.
- Archetypes Folder: Templates for new content with default Front Matter.
- Resources Folder: Stores transformed resource files like post-processed CSS.
- Config File: The main configuration file (hugo.toml/hugo.yaml/hugo.json) sets site-wide parameters.

## Build Your Site

Once you're satisfied with your content, you can build your site by running:

```
hugo
```

This command generates the static files in the "public" directory. The files includes HTML, and assets such as images, CSS files, and JavaScript files.

## Deploying Your Website

With your site built, you're ready to deploy it to a web hosting service or a content delivery network (CDN). You can simply upload the contents of the "public" directory to your hosting provider.

Congratulations! You've successfully set up Hugo and created your first website. Explore Hugo's documentation and themes to further customize and enhance your site. Happy building!

---

> _"The journey of a thousand miles begins with a single step."_ — Lao Tzu
