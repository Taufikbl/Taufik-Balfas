---
title: New in Chrome 60
description: >
  With Chrome 60, you can now measure time to first paint and time to first
  contentful paint with the Paint Timings API. You can control how fonts are
  rendered with the font-display CSS property. WebAssembly has landed and
  there's plenty more!
layout: 'layouts/blog-post.njk'
date: 2017-07-27
authors:
  - petelepage
hero: 'image/0g2WvpbGRGdVs0aAPc6ObG7gkud2/yP5iyf5SXH13fD8gxOiJ.png'
alt: 'Cropped Chrome logo on the left, version number on the right.'
tags:
  - new-in-chrome
  - chrome-60
---

{% YouTube id='vE7JTf2_-ws' %}

* [Paint Timing API](#paint) allows you to measure time to first paint and
  time to first contentful paint with the Paint Timings AP.
* The [`font-display`](#fontdisplay) allows you to control how fonts are
  rendered before they're downloaded.
* [WebAssembly](#wasm) has landed
* And there's [plenty more](#more)!

Want the full list of changes? Check out the
[Chromium source repository change list](https://chromium.googlesource.com/chromium/src/+log/59.0.3071.80..60.0.3112.78?pretty=fuller&n=10000)

I'm [Pete LePage](https://petelepage.com/). Let's dive in and see what's new for developers in Chrome 60!

## Paint timings API {: #paint }

When a user navigates to a web page, they're look for some visual feedback
to reassure them that everything is working. With the new paint timings API,
we can now measure that.

The API exposes two metrics:

* **Time to first paint** - which marks the point when the browser starts
  to render something, the first bit of content on the screen.
* **Time to first contentful paint** - which marks the point when the browser
  renders the first bit of content from the DOM, text, an image, etc.

{% Img src="image/0g2WvpbGRGdVs0aAPc6ObG7gkud2/Bwe8cTocyJGd5wNiaFMm.png", alt="", height="279", width="800" %}

Check out
[Leveraging the Performance Metrics that Most Affect User Experience](https://developers.google.com/web/updates/2017/06/user-centric-performance-metrics)
to learn how you can track these metrics and use them to improve your
experience.

## CSS `font-display` property {: #fontdisplay }

Web Fonts give you the ability to incorporate rich typography. But, if the
user doesn't already have the typeface, it needs to be downloaded,
potentially making your site appear slow.

Thankfully, most browsers will use a fallback if the font takes too long to
download. The new `font-display` property, allows you to control how a
downloadable font renders before it's fully loaded.

* **`auto`** uses whatever font display strategy the user-agent uses.
* **`block`** gives the font face a short block period and an infinite
  swap period.
* **`swap`** gives the font face a zero second block period and an infinite
  swap period.
* **`fallback`** gives the font face an extremely small block period and a
  short swap period.
* **`optional`** gives the font face an extremely small block period and a
  zero second swap period.

It's supported in Chrome 60 and Opera, and is in development on Firefox.
Check out
[Controlling Font Performance with `font-display`](https://developers.google.com/web/updates/2016/02/font-display)
for more information.

## WebAssembly {: #wasm }

{% YouTube id="6v4E6oksar0" %}

Web Assembly or wasm provides a new way to run code, written in languages like
C and C++ on the web, at near native speed.

It provides the speed necessary to build an in-browser video editor or to run
a Unity game at a high frame rate utilizing existing standards-based web
platform APIs.

You can find more info at [webassembly.org](http://webassembly.org), including
demos, docs and how to get started.

## And more! {: #more }

* The new [Web Budget API](https://developers.google.com/web/updates/2017/06/budget-api)
  enables sites with the Push Notification permission to send a limited number
  of push messages that trigger background work such as syncing data or
  dismissing notifications, without the need to show a user-visible notification.
* [`PushSubscription.expirationTime`](https://w3c.github.io/push-api/#dom-pushsubscription-expirationtime)
  is now available, notifying sites when and if a subscription will expire.
* [Object rest & spread](https://developers.google.com/web/updates/2017/06/object-rest-spread)
  properties are now supported, making it simpler to merge and shallow-clone
  objects and implement various immutable object patterns.

**Note:** The [Payment Request API](https://developers.google.com/web/fundamentals/discovery-and-monetization/payment-request/)
was pushed to Chrome 61.

These are just a few of the changes in Chrome 60 for developers.

Then [subscribe](https://goo.gl/6FP1a5) to our
[YouTube channel](https://www.youtube.com/user/ChromeDevelopers/), and
you'll get an email notification whenever we launch a new video.

I'm Pete LePage, and as soon as Chrome 61 is released, I'll be right
here to tell you -- what's new in Chrome!
