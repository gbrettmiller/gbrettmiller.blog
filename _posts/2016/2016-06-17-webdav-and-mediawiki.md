---
title: "WebDAV and MediaWiki"
date: "2016-06-17"
categories: 
  - "pound-of-obscure"
tags: 
  - "blue-spice"
  - "emwcon"
  - "emwcon-2016"
  - "enterprise-mediawiki"
  - "hallo-welt"
  - "mediawiki"
  - "webdav"
---

A few weeks back at [EMWCon 2016](https://gbrettmiller.com/2016/05/26/emwcon-2016-some-notes-day-2/), Angelika Müller from [Hallo Welt!](http://hallowelt.com/) spoke about the sales life cycle for enterprise wiki services, featuring their  [Blue Spice](http://bluespice.com/) MediaWiki Enterprise Distribution. During her talk, Angelika hinted at a project they had completed for some customers\* involving [WebDAV](http://www.webdav.org/). Unfortunately, the constraints of that engagement prevented them from speaking openly about it at the conference; the one year "gag order" was set to expire a few days **after** the conference.

![wikiDAV0.png](images/wikidav01.png)Well, that gag order is up and the Blue Spice team invited us to join a webinar today to show of what they've done. Very cool stuff. _(I have some screengrabs from the webinar, but they are on a different computer. I will add them in tomorrow.)_ 

The webinar was a demo conducted by [Markus Glaser](https://twitter.com/mrglaser) from the Blue Spice team, showing off how the WebDAV integration with [MediaWiki](https://www.mediawiki.org/wiki/MediaWiki), through Blue Spice, works. For those not familiar, WebDAV

> stands for "Web-based Distributed Authoring and Versioning". It is a set of extensions to the HTTP protocol which allows users to collaboratively edit and manage files on remote web servers.

Basically, it lets you interact with files on a remote web server as if they were local files. In the enterprise this typically means Microsoft Office files from a Windows computer.

To start the demo, Markus showed how you can access a wiki through Windows Explorer, with the ability to open and edit the actual wiki articles. Though this is a cool feature, as Markus noted it not an especially interesting use case. Opening a page and editing it on a text editor on your computer will be slower and more cumbersome than simply editing the page on the wiki, and you will still need to use wikitext for the content.

The really interesting, and valuable, aspect of WebDAV integration with wiki goes back to those MS Office files. With the access to the wiki through Windows Explorer, you can directly add files to the wiki through your computer file system. For example by dragging and dropping from another folder, or simply saving a new file to the Media folder (aka namespace) on the wiki.

In addition to adding files through Explorer you can open, edit, and save the file as if the file were stored locally on your computer. Which is, of course, what WebDAV does. The really great part, though, was that you can also open the file from within the wiki, edit it, and save it directly back to the wiki. No downloading, editing, and then uploading again. If you've ever had to do that, you know how nice this feature is. In both cases, the versioning info is maintained on the file's wiki page.

One of the challenges with the way MediaWiki handles files, of course, is that they typically all go into a single namespace, such as "File". Not only does this make it hard to keep things organized, all of the files have the same permissions. To address this, Markus demonstrated the [Extension:NSFileRepo](https://www.mediawiki.org/wiki/Extension:NSFileRepo) in action.

> The **NSFileRepo** extension restricts access to upload and read files and images to a given set of user groups associated with protected namespaces. Using this extension (within the security limitations noted above), you can protect not only pages and areas of your wiki, but also any uploaded images or files within those namespaces.

The WebDAV integration can be used on a "vanilla" MediaWiki install, but some of the features Markus demonstrated today are specific to Blue Spice. Installation is a bit more involved than simply installing an extension; the way that WebDAV works requires some web server configuration as well.

**tl;dr** Using WebDAV integration with MediaWiki provides a much more user friendly experience for uploading and working with files on MediaWiki.

\[gallery ids="11258,11260,11261,11262" type="slideshow" link="file"\]

_\* They built the WebDAV integration as a crowdsourced project, where several customers contributed to the project to ensure it was fully funded. Those customers agreed to making the project available to general customers, but only after a certain amount of time (a year) had passed. An interesting approach to getting open source work funded, one I'll probably come back to again later._
