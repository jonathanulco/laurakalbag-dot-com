---
title: "{{ replace .TranslationBaseName "-" " " | title }}"
date: {{ .Date }}
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

{{< figure figcaption="caption text" >}}

    {{< img src="filenameX" alt="alt text" >}}

{{< /figure >}}