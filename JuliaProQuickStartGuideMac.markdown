# JuliaPro #

# (v1.5.1-1) #

# Installation Manual and Quickstart Guide #

## Contents

 [*1. Objective*](#objective)

 [*2. Prerequisites*](#prerequisites)
 
 [*2.1. Installation of Xcode command line tools*](#installation-of-xcode-command-line-tools)

 [*2.2 Prerequisite for installing JuliaPro on macOS Catalina 10.15.3*](#Catalina)

 [*3. Installing JuliaPro*](#installing-juliapro)

 [*4. Launching Juno for JuliaPro*](#launching-juno-for-juliapro)

 [*4.1. Using Juno*](#using-juno)
 


1. Objective
==============

This guide details the installation procedure and usage of the JuliaPro.

2. Prerequisites
=================

* An appropriate version of Mac OS X or macOS, 10.11 (OS X 10.11 El Capitan) or higher
* Xcode command line tools installed
* 1.5 GB of disk space

2.1 Installation of Xcode command line tools
--------------------------------------------

To install the Xcode command line tools, first open a Terminal window.

To launch a Terminal window from within OSX, first click on the Launchpad icon in the Dock on your desktop, then click the "Other" icon, and select the "Terminal" application.

At the Terminal prompt, execute the following command:

```
$ xcode-select --install
```

If the Xcode command line tools are not already installed, then you will be prompted as to whether you would like to install them.


Click the "Install" button to install the Xcode command line tools.

2.2 Prerequisite for installing JuliaPro on macOS Catalina 10.15.3
--------------------------------------------

Since JuliaPro 1.5.1-1 binary is not notarized, you need to follow additional steps to install JuliaPro 1.5.1-1 on macOS Catalina 10.15.3

1) Double click on JuliaPro binary, you will encounter following error

\ ![](media/Catalina1.png)

2) After encountering above error, click on "Ok" and goto: System Preferences --> Security & Privacy  --> General

3) You should see an option to unblock JuliaPro installer similar to the following screenshot. Click on the button "Open Anyway".

\ ![](media/Catalina2.png)

4) Come back to the location where JuliaPro binary is located and double click on the JuliaPro binary

5) You should encounter following error once again, click on "ok" in the error dialog box, Mac OS should open the JuliaPro installer this time, follow the instructions in "Installing JuliaPro" section after this step.

\ ![](media/Catalina1.png)


3. Installing JuliaPro
======================

Before installing the latest version of JuliaPro for Mac, you must first uninstall any existing version of JuliaPro for Mac that is installed on your machine.

Once the requirements are met, you can start the JuliaPro installation using the installer provided.  

\ ![](media/mac_image1.png)

Upon starting the installation, you will be presented with the JuliaPro Software License Agreement.  After reading through the terms mentioned in the agreement, click “Agree” if you accept the terms of the license and proceed with the installation.

\ ![](media/mac_image2.png)

\ ![](media/mac_image3.png)

After accepting the license agreement, you can select the location where JuliaPro will be installed.

\ ![](media/mac_image4.png)

Depending on your current account security settings, you might need to provide your current user account password to proceed with the installation.

\ ![](media/mac_image5.png)

The installer will then request you to enter your JuliaTeam server URL. This prompt is applicable only for JuliaTeam customers, if you’re an individual or your company or organization is not using JuliaTeam, then you can leave the text box blank and click on “Ok” to close the prompt. The installer will configure JuliaPro with default package server ` pkg.juliahub.com`. You can download (Or update) packages and registries from this server even if you’re not a JuliaTeam customer.

If your organization is using JuliaTeam, then you can configure JuliaPro to work with your private package server (JuliaTeam enables you to create private package server) by entering the URL in the text box. Once you enter your private JuliaTeam package server URL in the text box and click on “Ok”, the installer will configure JuliaPro to download all the packages and registries from your private JuliaTeam server.

\ ![](media/mac_image9.png)

Upon clicking on “Ok” , the installer will then proceed to install JuliaPro in the chosen location.

\ ![](media/mac_image6.png)

Upon completion of the installer, press close to exit the installer.

\ ![](media/mac_image7.png)



4. Launching Juno for JuliaPro
===============================

From within the LaunchPad window, Double-Click on the JuliaPro icon to start a Juno session.  

\ ![](media/mac_image8.png)

Upon initially launching Juno, you will be presented with the following window.

\ ![](media/win12.png)

Juno is a full-featured and easily extensible integrated development environment based on the Atom editor.  

The previous screenshot shows the most important aspects of the Juno environment for working with Julia code:

  *  The Editor Tab - A tab that is primarily used for developing longer segments of Julia code, as well as code that will be saved to a file.  Multiple editor tabs can be opened within a single Juno session to develop multiple Julia files.
  *  Julia REPL - The tab that is primarily used for executing Julia commands interactively and displaying textual results from those commands.
  *  The Plots Tab - The tab used for display of visualizations produced by supported plotting packages.
  *  The Workspace Tab - The tab used for displaying the values of variables and functions that are in the current Julia scope.
  *  The Julia Toolbar - The primary toolbar containing buttons for controlling aspects of the use of Julia from within Juno.
  *  The Julia Menu - An entry in the the Atom Menu that is specific to control of Julia from within Juno.
  *  Documentation Tab - This tab provides a convenient way to access documentation in the Juno IDE, you can search for documentation of all imported Julia packages and you can also access Base Julia documentation using this tab.
  *  The Atom Command Palette (not shown in the screenshot above) - A pop-up window that allows for searching all commands available from within an Atom/Juno session, including "julia" specific commands.


4.1 Using Juno
--------------

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


Once you have `token.toml` , rename this file as `auth.toml` and then you can move this file to the machine where you have installed JuliaPro (If you're downloading token from a different machine), the default location to place this file is `~/.juliapro/JuliaPro_v1.5.1-1/servers/pkg.juliahub.com/auth.toml` i.e create following path `.juliapro/JuliaPro_v1.5.1-1/servers/pkg.juliahub.com/` in your home directory and place `auth.toml` in the path you just created. Once you place the file in this location, all subsequent `Pkg` and `BinaryProvider.jl` operations will use this token to authenticate the download from `pkg.juliahub.com`
