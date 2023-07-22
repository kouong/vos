# Setup guide for a development machine on Windows

This file contains the **Desktop Software** section of my [Setup guide for a development machine on Windows](https://github.com/EnduranceCode/windows-development-machine). The introduction to this guide as well as its full *Table of Contents* can be found on the [README.md](./README.md) file of this repository. The *Table of Contents* of this section is listed below.

## Table of Contents

3. [Desktop Software](#3-desktop-software)
    1. [Autenticação.gov](#31-autenticaçãogov)
    2. [Ferdium](#32-ferdium)
    3. [GIMP](#33-gimp)
    4. [Inkscape](#34-inkscape)
    5. [PDFsam](#35-pdfsam)
    6. [SpeedCrunch](#36-speedcrunch)
    7. [Spotify](#37-spotify)
    8. [VLC](#38-vlc)

## 3. Desktop Software

### 3.1. Autenticação.gov

[**Autenticação.gov App**](https://www.autenticacao.gov.pt/) application allows the Portuguese citizens to take advantage of the electronic features of their Citizen Card.

#### 3.1.1. Installation

Download the [**Autenticação.gov App**](https://www.autenticacao.gov.pt/) from the [official downloads page](https://www.autenticacao.gov.pt/web/guest/cc-aplicacao).
Then, execute the downloaded file (there will be a prompt for elevated permissions that must be accepted).

It will, probably, be necessary to restart the machine to complete the [**Autenticação.gov App**](https://www.autenticacao.gov.pt/) installation.

Download the [**Autenticação.gov Plugin**](https://autenticacao.gov.pt/fa/ajuda/autenticacaogovpt.aspx) from the [official downloads page](https://autenticacao.gov.pt/fa/ajuda/autenticacaogovpt.aspx). Then, execute the downloaded file (there will be a prompt for elevated permissions that must be accepted).

Rename the [**Autenticação.gov App**](https://www.autenticacao.gov.pt/) **Start Menu** shortcut to *Autenticação.gov - App* and rename the [**Autenticação.gov Plugin**](https://www.autenticacao.gov.pt/) Start Menu shortcut to *Autenticação.gov - Plugin*. Then, move both shortcuts to the `%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\Tools` folder (Create the `Tools` folder if it doesn't exits).

#### 3.1.2. Configuration

Go through the [**Autenticação.gov App**](https://www.autenticacao.gov.pt/) configuration options and set it as desired, but make sure that the auto start is disabled. Do the same with the [**Autenticação.gov Plugin**](https://autenticacao.gov.pt/fa/ajuda/autenticacaogovpt.aspx).

### 3.2. Ferdium

[**Ferdium**](https://ferdium.org/) is an application that helps to organize multiple web apps in one place for quick and easy access. It is very useful when, *e,g.*, you need to manage more than one [Team's](https://www.microsoft.com/microsoft-teams/group-chat-software/) account.

#### 3.2.1. Installation

Download [**Ferdium**](https://ferdium.org/) from the [official downloads page](https://ferdium.org/download). Then, execute the downloaded file.

Move the [**Ferdium**](https://ferdium.org/) **Start Menu** *shortcut* to the `%APPDATA%\Microsoft\Windows\Start Menu\Programs\Tools` folder (Create the `Tools` folder if it doesn't exits).

To enable sound on [**Ferdium**](https://ferdium.org/), at least with [Team's](https://www.microsoft.com/microsoft-teams/group-chat-software/) and bluetooth sound devices, on the [Windows](https://www.microsoft.com/en-us/windows) settings, select `System->Sound`. On the `Sound`tab, scroll down and click on the option `App volume and devices preferences`. Then, for the [**Ferdium**](https://ferdium.org/), replace `Default` in the *Output* and *Input* dropdowns with the device you want to use with[**Ferdium**](https://ferdium.org/).

### 3.3. GIMP

[**GIMP**](https://www.gimp.org/), an acronym for GNU Image Manipulation Program, is a multi-platform photo manipulation tool.

#### 3.3.1. Installation

To install [**GIMP**](https://www.gimp.org/), use a PowerShell console with *Administrator* privileges and execute the following command:

    choco install gimp

Rename the [**GIMP**](https://www.gimp.org/) **Start Menu** shortcut to *GIMP* and then move it to the `%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\Graphics` folder (Create the `Graphics` folder if it doesn't exits).

### 3.4. Inkscape

[**Inkscape**](https://inkscape.org/) is a Free and open source vector graphics multi-platform editor that uses the standardized SVG file format as its main format, which is supported by many other applications including web browsers.

#### 3.4.1. Installation

To install [**Inkscape**](https://inkscape.org/), use a PowerShell console with *Administrator* privileges and execute the following command:

    choco install inkscape

If the installation script doesn't create a *shortcut* for [**Inkscape**](https://inkscape.org/), inside the folder `%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\Graphics`, create a *shortcut* pointing to the file `%PROGRAMFILES%\Inkscape\bin\inkscape.exe` and name it (the *shortcut*) `Inkscape`. Then, edit the *shortcut* and point its icon to the main icon available on the file `%PROGRAMFILES%\Inkscape\bin\inkscape.exe`.

### 3.5. PDFsam

[**PDFsam Basic**](https://pdfsam.org/pdfsam-basic/) is a free and open-source cross-platform desktop application to split, merge, extract pages, rotate and mix PDF documents.

#### 3.5.1. Installation

Download [**PDFsam Basic**](https://pdfsam.org/pdfsam-basic/) portable archive from the [official downloads page](https://pdfsam.org/download-pdfsam-basic/). Then extract the downloaded archive and move the folder it contains to the `%USERPROFILE%\AppData\Local\` folder (`%LOCALAPPDATA%`). Rename the new folder to `PDFsam`.

Inside the folder `%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Tools`, create a *shortcut* pointing to the file `%USERPROFILE%\AppData\Local\PDFsam\pdfsam.exe` and name it (the *shortcut*) `PDFsam`. Then, edit the *shortcut* and point its icon to the main icon available on the file `%USERPROFILE%\AppData\Local\PDFsam\pdfsam.exe`.

### 3.6. SpeedCrunch

[**SpeedCrunch**](http://www.speedcrunch.org) is a high-precision scientific calculator featuring a fast, keyboard-driven user interface. It is free and open-source software, licensed under the GPL.

#### 3.6.1. Installation

Download [**SpeedCrunch**](http://www.speedcrunch.org) portable archive from the [official downloads page](https://heldercorreia.bitbucket.io/speedcrunch/download.html). Then extract the downloaded archive and move the extracted folder to the `%USERPROFILE%\AppData\Local\` folder (`%LOCALAPPDATA%`). Rename the new folder to `SpeedCrunch`.

Inside the folder `%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Tools`, create a *shortcut* pointing to the file `%USERPROFILE%\AppData\Local\SpeedCrunch\speedcrunch.exe` and name it (the *shortcut*) `SpeedCrunch`. Then, edit the *shortcut* and point its icon to the main icon available on the file `%USERPROFILE%\AppData\Local\SpeedCrunch\speedcrunch.exe`.

If the keyboard in use has a special key to start a calculator, assign [**SpeedCrunch**](http://www.speedcrunch.org) to key in question.

### 3.7. Spotify

[**Spotify**](https://www.spotify.com/) is a audio streaming and media services provider.

#### 3.7.1. Installation

Download [**Spotify**](https://www.spotify.com/) from the [official downloads page](https://www.spotify.com/us/download/windows/). Then, execute the downloaded file and when the installation process finishes, login into your [**Spotify**](https://www.spotify.com/) account.

Move the [**Spotify**](https://www.spotify.com/) **Start Menu** *shortcut* to the `%APPDATA%\Microsoft\Windows\Start Menu\Programs\Audio & Video` folder (Create the `Audio & Video` folder if it doesn't exits).

### 3.8. VLC

VLC is a free and open source cross-platform multimedia player and framework that plays most multimedia files as well as DVDs, Audio CDs, VCDs, and various streaming protocols.

#### 3.8.1. Installation

To install [**VLC**](https://www.videolan.org/), use a PowerShell console with *Administrator* privileges and execute the following command:

    choco install vlc

Move the [**VLC**](https://www.videolan.org/) **Start Menu** shortcut to the `%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\Audio & Video` folder (Create the `Audio & Video` folder if it doesn't exits). Then delete the folder `%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\VideoLAN`, including the rest of its contents.
