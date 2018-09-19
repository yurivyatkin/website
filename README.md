# John Butcher's website

## Introduction

This project is an attempt to replace the current Drupal-based website at [http://jcbutcher.com](http://jcbutcher.com) with a static website hosted on Netlify.com. It is not finished yet, but the the changes are coming soon, and the website will be redirected to Netlify in the nearest future.

In the meantime, this website is avaliable at https://jcbutcher.netlify.com/.

## Project management

The project is managed in this [Trello board](https://trello.com/b/hs9JZPJ1/website).


## Technology

1. Obviously, this is a [Git](https://git-scm.com/) repository, hosted on [Github](https://github.com/). Git is a version control system, used not only for software development, but in many other areas, where having a history of changes in collections of text files is beneficial. Github is a popular service for hosting (storing) remote (online) copies of Git-enabled projects (repositories). 

2. This project uses [Jekyll](https://jekyllrb.com/) as a [static website](https://www.netlify.com/blog/2016/05/18/9-reasons-your-site-should-be-static/) generator. Jekyll is a [Ruby](https://www.ruby-lang.org/en/) (a beautiful programming language) [gem](https://rubygems.org/) (a piece of software). Jekyll requires a [decent](https://jekyllrb.com/docs/installation/) version of Ruby to be installed on the system, on which it is supposed to run. The good news is that essentially any modern operating system will do, but using a [Mac computer](https://jekyllrb.com/docs/installation/macos/) has some benefits, such as easy-to-use package managers (e.g. [Homebrew](https://brew.sh/)).

3. A usable and nice looking layout for this website is provided by [Hyde](http://hyde.getpoole.com/), a popular Jekyll theme, which is totally awesome for individuals.

4. [Kramdown](https://kramdown.gettalong.org/index.html) is used as a parser for (a dialect of) Markdown. [Markdown](https://daringfireball.net/projects/markdown/) is a markup language, which is supposed to compile into HTML (the barebone language for web browsers). The files with Kramdown content have the extension `*.md`, the same as usual Markdown files do.

5. Kramdown has a nice support for insets written in [LaTeX](https://www.latex-project.org/) (via enabling [MathJax](https://www.mathjax.org/), for example), which makes it a popular choice for mathematically challenged developers (a joke, a joke...).

6. Jekyll can also compile [SASS](https://sass-lang.com/) into plain CSS, thus giving powerful tools for styling the website with unlimited possibilities. In order to repel the uninitiated, SASS files have `*.scss` extension.

7. This project has been bootstrapped with [Jekyll Boylerplate](https://github.com/HugoGiraudel/jekyll-boilerplate) by [Hugo Giraudel](https://twitter.com/HugoGiraudel).


## How to run this project locally

### Install Git

First of all, make sure that [Git](https://git-scm.com/) is installed onto your system. Here are [some instructions](https://gist.github.com/derhuerst/1b15ff4652a867391f03) on how to do this on a variety of systems.

### Clone the repository

Choose a separate folder for your website projects, and open it in a terminal. In this folder run the following command (the dollar sign `$` stands for the terminal prompt, which varies from system to system, and is not a part of the command):

```
$ git clone git@github.com:jcbutcher/website.git
```
After this command completes successfully, you may enter the folder by issuing
```
$ cd website
```
in the terminal.

### Install dependencies

Inside the 'website' folder, run 
```
$ bundle install
```
This command will read 'Gemfile.lock' (or, if it is not found, 'Gemfile') file and install all the pieces of software ("dependencies"), that are necessary to run Jekyll (with the extensions, configured within the project). 
If this command fails with errors, make sure that you have adequate versions of Ruby, Bundler and Jekyll installed (see the details [here]((https://jekyllrb.com/docs/installation/)).
Googling the error messages is the most efficient way to pin down the issues.

### Run the development server

Jekyll makes it easy to run a local copy of the website by issuing the command:

```
$ bundle exec jekyll serve
```

The `bundle exec` part ensures that the dependencies are taken from the project's 'Gemfile.lock'. In may cases this prefix may be safely omitted, and just `jekyll serve` will do. There is even shorter version of this command: `jekyll s`.

If this command runs successfully, it will show the link at which the local copy of the website can be opened in the browser. Usually, this is [http://localhost:4000](http://localhost:4000).

## How to make changes.

The project mainly consists of plain text files, with the exception of images, that may be binary files, of course. This means that any text editor will be good enough for making small changes, but for a convenient workflow a modern code editor would be a better choice. [Visual Studio Code](https://code.visualstudio.com/) is highly recommended (and free!)

Jekyll is simple enough but it still requires some time to get familiar with its concepts. Thomas Bradley created a great [video course](https://www.youtube.com/playlist?list=PLWjCJDeWfDdfVEcLGAfdJn_HXyM4Y7_k-) which can make getting started a pleasant journey.

## How to deploy this to production

If you are (the real) [John Charles Butcher](https://en.wikipedia.org/wiki/John_C._Butcher), then everything is already configured for you, and pushing commits to the repository will trigger automatic builds thanks to Netlify's magic.

In other cases, pressing the button below could be the easites way to go:

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/jcbutcher/website)

If you want to go an extra mile, then do the following steps:

- create an account on [Netlify.com](https://www.netlify.com) (using your Github account, obtained earlier, will simplify this task);
- install [Netlify-CLI](https://github.com/netlify/cli) following the instructions in the link;
- run `netlify login` and privide the required credentials to connect your computer to Netlify;
- check that everything is all right: `netlify status`.

More information can be found in [this article](https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/).


## How to contribute

Open an issue, (find a solution), and (or) make a pull request!


## License

MIT

