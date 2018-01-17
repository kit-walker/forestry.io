---
title: GitHub Pages
weight: 2
publishdate: 2017-12-31 04:00:00 +0000
expirydate: 2030-01-01 04:00:00 +0000
date: 2017-12-31 00:00:00 -0400
menu:
  docs:
    parent: hosting
layout: single
---
{{% tip "Disclaimer" %}}
This guide assumes you already have an existing [Forestry Account](https://app.forestry.io/signup), [GitHub account](https://github.com/signup), and a repository with a Jekyll or Hugo project. If you don't have an existing project, check out our [Quick start guide](/docs/welcome/quick-start), which contains guides and resources for building your first static site.
{{% /tip %}}

## Getting Started
To deploy a static site to GitHub pages using Forestry, you must first set up a new branch named `gh-pages` on your repo, which you can do by going to your repository in GitHub and using the branch management dropdown.

![](/images/2017/12/github-gh-pages-settings.png)

## Configuring Forestry

Once your new branch is created, navigate to the *Settings* page of your site in Forestry, click the *Hosting* tab, and set the *Connection* option to *GitHub Pages*.

TK: image

If you haven't authenticated with GitHub before, you'll be prompted to choose "[Public Repos](https://help.github.com/articles/making-a-private-repository-public/)" or "[Private Repos](https://help.github.com/articles/making-a-public-repository-private/)". Choose the option the applies to your repository. 

This will redirect you to GitHub, and prompt you to enter your login credentials if you are not already logged in.

TK: image

Give Forestry access to your GitHub repositories by clicking "Authorize application". You can also request access to any [GitHub organizations](#importing-from-a-github-organiation) you are a member of.

{{% warning %}}
In order to host a site with GitHub Pages, you will need [admin permissions](https://help.github.com/articles/repository-permission-levels-for-an-organization/) for the repository. This is because Forestry needs to add a web hook to your repository in order to watch for changes.
{{% /warning %}}

Once authorized, you will be redirected back to Forestry.

![](/images/2017/12/forestry-gh-pages-settings.png)

Next, choose your repository, select the new `gh-pages` branch, and then click *Save Settings*. 

From here on, every time you save or publish a page Forestry will build your site and deploy to this branch.

## Enable GitHub Pages

To have GitHub pages begin serving from your new branch, go to the `Settings` page of your GitHub repository and scroll down to the `GitHub Pages` section.

Then select the branch that contains your built static site and click on the Save button.

![](/docs/assets/images/branch-management.png)

Your site should now be served at `http://username.github.io/repository`.