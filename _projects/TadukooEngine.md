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
---

#### Table of Contents
* [Modules](#modules)
	* [Tadukoo Downloader](#tadukoo-downloader)
	* [Tadukoo Engine](#tadukoo-engine)
	* [Tadukoo Installer](#tadukoo-installer)
	* [Tadukoo Launcher](#tadukoo-launcher)

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
