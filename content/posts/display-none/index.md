---
title: "display: none;"
date: 2012-11-06T08:45:02+00:00
categories: ["Design Issues", "Markup"]
tags: ["CSS", "HTML", "javascript", "learning", "mobile first", "progressive enhancement", "responsive web design", "small screens"]
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

## *Or* The things you think are common knowledge but really they aren’t.

[I was on the ShopTalk show](http://shoptalkshow.com/episodes/040-with-laura-kalbag/) a few weeks ago, and a few people have asked me what I meant when I said “`display: none;` naughties.” I foolishly thought that people would understand what I meant, (and I’ll come to that later) so I thought I’d better explain myself.

## `display: none;` in responsive web design

When we’re [changing out layouts based on viewport sizes, using media queries](http://www.alistapart.com/articles/responsive-web-design), we tend to switch page elements about a bit. We might make our images display one-on-top-of-the-other for narrower layouts, we might make our text super big to take advantage of bigger spaces.

There can be a lot of content on one web page, and often there’s a temptation to hide some of it on narrower viewports. This walks hand-in-hand with the assumptions that narrow viewports are mobile devices and people using mobile devices are roving the planet using the web ‘on the go.’

### Assumptions

But those assumptions are exactly that, you’re just *assuming* that’s what the user is doing, you’re not basing that on real research or user testing. Why are you hiding so much of your content if you’re assuming it’s also useful to those browsing your site with a wider viewport?

### Don’t be lazy

Just hiding content is a lazy design solution. Yes, it’s hard designing for smaller screens, but maybe that will help you ensure that every little piece of content you’re putting on that site is worthwhile. Responsive design should be about rearranging, not changing, your page elements.

### And then you’re actually just loading it anyway…

When you’re putting content into your page, and *then* hiding it with CSS, it’s still there, it’s just not visible. So if you’re using this ‘technique’ across your site in numerous places, you’re likely taking a performance hit. And potentially, for narrower viewports/possible mobile devices, in the one place that a slow-loading page is likely to irritate a user. It’s just not worth that risk.

## Changing the display, not hiding the display

One solution I’ve been using is changing the display of the content. It is a real problem that CSS can’t easily manipulate all types of content into a readable fashion on all devices. This is particularly true for navigation that needs to be displayed in a significantly different way, and often tables need to be reinterpreted into a more digestible format for narrow viewports. And in these cases, javascript can be your friend.

### Mobile first

I always start mobile first, that’s not just in markup, it’s in content too. We don’t want to load up unnecessary HTML that creates performance problems, or javascript that may not working consistently on mobile devices.

If I’ve got a data table, and I think it would be better off displayed as a list of data, I would write the list of data into the HTML. This way it’ll load quickly, and those without javascript (or enough bandwidth to load javascript) will get a decent experience.

### Progressively enhancing with javascript

Then, I would use media queries, or some kind of clever javascript, to load in the fancy content for particular viewport widths. I’ve done this to load in tables of data, replacing data lists, and also for navigation, replacing a vertical list of links with a show/hide button that reveals the menu when tapped (as on this site.) None of this requires `display: none;`. No markup is wasted.

### [Edit]: Accessibility

The good [Steve Marshall](http://twitter.com/SteveMarshall) has pointed out that there are also accessbility issues related to `display: none;`. I didn’t want to cover too much in the post, but in case you want to know more about that too, I recommend [Aaron Gustafson’s ‘Now You See Me’ on A List Apart](http://www.alistapart.com/articles/now-you-see-me/) and [Chris Coyier’s ‘Places It’s Tempting To Use Display: None; But Don’t on CSS Tricks](http://css-tricks.com/places-its-tempting-to-use-display-none-but-dont/). [/edit]

---

## Writing about markup

I’m a little bit scared of writing about markup. I’m sure there are loads of front-end developers out there who know a huge amount more than me, and I’m worried I’ll get it wrong or make myself look stupid.

I also shy away from writing about the ‘easy’ stuff. This post about `display: none;` is a fairly simple principle and I really don’t want to patronise anyone.

### People do want to hear about the ‘simple’ stuff

Making these assumptions about it being a simple principle, and that everybody would know about it already, was daft. I was quickly proved wrong when people started asking me about it and then I realised how silly it was to think that we all have the same sources of information.

### Scattered learning

The web is a big and varied place. To assume that someone else has read something just because you’ve read it is foolish. How do we learn about these resources? When do we all decide that we’re all going to read these particular sites and articles so that we’re all equally informed?

Even on Twitter, the resources we hear from, and learn from, are wildly different. We may follow completely different individuals and so the resources we learn from are curated by these individuals, and these may not ever crossover. Even if we do follow the same people on Twitter, noone can be expected to read every tweet, and inevitably you’ll miss some, and then you may not know about this other new thing that everybody else has been doing for years.

### Where I get to the point…

The point I’m trying to make is that we shouldn’t be fearful of writing about what we know. Even if you write from the most basic point of view, about something which has been ‘around for ages’, you’ll likely be saying something new to someone. They might be new to the industry, you might just be filling in the holes in someone’s knowledge.

Every week I have a revelation on app.net or Twitter where I wonder how I didn’t know about this old technique or tool before… but we can’t be expected to keep up with everything. I hope this post does that for some people. It’s good to share what we know. You needn’t be the first, you’ll just help if you’re the first that somebody finds.

## 63 comments

<ol class="commentlist">
	<li class="comment even thread-even depth-1" id="li-comment-350">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/18592fc8bad8f92136390f52303ee29c?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/18592fc8bad8f92136390f52303ee29c?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://mrgwebdev.com' rel='external nofollow' class='url'>Mark Glover</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-350"><time datetime="2012-11-06T09:55:42+00:00" pubdate class="published">
		 at <span class="hours">09:55am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks for blogging this Laura, that’s really cleared up the podcast for me. I wasn’t really convinced about starting with mobile first, but using javascript to turn the mobile markup into the desktop markup makes far more sense than using display: none; or, worse, using javascript to turn desktop markup into mobile.

Regarding what people know, I’ve been worrying about the same thing for ages and avoiding writing about things that seem simple to me. I concluded a little while ago that what I’ve learnt so far comes mostly from other people writing about things that seem simple to them. As you say, we all look at different parts of the internet, and not everyone has been doing this job for years. I’m a pretty experienced PHP developer, but I’m perhaps still a little behind the recent changes in frontend development. Other people are probably in the reverse position.

Keep blogging the simple stuff, there will always be someone who needs that piece of knowledge :-) P.S I’d be interested to read a post from you on semantic HTML sometime. I know it’s one of your things, and I feel like I could be doing it a lot better (I still div a lot).
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-351">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/c083c7ffc86fab9e831990ad82033f99?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/c083c7ffc86fab9e831990ad82033f99?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.jasonbradberry.com' rel='external nofollow' class='url'>Jason Bradberry</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-351"><time datetime="2012-11-06T10:12:25+00:00" pubdate class="published">
		 at <span class="hours">10:12am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks, definitely a helpful post!

I’ve been working using a desktop first approach, and am considering switching to looking at ‘mobile’ first for my next project. One thing I’d like to hear more about – in the podcast you talked about loading content conditionally as browser window size is increased (using the example of the large illustration on the right hand side of your site). Can you recommend any good articles/links for further reading on this?
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-352">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/05a5dfd9e66b566bbb32091bb87ad202?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/05a5dfd9e66b566bbb32091bb87ad202?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://remy.bach.me.uk' rel='external nofollow' class='url'>Rémy</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-352"><time datetime="2012-11-06T10:17:24+00:00" pubdate class="published">
		 at <span class="hours">10:17am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		The last half of this article has really struck a chord with me. In the past, I’ve shelved so many potential blog posts because I think they’re too basic when they might actually have been useful to somebody.

There’s also a lot to be said for how easy something is to Google. Before posting on something, try doing a quick search for what you’re thinking of writing about. I think more often than not, you’ll find that what you want to post about either hasn’t been covered at all, is not visible enough using the search terms you used (which anyone else might easily have searched for as well), or you do it slightly differently. Either way, sharing even the smallest bit of knowledge only makes the web community stronger.

Thanks for the great thoughts (and inspiration) Laura!
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-353">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/043af7a7ebf89595bebc3364f933d648?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/043af7a7ebf89595bebc3364f933d648?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Richard Lewis</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-353"><time datetime="2012-11-06T10:26:59+00:00" pubdate class="published">
		 at <span class="hours">10:26am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		very informative laura, no one should assume that everyone knows a certain piece of info. Something that I have learned though is if you have an image for example and display :none on that then yes it still renders, however if you wrap that element in a div and then display none on that parent element the img doesn’t actually load&#8230; thought it may help
	</div>
	<ul class="children">
		<li class="comment even depth-2" id="li-comment-388">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/5b4885089cdfebb57d760e46e6275ad2?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/5b4885089cdfebb57d760e46e6275ad2?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://sarasoueidan.com' rel='external nofollow' class='url'>Sara</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-388"><time datetime="2012-12-10T06:36:16+00:00" pubdate class="published">
		 at <span class="hours">06:36am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		This is a great tip! thanks for mentioning it :)
	</div>
</li>
	<li class="comment odd alt depth-2" id="li-comment-395">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/565d2abdc8fc487b9cece74271a53d28?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/565d2abdc8fc487b9cece74271a53d28?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Jason</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-395"><time datetime="2012-12-10T18:01:43+00:00" pubdate class="published">
		 at <span class="hours">18:01pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>I’d be cautious with this approach as from my testing the images still get loaded.

[http://jsfiddle.net/jlaeser/pCbav/](http://jsfiddle.net/jlaeser/pCbav/" rel="nofollow)</p>
This could potentially make for a larger initial page load.
	</div>
	<ul class="children">
		<li class="comment even depth-3" id="li-comment-400">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/c5bd15f36ca445f33618e7aa6ffe5019?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/c5bd15f36ca445f33618e7aa6ffe5019?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">James</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-400"><time datetime="2013-03-06T15:37:39+00:00" pubdate class="published">
		 at <span class="hours">15:37pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Yes I tested this also and it does indeed load. Shame though as this could have been an ideal solution.
		</div>

		



</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-354">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/62f1c041b638db2c75f89405510c99ad?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/62f1c041b638db2c75f89405510c99ad?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://graphiceyedea.co.uk' rel='external nofollow' class='url'>Prisca</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-354"><time datetime="2012-11-06T10:42:05+00:00" pubdate class="published">
		 at <span class="hours">10:42am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>Laura :)

thanks for this post –; well explained :)

Also, just wanted to say that I agree: writing about what might simple is always a good idea. Teaching webdesign is changing all the time and there’s so much out there that it can be a tricky endeavour to point students to good resources. By now, I recommend people and high quality sites as good resources to follow ~ which essentially means that you writing about something simple will always have an audience, from students starting out with learning webdesign to the students of the web who we all are :)</p>	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-355">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/a9d07c20116fc86dfb522daaa1f0c923?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/a9d07c20116fc86dfb522daaa1f0c923?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://ianwootten.co.uk' rel='external nofollow' class='url'>Ian</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-355"><time datetime="2012-11-06T14:26:26+00:00" pubdate class="published">
		 at <span class="hours">14:26pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Hold on. “display: none;” is naughty? In all situations?

Then you Laura, are very naughty. For that’s exactly how you display your top menu at lower resolutions, no?
	</div>
	<ul class="children">
		<li class="comment byuser comment-author-laura bypostauthor odd alt depth-2" id="li-comment-356">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Laura</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-356"><time datetime="2012-11-06T14:42:31+00:00" pubdate class="published">
		 at <span class="hours">14:42pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Heh. Only in the form of a good old dropdown menu. So whilst `display: none;` is used to *temporarily* hide the sub navigation, it is visible on hover.

To be fair, I’m sure there are a lot of use cases where `display: none;` has its uses. As with every rule, there are always exceptions :)
	</div>
	<ul class="children">
		<li class="comment even depth-3" id="li-comment-357">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/a9d07c20116fc86dfb522daaa1f0c923?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/a9d07c20116fc86dfb522daaa1f0c923?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://ianwootten.co.uk' rel='external nofollow' class='url'>Ian</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-357"><time datetime="2012-11-06T14:57:55+00:00" pubdate class="published">
		 at <span class="hours">14:57pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Well, actually at lower resolutions, both menus are only available on click :)

I agree there are many use cases –; but this isn’t what’s implied here. I actually believe for performant web apps, using “display:none;” and modifying markup through js absolutely essential.
	</div>
	<ul class="children">
		<li class="comment odd alt depth-4" id="li-comment-385">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/058848a8098693e62eff155692cecb1e?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/058848a8098693e62eff155692cecb1e?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Harry Mansworth</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-385"><time datetime="2012-11-29T16:04:39+00:00" pubdate class="published">
		 at <span class="hours">16:04pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Using display:none has other disadvantages. In the (rare) case that javascript has been turned off or the device has insufficient resources to run the script, using something like `$('#element').hide();` will ensure that, should JS be turned off the elements will still be visible. **Essential**for things like navigation!
		</div>

		



</li>
	<li class="comment even depth-2" id="li-comment-358">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/153cbbe84fd0473ce666b479c52fb265?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/153cbbe84fd0473ce666b479c52fb265?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='https://twitter.com/crisgarner' rel='external nofollow' class='url'>Cristian Garner</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-358"><time datetime="2012-11-07T16:37:13+00:00" pubdate class="published">
		 at <span class="hours">16:37pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		I don’t think she meant on all situations, display:none is a useful tool, if it were really bad no one would use it, I believe what Laura wants to explain is that it must be used only in what it is needed and to stop over using it.
		</div>
	</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-359">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/8ea29219f41831044d8aba8c8dfb9309?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/8ea29219f41831044d8aba8c8dfb9309?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Dean</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-359"><time datetime="2012-11-07T20:45:29+00:00" pubdate class="published">
		 at <span class="hours">20:45pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Most people in this industry seem to fear that they will be found out and ridiculed by those with more experience. I am thankful that there are some of those people who write blog posts, and put themselves in the ‘firing line’ for us unassured types to lap up. I’m yet to see the ridiculing of anybody though, and that’s another thing to be thankful for! :)
	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-360">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/46c9d099a2dcb608f01b1eca5b07eb24?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/46c9d099a2dcb608f01b1eca5b07eb24?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Chris</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-360"><time datetime="2012-11-08T00:09:49+00:00" pubdate class="published">
		 at <span class="hours">00:09am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>Nice article :)

Like Jason mentioned in the comments I too would like to hear more about how you approach using JS for conditionally loading content.

Cheers</p>	</div>
</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-362">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/e1fb5c40b8e545b29fdf992b4cee083f?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/e1fb5c40b8e545b29fdf992b4cee083f?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://ayoungh.co.uk' rel='external nofollow' class='url'>Anthony Young</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-362"><time datetime="2012-11-08T21:43:08+00:00" pubdate class="published">
		 at <span class="hours">21:43pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Great post :) Very encouraging for me as I want to start blogging about little bits like this, although I doubt it will be as good as yours! Keep up the great articles
	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-364">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/766047c2f4d0bca639f03a66883197f6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/766047c2f4d0bca639f03a66883197f6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.markdixon.ca/design/blog/' rel='external nofollow' class='url'>Mark Dixon</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-364"><time datetime="2012-11-09T22:58:59+00:00" pubdate class="published">
		 at <span class="hours">22:58pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>I agree. It is fine to write about web design and front-end stuff even if you are not an “expert”. I have recently launched my new portfolio website and have included a blog section where I plan on writing about web design.

While doing client work we straddle a lot of areas and cannot be expected to know everything about everything.

Mea Culpa –; on my first responsive design I did a fair amount of display:none.

Cheers from Montreal,

Mark</p>	</div>
</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-366">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/68fc10515bccdf73374acc9fd8eaef1c?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/68fc10515bccdf73374acc9fd8eaef1c?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://rockfishdigital.com' rel='external nofollow' class='url'>John Jacobsen</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-366"><time datetime="2012-11-12T16:55:37+00:00" pubdate class="published">
		 at <span class="hours">16:55pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Excellent post. Very applicable across design, dev, and content creation. Thanks!
	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-368">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/156af4791ccd0d858fd2f8aba677d527?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/156af4791ccd0d858fd2f8aba677d527?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://carlhallberg.se' rel='external nofollow' class='url'>Carl Hallberg</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-368"><time datetime="2012-11-13T09:46:14+00:00" pubdate class="published">
		 at <span class="hours">09:46am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>Love the part on ‘Scattered learning’! Very important insight that not many of us think of from day to day. I feel safe to say that i’m learning new stuff each and every day, even the most basic tech but also on completely different topics that in hindsight definitely could have been worth blogging about.

Great post!</p>	</div>
</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-370">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/bf63dd177d3e9e747fa9541789477bec?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/bf63dd177d3e9e747fa9541789477bec?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://iloveresponsivedesign.com/' rel='external nofollow' class='url'>Fredrik Christensson</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-370"><time datetime="2012-11-14T08:27:34+00:00" pubdate class="published">
		 at <span class="hours">08:27am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Hey Laura, and thx for the post. I feel when we designing we dont get enough test time to see how the user are using the site. This is one of the biggest problems that I have encountered when iam design a responsive site.
	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-371">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/2a2eb8e1cdf0a995320902d12a8c1580?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/2a2eb8e1cdf0a995320902d12a8c1580?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Skweekah</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-371"><time datetime="2012-11-14T23:29:06+00:00" pubdate class="published">
		 at <span class="hours">23:29pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Very interesting article. I guess there’s always a better way of doing things, and if you can incorporate a little bit of better in each of the projects you are working on, you are challenging yourself and growing as a designer/developer.
	</div>
</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-372">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/6f9df81e888deeafc991848cccbec28a?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/6f9df81e888deeafc991848cccbec28a?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://velonomad.com' rel='external nofollow' class='url'>Tim</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-372"><time datetime="2012-11-15T20:51:49+00:00" pubdate class="published">
		 at <span class="hours">20:51pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		How about a concrete example workaround?
	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-374">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/cf358ee0bbb2df4a67b5ba0445d3ff7b?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/cf358ee0bbb2df4a67b5ba0445d3ff7b?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://lenanghai.net' rel='external nofollow' class='url'>Hai Web</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-374"><time datetime="2012-11-16T15:36:21+00:00" pubdate class="published">
		 at <span class="hours">15:36pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks bro.
	</div>
</li>
	<li class="comment odd alt thread-even depth-1" id="li-comment-377">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/8041da1c6cb6f4ad87734737c89b742e?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/8041da1c6cb6f4ad87734737c89b742e?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Søren Maarbjerg</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-377"><time datetime="2012-11-20T00:46:06+00:00" pubdate class="published">
		 at <span class="hours">00:46am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>Thanks for your encouragement.

Hiding images by display none is a big issue, because they load anyway. The following research breaks the ice by documenting that “background images attached to elements that are inside a element with display none are NOT loaded”: [http://timkadlec.com/2012/04/media-query-asset-downloading-results](http://timkadlec.com/2012/04/media-query-asset-downloading-results" rel="nofollow)

Loading images with a common 1x1px src (because the attribute cannot be empty) AND inline styling its background-image to the ‘original’ src you are able to control the load by conditionally replacing the src with the background-image src – and showing the parent element. Only then will the image load.</p>	</div>
</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-381">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/ff99ca2faa838f3836ed90270486551e?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/ff99ca2faa838f3836ed90270486551e?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Rob</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-381"><time datetime="2012-11-22T22:57:23+00:00" pubdate class="published">
		 at <span class="hours">22:57pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Good post, but I don’t see a concrete alternative solution here. An example would be beneficial.
	</div>
	<ul class="children">
		<li class="comment odd alt depth-2" id="li-comment-383">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/8041da1c6cb6f4ad87734737c89b742e?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/8041da1c6cb6f4ad87734737c89b742e?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Søren Maarbjerg</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-383"><time datetime="2012-11-23T11:51:54+00:00" pubdate class="published">
		 at <span class="hours">11:51am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Thanks Rob. Please see my replied suggestion on how to avoid caching images for a slideshow if viewport &lt; 480, on [http://timkadlec.com/2012/04/media-query-asset-downloading-results](http://timkadlec.com/2012/04/media-query-asset-downloading-results" rel="nofollow)
		</div>
	</li>
	<li class="comment even thread-even depth-1" id="li-comment-384">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/7b28ccde01ebe1b5f26ff4d1fac047d8?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/7b28ccde01ebe1b5f26ff4d1fac047d8?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.daydesignz.com' rel='external nofollow' class='url'>Dayana</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-384"><time datetime="2012-11-27T16:45:47+00:00" pubdate class="published">
		 at <span class="hours">16:45pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Great post, I always thought the same to myself about posting about things that should be “common knowledge” when indeed there can be several layers of knowledge to uncover. Loading mobile first is a great tip! Thanks for the post
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-386">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/cabf735ce7b8b4471ef46ea54f71832d?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/cabf735ce7b8b4471ef46ea54f71832d?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://player.fm' rel='external nofollow' class='url'>Michael Mahemoff</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-386"><time datetime="2012-12-10T03:46:30+00:00" pubdate class="published">
		 at <span class="hours">03:46am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Very familiar with this issue as I’ve strived to do RWD without having to customise much of the server-side or the JS. And doing so means display: none; is almost a necessity.

In an upcoming iteration, I’ve resorted to using more Ajax requests with checks for the user-agent. It’s arguably more naughty than just “display: none;”, because now there’s a bit of JS coupled to the stylesheet, but since it improves performance, it’s a net gain.
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-387">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/9400cb5aeb155ccec614652542fd274d?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/9400cb5aeb155ccec614652542fd274d?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://balupton.com' rel='external nofollow' class='url'>Benjamin Lupton</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-387"><time datetime="2012-12-10T05:08:14+00:00" pubdate class="published">
		 at <span class="hours">05:08am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		The last part raises a very interesting point, and is definitely something I find myself falling into a lot. Although, my train of thought feels that writing another blog post is just adding more noise to an already saturated library of good content –; if I figured it out already, then the answer is already there, what help does it do myself adding yet another article about it?

Perhaps the difference is how people get their learnings in the first place. A pre-supposition of this article appears that learning primarily occurs via blog posts and other forms of subscription based learning. I wonder how this mode of transport contrasts against learning when one encounters a problem then seeks an answer via google and stack overflow.

For instance, stack overflow is a fantastic place to ensure the content that is posted is of top notch quality, whereas with blog posts you do not have that guarantee that what you are reading is correct. However, with blog posts, you do get the subscription benefit.

Perhaps the solution to this dilemma is figuring out a way of combining stack exchange’s peer review and archival for searching abilities with blog posts careful curation, subscription and celebrity benefits.

Thoughts?
	</div>
	<ul class="children">
		<li class="comment byuser comment-author-laura bypostauthor odd alt depth-2" id="li-comment-390">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/55bb2acf65203dbb95c35a83e62e9ae6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Laura</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-390"><time datetime="2012-12-10T07:19:44+00:00" pubdate class="published">
		 at <span class="hours">07:19am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		While I think places like Stack Overflow are very useful and important, you really have to know the question that you want to ask. What if you just want to know tips and tricks?

I agree that me writing this on a blog doesn’t necessarily mean I’m right, or that I know what I’m talking about, but neither do I have that guarantee when I read blog posts written by other people. The ‘peer review’ element seems to come via social networks. If someone that I respect posts a link to a blog post, then they give that post credibility.

I think that learning on the web means we all need to doubt the credibility of what we read. We build up knowledge by reading a lot around these topics and then making judgments on what we choose to believe. These aren’t always black-and-white facts, there are a lot of grey areas where we rely on ‘opinion’ pieces to understand the ‘why’s to help us make more informed decisions about our work.
		</div>
	</li>
	<li class="comment even thread-odd thread-alt depth-1" id="li-comment-389">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/07fcd228af02d476b1b8367d85a903b2?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/07fcd228af02d476b1b8367d85a903b2?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://christianheilmann.com' rel='external nofollow' class='url'>Chris Heilmann</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-389"><time datetime="2012-12-10T06:42:10+00:00" pubdate class="published">
		 at <span class="hours">06:42am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Excellent points! What fascinates me more is that people are not taking advantage of matchmedia() enough –; it is the JS equivalent of mediaqueries. This means you can happily use the same query in CSS and JS to lazy-load content only when it is applicable. [https://hacks.mozilla.org/2012/06/using-window-matchmedia-to-do-media-queries-in-javascript/](https://hacks.mozilla.org/2012/06/using-window-matchmedia-to-do-media-queries-in-javascript/" rel="nofollow)
	</div>
	<ul class="children">
		<li class="comment odd alt depth-2" id="li-comment-394">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/fbdbe8df04185d71dc5a16ee749ad3a6?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/fbdbe8df04185d71dc5a16ee749ad3a6?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://NoTwoTheSame.com' rel='external nofollow' class='url'>Elliot Lewis</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-394"><time datetime="2012-12-10T17:22:21+00:00" pubdate class="published">
		 at <span class="hours">17:22pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		That is a great little function. But I didn’t think it worked in IE? I’m sure I tried it before and ended up using work arounds to stop IE exploding at unknown function.
		</div>
	</li>
	<li class="comment even thread-even depth-1" id="li-comment-391">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/a2da1a6747c31ab1587c665eb9a44e15?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/a2da1a6747c31ab1587c665eb9a44e15?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.maltonwebdesign.co.uk' rel='external nofollow' class='url'>Dave Andrew</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-391"><time datetime="2012-12-10T09:05:25+00:00" pubdate class="published">
		 at <span class="hours">09:05am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Great points Laura about sharing. IMO the more info the better. If think the more we share the more kudos you’ll gain and that respect may hopefully turn into business.
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-393">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/326239aac4f69abe4dc5285f21d6b902?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/326239aac4f69abe4dc5285f21d6b902?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.feliciafortes.com' rel='external nofollow' class='url'>Felicia Fortes</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-393"><time datetime="2012-12-10T16:31:53+00:00" pubdate class="published">
		 at <span class="hours">16:31pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>I like your thoughts and I’ve decided to share more of my newbie learnings.

I think every project has an individual path. For me blogging about things I’ve learnt during a project is a way to remember what I did  and at the same time being able to learn new stuff through the comments. </p>
Just look at all the new knowledge coming through this blog posts comments.
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-396">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/2c22ec5e9ac5e4af3a5853fe2fd67e77?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/2c22ec5e9ac5e4af3a5853fe2fd67e77?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://overthecounterdesign.com' rel='external nofollow' class='url'>Chatman R.</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-396"><time datetime="2012-12-11T12:55:09+00:00" pubdate class="published">
		 at <span class="hours">12:55pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		I haven’t actually been using `display: none;` very often on its own. I’ve mainly used JavaScript to hide elements I manipulate through a situational `.hide` class. I’ve gotten into a habit of using temporary classes for states to applied through JavaScript. This way, if something effs up, I won’t be hiding critical information from the user. 

If I ever find I’m hiding an element indefinitely, it usually means it’s time to figure out if it’s needed at all. And I liked your last point over not being afraid to contribute something to the pool of knowledge. My reluctance to write blog posts comes from the fact that I’m entirely self-taught, so I have a tendency to assume everything I know IS common knowledge and I have nothing to add. I may have to rethink that.
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-402">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/288f43b2e85b2451c08aa86f0e0453ad?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/288f43b2e85b2451c08aa86f0e0453ad?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.lockedowndesign.com/blog' rel='external nofollow' class='url'>John Locke</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-402"><time datetime="2013-06-09T09:26:24+00:00" pubdate class="published">
		 at <span class="hours">09:26am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Best practices are made up of all these little bits of information that we collect from people we trust in web development, and we don’t always listen the first time we hear things. But when we keep seeing the same things written over and over, then those standards and best practices begin to take hold in our own workflows.

I’m always looking for better ways to do things on the front-end, to make things faster loading, or smoother for the user. 

Thanks for being one of the voices of reason and being a mentor to many in the web industry.
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-404">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/d064c247ddb15d88a42533a8e1fac72c?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/d064c247ddb15d88a42533a8e1fac72c?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.catalystdesigns.co.uk' rel='external nofollow' class='url'>Paul</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-404"><time datetime="2013-07-21T18:04:53+00:00" pubdate class="published">
		 at <span class="hours">18:04pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Really well written post! Was looking into the use of display none to hide some elements on a responsive design and you’ve persuaded me to think otherwise! 

An article on how to do the JavaScript side of things would be great! Thanks.
	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-7385">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/21d7459891f57c63e6eb51b4861ce752?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/21d7459891f57c63e6eb51b4861ce752?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.kintoweb.com' rel='external nofollow' class='url'>Kintoweb</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-7385"><time datetime="2014-01-11T01:48:16+00:00" pubdate class="published">
		 at <span class="hours">01:48am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		It may be also possible to use iFrame and display:none on that to stop data downloading
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-33064">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/58ec733e2356433d0ec9af50ef904adb?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/58ec733e2356433d0ec9af50ef904adb?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://www.elmnt.com' rel='external nofollow' class='url'>Greg Smith</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-33064"><time datetime="2014-06-18T00:38:17+00:00" pubdate class="published">
		 at <span class="hours">00:38am</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		<p>“I’m a little bit scared of writing about markup. I’m sure there are loads of front-end developers out there who know a huge amount more than me, and I’m worried I’ll get it wrong or make myself look stupid.”

I bet most people feel the same way, so don’t worry. I’ve been designing &amp; (front-end) coding for more than 10 years, and I still read about &amp; play with the fundamentals all the time. I think it’s always important to keep re-visiting the basics, not just the very difficult stuff. Well done. Keep up the great work!</p>	</div>
</li>
	<li class="comment odd alt thread-odd thread-alt depth-1" id="li-comment-37332">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/54729a3423ebee623690bfc0c4edfa58?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/54729a3423ebee623690bfc0c4edfa58?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://blog.ki6i.com' rel='external nofollow' class='url'>Kalina</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-37332"><time datetime="2014-07-09T13:45:05+00:00" pubdate class="published">
		 at <span class="hours">13:45pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Most browsers like Chrome and Firefox doesn’t actually spend time on the display none content on page load. In other words the load time it about the same as if the content isn’t there.The only browsers that have this issues are IE&lt;11
	</div>
</li>
	<li class="comment even thread-even depth-1" id="li-comment-150438">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/93c1dd2037e7b96a0fcdffb20cb82bf4?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/93c1dd2037e7b96a0fcdffb20cb82bf4?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn"><a href='http://korosheh.com' rel='external nofollow' class='url'>korosheh</a></cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-150438"><time datetime="2016-09-19T21:13:31+00:00" pubdate class="published">
		 at <span class="hours">21:13pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Is nice article thanks
	</div>
</li>
</ol>
