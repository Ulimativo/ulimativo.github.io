+++
title = 'Local Setup'
date = 2023-11-19T18:57:00+01:00
draft = false
tags = ["github", "localdev"]
description = "How to set the website up as this very Github page."
ShowWordCount = true
+++

# Introduction

The page you're looking at right now is based on [Hugo](https://gohugo.io) and pushed via Git to Github Pages.

I found out about Hugo just recently and am still learning, but first results were very promising.

So this blog post is by no means a tutorial, but rather a collection of how I set it up and some thoughts along the way. And of course boosting my markup skills :smirk:

# The Setup

## Install Hugo & Basic Setup


I installed Hugo on my Macbook Air[^1] through [Homebrew](https://brew.sh).

`brew install hugo`

Then I created a hugo project setup using

`hugo new site . --force`

I used the `--force` flag as the directory was already setup as a git repository.

The created file structure looks as follows:

```shell
.
├── archetypes
├── assets
├── content
├── data
├── docs
├── hugo.toml
├── i18n
├── layouts
├── static
└── themes
```


~~What I find quite curious is that I was not able to change the configuration file format from `toml` to `yml` which I like much more for the better readability. But also my Google and Hugo Doc search was not too deep.~~

**Edit**: According to the docs, it seems Hugo is accessing the different config files in a certain order (1. TOML, 2. YAML, etc). Need to try that.

For a first test run I launched the local server with `hugo server -D`. The `-D`flag is used to include draft pages.

## The First Page

Used `hugo new content posts/my-first-post.md` to create a first page including Frontmatter for my blog.

And that was is for the very basics. I'm quite impressed. 4 commands and I have a blog with a first post ready to go. 


[^1]: I also tried on my Linux server, which worked just as well, but found it more convenient to have a local copy instead of remote development.