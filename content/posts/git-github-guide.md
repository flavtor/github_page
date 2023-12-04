---
title: "Understanding and Using Git and GitHub"
date: 2023-11-23
categories: ["Version Control", "Coding Tools"]
tags: ["Git", "GitHub", "Tutorial"]
author: "Hakan"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "A beginner's guide to understanding and using Git and GitHub."
canonicalURL: "https://agahakan.github.io/hugo-blog/posts/git-github-guide"
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

# Understanding and Using Git and GitHub

## Introduction

Hello, fellow coders! 👋 Today, we're diving into the world of **Git** and **GitHub**. Whether you're a budding developer or a seasoned coder, these tools are crucial in your coding arsenal. 🚀

But first things first, if you haven't set up Git on your terminal or created a GitHub account, no worries! Check out these handy guides:

- [Setting up Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Creating a GitHub account](https://github.com/join)
- [Generating SSH keys for GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

Done? Awesome! Let's get started. 🌟

## What is Git? 🤔

![Git Logo](https://git-scm.com/images/logos/1color-orange-lightbg@2x.png)

> "Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency." - The Git Team

In simpler terms, **Git** is like a time machine for your code. It lets you track changes, revert to previous stages, and work on different versions of your projects without a sweat.

### Key Features:

- **Branching**: Create independent lines of development.
- **Staging Area**: A prep room for your commits.
- **Commits**: Save snapshots of your projects.

## What is GitHub? 🐙

![GitHub Logo](https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png)

GitHub, the home of Git repositories, is a web-based platform where you can upload your Git repositories, collaborate with others, and manage your projects.

### Cool GitHub Features:

- **Issue Tracking**: Discuss and track bugs and features.
- **Pull Requests**: Propose changes and collaborate.
- **Forks**: Copy a repository to your account to modify without affecting the original.

### Issue and Pull Request Management

- **Issues**: Use issues to report bugs, request features, or discuss aspects of the project.
- **Pull Requests (PRs)**: Propose changes to the codebase and have them reviewed by team members.

### Automation with GitHub Actions

GitHub Actions is a powerful automation tool that lets you create custom workflows for testing, building, and deploying code directly from GitHub.

### Hosting with GitHub Pages

Host your static websites directly from a GitHub repository with GitHub Pages, an easy-to-use hosting service provided by GitHub.

## Git and GitHub in Action ⚡

### Basic Git Commands

1. **Clone a repository**: `git clone [URL]`
2. **Create a new branch**: `git branch [branch-name]`
3. **Switch to a branch**: `git checkout [branch-name]`
4. **Add changes**: `git add .`
5. **Commit changes**: `git commit -m "Your message"`
6. **Push to GitHub**: `git push origin [branch-name]`

### Working with GitHub

1. **Fork a repo**: Click the 'Fork' button on a repository page.
2. **Create a Pull Request**: After pushing changes, click 'New Pull Request' on your forked repo.
3. **Merge changes**: After review, you can merge the PR into the main branch.

## Conclusion

Git and GitHub are like peanut butter and jelly - perfect together for managing and collaborating on coding projects. 🥜🍇

Happy coding! 💻🎉

---

> _"Remember, with great power comes great responsibility."_ — Uncle Ben