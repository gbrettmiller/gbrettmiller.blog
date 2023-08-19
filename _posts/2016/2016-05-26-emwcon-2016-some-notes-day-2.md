---
title: "EMWCon 2016 - some notes (day 2)"
date: "2016-05-26"
categories: 
  - "pound-of-obscure"
tags: 
  - "emwcon"
  - "emwcon-2016"
  - "enterprise-mediawiki"
  - "enterprise-mediawiki-conference"
  - "liveblog"
  - "mediawiki"
  - "open-source"
  - "open-source-software"
coverImage: "emwcon_banner.jpg"
---

Live-blogging (kind of) again, day 2. Also, [livestream](http://livestream.com/internetsociety/emwcon/).

**Notifications in MediaWiki**

![EMWCon_yaron](images/emwcon_yaron.jpg)

Yaron discussing the current status of notification (poor), and what would make an ideal notification system for MediaWiki. Page creation, edit, etc in different sets of pages, such as all pages, pages in namespace, etc, and certain people notified, e.g. users in a user group, specified list, users signed up to be notified, maybe external users via email.

Notification done by maybe email, [Extension:Echo](https://www.mediawiki.org/wiki/Extension:Echo), or custom webhook of some kind. Echo (you can see on mediawiki.org) is planned to be added into MW Core. Several other extensions rely on Echo.

Many potential pitfalls. Too few options not helpful, too many confusing. Regular users vs. admins vs. "superadmins".

"Looked at SharePoint for bad notification design, and SharePoint didn't disappoint."

Google Summer of Code, Yaron is co-mentoring a project to create a "page notifications extension", started this past Monday. Goal is to create a framework that covers all the possible options, to make notifications in MediaWiki useful.

Jason mentioned [Extension:Notificator](https://www.mediawiki.org/wiki/Extension:Notificator), which allows users to set up notifications of others. NASA's [Enterprise Media Wiki](http://www.enterprisemediawiki.org) team released [Extension:WatchAnalytics](https://www.mediawiki.org/wiki/Extension:WatchAnalytics) and others that provide some insight into watching.

**Inside Wiki Sales**

![EMWCON_am](images/emwcon_am.jpg)

Angelika Müller from [Hallo Welt!](http://hallowelt.com/) talking about selling wiki services, especially [Blue Spice](http://bluespice.com/), their enterprise wiki distro. Covered the basic lifecycle of sales, from contact to requirements to estimates to doing the work and shipping the final product. Challenges include technical and organizational.

All development, as much as possible, should be customer driven. After all, they are the ones who know what they want.

Discussed some of their big use cases.

- Wiki farms
- Document management - they first ask, why not use a document management tool, why a wiki? Things to address - setting rights for files, managing and editing
- Quality management

In many ways, the same challenges any design / development shop has, but some uniqueness based on the product (MediaWiki based).

A big topic of interest is how they are using WebDAV with MS Office to allow their users to edit / save MS Office documents in-place inside the wiki, instead of having to download - edit - save - upload the file.  This was developed as custom work for a group of customers who came together to fund it, with a restriction that the code for doing it could not be shared for one year (which is almost up).

Anja offered that their WebDAV developer will have a webinar next week to discuss with those who are interested.

**Lightning Talks**

**CWIX Wiki for Interoperability Testing**

An overview of the [CWIX 2016](http://www.act.nato.int/cwix) wiki.

**Making Cool Directories with MediaWiki**

Yaron showed some examples of "cool" directory sites. Can you do this with MediaWiki? Functionally, yes. Visually / UI, no.

Question: how can we make our display as cool as theirs? Important for external facing wikis, but can be useful and important internally as well.

Check out [migadv](http://migadv.com/). And MITRE's [Gestalt](https://collaborate.mitre.org/gestalt/index.php/Main_Page).

Another option is to leverage the MediaWiki API to use MediaWiki as back end and build a custom front end using Javascript, etc.

**Social Semantic**

![EMWCon_jb2](images/emwcon_jb2.jpg)

Jason Bock sharing some of the things we've been working on using SMW for bringing some social features to MediaWiki. Started with a brief overview and history of milWiki (see [milSuite article](https://en.wikipedia.org/wiki/MilSuite) on Wikipedia) and installing SMW.

If you are going to use SMW, you should definitely use Semantic Forms. "Has default form" and "has alternate form" are crucial to make sure people are using forms to enter semantic data.

Create Templates based on Queries, makes it so the user doesn't need to understand how to create queries, they can just use them. Browse pages are the most popular click from homepage, a fact of life in a hierarchical-minded organization. Query forms, with filters, provides an "Amazon" like search / filter experience.

A 12 step training guide for general users to learn how to use SMW to create their own projects, covers basic overview through the more complex concepts. Crucial if you want your users to be able to create their own solutions.

Three examples of user created semantic projects: IT ticketing system, app store, unit training.

**Lunch**

**Anatomy of a Cyber Taxonomy Development Wiki**

![EMWCon_cc](images/emwcon_cc.jpg)

[Cindy Cicalese](https://www.mediawiki.org/wiki/User:Cindy.cicalese) from MITRE ([Extensions by MITRE](https://www.mediawiki.org/wiki/Category:Extensions_by_MITRE)). Demonstrated live at the [Malware ATtribute Enumeration and Characterization](https://collaborate.mitre.org/maec/index.php/Malware_Attribute_Enumeration_and_Characterization) wiki.

Purpose of the wiki is to help generate an ontology for describing malware. Includes consistant iconography to provide better navigation and visual indicators of what you're looking at. Built around hiearchies to work ([hierarchy builder](https://www.mediawiki.org/wiki/Extension:HierarchyBuilder)?). Uses a combination of Cargo and SMW, but the only SMW still in use will ultimately be converted to Cargo. It is an example of how the two can coexist, use each where best suited. (nts: Cargo vs. SMW?)

The "Graph this page" option uses MITRE's [VIKI](https://www.mediawiki.org/wiki/Extension:VIKI) extension. Very nice, reminds me of [The Brain](http://thebrain.com/).

Cindy walked through some key aspects of the site, how it's structured and configured. Went down the rabbit hole of walking through some of the code. (I stood at the top of the hole and watched her walk around, a bit beyond my own current knowledge :-)

**Contracting with the GPL**

![EMWCon_gr](images/emwcon_gr.jpg)

[Greg Rundlett](https://www.mediawiki.org/wiki/User:GregRundlett) talking about the challenges - and joys? - of doing MediaWiki work for large enterprise clients.

Challenge 1 - Lead time: Make sure lead time and discovery are in your pricing model

Challenge 2 - Payment: Large enterprises have set processes that may not be in your best interest. Negotiate for the best terms you can get (net 14 would be good).

Challenge 3 - Insurance: E&O (errors and omissions) and general liability

Challenge 4-6 - "All Your Base Are Belong to Us". The challenge is how to convince the client to allow you to publish the custom work as GPL.

The "Master Services Agreement" is a standard contract, typically a take-it-or-leave-it thing. But, you should try to write details into the agreement where details are allowed. This is especially needed for the code, how much can you "keep" for reuse or publishing to open repos.

Collaboration and cooperation, more is needed among consultants in EMW space. _We aren't competing against each other, we are competing against the Microsofts._ 

Comment from Mark - we need more consultants like freephile as members of the MediaWiki stakeholders.

A bit of discussion - and disagreement - around GPL and how it applies to custom/proprietary code development.

**Lightning Talk**

Me - MediaWiki as part of larger Enterprise Social Network

**Technical Collaboration - WMF**

![EMWCon_ckoerner](images/emwcon_ckoerner.jpg)

Chris Koerner providing some insight into the [technical collaboration team](https://meta.wikimedia.org/wiki/Technical_Collaboration) at WikiMedia Foundation.

The team primarily focuses on supporting the WMF and its official efforts, but they do take input from 3d party users and work on things that provide value to them as well.

[Phabricator](https://phabricator.wikimedia.org/) - bug tracking. Look at in more detail later.

The team hosts several events - [developer summit](https://www.mediawiki.org/wiki/Wikimedia_Developer_Summit_2016), [hackathons](https://www.mediawiki.org/wiki/Wikimedia_Hackathon_2016), [Wikimania](https://wikimania2016.wikimedia.org/wiki/Main_Page), and others. If you are doing good things with MediaWiki, let them know so they can get the word out.

**WMF - the ongoing saga**

General discussion of topics related to the WikiMedia Foundation. Didn't catch it all, so no real notes here.
