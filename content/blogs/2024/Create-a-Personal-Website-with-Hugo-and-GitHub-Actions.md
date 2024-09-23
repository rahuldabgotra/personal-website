---
title: 'Create a Personal Website with Hugo and GitHub Actions'
date: Sunday, September 1, 2024
time: 10:51:46 pm India Standard Time
tags: ["Hugo"]
draft: false
---

In today's digital world, having a personal website is a great way to showcase your work, share your thoughts, and build your online presence. In this guide, I'll show you how to create your website using **Hugo** and automate its deployment with **GitHub Actions**.

### Why Have a Personal Website?

Whether it's to share your portfolio, write blogs, or have a simple online presence, having a personal website is crucial. The great news is, you can manage it with markdown files on GitHub. Let’s walk through the steps to build and deploy your site.
***

### Prerequisites

Before we get started, install these tools:

- [**Hugo**](https://gohugo.io/installation/) - for building the website.
- **Git** - for version control.

### Let’s Get Started

#### Step 1: Create a New Hugo Site

Start by creating a new Hugo site and moving into its directory:

```bash
hugo new site my-website --format yaml
cd my-website
```

#### Step 2: Initialize Git and Add a Theme

Next, initialize Git and add the Hugo **PaperMod** theme:

```bash
git init
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
echo "theme: PaperMod" >> hugo.yaml
```

#### Step 3: Create a New Blog Post

Now, let's create your first blog post:

```bash
hugo new blogs/2024/blog_1.md
```

You can find your blog file under the `content` folder. To publish it, set `draft = false` in the blog file:

```md
title: "My First Blog"
date: 2024-04-22
draft: false
```

#### Step 4: Run the Website Locally

To preview your website locally, use this command:

```bash
hugo server
```

*Tip:* Use the `-D` flag to include draft content.

#### Step 5: Push Your Website to GitHub

Create a GitHub repository and run the following commands to push your website code:

```bash
echo "# mysite" >> README.md
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourname/repo_name.github.io.git
git push -u origin main
```

#### Step 6: Configure Hugo

In the `hugo.yaml` file, set the `baseURL` to your GitHub Pages URL:

```yaml
baseURL: "https://yourname.github.io/mysite/"
```

#### Step 7: Set Up GitHub Actions for Deployment

Create a `.github/workflows/hugo.yaml` file and paste this workflow configuration:

```yaml
# Sample workflow for building and deploying a Hugo site to GitHub Pages
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches:
      - main

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

# Default to bash
defaults:
  run:
    shell: bash

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.134.1
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
        uses: actions/configure-pages@v5
      - name: Install Node.js dependencies
        run: "[[ -f package-lock.json || -f npm-shrinkwrap.json ]] && npm ci || true"
      - name: Build with Hugo
        env:
          HUGO_CACHEDIR: ${{ runner.temp }}/hugo_cache
          HUGO_ENVIRONMENT: production
          TZ: America/Los_Angeles
        run: |
          hugo \
            --gc \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"          
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4 
```

#### Step 8: Commit and Push

Once you’re done with all the changes, commit and push your code to the GitHub repository. GitHub Actions will automatically deploy your site at:

```
https://yourname.github.io/mysite/
```

### Conclusion

That's it! You've successfully built and deployed your website using Hugo and GitHub Actions. From now on, all you need to do is write new blog posts, set `draft: false`, commit, and push. Your website will stay updated automatically!

***

### References

- **Video Tutorial:** [Deploy Hugo to GitHub Pages](https://youtu.be/_QSr2_pxIJs?si=W4HCuWr29bkutc8t)
- **Articles:** [Hosting on GitHub](https://gohugo.io/hosting-and-deployment/hosting-on-github/), [Hugo Quick Start](https://gohugo.io/getting-started/quick-start/)
