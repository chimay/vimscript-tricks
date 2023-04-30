<!-- vim: set filetype=markdown: -->

<!-- vim-markdown-toc GFM -->

* [Introduction](#introduction)
* [Installation](#installation)
    * [Using vim-packager](#using-vim-packager)
    * [Using minpac](#using-minpac)
    * [Using vim-plug](#using-vim-plug)
    * [Cloning the repo in a pack-start directory](#cloning-the-repo-in-a-pack-start-directory)
* [Usage](#usage)

<!-- vim-markdown-toc -->

# Introduction

VimL is full of features, but sometimes it is hard to find which function
or command will do the job you want.

If you ever searched the web for `vim script ex command output in a var`,
you surely have had results talking about `:redir`. This is ok, but
there is a more elegant solution for this particular problem.

This (neo)vim help page collects vim script snippets, whose some were
hard to find. You may already know some of them, and I hope you will
gladly discover the others.

# Installation
## Using vim-packager

Simply add this line after `packager#init()` to your initialisation file :

~~~vim
call packager#add('chimay/vimscript-tricks', { 'type' : 'start' })
~~~

and run `:PackagerInstall` (see the
[vim-packager readme](https://github.com/kristijanhusak/vim-packager)).

## Using minpac

Simply add this line after `minpac#init()` to your initialisation file :

~~~vim
call minpac#add('chimay/vimscript-tricks', { 'type' : 'start' })
~~~

and run `:PackUpdate` (see the
[minpac readme](https://github.com/k-takata/minpac)).

## Using vim-plug

The syntax should be similar with other git oriented plugin managers :

~~~vim
Plug 'chimay/vimscript-tricks'
~~~

and run `:PlugInstall` to install.

## Cloning the repo in a pack-start directory

You can clone the repository somewhere in your `runtime-search-path`. You
can get a minimal version by asking a shallow clone (depth 1) and
filtering out the screenshots blobs :

```vim
mkdir -p ~/.local/share/nvim/site/pack/foo/start
cd ~/.local/share/nvim/site/pack/foo/start
git clone --depth 1 --filter=blob:none https://github.com/chimay/vimscript-tricks
```

# Usage

Straightforward :

```vim
:help vimscript-tricks
```

Don't forget to run :

```vim
:helptags doc
```

to be able to use the inline help.
