---
title: "Design choices - web browsers"
date: "2016-11-10"
categories: 
  - "ounce-of-perception"
tags: 
  - "choices"
  - "decisions"
  - "design"
  - "web-browsers"
---

In addition to the many different features implemented in the various Web browsers, there are many  different decisions and choices made in the design of the features common across browsers. Some make sense to me and some don't. For example...

**Right-clicking**

Right clicking a link provides several options for interacting with the link, the options being different based on browser features. The most common of these options, listed at the top of the right-click list, are options for opening the link,  typically "Open in new tab" or "Open in new window". In IE11, however, the top option on right-click is simply "Open".

![rightclickdesign](images/rightclickdesign.png)

What decision process went it including the "Open" option on right-click in IE11?  Did the designers think that a lot of people would want the first option on right-click to be exactly the same option as simply left clicking? Indeed, how many people right-click and select "Open" when they could simply left-click and open the link?

**Smart card authentication**

I use a smart card to authenticate to our organizational websites. Different browsers have a different visual design of the dialog for selecting certificates and entering PINs, which makes sense to match the overall visual design of the browser. But the on-screen location of these dialogs differs in interesting, and significant, ways.

In Chrome, for example, the certificate selection dialog is displayed at the center-top of the browser window while the PIN entry dialog is displayed at the center of the screen. If you have the browser in full screen this is the center of the browser, otherwise not. This can be especially irritating if you have a multi-screen setup and you are using Chrome on the non-default screen: the PIN entry dialog will show up on a completely different screen from the browser in which you are working.

In IE, on the other hand, both the certificate selection and PIN entry dialogs are displayed in the center of the browser window. Not only is this more intuitive (to me, anyway), it provides consistency of location for all actions related to logging in via smart card.

_Update: It turns out that IE doesn't do this universally. When sending a digitally signed email using the smart card in Outlook Web Access, the PIN entry window is displayed in the center of the screen (the default screen if you have more than one)._ 

Were these conscious design decisions for placement of the smart card related dialogs? Did each of the design teams look at both options (center screen and center window) and simply make a difference decision? If so, what drove that decision? Or perhaps this is just default behavior for these types of actions based on the overall design and code of the browser. Perhaps something to do with the underlying OS (in this case Windows) since smart card authentication requires interaction with the OS?

**Intentional or incidental**

These are just the two design differences that I notice most frequently, I'm sure there are many many more. I can't help wondering are these choices intentional or incidental? Is it possible to make an intentional decision about every design element? Is it desirable?

How intentional are you about the design of your products, and how much of the design simply "is"?
