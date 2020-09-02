# JuliaPro #

# (v1.5.0-2) #

# Installation Manual and Quickstart Guide #

## Contents

 [*1. Objective*](#objective)

 [*2. Prerequisites*](#prerequisites)

 [*3. Installing JuliaPro*](#installing-juliapro)
 
 [*3.1. Installing JuliaPro on legacy Windows systems like Windows 7*](#legacy-windows)

 [*4. Using JuliaPro*](#using-juliapro)
 
 [*4.1. Launching JuliaPro*](#launching-juliapro)
 
 [*4.2. Getting Started with JuliaPro*](#getting-started-with-juliapro)

 [*5. Trademark Usage*](#trademark-usage)

 1. Objective
==============

This guide details the installation procedure and usage of the base JuliaPro package and JuliaPro's Juno IDE.

2. Prerequisites
=================

  * An appropriate version of Microsoft® Windows®
    * Windows 8.1, Windows 10
    * Windows Server 2012, Windows Server 2012 R2, Windows Server 2016
  * 5 GB of disk space
  * Active Internet connection
  * LinkedIn or Gmail or GitHub or JuliaComputing account (Either one of these accounts are required for authentication)

3. Installing JuliaPro
======================

Once the requirements are met, you can start the JuliaPro installation using the executable provided.  

\ ![](media/win1.png)

To execute the installer with Administrative privileges, right click on the JuliaPro_v1.5.0-2.exe and select “Run As Administrator”.  To execute the installer as the current user, just double-click on the executable.

\ ![](media/win2.png)

Upon launching the executable, you might be presented with a User Account Control permissions window.  

If the installer is being executed with Administrative privileges, then click “Yes” to proceed with the installation.  

\ ![](media/win3.png)

Upon starting the installation, you will be presented with the JuliaPro Software License Agreement.  After reading through the terms mentioned in the agreement, click “I Agree” if you accept the terms of the license and proceed with the installation.

\ ![](media/win4.png)

If the installer is being executed with Administrative privileges, then you will be presented with the following installation option:

\ ![](media/win6.png)

*	**All Users:** This installation option requires the current user to have Administrator privileges and will default to installing JuliaPro to a location available to all system users.  The default location is a folder created at the location of the current %HOMEDRIVE% environment variable.  Selecting this option also allows for a user with Administrative privileges to install Julia Professional to a shared network drive location.

If the installer is being executed without Administrative privileges, then you will be presented with the following two active installation options:

\ ![](media/win5.png)


*	**Current User (No Admin Privileges Required):** With this installation option, the selected directory into which JuliaPro is installed must be a directory for which the current user has read/write privileges.  The default directory chosen is within the “AppData” directory of the current user’s account.

*	**Shared Drive (No Admin Privileges Required):** With this installation option, the selected directory into which JuliaPro is installed can be a shared network drive location for which the current user has read/write privileges.  While the default directory chosen is within the “AppData” directory of the current user’s account, this option is useful when the current user intends to install Julia Professional to a shared location, but does not have administrative privileges.

Once you select the mode of installation, you will be presented with JuliaTeam configuration page

\ ![](media/win19.png)

This page is applicable only for JuliaTeam customers, if you’re an individual or your company or organization is not using JuliaTeam, then you can click on “Next” and continue with the installation. The installer will configure JuliaPro with default package server ` pkg.juliahub.com`. You can download (Or update) packages and registries from this server even if you’re not a JuliaTeam customer.

If your organization is using JuliaTeam, then you can configure JuliaPro to work with your private package server (JuliaTeam enables you to create private package server) by changing the URL in the text box. Once you enter your private JuliaTeam package server URL in the text box and click on “Next”, the installer will configure JuliaPro to download all the packages and registries from your private JuliaTeam server.


Once you're done with your JuliaTeam configuration, you will be presented with options related to: which components of the JuliaPro distribution you would like to install.  

\ ![](media/win7.png)

The first listed component is the Julia compiler, runtime and terminal application.  This component is required for installation.

The next listed component is the set of all "JuliaPro packages" to be installed as part of JuliaPro.  This component is also required for installation.

The next listed component includes "Juno for JuliaPro".  Selection of this component will install a copy of the Atom editor onto which various JuliaPro specific enhancements are continually being added.

The subsequent component is the entry for "Start Menu Icons".  By unselecting this entry, no entries for JuliaPro will be added to the Windows Start Menu.

The subsequent component is the entry for "Desktop Shortcuts".  By unselecting this entry, no desktop shortcut icons linking to various JuliaPro components are created.

The final component is the entry for "Associate .jl files with JuliaPro". By unselecting this entry, ".jl" will no longer be associated with JuliaPro.

Upon selecting your desired components, click “Next” to proceed.

\ ![](media/win8.png)

Next, select the folder into which you wish to install JuliaPro.  The selection must be a directory into which the current user has read/write privileges.  The installer provides an appropriate default location when either the “All Users”, “Current User” options were selected.

If the “Shared Drive” option was selected by a non-Administrative user, or an Administrative user selects the “All Users” option, then you will likely wish to click the “Browse…” button in order to select a shared network drive location into which to install JuliaPro.  Installing JuliaPro to a shared network drive location is useful for teams that plan to share access to a single Julia Professional installation among multiple user accounts on separate machines in the same Active Directory domain.

The following screenshot shows the JuliaPro installer during its installation phase.

\ ![](media/win9.png)

Upon completion of the installer, press close to exit the installer.

\ ![](media/win10.png)

**NOTE: Setting access permissions on your JuliaPro installation for shared installations.**

For shared network drive installations, if the directory into which JuliaPro was installed is currently accessible by multiple users, then an Administrator may desire to set access permissions for their JuliaPro installation to be read-only for non-Administrative users.  

By setting the JuliaPro installation to be read-only, only administrative users will be able to perform operations via Julia’s built-in Pkg package manager.  Operations such as `Pkg.add`, `Pkg.update`, and `Pkg.rm` can only be performed by users with write access to the `pkgs-1.5.0-2` directory of the Julia Professional installation.

Restricting write access to these directories to a single administrative user will ensure a consistent state of packages for all users of a shared installation.

To prevent unnecessary precompilation of Julia packages from being triggered by separate users, all users accessing a shared drive installation of JuliaPro from a mapped network drive must have the shared drive mapped to the same network drive letter and absolute path.

**NOTE: Copying of Atom Configuration Information on First Launch of Juno.**

For shared network drive installation, the first time a user launches Juno from their client machine, a `.atom` configuration folder will be copied from the Julia Professional installation into the directory `%HOMEDRIVE%\%HOMEPATH%\JuliaPro_Juno_1.5.0-2`.  This directory stores user specific configuration information for use of Juno for JuliaPro.

If you're using Windows Server 2012; Then you need to install following additional software's inorder to perform Pkg operations in JuliaPro  

*   The [TLS easy\_fix](https://support.microsoft.com/en-us/help/3140245/update-to-enable-tls-1-1-and-tls-1-2-as-a-default-secure-protocols-in) for the package manager to work, see [this Discourse thread](https://discourse.julialang.org/t/errors-for-git-pkg/9351) for more details.
*   [Windows Management Framework 3.0 or later](https://docs.microsoft.com/en-us/powershell/scripting/wmf/overview) to include PowerShell 3.0 or later.


3.1 Installing JuliaPro on legacy Windows systems like Windows 7
-------------------------------------------

NOTE:- Legacy Windows systems like Windows 7, Windows Server 2008 R2 SP1, etc are no longer supported by JuliaPro, following steps can be tried at your own risk. Julia Computing will not provide any support or assistance in installing these software's, nor does it provide any guarantee about the work-ability of JuliaPro after installing on these unsupported operating systems. 

If you're using Windows 7 or any other unsupported Windows operating systems; Then you need to install following additional software's inorder to perform Pkg operations in JuliaPro  

*   The [TLS easy\_fix](https://support.microsoft.com/en-us/help/3140245/update-to-enable-tls-1-1-and-tls-1-2-as-a-default-secure-protocols-in) for the package manager to work, see [this Discourse thread](https://discourse.julialang.org/t/errors-for-git-pkg/9351) for more details.
*   [Windows Management Framework 3.0 or later](https://docs.microsoft.com/en-us/powershell/scripting/wmf/overview) to include PowerShell 3.0 or later.

It is recommended that users on these legacy Windows systems install and use a terminal besides cmd.exe since the default terminal application has known issues which affect its usability with Julia and other libuv-based cross-platform software.



4. Using JuliaPro
=========================================

4.1 Launching JuliaPro
-------------------------------------------

If the Desktop Shortcuts components were selected during installation of the JuliaPro, then you should have a JuliaPro icon on your desktop.  Double-Click on the icon to start IDE.  

\ ![](media/win11.png)

If the Start Menu Shortcuts components were selected during the installation process, then you should have also an entry for the JuliaPro Command Prompt located under “Start -> JuliaPro -> Juno for JuliaPro 1.5.0-2”

Upon initially launching Juno, you will be presented with the following window.

\ ![](media/win12.png)


4.1 Getting Started with JuliaPro
-------------------------------------------

Naming convention for different layout (Panes) in Juno IDE can be seen below

\ ![](media/win13.png)

You can start Julia by pressing enter in “Julia REPL” pane

\ ![](media/win14.png)

By default, JuliaPro will download all the packages from `pkg.juliahub.com` , this website requires authentication, hence, you will go through the authentication process the first time you perform a `Pkg` operation; `JuliaPro` will open the authentication link in your default browser, once you successfully authenticate in your browser, JuliaPro will download a unique token for you and place it in the appropriate location. This token will be reused in your subsequent `Pkg` operations.

\ ![](media/auth1.png)

Once the URL link is open in your browser, you will be directed to authenticate by signing into either one of these accounts : LinkedIn or Gmail or GitHub or JuliaComputing account.

\ ![](media/auth2.png)

Once the authentication is done, you will get a message in browser saying "Authenticated. You may close this browser window now."

\ ![](media/auth3.png)

Your `Pkg` operation should continue as is, all your subsequent Pkg operations will use the token that JuliaPro just downloaded.

\ ![](media/auth4.png)

If the automated browser authentication is failing, then please report the issue to JuliaPro@juliacomputing.com and follow below instructions as a fallback to manually download the token and place it in the appropriate location:

NOTE:- YOU DON'T NEED TO FOLLOW THESE INSTRUCTIONS IF YOU SEE FOLLOWING MESSAGE IN YOUR JuliaPro REPL: "Authentication successful"

1. Open following link in your browser: `https://pkg.juliahub.com/auth`
2. Once you open the URL link, you will be directed to authenticate by signing into either one of these accounts : LinkedIn or Gmail or GitHub or JuliaComputing account.

\ ![](media/auth2.png)


Once the authentication is done, your `token.toml` file download should begin immediately , if your download doesn’t begin automatically, you can always click on “here” URL link to download the token

\ ![](media/linux3.png)


Once you have `token.toml` , rename this file as `auth.toml` and then you can move this file to the machine where you have installed JuliaPro (If you're downloading token from a different machine), the default location to place this file is `<HOME-FOLDER>/.juliapro/JuliaPro_v1.5.0-2/servers/pkg.juliahub.com/auth.toml` i.e create following path `.juliapro/JuliaPro_v1.5.0-2/servers/pkg.juliahub.com/` in your home directory and place `auth.toml` in the path you just created. Once you place the file in this location, all subsequent `Pkg` and `BinaryProvider.jl` operations will use this token to authenticate the download from `pkg.juliahub.com`



5. Trademark Usage
===================

Microsoft<sup>®</sup> and Windows<sup>®</sup> are registered trademarks of Microsoft Corporation.

Other names may be trademarks of their respective owners.
