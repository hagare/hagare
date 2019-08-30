--- 
layout: post
title:  Getting Started With Static Sites Using Jekyll 
date:   2019-08-23 14:24:32 -0400
tags: jekyll static blog markdown tutorial ruby git
categories: tutorial
comments: true
---

- **What is a Static Site?** Well a static site is not dynamic, but pre-built and served. The files are not changed dynamically on server side with scripts. Static sites serve up HTML files.
- **Why would I even use one?** They're easier to design and scale, safer, cheaper to run, and load faster
- **Some Cons:** You must build your site everytime you add content, you have to workaround features such as logins and forms

- There are many flavors you can use based on Node, Ruby, Python, Go etc. languages. This post focuses on **Ruby based Jekyll**.

## Pre-requisites
- Command Line Interface 
  - Windows: Command Prompt
  - Mac: Terminal
  - Linux: Shell/Terminal/Console/Prompt 

- Ruby <br />
Do you have Ruby? Find out using your command line:
``` bash
ruby -v
```
If you don't have Ruby, you'll need to install it first. You can find detailed instructions to install Ruby here: [Ruby installation instructions](https://www.ruby-lang.org/en/documentation/installation/){:target="_blank"}. As of writing this post you need at least version 2.6 to install Jekyll properly. You may need to use a ruby version manager such as [rbenv](https://github.com/rbenv/rbenv){:target="_blank"}.

- Bundler and Jekyll <br />
Once you have Ruby, you need to install *Bundler* and *Jekyll*.

``` bash
gem install bundler jekyll
```
You can find out more information at Jekyll's official site: [Jekyll](http://www.jekyllrb.com{:target="_blank"}

- Git <br />
For version control we will need git. You may already have it installed.
``` bash
git --version
```
If you have git you are good to go otherwise you'll need to install it. Download from here: [git-scm.com](https://git-scm.com/download){:target="_blank"}

##  Generate A New Jekyll Site
``` bash
jekyll new site-name
```
### Track Your Changes with Git
``` bash
git init
```
## Edit Your Site
This default starter site utilizes the *minimal* theme. 

### Basic Customization
Edit the file **_config.yml** to add your new site's detail.
Add your title, description, name, and url to this file.
You can also add information such as your *twitter handle, google analytics account, or disqus id* here.

### Add a new post to your blog
To add blog posts to your  new site create a markdown file with the the following format in the _posts directory:

>    yyyy-mm-dd-title-of-post.md
 
 ``` bash 
 cd site-name
 cd _posts
 touch 2019-08-23-new-post.md
 ```


 Using your favotite text editor create a markdown document. I like [Visual Studio Code](https://code.visualstudio.com/download){:target="_blank"} with vim enabled, edit file using markdown language.
 Visit [Markdown Cheatsheet]( https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf){:target="_blank"} for a quick refresher.



## View Site Locally
Within your site's directory execute jekyll server


``` bash
cd site-name
bundler exec jekyll serve
```

## 
Visit [http://localhost:4000](http://localhost:4000){:target="_blank"} in your favorite web/browser

## Upload Your Site Online
You have many options to upload your site online. Today we will use Github Pages
- Go to [Github.com](https://www.github.com){:target="_blank"} and signup for an account. 
- Then create a new repository. Which is just like a folder that will hold your site. You must add a name, description, and check the box to initialize a README file.
- Go to the repository you created and click on the Settings link.
- Scroll down to the section titled: **GitHub Pages** and under source select *master branch* 
- Go to the repository page and copy the https clone url
- Open your terminal and clone that new repository to your computer
``` bash 
git clone https://github.com/user/reponame.git # link you copied
```
- Move the jekyll files into this new folder
- Add the following lines to the _config.yml file as follows 
> url: user.github.io <br />
baseurl: /reponame

* **Note:** Your local site will now be accessible at [http://localhost:4000/reponame/](http://localhost:4000/reponame/){:target="_blank"}
- Upload your site to Github
``` bash
bundle install
git commit -m 'commit Jekyll site'
git push
```

- Visit your page at [https://user.github.io/reponame]() (inserting your username and reponame accordingly).
Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

