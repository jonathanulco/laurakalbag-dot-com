---
title: 17 July 2018 18:08 IST
date: 2018-07-17T18:08:36+01:00
tags: []
categories: []
visibility: ["public"]
body_classes: "notes latest"
colours:
    primary-bg: "3,100%,92%" # hsl(3,100%,92%)
    secondary-bg: "5,100%,89%" # hsl(5,100%,89%)
    text: "195,100%,20%" # hsl(195,100%,20%)
    linktext: "195,100%,25%" # hsl(195,100%,25%)
    darklinktext: "195,70%,14%" # hsl(195,70%,14%)
    brilliant: "196,100%,42%" # hsl(196,100%,42%)
    tab-two: "278,9%,83%" # hsl(278,9%,83%)
    tab-three: "205,35%,76%" # hsl(205,35%,76%)
    tab-four: "199,52%,67%" # hsl(199,52%,67%)
    tab-five: "197,62%,59%" # hsl(197,62%,59%)
    tab-six: "196,68%,51%" # hsl(196,68%,51%)
twitterurl: ""
mastodonurl: ""
instagramurl: ""
forumurl: "https://forum.ind.ie/t/cross-posting-and-automating/2220"
---

I seem to be doing a lot of cross-posting content in different locations. Not just farming out links all over the place, but cross-posting because the discussions we have in different locations (Twitter vs Mastodon vs here) are all valuable in their own ways.

This is in conjunction with Aral and I focusing more on our personal sites ([ar.al](https://ar.al) and [laurakalbag.com](https://laurakalbag.com). As we’re looking at how [what we’re building](https://ar.al/2018/06/26/web+/) works in conjunction with/layers on top of personal sites. 

[Aral has put together a setup where he can blog from a phone](https://www.ar.al/2018/07/05/web+-on-a-phone/). I have added a [Notes section on my site](https://laurakalbag.com/notes/) where I can post short-form stuff like photos and statuses (anything shorter than a blog post, really.) Though my setup is a little more static than Aral’s, as it is literally a static site built using [Hugo](https://gohugo.io) and I use an iPhone. So no posting from a phone for me. (Yet.)

[The idea is that the Notes section of my site is the canonical location for those bits of content](https://laurakalbag.com/owning-and-controlling-my-own-content/). Then I can cross-post to other locations. (This is similar to [IndieWeb](https://indieweb.org) concepts.)

However, **manual cross posting is a pain**. If I post a note to my site (create post, write in markdown, push to Git, deploy), I then have to manually go to wherever I want to cross-post (Twitter, Mastodon, Facebook, here etc) , rewrite the content/link to content in an acceptable format (under 260 chars etc), and post. The whole exercise takes time. It may be a worthwhile endeavour for a blog post about something meaningful. But it’s a lot of faff to share [a dog photo](https://laurakalbag.com/notes/2018/06/14/21/59/) or [a “subtweet”](https://laurakalbag.com/notes/2018/06/29/09/25/), let alone a reply or reposting of somebody else’s content.

Which finally brings me to my point… how do I make cross-posting easier?

Right now, I have an [IFTTT](https://ifttt.com) recipe that takes my RSS feed and publishes new posts to Twitter. [Like this on Twitter](https://twitter.com/laurakalbag/status/1015706163365732352).

It’s not great. It is only for Twitter (IFTTT doesn’t support Mastodon.)

How do I do this better? 

One extreme side is that I could build and maintain my [own interface for cross-posting like Jeremy has](https://adactio.com/journal/10728). There are alternatives to IFTTT like  [Trigger Happy](https://trigger-happy.readthedocs.io/en/latest/). Though some social networks (such as Instagram) only let you post from their interface, so this solution will never be entirely compatible with those particular walled gardens. Also, I’m not being defeatist in saying these solutions are somewhat [beyond my means](https://laurakalbag.com/beyond-my-means/).

The other extreme (the low-tech solution) is that I have a to-do list template for every time I post something to make sure I format my posts correctly, and don’t forget a particular social network.

If anyone has any ideas or thoughts on the matter, [I’d love to hear them!](https://forum.ind.ie/t/cross-posting-and-automating/2220)
