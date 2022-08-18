# Local Gov IMS Website

This is the repository for the website that lives at https://www.localgovims.digital.

## Table of contents

* Introduction
* Requirements
* Installation
* Configuration

## Introduction

The code here is intended to be used with the static site generator Jekyll. 

To work with the code, you can clone this repository into your own development environment and run jekyll serve. Jekyll will compile the site locally for you and present it at https://127.0.0.1:4000 to view. As you make changes to the code using your favourite IDE, you'll see those reflected on that URL.

When you're happy with your changes, you can commit them and push them back into this repository. This repository is set up such that GitHub will automatically recompile it's contents using Jekyll when changes are made to the main branch. That recompiling will create a fresh copy of the website and present it at https://www.localgovims.digital.

## Requirements

Jekyll must be installed on your machine to compile and view the website generated locally. For instructions on how to do this, please see [https://jekyllrb.com/](https://jekyllrb.com/).

You'll also need an IDE to run and edit the code. Visual Studio Code is a great option that can be downloaded from [https://code.visualstudio.com/](https://code.visualstudio.com/).

## Installation

TBC

## Configuration

Use the file _config.yml to change the way Jekyll compiles the code in this repository. You'll see it includes a bunch of key/value pairs that you can change. These are "site" level variables. You can add any new ones you'd like and reference those in webpages using {{ site.key }} as placeholders - at compile time those will be replaced with values.

Beyond that, webpages and directories are setup as markdown files in a typical folder/file structure, e.g. index.md, about/us.md. Each markdown file has a yaml section at the top that contains key/value pairs. The are page level variables. You can add your own and reference them in webpages using {{ page.key }} but to begin with we have:

* layout: The parent page into which its content should be injected. Layout files can be found in the _layouts folder and can parent each other.
* title: The title of the page to show in the visible page when rendered
* navTitle: The title of the page as it appears in the navigation menu and browser title
* description: The content to put in the meta description tag. Defaults to {{ page.excerpt }} (a reserved variable) if not provided.
* keywords: The content to put in the meta keywords tag. Defaults to {{ site.keywords }} if not provided.
* author: The content to put in the meta author tag. Defaults to {{ site.organisation }} if not provided.
