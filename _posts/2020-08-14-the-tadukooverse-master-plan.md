---
title:  "The Tadukooverse Master Plan"
author: Tadukoo
date:   2020-08-14 
series: "General Tadukooverse Development"
index: 1
categories: blog
tags: 
- Plans
- Programming
comment_issue_id: 43
---
{% assign TadukooMaven = site.projects | where:"short_name", "TadukooMaven" | first %}
{% assign TadukooUtil = site.projects | where:"short_name", "TadukooUtil" | first %}
{% assign TadukooView = site.projects | where:"short_name", "TadukooView" | first %}
{% assign TadukooDatabase = site.projects | where:"short_name", "TadukooDatabase" | first %}
{% assign TadukooParsing = site.projects | where:"short_name", "TadukooParsing" | first %}
{% assign TadukooWebServices = site.projects | where:"short_name", "TadukooWebServices" | first %}
{% assign TadukooGitHub = site.projects | where:"short_name", "TadukooGitHub" | first %}
{% assign TadukooEngine = site.projects | where:"short_name", "TadukooEngine" | first %}
{% assign TadukooAnnotations = site.projects | where:"short_name", "TadukooAnnotations" | first %}
For a while now, I've just been planning to have the first official release of [Tadukoo Util](/projects/TadukooUtil.html) and [Tadukoo Engine/Launcher](/projects/TadukooEngine.html) be Alpha v.0.1. 
I've realized that Tadukoo Util has enough plans that a higher version number would make sense, and I'm not really sure what plans I would have for either project beyond the current ones before 
labelling either as "official release 1.0".

For both projects (along with some others I'll go over later), the first official release will be v.1.0, but the release dates won't change (not that there are any planned dates). What I mean is 
that the current plans for Alpha v.0.1 will become the new plans for release v.1.0 (though over time more details will be added as progress is made on them). For both projects, what this will look 
like is that the current plans will be split into multiple versions ("unofficial versions"). These smaller versions will be releases that you can use and get support for, but they will not 
remain supported beyond the release of the next "unofficial version". e.g. Tadukoo Util will have Alpha v.0.1, Alpha v.0.2, Alpha v.0.3, and more. Once Alpha v.0.2 comes out, Alpha v.0.1 will no 
longer be supported, and we will not maintain documentation for Alpha v.0.1 anymore, or maintain backwards compatibility with it.

My typical progression of versions from first code to first release v.1.0 usually divides the original plan into 10 chunks and labels them as Alpha v.0.1 through Alpha v.0.4, then Beta v.0.5 through 
Beta v.0.9, and then Release v.1.0. I'm not sure why I didn't devise a plan like that for these projects from the start. Perhaps I thought both projects were too small to be divided that way? 
I definitely didn't expect Tadukoo Util to be as big a project as it currently is (I planned one module with a few utils).

Tadukoo Util will be split into at least 5 "unofficial" versions based on its current plans. Tadukoo Engine/Launcher needs some thinking through before it can be officially split up. But Tadukoo 
Engine/Launcher v.1.0 will depend on Tadukoo Util being completed, along with Tadukoo Parsing, Tadukoo Web Services, and Tadukoo GitHub (and potentially other projects depending on how plans 
work out). Tadukoo GitHub depends on Tadukoo Web Services; Tadukoo Web Services depends on Tadukoo Parsing; and Tadukoo Parsing depends on Tadukoo Util. So we have one long dependency tree here.

The Projects in Order
* Tadukoo Util - the base libraries upon which everything else is built
* Tadukoo Parsing - libraries for parsing different formats - e.g. JSON, XML, etc.
* Tadukoo Web Services - libraries for interfacing with web services - e.g. REST services
* Tadukoo GitHub - libraries for interfacing with the GitHub REST API
* Tadukoo Engine/Launcher - engine for running programs with libraries, and launcher for launching said programs

Tadukoo Util will be split into the following versions:
- Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util (basically just Javadocing and testing)
- Alpha v.0.2 - Complete Tadukoo Look & Feel
- Alpha v.0.3 - Complete Tadukoo View
- Alpha v.0.4 - Complete Tadukoo Database
- Beta v.0.5 - Complete Tadukoo File Format

Beta v.0.5 of Tadukoo Util will also be the release candidate for v.1.0, assuming no further plans are made for other versions by then. Essentially, it'll maintain a Beta status until Tadukoo 
Engine/Launcher is at v.1.0, in case any changes are required of it before then (e.g. Tadukoo Engine demands changes to Tadukoo Database for some reason).

Tadukoo Engine/Launcher will dictate the entire switch to v.1.0. When Tadukoo Engine/Launcher is released as v.1.0, all the other projects listed will also be released as v.1.0, with no sooner 
releases. In doing this, no other versions will be tied leading up to v.1.0 (e.g. Alpha v.0.1 of Tadukoo Util doesn't depend on Tadukoo Engine hitting Alpha v.0.1 - those will be separate). 
Also, versions past v.1.0 will probably not be linked either, I'm just doing it for the first major release so that everything has a decent/complete first release. I want to avoid releasing 
Tadukoo Util v.1.0 and then having to update it to v.1.2.6 to get it working with Tadukoo Engine v.1.0, because to me that would mean that those extra updates should've been in the original 
plans in the first place.

As of right now, Tadukoo Parsing, Tadukoo Web Services, and Tadukoo GitHub have no solid plans for where they should be for v.1.0 beyond being ready for Tadukoo Engine/Launcher. Tadukoo 
Engine/Launcher also doesn't have a firm plan (though does have a general listing of requirements), and the plans for the others will definitely evolve as Tadukoo Engine/Launcher is further 
figured out.

I will likely update this post as the master plan evolves with more details (though the finer details would appear on the project pages, this would just be an overview).

Just as a minor side-note, Old Tadukoo Util (a library that has deprecated Tadukoo View stuff in it) will also receive a v.1.0 release to coincide with the other releases. It's just not 
officially part of the Tadukooverse Master Plan here, and probably shouldn't be used anyway.

As part of Alpha v.0.1 of Tadukoo Util, I'll also be transitioning it over to Tadukooverse finally. This involves:
- The actual transfer
- Adding any missing labels
- Updating the license (Tadukooverse projects should be MIT license and list me (Logan Ferree/Tadukoo) and "other Tadukooverse contributors" in the copyright)
- Adding proper issues/milestones and cleaning up old ones
- Updating the Javadocs on this site

Other projects will also be transitioned as part of their first milestone if they've already been started (Tadukoo GitHub does not exist at all yet, so will probably just be created under 
Tadukooverse from the start).

## Progress
> Last Updated: May 30, 2021 4:45 PM
* [{{TadukooMaven.title}}]({{TadukooMaven.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.3" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1 - Tadukoo Maven Base POM and Library POM - Released May 28, 2021 6:56 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2 - Tadukoo Maven Parsing, Web Service, and View POMs - Released May 29, 2021 7:47 PM" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.3 - Tadukoo Maven Program POM" %}
* [{{TadukooUtil.title}}]({{TadukooUtil.url}}) - {% include text-color.html color="yellow" text="Working on Beta v.0.5" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util - Released September 5, 2020 8:01 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2 - Complete Tadukoo View - Released November 7, 2020 9:07 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2.1 - Fixes + Improvements - Released December 12, 2020 7:28 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2.2 - Reorganization - Released December 13, 2020 8:39 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.3 - More Tadukoo Functions - Released December 19, 2020 7:47 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.3.1 - Character Util and More String Utils - Released February 6, 2021 5:29 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.4 - Dictionary and Java 16 - Released April 17, 2021 9:22 PM" %}
  * {% include text-color.html color="yellow" text="Beta v.0.5 - ByteUtil and Other Changes" %}
  * {% include text-color.html color="red" text="Others TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0" %}
* [{{TadukooView.title}}]({{TadukooView.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.3.3" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2.2 - Moved from Tadukoo Util - Released December 13, 2020 8:48 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.3 - Complete Button + Label Customizations - Released January 17, 2021 3:29 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.3.1 - Update to Tadukoo Util Alpha v.0.3.1 - Released February 6, 2021 5:50 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.3.2 - Update to Tadukoo Util Alpha v.0.4 (and some changes) - April 25, 2021 2:20 PM" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.3.3 - Update to Tadukoo Util Beta v.0.5 (and some changes)" %}
  * {% include text-color.html color="red" text="Alpha v.0.4 - Complete Look & Feel Pieces Used in Form/Components" %}
  * {% include text-color.html color="red" text="Others TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0" %}
* [{{TadukooDatabase.title}}]({{TadukooDatabase.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.3" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2.2 - Moved from Tadukoo Util - Released December 13, 2020 8:56 PM" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.3 - Complete Tadukoo MySQL" %}
  * {% include text-color.html color="red" text="Others TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0" %}
* [{{TadukooParsing.title}}]({{TadukooParsing.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.3.1" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1 - Complete Tadukoo JSON - Released November 10, 2020 6:11 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2.2 - Moved Tadukoo File Format Over + Other Minor Changes - Released December 13, 2020 9:18 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.2.3 - Updated Tadukoo Util to Alpha v.0.3.1 + Other Minor Changes - Released February 6, 2021 6:43 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.3 - Complete Tadukoo File Format - Released April 24, 2021 11:00 PM" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.3.1 - Update to Tadukoo Util Beta v.0.5 + Other Minor Changes" %}
  * {% include text-color.html color="red" text="Alpha v.0.4 - Complete Tadukoo Java" %}
  * {% include text-color.html color="red" text="Others TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0" %}
* [{{TadukooWebServices.title}}]({{TadukooWebServices.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.1.2" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1 - Complete Tadukoo REST - Released February 6, 2021 9:26 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1.1 - Java 16 and Tadukoo Parsing Alpha v.0.3 - Released April 25, 2021 11:18 AM" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.1.2 - Tadukoo Parsing Alpha v.0.3.1" %}
  * {% include text-color.html color="red" text="Alpha v.0.2 - Complete Tadukoo SOAP" %}
  * {% include text-color.html color="red" text="Others TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0" %}
* [{{TadukooGitHub.title}}]({{TadukooGitHub.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.1.2" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1 - Complete Get Releases endpoints - Released February 6, 2021 10:22 PM" %}
  * {% include text-color.html color="lime" text="Alpha v.0.1.1 - Java 16 and Tadukoo Web Services Alpha v.0.1.1 - Released April 25, 2021 11:40 AM" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.1.2 - Tadukoo Web Services Alpha v.0.1.2" %}
  * {% include text-color.html color="red" text="Others TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0" %}
* [{{TadukooEngine.title}}]({{TadukooEngine.url}}) - {% include text-color.html color="yellow" text="Working on Alpha v.0.1" %}
  * {% include text-color.html color="yellow" text="Alpha v.0.1 - Informational Files" %}
  * {% include text-color.html color="red" text="Alpha v.0.2 - Auto-Updating" %}
  * {% include text-color.html color="red" text="Beta v.0.? - TBA" %}
  * {% include text-color.html color="red" text="Release v.1.0 - Needs Planning" %}

## Update 9/2/2020
Tadukoo Util is almost at the Alpha v.0.1 milestone (there's some testing left for the maps package at the moment), so now seems like a good time to clarify (and/or change) some things.

Tadukoo Util and Tadukoo Engine/Launcher will be tied together for release v.1.0 as said before, but the other projects will not have the same requirement. Tadukoo Engine/Launcher will 
not use the full Tadukoo GitHub project (e.g. why would we need to worry about GitHub issues in the engine/launcher? The main thing we need is the releases on GitHub). So it doesn't 
make sense to wait for Tadukoo GitHub to be complete to release the engine/launcher. In addition, GitHub uses REST, and so wouldn't need other types of services supported in Tadukoo 
Web Services. Also GitHub uses JSON, so we wouldn't need the XML support in Tadukoo Parsing. For all 3 projects (Parsing, Web Services, GitHub), we don't need the full release (and 
it's not planned what the full release of those will look like either). All of those could simply be Alpha v.0.1 when we release the Tadukoo Engine/Launcher, the only requirement is 
we have all the stuff we need and that it's a stable release (doesn't have to be a v.1.0 release, just stable enough that it's properly tested and works and is supported moving forward). 
As of right now, I still do not have a solid plan for Tadukoo Engine/Launcher and those 3 projects, but will likely figure it out soon after this Alpha v.0.1 milestone is complete for 
Tadukoo Util.

Regarding Tadukoo Util, there's the question of publishing it to Maven Central. I have taken steps to be able to do so, but do not plan to until it gets to Beta v.0.5. The reason for this 
is that while the Annotation Processor, Lang, and Util modules will be good at this milestone, the Look & Feel, View, Database, and File Format modules are not in a good releasable state. 
Publishing to Maven Central as a release in this state just doesn't feel right. Beta v.0.5 will represent the entire project being in a decent releasable state, though it's currently also 
equivalent to release v.1.0, which could also be a problem (releasing the same thing as two different versions). We'll have to wait until we get closer to that point before making a firm 
decision on it. We likely won't have this problem with the Parsing, Web Services, and GitHub projects due to not starting out in a weird place like Tadukoo Util did (I basically threw 
stuff from various projects into Tadukoo Util and am cleaning them up).

Another note with Tadukoo Util is that the milestone goals are not meant as restrictions, so there can be changes to the modules in later milestones (e.g. adding to the Util module during 
Alpha v.0.2 or to the View module during Beta v.0.5). I'm saying this because I'll likely add to the Lang and Util modules during several of the milestones moving forward, as those modules 
are meant to have general useful utilities added to them over time for use in projects.

## Update 9/5/2020
Now that I've released [{{TadukooUtil.title}}]({{TadukooUtil.url}})'s Alpha v.0.1 release on GitHub, let me update this. Note that it will be a release on GitHub, but not on Maven Central. 
To use it from Maven, you will need to use the snapshots repository at the moment (with version string 0.1-Alpha-SNAPSHOT).

I realized planning Tadukoo Parsing for the master plan is simple. All we need is to finish Tadukoo JSON (the module dealing with parsing to/from JSON), since the GitHub REST API only 
uses JSON. This will be Alpha v.0.1 of Tadukoo Parsing. Future versions will include more formats, such as XML, etc., but they're not needed for the Engine/Launcher for this plan. I 
will also need to transfer it to Tadukooverse, prepare the Javadocs, do proper testing, etc. of course, but as for the code itself, it's just the JSON parsing.

For all the projects, I will need to prepare them for use with [{{TadukooEngine.title}}]({{TadukooEngine.url}}) as part of the plan, so each of them will have a milestone for that. For 
now most of them will be unnamed due to not having solid plans beyond that though.

Tadukoo Util still needs a few changes now that it's over on Tadukooverse. It doesn't have a readme on its project, and it doesn't have proper issues for Alpha v.0.2 and higher. Also, 
now that it's in more of a proper setup, it needs to follow proper procedures for GitHub branches, issues, etc. in general. For this, I need to make some guides on this website so 
others can follow the guidelines. I wasn't exactly following everything appropriately up to this point due to the software being in a weird state from the start, but now that it's 
in an acceptable place, I can and ought to start following proper guidelines (excluding placing the readme, since that should've been there much earlier).

## Update 10/9/2020
As I've been working on Alpha v.0.2 for the Tadukoo Look & Feel, I've been doing a lot of work on Tadukoo View, and even doing more work on it than my work on the Look & Feel module. 
I've made Gradient stuff and Font stuff for Tadukoo View, and I'll be doing stuff with Shapes and Borders soon too. So Tadukoo View will be in a pretty good state when those are finished, 
just potentially needing some cleanup on the classes that already existed in it. At first I was thinking I'd just make it so Alpha v.0.2 counts as the first release for both Tadukoo View 
and Tadukoo Look & Feel (while maintaining the current milestone goals), but I've realized it makes a lot more sense to just swap the milestone goals. That way, I can release Alpha v.0.2 
earlier (in theory), and still maintain the idea of making each module have its first release separate (instead of having Tadukoo View be the weird exception).

So Alpha v.0.2 will now include supporting custom Shapes and Borders, creating forms, moving over anything from the Old Tadukoo View that's relevant, and potentially some other utilities. 
I'll also throw in the custom defaults option for the Tadukoo Theme, so that at least to some extent Tadukoo Look & Feel is usable (though not official yet until Alpha v.0.3 now)

Alpha v.0.3 will now have the current Alpha v.0.2 goals of completing Tadukoo Look & Feel.

As for other projects, I'm going to say that Tadukoo Web Services will have a release for "Tadukoo REST" (supporting general REST services) as its Alpha v.0.1 milestone necessary for the 
engine stuff. Tadukoo GitHub will have an Alpha v.0.1 of supporting the Releases endpoints of GitHub for use in the engine. Other than that, I don't have a solid plan for those, that's 
just the main stuff needed to complete the engine/launcher like I plan to at the moment, and plans can change as I get closer to that release.

## Update 11/7/2020
[{{TadukooUtil.title}}]({{TadukooUtil.url}}) Alpha v.0.2 is now released, so progress can start on Alpha v.0.3 of it.

Alpha v.0.2 of it also had some changes that impact Tadukoo JSON, so now I can properly release that in the near future (the other Tadukoo Util updates shouldn't impact Tadukoo JSON). 
I will probably release Tadukoo JSON Alpha v.0.1 before I release Tadukoo Util Alpha v.0.3, since it's probably closer at this point (both have progress due to how I've worked on them). 
Getting Tadukoo JSON released completes progress I need in order to work on Tadukoo GitHub, and to use Tadukoo Web Services with JSON, so working on it sooner than later would be nice.

## Update 11/10/2020
[{{TadukooParsing.title}}]({{TadukooParsing.url}}) Alpha v.0.1 is now released for Tadukoo JSON. Because of this, Tadukoo Web Services will likely be worked on next (potentially with 
starting work on Tadukoo GitHub finally).

I've noted that the "Prepare for Tadukoo Engine/Launcher" goals for Tadukoo Parsing, Web Services, and GitHub may not be needed. This is noted because it's possible that there will be 
no changes necessary after their previous releases, and thus we can just use Alpha v.0.1 of each for Tadukoo Engine/Launcher v.1.0 (their versions aren't to be tied to the engine/launcher 
in any way like Tadukoo Util is).

## Update 12/16/2020
I released Alpha v.0.2.2 of [{{TadukooUtil.title}}]({{TadukooUtil.url}}) a few days ago, which also includes splitting pieces of it into different projects, some of which are completely 
new projects, some already existed. Basically I decided that Tadukoo Util should only be the most basic stuff that actually every program would use, so not every program would use a 
database, or even have a GUI (there could be command line programs that use Tadukoo Util or whatever). The Engine/Launcher will still include most of the stuff by default, or it will 
be like other libraries, where you can easily handle dependencies for the stuff. For Tadukoo Util itself, there's a new release planned (Alpha v.0.3) to add more functional interfaces.

[{{TadukooAnnotations.title}}]({{TadukooAnnotations.url}}) is a new project that contains Tadukoo Annotation Processor and the @ShouldBeFinal annotation that was in Tadukoo Util. 
Tadukoo Annotations probably won't be touched again as part of this "master plan", because it was meant more for after the official release of the engine anyway, as a way of doing 
stuff for backwards compatibility.

[{{TadukooDatabase.title}}]({{TadukooDatabase.url}}) is a new project that contains the old Tadukoo Database module, now called Tadukoo MySQL. The plan is to still finish this module 
for the engine, for programs that will use MySQL databases. There are currently no other plans for it, but that could change by release of the engine, of course.

[{{TadukooParsing.title}}]({{TadukooParsing.url}}) already existed, but now it has Tadukoo File Format, which still needs completed for the engine. Also, Tadukoo Java got a partial 
release due to being present when I moved Tadukoo File Format over. Tadukoo Java will probably also be completed for the engine's official release.

[{{TadukooView.title}}]({{TadukooView.url}}) is a new project that contains the old Tadukoo Look & Feel and Tadukoo View modules from Tadukoo Util. Tadukoo View was split into 3 
modules - Tadukoo View, Tadukoo Components, and Tadukoo Form. Tadukoo Look & Feel still needs completed for the engine, and there will likely be more changes in this project in 
preparation for the engine, as we need a way to switch between forms.
