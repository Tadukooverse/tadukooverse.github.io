---
title: History
blurb: History of how Tadukooverse started
summary: The history of the Tadukooverse organization and how it started
---
# History

## KBWCO to Tadukoo Util
[Tadukoo](/contributors/Tadukoo.html) started working on a computer version of 1000 Blank White Cards (which is a story for another time to be put on his own personal blog). That project started as early as 
2016, and he worked on it on and off over the years. Because of working on it only a little at a time, and being in college learning better practices, the codebase for it got chaotic. There were some good 
ideas he had to make things more generic and extensible for the future, but they were in varying states of completion due to the haphazard nature of working on it.

By the summer of 2019, he had gotten three friends to agree to help him create KBWCO (1000 Blank White Cards Online), with the hopes to sell copies of it and start his own company. The plans fell through for 
personal reasons (along with general laziness on Tadukoo's part at the time, looking for a job after graduation, and lack of organization in the codebase and paperwork), so no such company was ever started 
and his friends didn't end up helping work on that. 

Tadukoo got a programming job in August and quickly learned even more programming patterns and better practices, and wanted to incorporate them into KBWCO. He was still working on trying to clean up the code 
base at the time, with the hope of just postponing the friends' help. On October 13, 2019, Tadukoo created a utilities package in the KBWCO project, with the intention of making utility classes to be 
eventually moved to a separate common project.

For a while, Tadukoo was developing these utilities in the KBWCO project, but development on them was slow and restricted by trying to maintain the current functionality of KBWCO without breaking anything. 
So on November 10, 2019, [Tadukoo Util](/projects/TadukooUtil.html) was born, by moving all the current utilities to a separate project. At this point, it was a single module that included some of the classes 
now present in Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util. Around Christmas 2019, we got Tadukoo Database and Tadukoo File Format added to the Tadukoo Util family.

In February 2020, Tadukoo View was transferred from classes in KBWCO. These classes were making custom UI components the hard way, so they were eventually deprecated and moved to Old Tadukoo Util instead to 
discourage using them. We have gotten a new Tadukoo View module in July 2020 that just provides View utilities instead of providing actual components, so this may cause confusion when looking into the history.

In March 2020, Tadukoo Annotation Processor and Tadukoo Lang were finally separated from the Tadukoo Util module, and in May 2020, we got Tadukoo Look & Feel, which provides a customizable look and feel beyond 
what the default Java ones allow for.

Since then, more changes have been made to Tadukoo Util to improve and expand upon it, and Tadukoo released it under the MIT license for anyone to use on GitHub.

## Tadukoo Engine/Launcher
In June 2020, Tadukoo started working on [Tadukoo Engine/Launcher](/projects/TadukooEngine.html). The intention was for him to be able to reuse [Tadukoo Util](/projects/TadukooUtil.html) easily across projects, 
along with any other utilities he created over time. The Tadukoo Launcher is a program that launches programs that run on the Tadukoo Engine. When you open Tadukoo Launcher, you're presented with a list of 
programs that you can run or download, and it will handle the dependencies for you, downloading and loading them as needed.

As of writing this (August 9, 2020), Tadukoo Engine/Launcher are early in development, but Tadukoo has released them on GitHub just like Tadukoo Util.

Tadukoo decided he likes the way that Tadukoo Engine/Launcher is being setup and wants to allow others to use it easily as well, in addition to providing a bunch of utility libraries for use with it. For this 
reason, he decided to start the Tadukooverse organization as a means for anyone to be able to find the information about this software and for them to get involved if they want to.

Tadukoo Util and Tadukoo Engine will be transferred to the Tadukooverse organization soon, and this website and the GitHub community health files are in development to be ready for people to join in on this, 
and to keep things organized so development can continue even without outside help.
