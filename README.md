Page, a static website generator
================================
[![Tests](https://github.com/fmalina/page/actions/workflows/ci.yml/badge.svg)](https://github.com/fmalina/page/actions?query=event%3Apush+branch%3Amain+workflow%3Atests)

![website = compile(markdown content, templates)](page.png)

- creates a well organized website with clear navigation
  reflecting the folder structure of source text documents
- fast, well compressed, mobile friendly pages
- feed and sitemap files for your subscribers and search engines
- import from any CMS DB (inc. Wordpress), import HTML sites

Writers love distraction free conventional plain text
[formatting](https://commonmark.org/help/).
Template designers love the easy to read, beautiful and powerful
[template language](https://palletsprojects.com/p/jinja/).

Installation and run
--------------------
Page is a small command line program written in Python programming language.
It requires [python installed](https://www.python.org/downloads/), which lets user
install Page on any platform in a single command.

    pip install page

By default, Page will collect all text files in current folder
and create a HTML website in a static folder using default templates. Run the program

    page

it will look for a config file
[`./page.yml`](https://github.com/fmalina/page/blob/main/page.yml)
with custom options.

    source: /markdown/source/folder/
    target: /target/folder/
    tpl: /custom/template/folder/
    ext: ''  # or '.htm'
    ctx:
        site_name: 'My Site'
        site_url: https://example.org


Batteries included
------------------
Minimal default template.

Page has lots of tests including one importing an existing HTML site,
converting it to source markdown files and then back into a static HTML site
in full circle. This code can inspire users to convert existing static site
or one powered by a slow Content Management System to simple
markdown powered static site and maintain it with Page.

Static cache generation helpers provided for Django.

