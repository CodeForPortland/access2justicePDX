# Access2Justice 
>by [The Commons Law Center](https://thecommonslawcenter.org) and [Code4PDX](https://codeforpdx.herokuapp.com)

This is the code base (aka **The WWW**)for the public facing site of the project, it will provide and collect information regarding project progress and releases, documentation, server status, contacts, and contribution information.

# Contributing To The WWW

There are multiple ways you can help out. Contributions should be made through **Pull Requests(PRs)**, from a personal fork or from your own branch. Editing the content can be done directly from GitHub, however, any logic contribution is developed and tested first, in your own enviornment, before a *PR* should be made.

## Locally
1. Clone the repo to your local development environment (check below for instructions)

2. Develop/Write - [Hugo](https://gohugo.io) provides static web page generation based on the hierarchy of the information architecture (IA). [Girafe Academy](https://youtu.be/qtIqKaDlqXo) has some great videos on giving a quick overview of the different features *Hugo* provides.

3. Make a PR - Always work in your own branch (or fork). Label your PR's to the <strike>[contribution standards](#)</strike>(comming soon) stated in the contribution guide.

4. Declare your PR - When your *PR* is made, let us know in *Slack*. We are interested in what you did and what you think. :) 

# Local Deploy

1. Make sure you have [Hugo](https://gohugo.io) installed in your local dev environment. 
2. Clone repo
```bash
git clone git@github.com:CodeForPortland/access2justicePDX.git
```
3. Install the theme submodule
```bash
git submodule init
git submodule update
```
4. Launch with **Hugo's** dev server
```bash
hugo -b localhost serve --disableFastRender
```
