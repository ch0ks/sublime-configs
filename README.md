# Ch0ks' Sublime Text 3 Configuration Sync

<!-- MarkdownTOC -->

1. [Introduction](#introduction)
1. [How It Works](#how-it-works)
1. [Installation](#installation)
1. [Syncronization](#syncronization)
1. [Troubleshoot](#troubleshoot)

<!-- /MarkdownTOC -->

<a id="introduction"></a>
## Introduction

The purpose of this respotiroy is to keep my Sublime Text 3 configuration files so I can syncronize it through all my laptops where I code.

feel free to fork and submit your changes, I am always open to test new things.

<a id="how-it-works"></a>
## How It Works

Sublime Text 3 keeps all its configuration files in a unique folder. Depending on your operating system, this folder is located in:

* Linux: ~/.config/sublime-text-3
* OS X: ~/Library/Application Support/Sublime Text 3
* Windows: %APPDATA%\Sublime Text 3

<a id="installation"></a>
## Installation

To install this configuration files and keep them updated do the following.

First kill all instances of Sublime Text 3, now run the command depending on your Operating System.

**OS X**

```
ln -s "/PATH/To/Repo/Sublime Text 3" "~/Library/Application Support/Sublime Text 3"
```

**Linux**

```
ln -s "/PATH/To/Repo/Sublime Text 3" "~/.config/sublime-text-3"
```

**Windows**

```
$ mklink /J  "C:\PATH\To\Repo\Sublime Text 3" "%APPDATA%\Sublime Text 3"
```

Start Sublime 3 Text. It will take a little bit longer because it is recreating the cache.

<a id="syncronization"></a>
## Syncronization

Let's say that you made some changes on your current configuration and want it to be reflected in your other computers. So run the following commands:

**Current Computer**

Change to the directory where the repository is stored.

`` $ cd /PATH/To/Repo/``

Sync with the remote repository to the latest version.

``$ git pull``

If everything went well then there should be no conflicts. Now we add whatever new files we installed and commit the code.

```
$ git add *
$ git commit -am "Latest version as of today"
$ git push
```

Now the latest version is sitting in github. Now we synchronize the new version in the other computer.

**Second Computer**

Follow these steps if you have already installed the files in this computer. If not follow the steps in the Installation section.

Close all instances of Sublime Text 3, change to the directory where the repository is stored and run the following commands:

```
$ cd /PATH/To/Repo/
$ git pull
```

Now start Sublime Text 3 as always, it can take a little longer because of the cache recreation.

<a id="troubleshoot"></a>
## Troubleshoot

If everything fails or your Sublime Text 3 configuration files got corrupted, DO NOT SYNC to the latest version, instead just delete the current repository folder and follow the steps in the Installation section.
