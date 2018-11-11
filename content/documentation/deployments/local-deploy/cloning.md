---
title: Cloning the Repos 
description: How to retrieve the latest version of the router, demo service and interface.
weight: 20
---

Now you will retrieve the master branches of the needed repos, there will be an explanation of each one and how they relate to the whole of the project in the following chapters.

We are going to use *Go* to retrieve our repos, using the `go get` command. [ref](https://golang.org/cmd/go/)


### Repos

Now to clone our first two repos we can run the following commands. 
```bash
go get github.com/CodeForPortland/ctl-aura/...
go get github.com/CodeForPortland/ctl-authentication-service/...
```

When you install *Go*, it usually sets up a *workspace directory* called `GOPATH`, which you are going to navigate too. 

A `src` folder should be in your `$GOPATH`, inside that there should be a `github.com/CodeForPortland` folder. You should step into that. The whole directory path should be `{$GOPATH}/src/github.com/CodeForPortland/`. On my machine it's located at `/Users/rex/go/src/github.com/CodeForPortland/`, however I'm on a linux flavored machine and this might be different for *Windows*. [Here](https://www.metaltoad.com/blog/golang-environment-configuration) is great article form [MetalToad](https://www.metaltoad.com) about *GoLang Environment Variables* that explains it more in depth and can help you debug if your `GOPATH` is not set properly. 

Now let's `git clone` the *Dashboard*

```bash
git clone git@github.com:CodeForPortland/a2j-front-end_dashboard.git
```

### Verify

If all went well you should now have the following three repos in your `CodeForPortland` folder.

- [ctl-aura](https://github.com/CodeForPortland/ctl-aura)
- [ctl-authentication-service](https://github.com/CodeForPortland/ctl-authentication-service)
- [a2j-front-end_dashboard](https://github.com/CodeForPortland/a2j-front-end_dashboard)

If you step into each of the project folders and run a `git branch` it should show you that you are on the **master** branch for each one.

### Next

Next you will sww how to launch the router and learn what it's core responsibilities are as well as some core **WAMP v2** paradigms.  