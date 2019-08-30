--- 
layout: post
title:  Getting Started With Git
date:   2019-08-28 11:45:32 -0400
tags: git
categories: tutorial
comments: true
---
## Version Control
Have you ever worked on a project with a group of people, or made edits to a file only to realize it was a huge disaster? Version control allows you to track all the changes that are made and coordinate which will be kept and which can be dumped.

## Git
Git is a distributed version control system, and you may already have it installed on your computer. In your command line interface (CLI) type:

``` bash
git --version
```
If you have git you are good to go otherwise you'll need to install it. Download from here: [git-scm.com](https://git-scm.com/download){:target="_blank"}

## Track Your Changes with Git
``` bash
git init
```
## Upload Your Site Online
You have many options to upload your site online. Today we will use Github Pages
- Go to [Github.com](https://www.github.com){:target="_blank"} and signup for an account. 
- Then create a new repository. Which is just like a folder that will hold your site. You must add a name, description, and check the box to initialize a README file.
- Go to the repository you created and click on the Settings link.
- Go to the repository page and copy the https clone url
- Open your terminal and clone that new repository to your computer

``` bash 
git clone https://github.com/user/reponame.git # link you copied
```
