---
title: "Squashing Trackers"
date: 2018-09-12T13:58:19+01:00
draft: true
tags: []
categories: []
type: "post"
body_classes: "blog"
colours:
    primary-bg: "58,95%,83%" # hsl(58,95%,83%)
    secondary-bg: "60,76%,76%" # hsl(60,76%,76%)
    text: "212,47%,25%" # hsl(212,47%,25%)
    linktext: "193,100%,19%" # hsl(193,100%,19%)
    darklinktext: "0,0%,0%" # hsl(0,0%,0%)
    brilliant: "208,100%,44%" # hsl(208,100%,44%)
    tab-two: "83,45%,80%" # hsl(83,45%,80%)
    tab-three: "152,28%,74%" # hsl(152,28%,74%)
    tab-four: "189,37%,64%" # hsl(189,37%,64%)
    tab-five: "200,54%,57%" # hsl(200,54%,57%)
    tab-six: "205,68%,51%" # hsl(205,68%,51%)
image: ""
imagealt: ""
description: ""
---

Post text<!--more-->

{{<figure class="note-image" src="office-dog.png" link="https://alink.com" alt="alt text" caption="caption text">}}

Log

1. Go to my email and issues on source.ind.ie to see what I’m going to tackle today.
2. For each site reported broken with Better I:
    a. Load the site up in Safari on macOS, see if I can see the problem
    b. Load the site up in Safari on iOS, see if the problem occurs there too
    c. If I can’t reproduce the problem, I respond to the person who reported it asking them for more information.
    d. If I can reproduce the problem, I make an issue for it on source.ind.ie content, or re-open an old issue if it’s an old problem recurring, 
    e. For each issue, I take screenshots of the problem on macOS and iOS, copy paste the contents of the console, and include details as reported by the person, and/or my own suspicions for what’s causing the problems
    e. If it’s an issue I don’t think I can handle today, I make an issue for it and let the person reporting the problem that it’s on my list
3. Add all the issues I think I can handle today to a Milestone. Things I prioritise: popular sites, trackers with an epidemic status, blocker blockers, problems where we’ve had reports from multiple people
4. Set up my working environment, starting with pulling all the relevant repositories to my machine
5. Start with the oldest issue first.
6. Run an inspection on the site to find the trackers
7. Commit the trackers whose prevalence have been updated after running the inspection
7. Compare the list of trackers found with the list of trackers we’re already blocking
8. For each tracker we are not yet blocking:
    a. Paste the URL into Safari to see what the tracker is
    b. If the site loads:
        i. If it’s not a tracker (e.g a site’s own CDN domain), I move on
        ii. If it is a tracker of some kind, I try to get a vague idea of what it does from the site, but inevitably end up reading their privacy policy to truly understand what they might be doing with a site visitor’s information
        iii. Copy the tracker from the inspector’s drafts to the block list
        iv. Fill out information about the tracker including a description from a neutral party, and key excerpts from their privacy policy. Things I pay particular attention to: who the policy applies to, what information is collected, what technology is used to collect information, who the information is shared with
    c. If nothing loads on the URL:
        i. Do a whois lookup to see who owns it. If they (as a commercial entity) use a privacy service to obscure their ownership, that’s a big red flag for dodginess, and I note this in the tracker notes
        ii. If I can’t find them using whois lookup, search the web til I work out who it is, and note how I found out in the tracker notes
9. Run Better locally to see if blocking the new trackers have fixed the problem
11. If trackers are effectively blocked/unblockers unblocked/broken site fixed, I commit the changes to the repository
12. When I’ve fixed all the issues/run out of time, I push the changes to the content repository