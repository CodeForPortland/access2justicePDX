---
title: Local Dependencies
description: This will set up your machine with the dependencies needed to run the router and demo service.
weight: 1
---  

## Dependencies

|Title| Type | Link |
|:---|:---:|:----:|
|Git| Version Control System|[git-scm](https://git-scm.com/)|
|GoLang| Programming Language|[GoLang](https://golang.org/)|
|NodeJS| JavaScript Framework/Engine |[NodeJS.org](https://nodejs.org/)|
|AngularCLI| Command Line Tool |[AngularCLI](https://cli.angular.io/)|

## Git

You should have **Git** installed on your machine. If you don't, you might want to stop reading this guide for right now and familiarize yourself [contributing](https://egghead.io/courses/how-to-contribute-to-an-open-source-project-on-github) and the *Git* specs here, [git-scm](https://git-scm.com/). 
You should have a basic grasp of how to push and pull from a repo with git, before continuing. 

## GoLang

{{% notice info %}}You wont need to learn **Go** to follow along in this, but you do need to compile it and some basic knowledge of code will help you understand what I'm rambling about. 
{{% /notice %}}

[Go](https://golang.org) is an open source language developed by *Google*. It is a lower-level language like `C++` but built with the wisdom from years of toil and headaches from code. It's also pretty dang fast. If your interested, you can explore more about it at the [Go Tour](https://tour.golang.org/welcome/1).  
 
### Installing Go 

If you like to manually install things. You can find the binaries for your machine's processor [here](https://golang.org/dl/).

Some common dependency managers can install Go as well.

#### Homebrew
```bash
$ brew install go
```

#### Chocolatey

```bash
C:\> choco install golang
```

#### Ubuntu
{{% notice warning %}}You may need to use `sudo` to install **GoLang**.
{{%/ notice %}}
```bash
$ apt-get install golang
```

### Check Installation

Run this in your bash or terminal.
```bash
 $ go version
```

You should see something similar to...

```bash
go version go1.11 darwin/amd64
```

## Angular CLI and NodeJS

The dashboard is composed in [TypeScript](https://www.typescriptlang.org) and uses the [Angular.io](https://angular.io) framework. The easiest way to set up these dependencies is by using *NodeJS's* package manager, **NPM** and the [AngularCLI](https://cli.angular.io/) . 
You can download *NodeJS* [here](https://nodejs.org) and just follow along with the instructions to install it.

After you have *NodeJS* installed, run the following command to install *AngularCLI* into your global `node_modules` folder.

```bash
$ npm i -g @angular/cli
```

## Next

Next we will clone the **router**, a **service** and then an **interface** to set up our basic example of a *WAMP v2* microservice system.