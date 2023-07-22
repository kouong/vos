# Setup guide for a development machine on Windows

## Introduction

My [operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) of choice is [Linux](https://en.wikipedia.org/wiki/Linux) and the distribution that I like to use is [Lubuntu](https://lubuntu.me). But, the majority of my professional work is done on [Windows](https://www.microsoft.com/en-us/windows) and I often need to setup a new machine or setup my machine to work on a new project. Therefore, I've created this guide to help me every time I need to perform such task.

This is my personal guide to setup a development machine on Windows. Although this is a very opiniated guide, I've decided to share it because it might be useful to somebody and, maybe, there will be someone out there that might be willing to help me improve the methodology that I normally follow. Please feel free to use this guide and make a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) to suggest any improvement that you find important.

## Table of Contents

1. [Fundamental Software](./1-fundamental-software.md)
    1. [Google Chrome](./1-fundamental-software.md#11-google-chrome)
    2. [KeepassXC](./1-fundamental-software.md#12-keepassxc)
    3. [Windows Subsystem for Linux](./1-fundamental-software.md#13-windows-subsystem-for-linux)
    4. [Windows Terminal](./1-fundamental-software.md#14-windows-terminal)
    5. [Chocolatey](./1-fundamental-software.md#15-chocolatey)
    6. [Project specific software and tools](./1-fundamental-software.md#16-project-specific-software-and-tools)
2. [Windows Configuration](./2-windows-configuration.md)
    1. [Keyboard and Mouse Software](./2-windows-configuration.md#21-keyboard-and-mouse-software)
    2. Windows Start Menu
    3. Power Management
3. [Desktop Software](./3-desktop-software.md)
    1. [Autenticação.gov](./3-desktop-software.md#31-autenticaçãogov)
    2. [Ferdium](./3-desktop-software.md#32-ferdium)
    3. [GIMP](./3-desktop-software.md#33-gimp)
    4. [Inkscape](./3-desktop-software.md#34-inkscape)
    5. [PDFsam](./3-desktop-software.md#35-pdfsam)
    6. [SpeedCrunch](3-desktop-software.md#36-speedcrunch)
    7. [Spotify](./3-desktop-software.md#37-spotify)
    8. [VLC](./3-desktop-software.md#38-vlc)
4. [Development Software & Tools](./4-development-software-and-tools.md)
    1. [Notepadd++](./4-development-software-and-tools.md#41-notepad)
    2. [Meld](./4-development-software-and-tools.md#42-meld)
    3. [Git & Git Bash](./4-development-software-and-tools.md#43-git--git-bash)
    4. [Java](./4-development-software-and-tools.md#44-java)
    5. [Apache Maven](./4-development-software-and-tools.md#45-apache-maven)
    6. [Apache Tomcat](./4-development-software-and-tools.md#46-apache-tomcat)
    7. [Quarkus CLI](./4-development-software-and-tools.md#47-quarkus-cli)
    8. [AWS CLI](./4-development-software-and-tools.md#48-aws-cli)
    9. [Make](./4-development-software-and-tools.md#49-make)
    10. [Rancher Desktop](./4-development-software-and-tools.md#410-rancher-desktop)
    11. [Terraform](./4-development-software-and-tools.md#411-terraform)
    12. [NVS (Node Version Switcher)](./4-development-software-and-tools.md#412-nvs-node-version-switcher)
    13. [IntelliJ IDEA](./4-development-software-and-tools.md#413-intellij-idea)
    14. [Visual Studio Code](./4-development-software-and-tools.md#414-visual-studio-code)
    15. Eclipse
    16. [DBeaver](./4-development-software-and-tools.md#416-dbeaver)
    17. [Postman](./4-development-software-and-tools.md#417-postman)
