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
comment_issue_id: 
---
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
