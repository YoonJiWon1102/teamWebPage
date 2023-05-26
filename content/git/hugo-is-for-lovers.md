+++
title = "Hugo is for lovers"
date = "2015-08-03T13:39:46+02:00"
tags = ["hugo"]
categories = ["pseudo"]
banner = "img/banners/banner-3.jpg"
summary="This is the summary Goto [hugo releases](https://github.com/spf13/hugo/releases) and download the appropriate version for your os and architecture. Save it somewhere specific as we will be using it in the next step. More complete instructions are available at [installing hugo](/overview/installing/)"
+++

## What is branch? 
다른 작업에 영향을 받지 않고 독립적으로 작업을 하기 위한 개념.
여러 작업을 동시에 하기 편함.


## How to create a branch?

Follow the following steps:

 1. Clone the [hugo repository](http://github.com/spf13/hugo)
 2. Go into the repo
 3. Run hugo in server mode and build the docs
 4. Open your browser to http://localhost:1313

Follow the following steps:
 1. 원격에서 브랜치 만들기
    1. 깃허브에서 브랜치 만들기
    2. git fetch -p
    3. git checkout <브랜치 이름>
 2. 로컬에서 브랜치 만들고 원격에 올리기
    1. git branch <브랜치 이름>
    2. git checkout <브랜치 이름>
    3. git push <원격><브랜치 이름>
    4. git branch -a
 

Corresponding pseudo commands:

    git clone https://github.com/spf13/hugo
    cd hugo
    /path/to/where/you/installed/hugo server --source=./docs
    > 29 pages created
    > 0 tags index created
    > in 27 ms
    > Web Server is available at http://localhost:1313
    > Press ctrl+c to stop

Once you've gotten here, follow along the rest of this page on your local build.

## Step 3. Change the docs site

Stop the Hugo process by hitting ctrl+c.

Now we are going to run hugo again, but this time with hugo in watch mode.

    /path/to/hugo/from/step/1/hugo server --source=./docs --watch
    > 29 pages created
    > 0 tags index created
    > in 27 ms
    > Web Server is available at http://localhost:1313
    > Watching for changes in /Users/spf13/Code/hugo/docs/content
    > Press ctrl+c to stop


Open your [favorite editor](http://vim.spf13.com) and change one of the source
content pages. How about changing this very file to *fix the typo*. How about changing this very file to *fix the typo*.

Content files are found in `docs/content/`. Unless otherwise specified, files
are located at the same relative location as the url, in our case
`docs/content/overview/quickstart.md`.

Change and save this file.. Notice what happened in your terminal.

    > Change detected, rebuilding site

    > 29 pages created
    > 0 tags index created
    > in 26 ms

Refresh the browser and observe that the typo is now fixed.

Notice how quick that was. Try to refresh the site before it's finished building.. I double dare you.
Having nearly instant feedback enables you to have your creativity flow without waiting for long builds.

## Step 4. Have fun

The best way to learn something is to play with it.
