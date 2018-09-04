---
title: "Custom Emoji on Mastodon"
date: 2018-09-04T09:11:42+01:00
tags: ["emoji"]
categories: ["Mastodon"]
type: "post"
body_classes: "blog"
colours:
    primary-bg: "327,100%,93%" # hsl(327,100%,93%)
    secondary-bg: "330,66%,86%" # hsl(330,66%,86%)
    text: "229,16%,19%" # hsl(229,16%,19%)
    linktext: "208,92%,30%" # hsl(208,92%,30%)
    darklinktext: "204,16%,6%" # hsl(204,16%,6%)
    brilliant: "208,63%,52%" # hsl(208,63%,52%)
    tab-two: "277,40%,86%" # hsl(277,40%,86%)
    tab-three: "235,40%,82%" # hsl(235,40%,82%)
    tab-four: "219,50%,74%" # hsl(219,50%,74%)
    tab-five: "213,56%,66%" # hsl(213,56%,66%)
    tab-six: "211,61%,60%" # hsl(211,61%,60%)
image: "/images/2018/09/toot-on-dark.png"
imagealt: "a toot in the dark Mastodon theme with a little Indie heart emoji."
description: ""
---

This morning I made an `:indieHeart:` custom emoji for Mastodon. Here are some things I learned.<!--more-->

{{<figure src="/images/2018/09/local-emoji.png" max-width="800px" alt="screenshot of the Mastodon admin showing my local instance’s custom emoji including two Indie heart emojis." caption="One of the many cool features of Mastodon is that you can create custom emoji for your instances which can be duplicated and adopted by other instances.">}}

{{<figure class="grid two" max-width="1000px" src="/images/2018/09/toot-on-dark.png" link="https://mastodon.ind.ie/web/statuses/100661113916027342" alt="a toot in the dark Mastodon theme with a little Indie heart emoji." src2="/images/2018/09/toot-on-light.png" alt2="the same toot in the light Mastodon theme with a little Indie heart emoji." caption="The :indieHeart: shortcode in action">}}

- Firstly, you need to have admin access to your instance to add custom emoji. ([Another reason to get your own instance!](/what-is-mastodon-and-why-should-i-use-it/#why-set-up-an-instance-of-one)) If you don’t have admin access, you could probably politely ask your instance’s admin to add your emoji to the instance’s list.
- You need to be able to tell what the emoji is at 20x20 pixels, as this is the standard size it’s displayed on the Mastodon web view.
- The emoji could be displayed on any colour background as different Mastodon themes have different coloured backgrounds. If you’re looking for compatibility with the (current) default Mastodon themes, check your emoji graphic with these hex colours as backgrounds: `#1F232B`, `#282C37`, `#D9E1E8`, `#E6EBF0`, `#FFFFFF`.
- Make the bounding box square, even if your graphic is tall and narrow. It looks like some apps might render all emoji as the same height and width, so this will avoid your emoji looking stretched or squashed.
- The 50KB limit for emoji files is fairly high for a simple shape, so you can afford to scale your image up to be pretty big (the indieHeart is 520x520px) so it looks sharp on screens with a higher resolution.
- Thickening lines in the graphic will make them look better when the emoji is scaled down very small, as it will increase the contrast and visibility of the lines, particularly on higher resolution screens where fine lines can appear very thin.
- You need to post a toot with the emoji shortcode in it on your own instance before it becomes available to copy by other instances.

Lastly, but importantly: the macOS screenreader VoiceOver reads “indie underscore heart, image” for `:indie_heart:` and “indie heart, image” for `:indieHeart:`.

So while `word_word` or `wordword` seems to be the standard for multiple-word emoji on Mastodon, using camel case is probably more accessible.