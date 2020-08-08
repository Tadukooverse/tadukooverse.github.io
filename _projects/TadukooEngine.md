---
short_name: TadukooEngine
name: Tadukoo Engine/Launcher
blurb: >
  Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. Having a common launcher makes it easier to handle 
  common dependencies across projects.
summary: '<p>Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. By using the launcher/engine combo instead 
  of having completely standalone programs, any libraries used by multiple programs only need to be stored once and loaded as needed. This saves memory on the host machine by not having a 
  library duplicated within the actual program jars.</p>
  <p>Tadukoo Launcher provides a list of programs that are installed or may be downloaded. Once a program is selected, the launcher will download it along with its required libraries. Then 
  the libraries and program will be loaded into memory and launched.</p>
  <p>Tadukoo Engine provides the proper interfaces that programs should use to allow the launcheer to connect to and load them. In addition, the engine and launcher come with standard 
  libraries from Tadukoo Util by default so they don’t need to be downloaded separately later.</p>
---
