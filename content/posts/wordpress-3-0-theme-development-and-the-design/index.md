---
title: "WordPress 3.0 Part 3—Theme Development and the Design"
draft: false
colours: ["#dc7a1e", "#216F94", "#F7F7F7", "#D54E21", "#D7D7D7", "#B4411B", "#525252"]
date: 2010-07-16T21:50:57+00:00
categories: ["WordPress"]
tags: ["accessibility", "custom backgrounds", "custom headers", "menus", "theme development", "twentyten", "usability", "wordpress", "wordpress 3.0", "wordpress admin"]
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

This post has three parts. This is part three. Visit the other parts below:

* Part 1: [WordPress 3.0—Pre 3.0 and Beyond](/wordpress-3-0-pre-3-and-beyond)
* Part 2: [WordPress 3.0—Really WordPress 3.0](/wordpress-3-0-really-wordpress-3)

---

## Easier for theme developers to make it easy for users

The following WordPress 3.0 features really make it easier for the big-time theme developers who create highly customisable themes.

### Menus

This is brilliant. Before the menus feature, we had to bodge any extra links we wanted on to the end of the wp_list_pages (that just lists pages!) function without much control on what was shown, and only being able to adjust the orders of the pages by entering a number into a clunky text box.

Now you can easily create drag-and-drop menus with custom links place anywhere within the navigation. This enables users to:

* Nest pages and links that don’t already have parent-child relationships in the Page hierarchy.
* Use different names for the pages in the navigation (handy if you want to call the ‘About’ page ‘Home’ in the navigation.
* Link to pages on totally different websites.

{{< figured caption="WordPress menus in action" >}}
  {{< imgsrcset original="Screen-shot-2010-07-16-at-20.42.35.png" alt="WordPress menus in action" >}}
{{< /figured >}}

All these functions are perfect for users who don’t want to get their hands dirty in the PHP files and make it easier for theme developers as they just need to add the menu function to their functions.php file and use the right template tag to include the customised menus in their themes.

```add_action( 'init', 'register_my_menu' ); function register_my_menu() { register_nav_menu( 'navigation-menu', __( 'Navigation Menu' ) ); }```

Add this to the functions.php file to register a menu by the name of ‘Navigation Menu’

```&lt;?php wp_nav_menu( array( 'theme_location' =&gt; 'navigation-menu' ) ); ?&gt;```

Add this to the template file wherever you want to include the menu.

### Custom backgrounds and headers

For theme creators making themes for a wide user base, custom backgrounds and headers are very useful. Most of the big name theme producers have offered custom backgrounds and headers as part of their ultra-sexy, ultra-customisable themes for a long time but now the smaller scale theme developers can do this by adding some extra functions to their functions.php file and into the relevant template files.

I haven’t tried creating a theme with these features yet, as I tend to give my clients one custom-created choice as part of the web design, but you can see custom backgrounds and headers in action in the new default theme, TwentyTen, which I use on this blog. You should be able to see that big yellow block at the top of the page. This is a custom header image I created and uploaded using the settings under Appearance &gt; Header.

As you can see from my image below, it’s incredibly easy to upload your own header or you can pick from one of the beautiful photographs taken by Matt Mullenweg, the creator of WordPress.

{{< figured caption="Custom headers in WordPress 3.0" >}}
  {{< imgsrcset original="Screen-shot-2010-07-16-at-19.45.28.png" alt="Custom headers in WordPress 3.0" >}}
{{< /figured >}}

If you want to know more about using custom backgrounds and headers, I’d recommend taking a look at the reasonably well-commented code in the [TwentyTen theme](http://wordpress.org/extend/themes/twentyten). Unfortunately I haven’t got any other recommended bookmarks for this yet, I hope you’ll forgive me!

## Change in design

### TwentyTen

WordPress 3.0 also comes with a cool new default theme called TwentyTen. It was getting to the point where no decent blog would be seen dead in the old WordPress default theme, so it was definitely in need of change.

TwentyTen is clean and simple (and the theme I use on my blog) and takes advantage of the custom backgrounds, headers and menus to make it easy to change the look and feel without having to get into the CSS.

{{< figured caption="TwentyTen default theme preview" >}}
  {{< imgsrcset original="Screen-shot-2010-07-16-at-20.45.55.png" alt="TwentyTen default theme preview" >}}
{{< /figured >}}

If you want to try TwentyTen out, you can find it in the [WordPress theme repository](http://wordpress.org/extend/themes/twentyten) and through the Themes &gt; ‘Install’ section in your WordPress admin by searching ‘twentyten’.

### WordPress admin realign

If you follow me on Twitter, you might have heard me whining a bit about the new WordPress admin realign. I’ll call it a realign as they’ve only made some changes, not redesigned the lot.

The idea behind these changes is that it brings the content into focus, and it is more legible to read dark text on a light background so it makes the WordPress admin, which is now entirely dark on light, more accessible.

{{< figured caption="WordPress 3.0 admin" >}}
  {{< imgsrcset original="Screen-shot-2010-07-16-at-20.48.11.png" alt="WordPress 3.0 admin" >}}
{{< /figured >}}

I have the utmost respect for those working on the WordPress admin interface, and have briefly discussed the decisions with [John O’Nolan](https://twitter.com/JohnONolan), member of the Core WordPress UI Team, on Twitter. I appreciate their reasons behind the changes and that it must be very difficult to please everybody in these scenarios. (Here comes the *but*)

**But** I find the new admin harder to use, and I don’t believe it is out of a lack of familiarity. Here are my reasons:

1. #### There is a general lack of contrast across all the admin

{{< imgsrcset original="Screen-shot-2010-07-16-at-20.48.11.png" alt="WordPress 3.0 admin" >}}

It is all dark grey against white and light grey backgrounds separated by light grey border lines. My eye isn’t drawn to any different elements anymore, it doesn’t suggest so strongly where I am or where I should go first. I’m an idiot and need to be led!

2. #### When you select the title text box when creating a new post, the label for the text box disappears

{{< figured caption="Um, what does that empty box do again? (title input in editor)" >}}
  {{< imgsrcset original="Screen-shot-2010-07-16-at-20.50.52.png" alt="The title input box in the WordPress editor with no label text" >}}
{{< /figured >}}

If you have cognitive issues, I can’t see how this is accessible. Chances are, you’ll select that first input box available and then be clueless about what that box is for. The label-in-an-input-box isn’t yet a strong-enough standard to make it obvious that you need to deselect the text input. It’s more of a consistent pattern for search input boxes, where the function is made obvious by the accompanying presence of a ‘Search’ button.

3. #### I find dark grey a really peculiar choice of colour for an alert

{{< figured caption="Grey alert bubble" >}}
  {{< imgsrcset original="Screen-shot-2010-07-16-at-20.52.41.png" alt="Grey alert bubble on the WordPress admin" >}}
{{< /figured >}}

This little alert that lets you know if you have comments, or need to update your plugins or WordPress installation, used to be orange. Orange stood out against the mostly white/grey/blue colour scheme and was clearly there to be noticed. Orange signifies something to be aware about, not quite red being something dangerous but not green for ‘everything is fine’. Even though this new alert style is a reversible of the dark-on-light text shown everywhere else, I think it’s a very unusual choice to have something less colourful for an alert.

To be fair these changes haven’t made the admin unusable. I am being picky. It would be very difficult to undo all the great work of Jane Wells and the UI team since WordPress 2.7.

---

This post has three parts. This is part three. Visit the other parts below:

* Part 1: [WordPress 3.0—Pre 3.0 and Beyond](/wordpress-3-0-pre-3-and-beyond)
* Part 2: [WordPress 3.0—Really WordPress 3.0](/wordpress-3-0-really-wordpress-3)

## One comment

<ol class="commentlist">
	<li class="comment even thread-even depth-1" id="li-comment-25">
			<div class="comment-author vcard">
			<img alt='' src='https://1.gravatar.com/avatar/41548ecfe0816ed4a7c8817472993478?s=72&amp;d=mm&amp;r=g' srcset='https://1.gravatar.com/avatar/41548ecfe0816ed4a7c8817472993478?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">pronebird</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-25"><time datetime="2010-10-26T19:44:13+00:00" pubdate class="published">
		 at <span class="hours">19:44pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		The dark gray is not flaring but better than annoying orange(maybe even closer to red) that was before, in WordPress 2.6.
	</div>
</li>
</ol>

	
