---
title: "Cross-posting using meta information"
date: 2018-07-25T10:31:01+01:00
tags: []
categories: []
body_classes: "blog colours-001"
image: ""
description: "Writing a few blog posts last week, and cross-posting them in various locations, got me thinking about how meta information can be reused."
---

Writing a few blog posts last week, and cross-posting them in various locations, got me thinking about how meta information can be reused.<!--more-->

I started looking into the meta information in the `<head>` of each page, and how best to format it so that social networks (Twitter, Facebook, messaging apps…) would pick up on titles, descriptions and images. That way, when I share a URL from my site, if the site/app has the functionality, they can expand that URL into a preview including a nicely-formatted title, summary, and image. When a platform expands a URL like this, it also saves on the cross-posting hassle, as just posting a URL pulls in the acceptable length of text, correct number of images, and any other arbitrary platform-specific limits. I can just paste a URL into an Apple Message, Slack, Facebook, Wire, and Twitter, and those platforms do the work:

<figure> 
    <img src="/images/2018/07/on-slack.jpg" alt="On Slack the URL expands to a tiny thumbnail image, title, and summary, as well as the site’s favicon." style="max-width:482px;">
    <ficaption><p>The URL expanded on Slack</p></figcaption>
</figure>
<figure> 
    <img src="/images/2018/07/on-twitter.png" alt="On Twitter the URL expands to a thumbnail image, title, and summary." style="max-width:587px;">
    <ficaption><p>The URL expanded on Twitter</p></figcaption>
</figure>
<figure> 
    <img src="/images/2018/07/on-wire.jpg" alt="On Wire the URL just expands to include the title."  style="max-width:475px;">
    <ficaption><p>The URL expanded on Wire</p></figcaption>
</figure>
<figure> 
    <img src="/images/2018/07/on-messages.png" alt="On Apple Messages the URL expands to a large image and title." style="max-width:227px;">
    <ficaption><p>The URL expanded on Apple Messages</p></figcaption>
</figure>
<figure> 
    <img src="/images/2018/07/on-facebook.png" alt="On Facebook the URL expands to a large image, title, and summary." style="max-width:502px;">
    <ficaption><p>The URL expanded on Facebook</p></figcaption>
</figure>

An additional bonus is that if anyone else shares that URL from my site, the same preview will usually be shown, so I have some additional control.

Writing `<meta>` tags for each blog post or note could be very time-consuming, especially as [Twitter cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards.html)
 and [Open Graph](http://ogp.me)
 require different formats, resulting in (currently) sixteen meta tags on each page of my site. Fortunately, it seems like most sites pull from these same formats, or the standard `<meta name>`, `<meta author>` etc. Hugo can generate these from its [embedded templates](https://github.com/gohugoio/hugo/tree/master/tpl/tplimpl/embedded/templates), or you can use something like the [Indiego theme](https://www.indiego.org.uk), which helps with other useful meta information such as microformats. Both types of templates use either the default title and summary in your post/page and site config, but can also use the [front matter](https://gohugo.io/content-management/front-matter#readout) from each post/page to override or add additional meta information. For example, here’s the extra front matter from my [Insecure blog post](/insecure):

```
image: "/images/2018/07/weary-laura.jpg"
imageAlt: "Photo of me looking wearily at the camera."
description: "The state of sharing on the web is broken."
```

Using this front matter, the platforms use the specified image, rather than my site’s favicon, and the specified description, rather than a truncated form of the first paragraph.

When I wrote a [note about cross-posting the other week](/notes/2018/07/17/18/08/)
, I talked about manually producing summaries for different social media platforms. But when I was starting to add `description` and `image` to the front matter for my latest blog posts and site pages, I realised that the custom-written summaries and descriptions would be far more reusable if I wrote and stored them on my site, at the time of writing.

Maybe something like:

```
image: "/images/2018/07/weary-laura.jpg"
imageAlt: "Photo of me looking wearily at the camera."
description: "The state of sharing on the web is broken."
description280chars: "The state of sharing on the web is broken. After the Snowden revelations, it became clear that my sharing “content” willy-nilly was a potential danger to me. I was previously oblivious to the risk of sharing everything about myself on social media…"
description500chars: "The state of sharing on the web is broken. After the Snowden revelations, it became clear that my sharing “content” willy-nilly was a potential danger to me. I was previously oblivious to the risk of sharing everything about myself on social media. The tiniest most harmless piece of information about me could be derived in a data set somewhere to become something very meaningful (even if it’s wrong) and potentially dangerous."
```

I’d make the description lengths (280 characters for Twitter, 500 for Mastodon) generic, rather than specific to the social networks (e.g `descriptionMastodon`) as I might want to use those description lengths for other platforms, and those may not be my platforms of choice in the future.

With these custom descriptions, I can either use them for automated posting (using something like [IFTTT](https://ifttt.com) or clever API integration), or just copy and paste the text out if I want to manually post somewhere. The descriptions are stored in a memorable and canonical location.

I suspect the arrival of [image resources](https://gohugo.io/content-management/image-processing/#the-image-page-resource) and [page bundles](https://gohugo.io/content-management/organization/#page-bundles) in Hugo will help with automating meta information around images. Though I’m yet to get my head around bundles, and I’m concerned that automatically grabbing images from folders means it may not be easy to include vital meta information like alternative text.

As I continue making my site more useful and efficient, I’m sure I will find other ways to automate as much of this as possible. Nothing beats handwritten copy, but I don’t need to be writing the same thing over and over again.
