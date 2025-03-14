---
title: "A little realign"
date: 2014-05-02T13:10:30+00:00
categories: ["Design", "Development", "Milestones"]
tags: ["case studies", "CSS", "portfolio", "realign", "redesign", "Sass", "typography", "update"]
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

Things are looking a bit different around here. It’s not a redesign so much as a [realign](http://alistapart.com/article/redesignrealign). I’ve been tinkering for a few months, and finally got to the point where I’m happy to push it live (even though there’s more I could do.)

There were a few particular goals for this redesign:

## Rewrite the CSS

I lived in fear that someone might look closely at my CSS. My last redesign came about when responsive web design was still young, and I was incredibly foolish. I linked to three different stylesheets in my header, one for 320px and up, one for 768px and up, and one for 1024px and up. There were some “minor” breakpoints in these stylesheets, but yes, I was using fairly device-based breakpoints, and that was three HTTP requests in the head. Certainly not ideal.

The previous version was also a peculiar Sass/plain CSS hybrid as I’d started learning Sass a few months into the redesign. As Sass is so easy to integrate into ordinary CSS, it wasn’t too problematic, but I knew I could lessen repetition and make the structure of my CSS much easier to maintain if I moved it all into a consistent format.

Now I’ve rewritten all the CSS from scratch using Sass, and added in a few new techniques, such as flexbox, for some of the form elements. If you’re interested in how badly I write Sass, I’ve uploaded those files (in the spirit of Dan Eden’s max CSS) into a /sass folder and you can find the file references in the main file, [style.scss](/wp-content/themes/laurakalbag-2014/sass/style.scss).

## Reboot the typography

I love Avenir, I really do, but I was increasingly aware that it can be hard work to read as body text. After falling in love with [Brandon Text](http://hvdfonts.com/#189-Brandon%20Text "Brandon Text typeface"), I decided it was a nice evolution from Avenir, keeping the geometric shapes but in a softer, more legible, way.

{{< figure figcaption="Avenir as display and body text on the old version of my site" >}}
  {{< img class="wp-image-4455" alt="Avenir as display and body text" src="previous-typography.jpg" >}}
{{< /figure >}}

I recently read Tim Brown’s fantastic [Combining Typefaces](http://nicewebtype.com/notes/2013/04/23/pocket-guide-to-combining-typefaces/) book and felt encouraged to be braver with my typefaces choices. I didn’t want to just keep using different weights of the same family as I had before. After some [deliberation](https://dribbble.com/shots/1510342-Freight-Micro-and-Brandon-Text-dilemma?list=users&amp;offset=6 "Dribbble shots showing the process of my heading typeface choice") and advice, I settled on [Arek](http://www.rosettatype.com/Arek) for headings, to add a bit of quirky personality to my site. This is the first time I’ve used [Fontdeck](http://fontdeck.com) properly, and I’m really pleased with the quality of the font and the speedy rendering.

{{< figure figcaption="Arek for the display, and Brandon Text for the body on the new realign" >}}
  {{< img class="wp-image-4456" alt="Arek for the display text, and Brandon Text for the body text" src="new-typography.jpg" >}}
{{< /figure >}}

I’m both self-hosting and using external JavaScript to pull in fonts for my site. Brandon Text is self-hosted whereas Arek is hosted on Fontdeck. I can’t quite make up my mind whether I prefer to suffer slow loading times on my self-hosted fonts, or the risk of my site depending on another site for the fonts to load with a font delivery service.

## Simplify

The illustrations had to go. I’m always trying to tame my temptation to over-decorate, and while the illustrations in the previous version were a nice responsive bonus for large screens, a cleaner design is less distracting.

{{< figure figcaption="Previous homepage layout, with portfolio images, blog posts and a messy illustration" >}}
  {{< img class="wp-image-4460" alt="Previous homepage layout, with portfolio images, blog posts and a messy illustration" src="previous-homepage.jpg" >}}
{{< /figure >}}

For a long time, my homepage was my most hated page. And the most visited. It just felt like everything had been thrown on, it was unstructured and untidy. Given that the second most popular area of my site is the Past Projects, I decided to include twelve (nicely divisible for smaller screen sizes) images from my past projects and a brief introduction.

{{< figure figcaption="New version of the homepage, with just an introduction and larger portfolio images" >}}
  {{< img class="wp-image-4458" alt="New version of the homepage, with just an introduction and larger portfolio images" src="new-homepage.jpg" >}}
{{< /figure >}}

WordPress, by default, gives you so many options for meta information on archive pages. I previously listed the amount of comments, categories and tags on each post on the blog archive. On the projects archive I listed the dates and type of project. I realised these were unnecessary chunks of information that were easy enough to find on the single post or project pages. Just because I *could* add everything to each template, it didn’t mean I should. Less repetitive content means the pages are now cleaner, easier to read, and nowhere near as long as before.

{{< figure figcaption="Previous blog, with lots of information about each post" >}}
  {{< img class="wp-image-4459" alt="Previous blog, showing comments, categories and tags for each post" src="previous-blog.jpg" >}}
{{< /figure >}}

{{< figure figcaption="New blog post layout with no unnecessary meta information" >}}
  {{< img class="wp-image-4457" alt="New blog post layout without comments, tags or category information" src="new-blog.jpg" >}}
{{< /figure >}}

## New projects with Dribbble shots

I’ve been terrible at keeping my portfolio up to date in the last year. I’ve still got five projects that are halfway to being documented, but I’ve added four recent projects with some more in-depth explanations of the process. I want to keep adding more useful explanations to each project, making it more of a case study, so they’ll inevitably take a little longer.

{{< figure figcaption="four new case studies: Indie Phone, Freelancing map illustration, Rachel Andrew’s site and the Turbine logo" >}}
  {{< img class="wp-image-4454" alt="thumbnails of four new case studies" src="Screen-Shot-2014-05-02-at-13.07.28.png" >}}
{{< /figure >}}

After hearing [Andy Clarke chat with Dan Cederholm on Unfinished Business](http://unfinished.bz/37) a few months ago, I shamelessly borrowed Andy’s great idea to include Dribbble shots from a project in my portfolio. I found a handy plugin to grab my Dribbble shots as they’re posted and add them into WordPress, so I can now easily connect my Dribbble shots to the relevant post and include a little gallery at the end of each project case study.

{{< figure figcaption="progress shots from the Indie Phone project" >}}
  {{< img class="wp-image-4453" alt="four Dribbble shots showing the rocket logo design process" src="Screen-Shot-2014-05-02-at-12.58.24.png" >}}
{{< /figure >}}

## There’s probably more to do…

As ever, there’s always more testing to be done. I don’t expect this site to be perfect, but I thought it was about time I hurried up and pushed it live. If you spot anything wonky, please let me know in the comments, [on Twitter](http://twitter.com/laurakalbag) or [send me an email](/contact-me/ "Contact Me"). I’ll be very grateful!


## 2 comments

<ol class="commentlist">
	<li class="comment even thread-even depth-1" id="li-comment-17622">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/2cedd48cbe620346d6628ab04c5cc192?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/2cedd48cbe620346d6628ab04c5cc192?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://leegargano.com' rel='external nofollow' class='url'>Lee Gargano</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-17622"><time datetime="2014-05-02T13:50:57+00:00" pubdate class="published">
		 at <span class="hours">13:50pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Great decisions, Laura! I agree with you wholeheartedly on the font selections and home page redesign. I need to reanalyze my own site soon now that I have enough data to make those decisions. That’s the beauty of launching a product (your site) and then adjusting it as you go along based on the results you find.
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-17629">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/c24bc4315ae99321925696e8092fdc1e?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/c24bc4315ae99321925696e8092fdc1e?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://mattsoria.com' rel='external nofollow' class='url'>Matt Soria</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-17629"><time datetime="2014-05-02T14:37:38+00:00" pubdate class="published">
		 at <span class="hours">14:37pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>Hey Laura!

I have frequently visited your site in the past year for reference and inspiration. Even before the new “realign” I appreciated your bold choice of color and great copy (especially the “about” page).

I just so happened to be making a few adjustments to my own site late last night and turned to your site again for inspiration when I noticed the changes on your homepage, and I must say — brilliant little improvements. The fonts look great, and the new layout on the homepage is indeed simpler and quite inviting I think.

It reminds me also that as designers, and as people that grown and change, our websites don’t have to be something that we re-design every year-or-so — they can be continuously changed and adapted as we grow and learn, and our design tastes change as well.

It makes me think of [Frank Lloyd Wright’s Home and Studio](https://www.google.cl/search?q=inside+frank+lloyd+wright%27s+home+and+studio&amp;client=firefox-a&amp;hs=PHG&amp;rls=org.mozilla:en-US:official&amp;channel=sb&amp;source=lnms&amp;tbm=isch&amp;sa=X&amp;ei=SK1jU5SPDPO0sASJkoHoBw&amp;ved=0CAgQ_AUoAQ&amp;biw=1360&amp;bih=631" rel="nofollow) in Hyde Park, Illinois (US). When you walk through it much of it seems like a hodgepodge of different styles and periods, and it was because it was his home, and he was constantly experimenting on it with new ideas that he would then take out into the wild and use on his paid projects. Shouldn’t our own websites be that too? Besides a portfolio or résumé or whatever, what better place for experimentation and growth? If you got feedback today that was overwhelming negative about the changes you made (doubt you will), well you’d just change them again. No big deal, right? What a great way to learn?!

Anyway, cheers to the realign, and keep killing it!</p>	</div>
</li>
</ol>
