---
title: "How to Download and Install JDK 11 on Windows"
permalink: /download-install-jdk-11-windows.html
excerpt: "A detailed step-by-step tutorial on how to download and install JDK 1.11 on Windows 10."
date: 2018-09-29
last_modified_at: 2018-09-29
header:
  teaser: "assets/images/posts/development/jdk/download-install-jdk-11-windows.png"
categories: [Development]
tags: [Download, Install, JDK, Setup, Tutorial, Windows]
published: true
---

<img src="{{ site.url }}/assets/images/posts/development/jdk/download-install-jdk-11-windows.png" alt="download install jdk 11 windows" class="align-right title-image">

In this guide, I’m going to show you exactly **how to download and install JDK 11 on Windows**.

(Step-by-step)

First, I’ll show you where you can get JDK 11.

Then you’ll see how to configure it.

And finally **how to verify if everything is working**.

Let’s dive right in…

Check following post if you are looking to download and install [JDK 1.5]({{ site.url }}/download-install-jdk-5-windows.html), [JDK 1.6]({{ site.url }}/download-install-jdk-6-windows.html), [JDK 1.7]({{ site.url }}/download-install-jdk-7-windows.html), [JDK 1.8]({{ site.url }}/download-install-jdk-8-windows.html) or [JDK 10]({{ site.url }}/download-install-jdk-10-windows.html).
{: .notice--primary}

## What is a JDK?

When you want to create a Java application you need a [Java Development Kit](https://en.wikipedia.org/wiki/Java_Development_Kit){:target="_blank"} (JDK). It contains tools that allow you to develop and run your Java program.

<img src="{{ site.url }}/assets/images/posts/development/jdk/what-is-a-jdk.png" alt="what is a jdk">

One of these tools is a **compiler** (javac) that converts Java source code (`.java` files) into Java bytecode (`.class` files). Other tools include an archiver (jar) and a documentation generator (javadoc).

The JDK also contains a **Java Runtime Environment** (JRE) that is able to run compiled Java code. To do this the JRE uses Java libraries and a Java Virtual Machine (JVM) that executes the compiled Java code.

## Step #1: Download

There are [several Java packages](https://docs.oracle.com/javaee/6/firstcup/doc/gkhoy.html){:target="_blank"} available. In this tutorial, we will install the Java Standard Edition (SE).

Head over to the [Oracle Java download page](http://www.oracle.com/technetwork/java/javase/downloads/index.html){:target="_blank"}.

Look for the `Java SE 11 (LTS)` section.

> Starting with Java 9, Oracle introduced a new support model. Versions tagged as LTS (long-term support) will receive support for 3 years. Non-LTS versions will be out of support as soon as a new major version is released.

Click on the `Download` button right below `Oracle JDK`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-download-java-se.png" alt="jdk 11 download java se">

Click on the radio button next to `Accept License Agreement`.

Click on the Windows download link: `jdk-11_windows-x64_bin.exe`.

> Note that as from version 9, Oracle no longer provides 32-bit JDK builds.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-download-java-se-windows-binary.png" alt="jdk 11 download java se windows binary">

Wait for the download to complete.

## Step #2: Install

Open the location of the downloaded executable.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-downloaded-installer.png" alt="jdk 11 downloaded installer">

Double-click it to run the installer.

On Windows 10 a pop-up window will appear: `The app you're trying to install isn't a verified app from the Store`

Click on `Install anyway`.

<img src="{{ site.url }}/assets/images/posts/windows-10-install-app-not-in-store.png" alt="windows 10 install app not in store">

The JDK installer will start. Click `Next`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-installer-start.png" alt="jdk 11 installer start">

You can change the installation location by clicking on the `Change…` button.

In this example, we keep the default install location of `C:\Program Files\Java\jdk-11\`. From now on we will refer to this directory as `[JAVA_INSTALL_DIR]`.

Click `Next` to start the installation.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-installer-default-location.png" alt="jdk 11 installer default location">

The JDK installation will now start.

A progress bar shows the various steps that are executed.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-installer-progress.png" alt="jdk 11 installer progress">

Once the installation is complete, click `Close`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-installer-complete.png" alt="jdk 11 installer complete">

## Step #3: Setup

We need to set up an environment variable that will point to our JDK installation.

Click on the search button. Then type "<kbd>env</kbd>" (without quotes).

> On Windows 7 click on the Windows button.

Click on the `Edit environment variables for your account` shortcut.

<img src="{{ site.url }}/assets/images/posts/development/windows-search-env.png" alt="windows search env">

Wait for the environment variables window to open.

Click on `New…`.

<img src="{{ site.url }}/assets/images/posts/development/windows-account-environment-variables-new.png" alt="windows account environment variables new">

Enter "<kbd>JAVA_HOME</kbd>" as variable name. Enter the `[JAVA_INSTALL_DIR]` as variable value.

In this tutorial, the Java installation directory is `C:\Program Files\Java\jdk-11`.

Click `OK`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-home-variable.png" alt="jdk 11 home variable">

Next, we need to configure the PATH environment variable so we can run Java from a command prompt.

Select the `Path` variable. Click on `Edit…`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-edit-path-variable.png" alt="jdk 11 edit path variable">

Click on `New` and type "<kbd>%JAVA_HOME%\bin</kbd>" as shown below.

Click `OK`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-edit-path-variable-add-java-home.png" alt="jdk edit path variable add java home">

Click `OK` once more to close the environment variables window.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-windows-account-environment-variables.png" alt="jdk 11 windows account environment variables">

> If a `Path` variable does not exist you need to create it. Use "<kbd>Path</kbd>" as variable name and "<kbd>%JAVA_HOME%\bin</kbd>" as variable value.

> On Windows 7 you cannot add extra values for an existing `Path` variable. You need to append "<kbd>;%JAVA_HOME%\bin</kbd>" at the end of the variable value instead.

## Step #4: Test

Let's test the setup.

Click on the search button. Then type "<kbd>cmd</kbd>" (without quotes).

Click on the `Command Prompt` shortcut.

<img src="{{ site.url }}/assets/images/posts/development/windows-search-cmd.png" alt="windows search cmd">

Wait for the command prompt to open.

Type "<kbd>java -version</kbd>" and press `ENTER`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-version-command.png" alt="jdk version command">

The above command prints the installed JDK version: `11`.

<img src="{{ site.url }}/assets/images/posts/development/jdk/jdk-11-version-output.png" alt="jdk 11 version output">

**Congratulations, you have installed JDK 1.11 on Windows 10!**

Now take the next step and [write your first Java program](https://introcs.cs.princeton.edu/java/11hello/){:target="_blank"}.

Leave a comment if you liked this post.

Thanks!