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