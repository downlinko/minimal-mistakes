---
title: "How to Download and Install GitHub Desktop on Windows"
permalink: /download-install-github-desktop-windows.html
excerpt: "A quick step-by-step tutorial on how to download and install GitHub Desktop on Windows 10."
date: 2018-09-25
last_modified_at: 2018-09-25
header:
  teaser: "assets/images/posts/development/git/download-install-github-desktop-windows.png"
categories: [Development]
tags: [Download, GitHub Desktop, Install, Setup, Tutorial, Windows]
published: false
---

<img src="{{ site.url }}/assets/images/posts/development/git/download-install-github-desktop-windows.png" alt="download install github desktop windows" class="align-right title-image">

Do you want to download and install [GitHub Desktop](https://desktop.github.com/){:target="_blank"} on Windows?

You’ve reached the right place.

Because in this tutorial **I'll show you the different setup steps**.

So let’s get busy!

## What is GitHub Desktop?

[GitHub Desktop](https://en.wikipedia.org/wiki/Git){:target="_blank"} is an open source [Electron](https://electronjs.org/){:target="_blank"}-based desktop application.

Linus Torvalds created Git. Its current maintainer since 2005 is Junio Hamano.

## Step #1: Download

Head over to the [Git downloads page](https://git-scm.com/download){:target="_blank"}.

Click on the `Download X.X.X for Windows` button.

At the time of writing the latest Git release was version: `2.18.0`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-download-installer.png" alt="git download installer">

Wait for the download to complete.

## Step #2: Install

Open the location of the downloaded executable.

<img src="{{ site.url }}/assets/images/posts/development/git/git-downloaded-installer.png" alt="git downloaded installer">

In this tutorial, we install Git only for the current user. Double-click the installer to start the setup.

> You can install Git for your current user account or for all users on the system. For the last option, you need to run the installer with administrative privileges. To do this on Windows, right click on the executable and select `Run as administrator`.

On Windows 10 a pop-up window will appear: `The app you're trying to install isn't a verified app from the Store`

Click on `Install anyway`.

<img src="{{ site.url }}/assets/images/posts/windows-10-install-app-not-in-store.png" alt="windows 10 install app not in store">

The installer setup wizard will open.

Click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-license.png" alt="git installer license">

The default install location is the user home folder. This is because we install Git for the current user.

Leave the default suggested location and click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-destination-location.png" alt="git installer destination location">

Keep the default selection of components and click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-select-components.png" alt="git installer select components">

Keep the default start menu folder and click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-select-components.png" alt="git installer select components">

Some Git commands will launch a text editor to prompt for further input. You can use the drop-down select the editor you would like Git to use.

> Note that you can always [change the default text editor Git uses](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup#_your_editor){:target="_blank"} at a later point.

In this guide, we keep the default editor (Vim) that ships with Git. Click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-default-editor.png" alt="git installer default editor">

To use Git from a Windows command prompt it needs to be added it to your environment `PATH` variable.

Select the `Use Git from the Windows Command Prompt` option and click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-configure-path-variable.png" alt="git installer configure path variable">

Keep the default `Use the OpenSSL library` option selected and click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-https-transport.png" alt="git installer https transport">

Different operating systems use different character(s) to represent the end of a line. Git uses these characters to compare files. As a result, it may cause unexpected issues when you edit a file on different machines.

To avoid this keep the recommended setting which is the first option: `Checkout Windows-style, commit Unix-style line endings`.

Click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-line-endings.png" alt="git installer line endings">

Keep the default terminal emulator for Git Bash (MinTTY) and click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-terminal-emulator.png" alt="git installer terminal emulator">

Leave the selection of extra options untouched.

Click `Install` to start the installation.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-extra-options.png" alt="git installer extra options">

The Git installation will now start.

A progress bar shows the various steps that are executed.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-progress.png" alt="git installer progress">

Once the installation is complete, click `Finish`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-installer-finish.png" alt="git installer finish">

## Step #3: Test

To test the setup click on the search button. Then type "<kbd>cmd</kbd>".

Click on the `Command Prompt` shortcut.

<img src="{{ site.url }}/assets/images/posts/development/windows-search-cmd.png" alt="windows search cmd">

Wait for the command prompt to open.

Type "<kbd>git --version</kbd>" and press `ENTER`.

<img src="{{ site.url }}/assets/images/posts/development/git/git-version-command.png" alt="git version command">

The above command prints the installed Git version.

<img src="{{ site.url }}/assets/images/posts/development/git/git-version-output.png" alt="git version output">

**Congratulations, you have installed Git on Windows 10!**

Now it's time [to perform a first-time Git setup](https://www.codebasehq.com/blog/using-git-on-windows#configuring-git){:target="_blank"}.

If you enjoyed this guide leave a short message below.

Thanks!
