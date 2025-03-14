---
title: "Grids, flexibility and responsiveness"
date: 2012-10-12T21:39:30+00:00
categories: ["Design"]
tags: ["base units", "choosing typefaces", "columns", "content-first", "grids", "responsive web design"]
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

## First steps: choosing a typeface

The first step in my grid design was to choose an appropriate typeface. I knew this would be everything on such a text-heavy site, and I really struggled because, as with all the elements on my personal site, I wanted it to reflect “me”. I wanted a typeface that felt friendly and not too formal whilst still appearing clean, readable and professional. I sunk money on a few lesser-known typefaces (everybody wants to be different and original, right?!) before completely falling for Avenir. [Avenir was only available (with the delivery method I preferred) as a web font from fonts.com](http://www.fonts.com/font/linotype/avenir?QueryFontType=Web "Avenir web font on fonts.com") so that made choosing the font service much easier.

{{< figure figcaption="Avenir typeface sample" >}}
  	{{< img src="72.png" alt="Avenir typeface sample" >}}
{{< /figure >}}

### Basic setting of the typeface

Playing with Avenir in [Typecast](http://beta.typecastapp.com/) gave me an idea of the size I wanted to use it. Making it pretty big allowed its character to show whilst maximising readability. I’m also keen on a bigger line height on rounded sans serif type faces as their spacious counters can make their lines harder to distinguish if the leading is tighter.

{{< figure figcaption="Playing with content set in Avenir in Typecast" >}}
  	{{< img src="Screen-Shot-2012-10-12-at-19.58.47.png" alt="Playing with content set in Avenir in Typecast" >}}
{{< /figure >}}

## Base units and vertical rhythm

It was then time to decide on the base unit I was going to use as the foundation for my grid. Admittedly, I did this somewhat arbitrarily; I tend to go with multiples of 10 (occasionally using 5) as it makes the maths easier, so this time I challenged my maths with multiples of 12 (using 6 for detail.) Another justification I had was that it would be more harmonious working with what would probably become a three column grid, thus roughly using “thirds” as a concept. To create a consistent vertical rhythm I used multiples of my base unit on all vertical measurements, including line-heights, margins and padding.

## Horizontal grids

When I was creating the grid design for this site I was dying to play more with [Gridset](https://gridsetapp.com/). My content was fairly flexible; most pages consisted of a large amount of body text, which just needed to be as readable and digestible as possible, and some meta information which could sit to one side or above the content depending on the space available in the viewport.

Having this flexibility in my content meant the fancy grids in Gridset were mine to try out. I chose grid A as my primary grid to stick to for as many of the layouts as suited the content, and B as my secondary grid when the content better fitted to points between the grid A’s columns. Using the grids overlaid in this way gave me consistency whilst still maintaining a level of flexibility.

{{< figure figcaption="Grid A and Grid B overlaid on my base unit grid" >}}
  	{{< img src="grid-a-and-grid-b.png" alt="Grid A and Grid B overlaid on my base unit grid" >}}
{{< /figure >}}

{{< figure figcaption="Grids A and B overlaid" >}}
  	{{< img src="grids-a-and-b-overlaid.png" alt="Grids A and B overlaid" >}}
{{< /figure >}}

### Flexible grids

Now I don’t really believe in creating a fully (often based entirely on percentages) horizontal grid *along with* a fixed vertical grid (usually described through line-heights and vertical margins/padding.) If you do this, the ratio/proportions relating the horizontals and verticals change every time the page is loaded in a different width viewport. This can have far less than harmonious results.

Instead, as my viewport reduces in width, I remove the columns from the right end of the grid and re-distribute the content where relevant in order to achieve readable content and consistent, structured feel. So this might be me as designer ‘not letting go’ of fixed constraints or embracing fluidity as much as I possibly can, but I believe that it’s this structure that allows us to maintain a level of control over the measure (line length) necessary for pleasurable reading experience. If you’re going to create breakpoints at arbitrary positions in order to keep your text readable, why not fit it around a balanced grid layout instead?

{{< figure figcaption="Wide About page, utilising the full grid" >}}
  	{{< img src="about-large.png" alt="Wide About page" >}}
{{< /figure >}}

{{< figure figcaption="Wide Blog page, utilising the full grid" >}}
  	{{< img src="blog-large.png" alt="Wide Blog page" >}}
{{< /figure >}}

{{< figure figcaption="Medium-width About page, moved one column to the left" >}}
  	{{< img src="about-medium.png" alt="Medium-width About page" >}}
{{< /figure >}}

{{< figure figcaption="Medium-width blog page, with meta content shown below the main content rather than in left column" >}}
  	{{< img src="blog-medium.png" alt="Medium-width blog page" >}}
{{< /figure >}}

{{< figure figcaption="Smaller-width About page, not using the grid structure but using padding based on the base unit size" >}}
  	{{< img src="about-small.png" alt="Smaller-width About page" >}}
{{< /figure >}}

{{< figure figcaption="Smaller-width Blog page, not using the grid structure but using padding based on the base unit size" >}}
  	{{< img src="blog-small.png" alt="Smaller-width Blog page" >}}
{{< /figure >}}

### Paddings and margins

Just like in my vertical rhythm my column padding, and with any horizontal margins in the layout, I stuck to multiples of my base unit. This helps keep the balance between the horizontal and vertical elements of the layout and prevents it from feeling stretched or condensed in some viewports, which I think is often an unfortunate side effect of a truly fluid layout with a stingy lack of breakpoints.

### Breaking the grid (content comes first)

There were points at which I broke from my grid structure in order to better serve my content: project archive pages. These are more optimised for the viewport width to keep the images big enough to identify their subject but small enough that they’re not creating excessive page length (or indeed weight.) But these image/column widths are still multiples of the base unit grid, so subtly remain consistent and true to my grid design.

{{< figure figcaption="Past projects page breaks the grid by having a more content-appropriate layout" >}}
  	{{< img src="past-projects.png" alt="Past projects page" >}}
{{< /figure >}}

### Left-aligning the grid

For a long time, I had centred my page layouts in the browser window, believing that it was the most optimal use of space (or rather broke up large expanses of white space!) However, for this design I decided that I’d left-align the grid to the viewport. This kept my grid looking structured as it didn’t leave an infinitely resizable column on the left side of the browser, and also preserved the rigidity of that left-aligned grid as I removed right-hand columns as the viewport width was reduced.

Often the whitespace resulting from a left-aligned page layout would could feel gaping, so I decided (on pages that didn’t otherwise have much imagery) I would use that space for a background illustration that I hoped would be better use of otherwise redundant space.

{{< figure figcaption="Very wide About page showing the background illustration" >}}
  	{{< img src="about-wide.png" alt="Very wide About page" >}}
{{< /figure >}}

## Tweaks

A few days after the launch of my site I made a few tweaks. The most significant to my grid being adjusting the main content font size and line height on narrower viewports. I didn’t want to go with that awful trend of shrinking text to an unreadable size just because the screen is smaller. As [Simon Foster](http://simonfosterdesign.com/) said in his great Responsive Designer talk at [Web Expo Guildford](http://webexpoguildford.co.uk/) just today; it’s about balancing measure with a readable font size and a readable font size should always win. I shrunk the font size by only 1 (1/12) unit , but shrunk the line-height by 6 (1/2) units. This made the measure a little better whilst still preserving a (hopefully) readable font size, but also fitted considerably more text into smaller viewports making it a little less distracting to read.

## Evaluating

This approach to grid design works for me. I’m not saying I will use it for every project in the future, but at the moment it feels like it has the right balance of flexibility and control with content- and experienced-based priorities. Perhaps I could make my base unit em-based, or even percentage based (that’s got to be one hell of a Sass mixin) to make it even more ‘responsively’ flexible, I’m still exploring what’s possible.

## 15 comments

<ol class="commentlist">
	<li class="comment even thread-even depth-1" id="li-comment-308">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/ddd8d891066d9e31a3ee7b1ea4d8d4ab?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/ddd8d891066d9e31a3ee7b1ea4d8d4ab?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.clintonbeattie.com' rel='external nofollow' class='url'>Clinton</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-308"><time datetime="2012-10-14T18:10:06+00:00" pubdate class="published">
		 at <span class="hours">18:10pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Nice insight into your workflow when considering grids in a responsive sight. Great final product!
	</div>
	<ul class="children">
		<li class="comment byuser comment-author-laura bypostauthor odd alt depth-2" id="li-comment-310">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Laura</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-310"><time datetime="2012-10-15T09:41:59+00:00" pubdate class="published">
		 at <span class="hours">09:41am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thank you Clinton!
		</div>
	</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-309">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/0f0a06c9bd1abfd7d77d43419c2d1ee4?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/0f0a06c9bd1abfd7d77d43419c2d1ee4?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.renaissance-design.net' rel='external nofollow' class='url'>Chris</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-309"><time datetime="2012-10-14T21:06:49+00:00" pubdate class="published">
		 at <span class="hours">21:06pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		I like your thinking there. Comment form fields butt against the right of the container for me, btw. Firefox/Android/800*480 portrait. Shamefully unsure of logical pixels, sorry.
	</div>
	<ul class="children">
		<li class="comment byuser comment-author-laura bypostauthor odd alt depth-2" id="li-comment-311">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Laura</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-311"><time datetime="2012-10-15T09:42:57+00:00" pubdate class="published">
		 at <span class="hours">09:42am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks for the heads-up, Chris. It was on my radar but your comment finally pushed me to deploy a fix!
		</div>
	</li>
	<li class="comment even thread-even depth-1" id="li-comment-312">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/4eda1192a9edcae9c871352ef3d36910?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/4eda1192a9edcae9c871352ef3d36910?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Steve</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-312"><time datetime="2012-10-16T14:14:55+00:00" pubdate class="published">
		 at <span class="hours">14:14pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Really great article&#8230;one of the best I’ve seen on the subject this year.
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-313">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/68e3021411e20a569331fadd3c1dd114?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/68e3021411e20a569331fadd3c1dd114?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://Cloudacre.co.uk' rel='external nofollow' class='url'>Daniel</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-313"><time datetime="2012-10-17T13:09:44+00:00" pubdate class="published">
		 at <span class="hours">13:09pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>A great article Laura, I’ve always wanted to try using grids and after reading about your workflow am certain to give it a try. I love seeing how other people approach their layouts. :)

P.S. I’m still a sucker for centre aligning! :D

Thank you for the insight. :)</p>	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-315">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/78de844f58c7802850fd81dbec312b4d?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/78de844f58c7802850fd81dbec312b4d?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Wayne</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-315"><time datetime="2012-10-19T20:32:03+00:00" pubdate class="published">
		 at <span class="hours">20:32pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Brilliant to read about your thought process! Thanks so much. One of your image captions confused me –; “Medium-width blog page, with meta content shown above the main content rather than in left column”.

It appears that the meta content is shown <i>below</i> the main content, actually b/w the main content and the comments.

I also see you fixed the Menu bounce problem on iOS 4 (at least it now works on my iPhone 4). Are you going to write about that as well?
	</div>
	<ul class="children">
		<li class="comment byuser comment-author-laura bypostauthor odd alt depth-2" id="li-comment-317">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Laura</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-317"><time datetime="2012-10-21T18:59:26+00:00" pubdate class="published">
		 at <span class="hours">18:59pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks Wayne, I’ve now fixed that caption.

And yes, I fixed the menu bounce problem. It was actually thanks to the lovely [Berklee](http://alpha.app.net/berklee" title="Berklee on app.net" rel="nofollow), who rewrote my function slightly and had the ability to test it on iOS5 (something I was struggling with!)
		</div>
	</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-318">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/9a084c9c6f85b04026a9253828b6fe0e?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/9a084c9c6f85b04026a9253828b6fe0e?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Reinier Kaper</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-318"><time datetime="2012-11-08T18:27:34+00:00" pubdate class="published">
		 at <span class="hours">18:27pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks for this insightful article, it’s always good to see how other approach it.

One thing I have noticed recently is that using ’em’s for media queries seems to be working a little better than pixel values. You can view what happens when you zoom in to the page with the browser (CTRL + usually) and see that the media query ‘breaks’. By using ’em’s, which are relative, they will keep working, which is great if content should decide the breakpoints and you value your users settings.

My 2 cents on this subject!
	</div>
	<ul class="children">
		<li class="comment byuser comment-author-laura bypostauthor odd alt depth-2" id="li-comment-319">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Laura</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-319"><time datetime="2012-11-09T11:52:10+00:00" pubdate class="published">
		 at <span class="hours">11:52am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		I completely agree. I just find it really hard to work in ems, the maths breaks my brain. I use rems based on a root % value, but all the while I’m falling back to px, it’s not quite the same.
		</div>
	</li>
	<li class="comment even thread-even depth-1" id="li-comment-320">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/b32b96a09533a09b1511b650602767d7?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/b32b96a09533a09b1511b650602767d7?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://llucas.org' rel='external nofollow' class='url'>Lucas</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-320"><time datetime="2012-12-09T20:12:36+00:00" pubdate class="published">
		 at <span class="hours">20:12pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>Great article, Laura :)

I really like the design of you site, so simple and beautiful.</p>	</div>
</li>
</ol>
