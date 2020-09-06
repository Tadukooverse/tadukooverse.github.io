---
short_name: TadukooEngine
title: Tadukoo Engine/Launcher
blurb: 'Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. Having a common launcher makes it easier to handle 
  common dependencies across projects.'
summary: 'Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. By using the launcher/engine combo instead 
  of having completely standalone programs, any libraries used by multiple programs only need to be stored once and loaded as needed. This saves memory on the host machine by not having a 
  library duplicated within the actual program jars.
  
  
  Tadukoo Launcher provides a list of programs that are installed or may be downloaded. Once a program is selected, the launcher will download it along with its required libraries. Then 
  the libraries and program will be loaded into memory and launched.
  
  
  Tadukoo Engine provides the proper interfaces that programs should use to allow the launcheer to connect to and load them. In addition, the engine and launcher come with standard 
  libraries from Tadukoo Util by default so they don’t need to be downloaded separately later.'
version: Alpha v.0.1 SNAPSHOT
github: https://github.com/Tadukoo/TadukooEngine
---

#### Table of Contents
* [Modules](#modules)
	* [Tadukoo Downloader](#tadukoo-downloader)
	* [Tadukoo Engine](#tadukoo-engine)
	* [Tadukoo Installer](#tadukoo-installer)
	* [Tadukoo Launcher](#tadukoo-launcher)
* [Current Plans](#current-plans)

## Modules

### Tadukoo Downloader
Tadukoo Downloader is a small file that can be used to download the Tadukoo Installer and run it to install Tadukoo Launcher.

The purpose of this is to have a small file that can be sent around when file size is limited.

### Tadukoo Engine
Tadukoo Engine provides the interfaces/classes needed to create a program that will run on the Tadukoo Launcher.

Currently you just need to implement Program and its methods, but this is in early development, so it will change in the future.

For more information on creating programs to run in Tadukoo Launcher, check out the Tadukoo Launcher Program Guide (Coming Soon)

### Tadukoo Installer
Tadukoo Installer is an installation executable for Windows. It will install Tadukoo Launcher and ensure that the proper Java version is installed.

Currently there are no Mac or Linux installers, because [Tadukoo](/contributors/Tadukoo.html) doesn't own a Mac or use Linux.

### Tadukoo Launcher
Tadukoo Launcher provides a launcher that shows programs that can be downloaded and/or run and will handle loading library dependencies for the programs.

## Current Plans
> **[Main Page/Progress]({{page.github}}/milestone/1)**

Currently, progress is moving forward on the first release of Tadukoo Util, Alpha v.0.1.

The overall goals are:
- Running and terminating programs
- Making the launcher able to auto-update
- Handling informational files
- Downloading files
- Handling dependencies
- Allow installation on Windows, Mac, and Linux

### Running and Terminating Programs
The launcher should be able to successfully run and terminate programs created with the Tadukoo Engine.

This is basically development of the Tadukoo Engine, with the proper interfaces for programs to use in running.

### Auto-Updating the Launcher
The launcher should be able to auto-update.

To do this, the plan is to create a new module called Tadukoo Updater (or similar). The launcher will check for new releases of Tadukoo Engine on GitHub, 
and download the latest Tadukoo Updater if it's new. It will then close the launcher and run the updater (after prompting the user to update?)

The updates would usually just update the main jars (Tadukoo Engine, Tadukoo Launcher, Tadukoo Util jars, etc.), but there may be cases where it has to do 
more complex operations.

### Handling Informational Files
There will be 3 types of files that the launcher cares about:
- Library Description Files
- Program Description Files
- Program Library Files (name TBD)

Library Description Files include the details about libraries (where to get them, dependencies if any, etc.)

Program Description Files include the details about programs (where to get them, dependencies if any, etc.)
- In this way, they'll be similar to Library Description Files, and may even be the same?

Program Library Files include lists with links to Library and Program Description Files
- These are used to find libraries and programs to populate the launcher with
- Basically you'd add trusted Program Library Files to your launcher based on who you trust
  - Like you could take the official Tadukooverse one, and add in one from your friend's projects

### Downloading Files
The launcher should be able to download programs and libraries (based off details from the informational files). 
For now, this will go off of the GitHub releases.

### Handling Dependencies
The launcher should be able to look at the Program Description File and determine if it has the proper libraries and if not, download and install them properly, 
then load them properly with the program.

### Allow Installation on Windows, Mac, and Linux
Windows installation is figured out already with the installer, but Mac and Linux would need a guide to install it at the moment.
