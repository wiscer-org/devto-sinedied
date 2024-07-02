---
title : Linux WSL for Development Environment
tags : wsl, ubuntu, node, nodejs, windows11
published : true
published_at: 2022-11-11 04:00 +0000
description : The benefit of using Linux WSL (Windows Sybsystem for Linux) as development environment. 
id : 1247908
---

## Linux WSL for Development Environment 

WSL, stands for **Windows Subsystem for Linux**, is a sub system within Windows OS allowing users to install one or many Linux distributions.

## Environment Used in this Article

In this article the following environment / applications are used : 
Windows 11, WSL2, Ubuntu 20.04 LTS, Windows Terminal, NVM, and Node.js. 

**This article and all of the videos are made with NVDA screen reader.**
## Flexibility
 
Since I became a screen reader user, due to eye problems, I moved to Windows from Linux Ubuntu. 
I am now depend on Windows based NVDA screen reader to use the computer.
Developing on Windows machines means that there will be different environment between development and deployment machines (mostly Linux).

WSL allows me to have a more 'screen reader friendly' environment (Windows desktop)
while having the same environment with the deployment machines (Linux server).

## Clean Installation

The next benefit of using WSL is that we will have clean installation since all development tools / modules will be on LinuxWSL.
We will have a much more 'clean' Windows installation. 

We can install more than one Linux distributions on one Windows machine.
We can also reset each installed Linux, meaning we can easily have fresh Linux installation on our Windows machine. 
To demonstrate 'clean installation' we will install Node.js on Ubuntu and will reset the Ubuntu as below.

### Install Ubuntu WSL

To show available Linux distros online, open Windows Terminal / Powershell and run :

> wsl --list --online 

To install Ubuntu 20.04 use `-d <NAME>` as below :

> wsl --install -d Ubuntu-20.04

After executing the command above, wait and follow instructions on screen.
Upon completion we need to search for `Ubuntu` in the Windows Start menu and execute the installed Ubuntu.
This will start Ubuntu initialization, and then we will be asked to supply username and password.
Up until this point the Ubuntu installation process has been completed.

To display available wsl commands and options, run command below:

> wsl --help

If you are interested on watching realtime demonstration videos on how to install Ubuntu WSL on Windows 11,
you can listen / watch it on 2 videos below.

<fig>
{% youtube PD1FeVtIpLs %}
<figcaption>Video 1: How to install Ubuntu WSL on Windows 11 (using NVDA). </figcaption>
</fig>

<fig>
{% youtube fGFPUlSPA34 %}
<figcaption>Video 2: How to install Ubuntu WSL on Windows 11 (using NVDA). </figcaption>
</fig>

### Ubuntu Terminal in Windows Terminal

Follow steps below to run Ubuntu Terminal:

1. Run `Windows Terminal`. By default, `Windows Terminal` will run `Powershell`.
2. Press `Ctrl` + `Shift` +`Space` to show list of available CLI applications.
3. Use up and down arrow to focus on 'Ubuntu'. Then press `Enter`.
4. Ubuntu terminal should be opened right now. To test, run `lsb_release -a` to display the Ubuntu version.

<fig>
{% youtube 3d5C2w0NFXk %}
<figcaption>Video: Start Ubuntu WSL Terminal in Windows Terminal (using NVDA)</figcaption>
</fig>

### Install NVM

NVM, stands for Node Version Manager, is a tool to manage Node.js versions in a machine.
NVM can be used to install, remove, and set which version of the currently installed Node.js in a computer.

To install NVM, open Ubuntu Terminal and execute command below.
Command below will pipe the `stdout` from `curl` to `bash`:

> curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash

Visit [NVM Github page][nvm github] for more detail info.
Demonstration video, about how to install NVM, is available below.

### Install Node.js

To test if `nvm` is already installed, run `nvm --version` on your Ubuntu Terminal.
If `nvm` is not recognized by Ubuntu, close the Terminal and try again in a new Terminal.

To install the latest node version, run below command on Ubuntu Terminal.
`node` is an alias for 'node latest version'.
> nvm install node

To install node with a specific version, put he version like below:
> nvm install 14.7.0 

To display list of available downable version of node.js, run:
> nvm ls-remote

I mostly install LTS versions for have a more stable Node.js. To display only LTS versions run :
> nvm ls-remote --lts

To install the latest LTS:
> nvm install 'lts/*'

To install the latest version of a specific codename LTS:
> nvm install lts/hydrogen

The following command can be used to install LTS version:
> nvm install --lts 
> nvm install --lts=argon 
> nvm install 'lts/*' 
> nvm install lts/hydrogen 

To select version of node.js to be used, use the command `use`:
> nvm use 20.04

Up until this point we already have Node.js installed on our Ubuntu WSL. That means we can develop apps in Linux environment on our Windows machine. If you are using VSCode as IDE, you can install extension to access WSL system file.

This is only a demo of using Linux WSL as our development environment. 
We can also install other tools for other programming languages.

<fig >
{% youtube uYkNbdxf1Co %}
<figcaption>Video: How to Install NVm (Node Version Manager) and Node.js in Windows 11</figcaption>
</fig>

### Reset Ubuntu

Once we feel to have a clean dev environment, we can reset the Ubuntu from start. After reset the Ubuntu we will be prompted to input username and password again before start using Ubuntu.

Follow steps below to reset Ubuntu:
1. On Windows, search and open `Settings`.
2. On the navigation (left side) use up/down arrow to select `Apps` and then press `Enter`.
3. Press `Tab` to move focus to selected `Apps` section.
4. Press `Tab` to move focus to `Apps and Features` then press `Enter`.
5. Press `Tab` several times until find `Apps list`, which contains list of applications. Prior to the Apps list there is a search box to filter the apps.
6. Use up / down arrow to look for 'Ubuntu' app.
7. Press `Tab` once to focus on the overflow button.
8. Press `Enter` on the `Advanced Options`.
9. Press `Tab` multiple times to move focus to `Reset grouping`. Afterward press `Tab` 2 more times to focus on the `Reset` button, then press `Enter`.
10. After Ubuntu app has been reset, go to `Windows Start Menu` to search and run the Ubuntu app.
12. Run the Ubuntu app then provide the prompted username and password. Ubuntu is now ready to be used again from the fresh start. 

<fig>
{% youtube elf4y2MdKb8 %}
<figcaption>Video: Reset Ubuntu WSL in Windows 11 using NVDA</figcaption>
</fig>



## Conclusion and Docker

WSL, Windows Subsystem for Linux, is a breakthrough technology for developers to have multiple and different ecosystem in one machine.
This option is much practical for software developers compare to use technology such as virtual machine,
since developers mostly only want separation  down to OS layer and no separation required onn physical layers (memory allocation).

Next, we are going to install Docker wich offers more portability and modularity.
Docker natively runs on Linux. That is why we need to install WSL prior to installing Docker in Windows.

Hope this post useful. Cheers!


[nvm github]: https://github.com/nvm-sh/nvm

