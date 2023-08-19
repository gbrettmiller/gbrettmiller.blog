---
title: "EMWCon 2016 - some notes (day 1)"
date: "2016-05-25"
categories: 
  - "pound-of-obscure"
tags: 
  - "emwcon-2016"
  - "enterprise-mediawiki"
  - "liveblog"
  - "mediawiki"
  - "nyc"
coverImage: "emwcon_banner.jpg"
---

A live blog (of sorts) for [Enterprise MediaWiki Conference (EMWCon) 2016](https://www.mediawiki.org/wiki/EMWCon_Spring_2016). The conference is also being [livestreamed](http://livestream.com/internetsociety/emwcon/).

## Panel - Towards a MediaWiki Foundation

![EMWCon_panel1](images/emwcon_panel1.jpg)

Cindy Cicalese, Anja Ebersbach, Mark Hershberger, Chris Koerner, Yaron Koren

Panel discussion to address some of the challenges around the development, maintenance, and use of MediaWiki and related software (extensions). Not a discussion of separating Wikipedia ops from MediaWiki core (which would be something similar to how WordPress is set up).

Yaron presented a [case for a MediaWiki foundation](https://www.mediawiki.org/w/index.php?title=File:EMWCon_Spring_2016_-_EMW_Foundation.pdf) that would help fund "unfunded" software. Specifically, funnel money from the users of the software to the developers of the software. Similar to other open source "foundations", example given was the Linux Foundation. aka pay to play.

Part of the challenge is that the Wikimedia foundation is focused almost exclusively on Wikipedia and their other projects. Desire is to make sure that the MediaWiki software remains usable by other 3d party users, and actually includes development specifically to meet the needs of those 3d party users. For example, the [MediaWiki Stakeholders Feature Wishlist](https://www.mediawiki.org/wiki/MediaWiki_Stakeholders%27_Group/Tasks/Feature_wishlist).

An interesting mess.

## Social Semantic

![EMWCon_jCantRoot](images/emwcon_jcantroot.jpg)

[Jason Bock](https://www.mediawiki.org/wiki/User:Jcantroot) talking about applying [SMW to achieve social objectives](https://www.mediawiki.org/wiki/File:Social_Semantic-_EMWCon_May_25_2016.pdf) on MediaWiki: standard profiles, rate/review articles, user point system, user badges. Shared some of the specific extensions used.

It is possible to create a template for userpages and have it pushed automatically, need to get user feedback on whether they like this or not. Some people prefer freeform userpage. Balance between user needs / desires and the enterprise's needs.

All uses existing extensions, doesn't require any development just "front end" SMW work. Walked through examples the "code" for each. This has potential to cause significant performance issues, will work to have some of this turned into extensions.

Questions about gamification: how do you handle cheating (don't really), has it helped with adoption (with some people).

## Improving Enterprise Findability with SMW

Laurent looking at how SMW can be used to help people find answers to their questions.

"Searching doesn't give you answers, it gives you search results."

Use the wiki as a wiki; keep it lean and fast. Use APIs to access other systems. Such as WordPress.

## Lightning Talks

### MediaWikiFarm extension

Nicolas Nallet talking about the [MediaWikiFarm extension](https://www.mediawiki.org/wiki/Extension:MediaWikiFarm). [Slides from the talk](https://www.mediawiki.org/wiki/File:MediaWikiFarm_Extension_Presentation.pdf).

### US Federal Government MediaWikis

[Peter Meyer](https://www.mediawiki.org/wiki/User:Econterms) talking about MediaWiki installations in U.S. Federal Government. [Full notes](https://www.mediawiki.org/wiki/User:Econterms/U.S._Federal_Government_MediaWikis). Something to follow up on - Federal MediaWiki Demonstration and Discussion Group, a monthly gathering to share ideas, practices, and demo ideas. A call for a more consistent coherent wiki policy across the Federal Government.

"Knowledge management is not a curse word." -- Peter Woudsma

## Lunch

## Wiki Farms (again)

Peter Woudsma. Reasons for multiple wikis: ownership, access, control, processing. Defined: MediaWiki server install that includes core and some extensions and supports multiple otherwise independent wikis. Went through an example putting three wikis on one MediaWiki server. Reasons to use common elements: data re-use, template re-use, branding, data processing (inter-wiki data data exchange, queries, transposition)

Question: how much is common to all wikis in the farm? Many possible options.

Discussion among the group about approaches they have taken.

 

## SMW Factory

[Lex](https://www.semantic-mediawiki.org/wiki/User:Lex) Sulzer spoke about [SMW Factory](https://smw-cindykate.com/main/Component_947746). Offline, secure, encrypted, backup (and a bunch of other terms). Duplicity, Vagrant, Ansible (executable documentation). Details in the link. An easy way to "clone" a wiki soyou can work on it offline, then push changes back to production. (Meant for dev, not content.)

Ultimate goal - ability to have "offline" wikis that can be updated and merged back in with the main wiki. This would be huge. A project for Friday.

## Single enterprise wiki

[me](https://www.mediawiki.org/wiki/EMWCon_Spring_2016/Merits_and_Challenges_of_a_Single_Enterprise_Wiki)

## What's new in Semantic Forms

Jaron giving an update.

Change 1 - Spreadsheet display. "display = spreadsheet" Each entry becomes a separate instance of  the template on the page. Less work for admins, allows for better HTML, such as <label> (important for accessibility)

Change 2 - Some input types moved from Semantic Forms Input extension to Semantic Forms, continues a process started with other input types. Few extensions, less work for admins and developers.

Semantic Forms is now its own thing, no longer requires Semantic MediaWiki.

Change 3 - removed some params, some of the long-deprecated parameters.

Thinking of changing the name, to reduce confusion with other "semantic" things.

Important takeaway - cleaning up Semantic Forms to make it better, easier for developers and admins.

Also discussed changes to Cargo (an alternative to SMW). Key feature of note (to me) - text search of articles.

## Opening Session

![EMWCon_pw](images/emwcon_pw1.jpg)

Peter Woudsma gave a quick overview of the history of MediaWiki in the enterprise and some of the challenges of taking a tool designed as an easy way to update content and making it useful and valuable at the enterprise level. A nice summary of Enterprise aspects of previous conferences, and the need for balance in discussing the non-technical aspects along with the technical.

He gave us quite a few questions, homework if you will, to consider as the conference progresses. Not just in how we use the tools, but how we influence the future development of the tools, and the support infrastructure.

Good discussion around the philosophy and implementation. Differences between what's going on with MediaWiki software and WikiMedia. Need to show off who is using MediaWiki, and how they are using it. [WikiReport](http://www.freephile.org/wikireport).

Lex - SMW power user is critical to success. SMW is a digital co-worker.

## Introductions

Mix of corporate, government, and non-profit interests represented. People from several places in US and Europe (France, Germany, Switzerland).
