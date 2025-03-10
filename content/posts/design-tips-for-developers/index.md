---
title: "Design Tips For Developers"
date: 2010-11-04T16:26:24+00:00
categories: ["Design"]
tags: ["'design eye'", "bathcamp", "colour", "contrast", "CSS", "design", "fonts", "gradients", "grids", "icons", "imagery", "layout", "light", "noise", "shadows", "talk", "textures"]
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
---

This little post is based around the talk I gave at Bathcamp. [Rich Quick](http://twitter.com/richquick) came up with the great idea that, whilst [Bathcamp](http://bathcamp.org) attendees are mostly developers, a talk on design for developers was probably appropriate.

And you might have seen on [my post from last week](/bathcamp-plea-for-bad-designs-by-developers/), I was looking for a case study to use in my talk. As happens with everything, I just didn’t have time to include the case study in the talk, so I thought I would blog it here as a follow-up from Bathcamp.

## The original

[Tim Perrett](http://twitter.com/timperrett) had been asking me for a while to help redesign [liftweb.net](http://liftweb.net). Even though the design isn’t awful, and I’m not even sure whether it was done by a developer, it did need some designery love.

{{< img src="original.png" alt="liftweb.net original homepage design" >}}

## My redesign

I wasn’t aiming for a full-on redesign, more of a re-alignment of the existing design. I tried to take all the elements that I thought were successful, and continue using those, and try to improve on the areas that I thought had issues.

I’ll explain my decisions below, based on my design tips for developers. I’m only including the most relevant tips from my talk, as very few designs would cover all of them!

{{< img src="01.png" alt="my redesign of liftweb.net" >}}

## My Design Tips For Developers

1. ### Design isn’t all about having an ‘eye’

A lot of people just have an ‘eye’ for design. Knowing what looks good to the masses comes fairly easily. This doesn’t mean that if you don’t have that ‘eye’, you can’t design. A lot of design principles are based on simple theories and rules that anybody can follow.

All good designers know the rules, the best designers know how to break them effectively.

2. ### Colour

#### Contrast is the most important aspect of colour when you’re trying to make text readable

The inconsistency in colour contrast was fairly noticeable on the original Lift page. In some places, it was dark on light and in some places it was light on dark, this makes sense.

However, in the ‘Taking Off’, ‘Flying in Formation’, ‘Team’ and ‘Wiki’ pages, the descriptions are black on a dark gradient background. This makes the text harder to read, as well as drawing attention to this part of the text as it’s significantly different from the contrast patterns on the rest of the page.

{{< figure figcaption="Black on a coloured gradient is quite hard to read" >}}
  {{< img src="odd-contrast.png" alt="Black on a coloured gradient is quite hard to read" >}}
{{< /figure >}}

Contrast is something that loads of designers get wrong, as well as developers. Silly things like light grey text on a white background, a big hit with print designers. Screens are incredibly inconsistent, and our eyesight is better saved for more important things than squinting at text on a screen.

I really recommend using [Jonathan Snook’s Colour Contrast Check](http://www.snook.ca/technical/colour_contrast/colour.html). This analyses the contrast between your foreground and background colours against the WCAG guidelines. Everybody knows that guidelines are just for guidance, so I wouldn’t stress if you’re colours aren’t AAA compliant (this produces very extreme contrasts that are pretty hard on the eyes) but if you make sure your colours are AAA compliant at 18pt+ then you should be on to a readable winner.

{{< figure figcaption="Checking my redesign colour contrast on the quotes section" >}}
  {{< img src="snook-colour-contrast.png" alt="Checking my redesign colour contrast on the quotes section" >}}
{{< /figure >}}

#### If you’re going to use a strong colour, just use one

With a lot of purples and blues teamed with white, the Lift page was suffering from a bit of a 90s colour scheme. The trick is to stay away from using multiple strong colours (the dark blue and purpley blue) together.

{{< img src="original-scheme.png" alt="The original Lift main colours" >}}

To calm a design like this down, I tried using less of the extreme colour contrasts (dark blue and white) and more of the in-between, softer and more muted colours. Where I felt the purpley blues and dark blues were a bit harsh, I just toned them down to a slightly greyer version.

{{< img src="my-scheme.png" alt="My Lift redesign main colours" >}}

I then used these colours to help differentiate between areas of content. The original Lift design did a good job of emphasising the quotes at the top of the page through using dark text on a light background, where the rest of the page used the inverse. I took this theory further.

{{< figure figcaption="On the original design, you can see how the quote area stands out" >}}
  {{< img src="light-on-dark.png" alt="On the original design, you can see how the quote area stands out" >}}
{{< /figure >}}

Whilst I thought it was good to keep the quotes at the top of the page, as they’re vital to helping sell the benefits of Lift to potential high-profile groups, they’re not really as valuable as the four links below to ‘Get Started’, ‘Lift community’ etc.

As this content, and the content immediately below is most useful to the page visitors, I used the dark-on-light contrast to draw the user to those areas. It stands out more than the light-on-dark areas above as it is a greater contrast against the overall page background.

{{< figure figcaption="At this small size, you can see how my redesign colours draw the eye to the most important content" >}}
	{{< img src="dark-on-ligt.png" alt="At this small size, you can see how my redesign draws the eye to the most important content" >}}
{{< /figure >}}


2. ### Layout

#### Give everything more space, and share the space equally between the elements

When you look at the original design, what really jumps out is the huge amount of space in the middle of the page. This is caused by the amount of ‘Latest Happenings’ appearing down the right hand column. Obviously, this wouldn’t have been originally designed like this, but it emphasises the importance of imagining how the content on a page may evolve.

{{< figure figcaption="the main page content on the original Lift page" >}}
  {{< img src="original-middle.png" alt="the main page content on the original Lift page" >}}
{{< /figure >}}

I’ve limited the ‘Latest Happenings’ to only five events on my design. My reasoning being that if you have many more than that, they’re not really ‘latest’ anymore. This way we can ensure that the amount of happenings are well-balanced with the content on the left side of the page. Although the ‘What is Lift?’ content is liable to changing, I imagine that it wouldn’t increase too much more in length, as any further information and you’re going into the depths of documentation that probably isn’t suitable for a home page.

{{< figure figcaption="my redesigned main content area" >}}
  {{< img src="middle.png" alt="my redesigned main content area" >}}
{{< /figure >}}

I felt that the ‘What is Scala?’ and ‘Lift Books’ information was also a little hidden-away at the bottom of the ‘Latest Happenings’ sidebar. I brought this out into its own area underneath the main content and gave it a light-on-dark contrast to clearly separate it from the content above. This also makes the text look less intimidating. As the areas are clearly separated, it doesn’t look like a huge amount to read.

#### Try to base your design around a grid

With some large areas of white space and some slightly squashed looking text in boxes, the structure of the original page design doesn’t look like it is based on a grid. However it is fairly simply laid-out and does have gridded elements to it.

Using a grid makes a lot of the design decisions less of a decision, as your grid will help dictate where the elements belong. Little details like having all the bottom of the text line up against a base grid, and main content areas having the same proportions, make a design look a lot cleaner and much classier.

{{< figure figcaption="The grid I used for my redesign" >}}
  {{< img src="gridded.png" alt="The grid I used for my redesign" >}}
{{< /figure >}}

Above you can see how I used a grid to line up all of my elements. I started with a main content area width of 960px. This is a useful value as it’s divisible by many different multiples, giving you nice round numbers to work with. It doesn’t really matter if you’re using pixels, ems or percentages, it’s just working from one value to get your proportions that helps.

The yellow grid lines are where I started, I divided my main content area into four, as this suited the four main calls-to-action (‘Get Started’, ‘Lift Community’) well. Usually, I’d probably design around three columns as this corresponds well with the [golden section](http://en.wikipedia.org/wiki/Golden_section) which creates a very harmonious balance in your design. You can combine three and four column grids in one, but this is probably a bit complicated for this post!

All of my main content areas sit within these yellow columns. The logo is in the first column, the navigation in the next three columns. The testimonials sit in all four columns, and the calls-to-action each sit in their own column. The main content areas are split into two sets of two columns.

What might stand out to you is that the ‘Demo’ and ‘Download’ buttons don’t sit entirely comfortably into columns. This is intentional. By moving some elements out of the column structure, it creates a tension against those that are within the columns, and draws attention to them.

The orange lines are an example of how I divided the columns further to decide where the margins should be. Each column of about 240px is divided by 4 and then those columns are divided by 2 again to get 30px, which is the width of the margin.

For areas like the width of the selected testimonial link, I just split the column by two as I needed a wider space to hold that text.

I also used the yellow grid lines for rows. It’s hard designing with rows on a web design as the content is always liable to change and no longer fit within those rows if there’s more or less text or an image gets put in. You can see that the content roughly sits on these rows by not completely.

I actually work on all web designs with a 10px square grid underneath as a baseline for all content, especially text. As most of the text has a line-height of 25px, every other line of text sits on the 10px grid. Below is what a small segment of the design looks like sitting on a 10px grid.

{{< figure figcaption="my redesign on 10px grid" >}}
  {{< img src="Screen-shot-2010-11-04-at-14.07.13.png" alt="my redesign on 10px grid" >}}
{{< /figure >}}

And that’s where the bananas go. *Just seeing if you’re still here!*

### Imagery

#### Avoid generic stock photography

I know the original page didn’t have any stock photography. In fact, I think that was the problem. There wasn’t any kind of imagery to break up the text. The closest it came was quote marks and gradients.

So first off I found some appropriate images to illustrate the content. A quick bit of Googling and I located the book covers for the Lift books. This will make the books easier to identify in passing, and really work to break up that text-heavy area at the bottom.

{{< figure figcaption="Book information with book images on my redesigned page" >}}
  {{< img src="Screen-shot-2010-11-04-at-15.41.35.png" alt="Book information with book images on my redesigned page" >}}
{{< /figure >}}

The difficulty in sites about web development and other non-visual subjects is there isn’t much in the way of obvious imagery you can use to illustrate your pages. But stay away from the stock photos! These are never the solution as they mostly look generic, cheesy and cheap.

Illustrations can be expensive, though stock illustrations are often better than stock photos. However there are a lot of high quality free icon sets out there. If you find icons relevant to the content, they can serve to break up a very text-heavy site *and* act as signifiers to help the user understand what the text, call-to-action or button is for.

{{< figure figcaption="the icons I used to illustrate my redesign" >}}
  {{< img src="icons.png" alt="the icons I used to illustrate my redesign" >}}
{{< /figure >}}

I had a look through my icon collections and found some [Shine icons](http://www.iconeden.com/icon/shine.html) that suited the content and were the right sizes for button links and bigger calls-to-action.

#### Use subtle patterns and textures to add depth to a page

I’d almost completed my design, and it felt like it was looking a bit flat. This is usually the way when you’re using a different solid colours. To combat this effect, I added some subtle noise and shadows to give it a more ‘real’ feeling.

{{< figure figcaption="the background of my redesign without (above) and with (below) noise textured background" >}}
  {{< img src="noise2.png" alt="the background of my redesign without (above) and with (below) noise textured background" >}}
{{< /figure >}}

I know I’d usually say that something like ‘noise’ is [possibly a current trend](http://dribbble.com/search?q=noise&amp;x=0&amp;y=0 "Search noise on Dribbble"), but I think it’s more of a recent discovery. It’s all very well using grungy textures if it’s appropriate to your site, but it really wouldn’t be for most software, corporate or family sites. Subtle noise is a great way to add some texture and definition without theming a site. Just make sure it’s very gentle. It looks best when not instantly visible, it should be *that* subtle.

3. ### Light

#### Choose one imaginary light source, and make the shadows follow that source

The thing that people forget when they use gradients, box shadows and text shadows on websites is that these elements are all used to recreate the illusion of light. Having light and dark on a site imitates real life, it makes your design more ‘real’, it makes it easier for your users to identify with it.

The incoming problems with [CSS3](http://www.css3.info/) is that people are using shadows willy-nilly, chucking them in to make their design look fancy without thinking about the effect they’re creating. This is visible on the random text-shadow on the original Lift design.

{{< figure figcaption="Random text-shadow on the Lift original design" >}}
  {{< img src="odd-contrast.png" alt="Random text-shadow on the Lift original design" >}}
{{< /figure >}}

If  you want to use gradients and shadows to make your site feel more real, and give it more depth, the trick is to choose a natural-style imaginary light source, and make all your shadows follow that.

There could be two light sources, though that could quickly get complicated, and beyond the realms of CSS, so I just went with the simplest possible for my design–;top-down. I imagined there was a light behind/above me and so it was projecting shadows that were equal sizes on each side of the boxes. It might not be completely scientifically sound, but it’s close-enough to feel real.

{{< figure figcaption="Light shadows visible around the boxes" >}}
  {{< img src="shadows.png" alt="Light shadows visible around the boxes" >}}
{{< /figure >}}

Colour is also important. Since when have you seen a white shadow? Pure black shadows are also very rare unless it’s very very dark. A shadow is usually just a darker shade of the surface it’s casting on to, follow that principle and you’ll have realism in no time.

#### Make your light source subtle

The other issue with the text shadow on the original Lift design is that it’s really screamingly obvious. From day-to-day we don’t really notice or comment on shadows much, even though they’re used *everywhere*, occurring in real life and almost every piece of software. The reason we barely notice is them is because they’re so subtle. I know I’ve used the ‘subtle’ word about a million times now but it really is the key to making a design look sophisticated.

4. ### If in doubt, keep it simple

#### Less looks more sophisticated

There’s no crime in creating a site with a white background, and no crime in being ‘basic.’ All the best sites are noted for their simplicity and how clean they look and not how garish and full-of-stuff (my particular design weakness) they are.

I really hope these tips and this sort-of walkthrough has been helpful. I’ll be happy to do more in the future if anybody wants them, or further explain any more elements of this design if anybody asks.

## 6 comments

<ol class="commentlist">
	<li class="comment even thread-even depth-1" id="li-comment-159">
			<div class="comment-author vcard">
			<img alt='' src='https://0.gravatar.com/avatar/ccea4ad19061493912796b6877b9d526?s=72&amp;d=mm&amp;r=g' srcset='https://0.gravatar.com/avatar/ccea4ad19061493912796b6877b9d526?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://matt-fuller.com' rel='external nofollow' class='url'>Matt</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-159"><time datetime="2010-11-04T16:34:19+00:00" pubdate class="published">
		 at <span class="hours">16:34pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		first.

x
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-160">
			<div class="comment-author vcard">
			<img alt='' src='https://2.gravatar.com/avatar/576f5c4bb54b8c197174b1a61cd15ed2?s=72&amp;d=mm&amp;r=g' srcset='https://2.gravatar.com/avatar/576f5c4bb54b8c197174b1a61cd15ed2?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://jackfranklin.co.uk' rel='external nofollow' class='url'>Jack Franklin</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-160"><time datetime="2010-11-04T16:38:35+00:00" pubdate class="published">
		 at <span class="hours">16:38pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		I think Lift should get in touch with you! I loved your talk and this follow up is superb. I&#039;m loving your blog more and more every time I visit!
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-161">
			<div class="comment-author vcard">
			<img alt='' src='https://2.gravatar.com/avatar/?s=72&amp;d=mm&amp;r=g' srcset='https://1.gravatar.com/avatar/?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo avatar-default' height='72' width='72' /><cite class="fn"><a href='http://twitter.com/jamienewman' rel='external nofollow' class='url'>@jamienewman</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-161"><time datetime="2010-11-04T16:41:24+00:00" pubdate class="published">
		 at <span class="hours">16:41pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Great post. Love the new design and some very useful tips here!
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-162">
			<div class="comment-author vcard">
			<img alt='' src='https://0.gravatar.com/avatar/0d26a7f9ca0188555680a8b8dcd71242?s=72&amp;d=mm&amp;r=g' srcset='https://0.gravatar.com/avatar/0d26a7f9ca0188555680a8b8dcd71242?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://experimentsincode.com/' rel='external nofollow' class='url'>Mike</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-162"><time datetime="2010-11-04T16:54:36+00:00" pubdate class="published">
		 at <span class="hours">16:54pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks great article!! Shame I missed your talk at BathCamp.
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-163">
			<div class="comment-author vcard">
			<img alt='' src='https://1.gravatar.com/avatar/1aad914af34dbc6eac1b7cd9b40b86ed?s=72&amp;d=mm&amp;r=g' srcset='https://1.gravatar.com/avatar/1aad914af34dbc6eac1b7cd9b40b86ed?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://levibreederland.com' rel='external nofollow' class='url'>Levi</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-163"><time datetime="2010-11-08T20:39:50+00:00" pubdate class="published">
		 at <span class="hours">20:39pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		I totally agree with the other comments (except for that first one). Very good summary of handy tips!
	</div>
</li>
</ol>

	
