---
date: 2000-01-01T10:00:00+01:00
draft: false
slug: tracker-free
title: "Tracker Free"
---
TL;DR: This theme is modified lovingly to reduce your exposure to the global surveillance apparatus,
meaning Google, Cloudflare, Facebook, and other "social" sites. You should take this and other
aspects of privacy and rights seriously.

## The Problem
The internet was never designed with privacy in mind. That isn't because privacy wasn't important
to its inventors, rather it was because they never saw the abuses coming.

Today, most sites will instruct your browser, deliberately or accidentally, to reveal to Google
(almost certainly), and a variety of other bad actors, that you have visited. You, gentle reader,
and not merely "someone", because thanks to browser profiling, cookies, and a host of other
factors you can usually be identified with uncanny accuracy even if you think you're logged out
and incognito.

Some of the ways this happens:

* Deliberate efforts by the website owner to spy on you, by installing Google "Analytics"
  (spyware) scripts and other trackers. Ethical website owners run their own analytics
  applications, but they are few and far between.
* Using proprietary browsers like Google Chrome, MS Edge, Apple Safari, etcetera, that are designed
  specifically to spy on you.
* Loading of Images, Videos, Fonts, CSS files and Javascript from "Content Delivery Networks" and
  repositories. Most such repositories for CSS and JS are owned by Google, and of course the
  biggest video repository is Google-owned, also. Whenever you request these files, you announce
  who you are.
* Third-party cookies, which, if enabled, scream vigorously who you are and where you are. Turn
  these off in your browser, they are not required for anything and you won't suffer for it.
  They are toxic and unnecessary.
* Non-https connections, which let anyone between you and the site observe you and even inject
  malicious code to track you even more viciously. ISPs around the world have been caught injecting
  such malware into customers' traffic many times.
* Intermediation by CloudFlare, who get to spy on your traffic whenever you visit a "protected"
  site. CloudFlare and other load balancers are usually not required by the sites that use them,
  and their on-top position makes them the perfect passive spy.

## Solution and Suggestions
This theme builds upon the Blackburn theme for Hugo, to remove trackers wherever I could find
them and to locally serve all Javascript, CSS, fonts, and images. Wheresoever I could, I have
removed all means of tracking that are within my power to control. For everything else, it's your
responsibility to start protecting yourself.

At the minimum, I suggest the following steps to improve your privacy. All of these apply equally
to Firefox for Android as to Chromium or Firefox.

1. Disable "Third-Party" Cookies (the most awful kind) in your browser. They all make this awkward and hide it,
   because they all (to varying extents) profit from injuring your privacy. Go to the effort of finding out how,
   and do it right away. You will never need them, and you won't regret it.
1. Install [HTTPS Everywhere in your browser][httpseverywhere]
1. Install [uBlock Origin ad-blocker][ublock], and enable some of the better tracker/privacy lists.
1. Install [Self-Destructing Cookies][sdcookies] in Firefox, and [Vanilla Cookies][vanilla] in Chromium, and
   configure them to preserve only the cookies you need for your favourite sites and logins.

[httpseverywhere]: https://eff.org/https-everywhere
[ublock]: https://www.ublock.org/
[sdcookies]: https://addons.mozilla.org/en-US/firefox/addon/self-destructing-cookies/
[vanilla]: https://chrome.google.com/webstore/detail/vanilla-cookie-manager/gieohaicffldbmiilohhggbidhephnjj
