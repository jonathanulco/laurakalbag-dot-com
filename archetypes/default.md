---
title: "{{ replace .TranslationBaseName "-" " " | title }}"
date: {{ .Date }}
draft: true
body_classes: "blog"
image: ""
description: ""
colours:
    primary-bg: "0,0%,91%" # hsl(0,0%,91%)
    secondary-bg: "0,0%,82%" # hsl(0,0%,82%)
    text: "0,4%,26%" # hsl(0,4%,26%)
    linktext: "0,0%,19%" # hsl(0,0%,19%)
    darklinktext: "0,0%,1%" # hsl(0,0%,1%)
    brilliant: "180,1%,50%" # hsl(180,1%,50%)
    tab-two: "0,0%,84%" # hsl(0,0%,84%)
    tab-three: "180,2%,78%" # hsl(180,2%,78%)
    tab-four: "180,2%,71%" # hsl(180,2%,71%)
    tab-five: "0,0%,64%" # hsl(0,0%,64%)
    tab-six: "180,1%,57%" # hsl(180,1%,57%)
---

Default text<!--more-->

{{< figured caption="caption text" >}}

    {{< imgsrcset original="filenameX" alt="alt text" >}}

{{< /figured >}}