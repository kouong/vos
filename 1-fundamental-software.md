# Setup guide for a development machine on Windows

This file contains the **Fundamental Software** section of my [Setup guide for a development machine on Windows](https://github.com/EnduranceCode/windows-development-machine). The introduction to this guide as well as its full *Table of Contents* can be found on the [README.md](./README.md) file of this repository. The *Table of Contents* of this section is listed below.

## Table of Contents

1. [Fundamental Software](#1-fundamental-software)
    1. [Google Chrome](#11-google-chrome)
    2. [KeePassXC](#12-keepassxc)
    3. [Windows Subsystem for Linux](#13-windows-subsystem-for-linux)
    4. [Windows Terminal](#14-windows-terminal)
    5. [Chocolatey](#15-chocolatey)
    6. [Project specific software and tools](#16-project-specific-software-and-tools)
        1. [BMW Root Certificate](#161-install-bmw-root-certificate)

## 1. Fundamental Software

[**Google Chrome**](https://www.google.com/chrome/) is a cross-platform web browser developed by [Google](https://en.wikipedia.org/wiki/Google). With [Lubuntu](https://lubuntu.me) I normally choose [Firefox](https://www.mozilla.org/firefox/new/) but on Windows I normally use [**Google Chrome**](https://www.google.com/chrome/).

### 1.1. Google Chrome

[**Google Chrome**](https://www.google.com/chrome/) is a cross-platform web browser developed by [Google](https://en.wikipedia.org/wiki/Google).

#### 1.1.1. Installation

To install [**Google Chrome**](https://www.google.com/chrome/), start by downloading the latest version from [official downloads page](https://www.google.com/chrome/). Then, execute the downloaded file (there will be a prompt for elevated permissions that must be accepted).

#### 1.1.2. Configuration

Set [**Google Chrome**](https://www.google.com/chrome/) preferences as desired and then install the following extensions:

+ [AWS Extend Switch Roles](https://chrome.google.com/webstore/detail/aws-extend-switch-roles/jpmkfafbacpgapdghgdpembnojdlgkdl)
+ [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa)
+ [KeePassXC-Browser](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)
+ [Proxy SwitchyOmega](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif)
+ [Tab Session Manager](https://chrome.google.com/webstore/detail/tab-session-manager/iaiomicjabeggjcfkbimgmglanimpnae)
+ [xBrowserSync](https://chrome.google.com/webstore/detail/xbrowsersync/lcbjdhceifofjlpecfpeimnnphbcjgnc)

Set the options of all the above extensions.

### 1.2. KeePassXC

[**KeePassXC**](https://keepassxc.org/) is a cross-platform community-driven port of the Windows application [Keepass Password Safe](https://keepass.info/) that I choose to use precisely because it's cross-platform and it allows me to use it on every operating system that I work with.

#### 1.2.1. Installation

[Download](https://keepassxc.org/download/) the latest portable version of [**KeePassXC**](https://keepassxc.org/). Then extract the downloaded archive to the `%USERPROFILE%\AppData\Local\` folder (`%LOCALAPPDATA%`). Rename the new folder to `KeepassXC`.

Inside the folder `%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Tools`, create a *shortcut* pointing to the file `%USERPROFILE%\AppData\Local\KeepassXC\KeePassXC.exe` and name it (the *shortcut*) `KeepassXC`. Then, edit the *shortcut* and point its icon to the main icon available on the file `%USERPROFILE%\AppData\Local\KeepassXC\KeePassXC.exe`.

#### 1.2.2. Configuration

Set [**KeePassXC**](https://keepassxc.org/) preferences (`Tools->Settings`) as desired but make sure to enable the `Browser Integrations`. Then, setup [KeePassXC-Browser](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk) extension to integrate it with the machine's installation of [**KeePassXC**](https://keepassxc.org/).

#### 1.2.3. Upgrade

To upgrade [**KeepassXC**](https://keepassxc.org/), delete all files and folders inside the folder `%USERPROFILE%\AppData\Local\KeepassXC`, **EXCEPT** the folder `config`, and then extract the content of the archive of the new version to that `KeepassXC` folder.

### 1.3. Windows Subsystem for Linux

[Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/windows/wsl/) lets developers run a GNU/Linux environment directly on Windows.

#### 1.3.1. Installation

Follow the [Official instructions](https://learn.microsoft.com/en-us/windows/wsl/install-manual) to manually install [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/). Open a PowerShell console as *Administrator* and [enable WSL](https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-1---enable-the-windows-subsystem-for-linux) with the following command:

    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

Before restarting the machine to [enable the Virtual Machine feature](https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-3---enable-virtual-machine-feature), execute the below command on a PowerShell console with administrator privileges:

    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

Restart the machine to complete the [WSL](https://learn.microsoft.com/en-us/windows/wsl/) installation and update to **WSL 2**.

[Download the latest Linux kernel update package](https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package) and then execute the downloaded package to install it in the machine (there will be a prompt for elevated permissions that must be accepted). A new restart of the machine will probably be needed.

Set [WSL 2 as your default version](https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-5---set-wsl-2-as-your-default-version) executing the below command on a standard PowerShell command:

    wsl --set-default-version 2

Open the [Microsoft Store](https://aka.ms/wslstore) and install the latest [Ubuntu LTS version](https://ubuntu.com/about/release-cycle).

On a regular PowerShell console, execute the below command to list the installed Linux distributions and check if everything is correct:

    wsl --list --verbose

If Ubuntu is not running with **WSL 2**, replace the **{LABEL}** in the below command as appropriate and execute it on a PowerShell console.

    wsl --set-version {DISTRO_NAME} 2

> **Label Definition**
>
> + **{DISTRO_NAME}** : Name of the Linux distribution to be executed with WSL 2

The article [Set up a WSL development environment](https://learn.microsoft.com/en-us/windows/wsl/setup/environment) has some good optional advices to setup a development environment with **WSL**, but the most useful is the installation of the [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701).

### 1.4. Windows Terminal

The [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701) is a terminal application for users of command-line tools and shells like Command Prompt, PowerShell, and WSL. Its main features include multiple tabs, panes, Unicode and UTF-8 character support, a GPU accelerated text rendering engine, and custom themes, styles, and configurations.

#### 1.4.1. Installation

Open the [Microsoft Store](https://aka.ms/wslstore) and install the [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701).

### 1.5. Chocolatey

[**Chocolatey**](https://chocolatey.org/) is a universal package manager for Windows.

#### 1.5.1. Installation

To install [**Chocolatey**](https://chocolatey.org/), open a PowerShell console as *Administrator* and execute the following command:

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

To list the installed chocolatey packages, execute the following command on a PowerShell console:

    choco list --local-only

### 1.6. Project specific software and tools

#### 1.6.1. Install BMW Root Certificate

Double click on the supplied certificate file and on the pop up that shows, click the button `Install Certificate...`. The choose the option `Current User` and click the button `Next`. On the following window, choose the option `Place all certificates in the following store`, browse to the folder `Trusted Root Certification Authorities`and then click the button `Next`. On the following screen click the button `Finish` and then click `Yes`to confirm the installation of the certificate.
