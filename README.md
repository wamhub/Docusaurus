# Docusaurus on Github Pages

This is a demo repo to allow for a fast setup of Docusaurus on Github pages

# Instructions

To begin with this repository you have two options:
- (a) Fork this repository. When you do it, make sure you fork all branches, not only main. Github Actions need the "gh-pages" branch to deploy the site.
- (b) Clone it to your local filesystem, create a new repository on your github account and push it there. Upon pushing the github actions should trigger and create the gh-pages branch. If it doesn't, make a small change to this file and push it again.

There are other changes you need to do: 

- Github Actions need to be enabled (Settings -> Actions -> General)
    - Actions permissions:
        - Allow all actions and reusable workflows
    - Workflow permissions:
        - Read and write permissions
- Github Pages must also be enabled (Settings -> Pages)
    - Source
        - Deploy from a branch
    - Branch
        - gh-pages (on the dropdown)

# Generate a PDF from the Docs section

You can generate a PDF from the docs section of your Docusaurus website. Just run the following command after replacing the URL with your own:

```
npx docusaurus-prince-pdf --include-index -u https://masaleiro.github.io/docusaurus-ghpages/docs/intro
```

Another alternative is using [Docs-to-pdf](https://github.com/jean-humann/docs-to-pdf) with the following command as example:

```
npx docs-to-pdf --initialDocURLs="https://masaleiro.github.io/docusaurus-ghpages/docs/intro" --contentSelector="article" --paginationSelector="a.pagination-nav__link.pagination-nav__link--next" --excludeSelectors=".margin-vert--xl a,[class^='tocCollapsible'],.breadcrumbs,.theme-edit-this-page" --coverImage="https://docusaurus.io/img/docusaurus.png" --coverTitle="Docusaurus v2" --pdfMargin="40,60,70,80"
```