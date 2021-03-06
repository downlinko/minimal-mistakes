---
title: "Download and Install Python 3.4 on Windows"
permalink: /download-install-python-3-4-windows.html
excerpt: "A detailed step-by-step tutorial on how to download and install Python 3.4.4 on Windows 10."
date: 2018-08-09
last_modified_at: 2018-08-09
header:
  teaser: "assets/images/posts/development/python/download-install-python-3-4-windows.png"
categories: [Development]
tags: [Download, Install, Python, Setup, Tutorial, Windows]
published: true
---

<img src="{{ site.url }}/assets/images/posts/development/python/download-install-python-3-4-windows.png" alt="download install python 3-4 windows" class="align-right title-image">

This is a complete guide to download and install [Python](https://www.python.org){:target="_blank"} 3.4 on Windows.

So if you **want to know how to set up Python**, you’ll love the step-by-step approach in this tutorial.

We’ve got a couple of items to cover.

Let’s get started.

Check following post if you are looking to download and install [Python 2.7]({{ site.url }}/download-install-python-2-7-windows.html).
{: .notice--primary}

## Step #1: Download

Head over to the [Python downloads page](https://www.python.org/downloads/){:target="_blank"}.

<img src="{{ site.url }}/assets/images/posts/development/python/python-download-page.png" alt="python-download-page">

Scroll down to the `Looking for a specific release?` section.

Look for the `Python 3.4.4` entry in the list. This is the last official binary installer released for version 3.4.

Click on `Download`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-specific-release-section.png" alt="python 3-4-4 specific release section">

Scroll down until the `Files` section.

[Check your windows bit version]({{ site.url }}/windows-10-bit-version-check.html) and click on the corresponding link:

* For 32-bit = Windows <kbd>x86</kbd> MSI installer
* For 64-bit = Windows <kbd>x86-64</kbd> MSI installer

In this guide, we will install the 64-bit version. So we click on `Windows x86-64 MSI installer`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-windows-installer.png" alt="python 3-4-4 windows installer">

Wait for the download to complete.

> Do you want to skip the above steps? Here is the direct link to download the [32 bit](https://www.python.org/ftp/python/3.4.4/python-3.4.4.msi){:target="_blank"} or [64 bit](https://www.python.org/ftp/python/3.4.4/python-3.4.4.amd64.msi){:target="_blank"} Python 3.4.4 installer for Windows.

## Step #2: Install

Open the location of the downloaded installer.

Double-click the installer to start the installation.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-downloaded-installer.png" alt="python 3-4-4 downloaded installer">

On Windows 10 a pop-up window will appear: `The app you're trying to install isn't a verified app from the Store`

Click on `Install anyway`.

<img src="{{ site.url }}/assets/images/posts/windows-10-install-app-not-in-store.png" alt="windows 10 install app not in store">

The Python installer setup screen will open.

Leave the `Install for all users` radio button selected.

Click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-installer-start.png" alt="python 3-4-4 installer start">

You can change the installation location by clicking on the `Change…` button.

In this example, we keep the default install location of `C:\Python34`. From now on we will refer to this directory as `[PYTHON_INSTALL_DIR]`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-installer-select-destination.png" alt="python 3-4-4 installer select destination">

We keep the default Python features.

Click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-installer-customize.png" alt="python 3-4-4 installer customize">

The Python installation will now start.

A progress bar shows the various steps that are executed.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-installation-progress.png" alt="python 3-4-4 installation progress">

Once the installation is complete, click `Finish`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-installer-complete.png" alt="python-3-4-4-installer-complete">

## Step #3: Setup

We need to set up an environment variable that will point to our Python installation.

Click on the search button. Then type "<kbd>env</kbd>".

> If you have Windows 7 click on the Windows button.

Click on the `Edit environment variables for your account` shortcut.

<img src="{{ site.url }}/assets/images/posts/development/windows-search-env.png" alt="windows search env">

Wait for the environment variables window to open.

Click on `New…`.

<img src="{{ site.url }}/assets/images/posts/development/windows-account-environment-variables-new.png" alt="windows account environment variables new">

Enter "<kbd>PYTHONPATH</kbd>" as variable name. Enter the `[PYTHON_INSTALL_DIR]` as variable value.

In this tutorial, the installation directory is `C:\Python34`.

Click `OK`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-home-variable.png" alt="python 3-4-4 home variable">

Next, we need to configure the PATH environment variable so we can run Python from a command prompt.

Select the `PATH` variable. Click on `Edit…`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-edit-path-variable.png" alt="python 3-4-4 edit path variable">

Click on `New` and type "<kbd>%PYTHONPATH%\bin</kbd>" as shown below.

Click `OK`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-path-variable.png" alt="python path variable">

Click `OK` once more to close the environment variables window.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-windows-account-environment-variables.png" alt="python 3-4-4 windows account environment variables">

> On Windows 7 you cannot add extra values for an existing `Path` variable. You need to append "<kbd>;%PYTHONPATH%</kbd>" at the end of the variable value instead.

## Step #4: Test

To test the setup click on the search button. Then type "<kbd>cmd</kbd>".

Click on the `Command Prompt` shortcut.

<img src="{{ site.url }}/assets/images/posts/development/windows-search-cmd.png" alt="windows search cmd">

Wait for the command prompt to open.

Type "<kbd>python -V</kbd>" and press `ENTER`.

<img src="{{ site.url }}/assets/images/posts/development/python/python-version-command.png" alt="python version command">

The above command prints the installed Python version: 3.4.4.

<img src="{{ site.url }}/assets/images/posts/development/python/python-3-4-4-version-output.png" alt="python 3-4-4 version output">

**Congratulations, you have installed Python 3.4.4 on Windows 10!**

Good luck and leave a comment if you liked this post.

Thanks!
