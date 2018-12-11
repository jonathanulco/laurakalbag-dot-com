---
title: "Sass for Designers — The Setup"
draft: false
colours: ["#b047b6", "#404040", "#bb1e88", "#783b7b", "#d39ed6", "#652a5e", "#d7d7d7"]
date: 2012-12-28T17:51:36+00:00
categories: ["Markup"]
tags: ["Codekit", "CSS", "preprocessors", "Sass"]
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

As an accompaniment to my post on [Sass for Designers](/sass-for-designers/ "Sass for Designers") (why and how you should use Sass) I thought I’d better include a quick writeup on my setup for working with Sass in the hope that it’ll help you get started. I’m afraid I work on a OS X, so my instructions will only be good for Macs.

Of course, all of this can be done with the command line and other terrifying tools. I’m very impressed by those who can remember all the commands and quickly get everything working silently in the background. I don’t find this very easy, and prefer to use apps to help me out.

## Codekit

[Codekit](http://incident57.com/codekit/) does all the processing for you. It takes your Sass and spits it out into fully-working CSS. It does loads of other clever things too, but I mostly just use it for Sass. [Go download it](http://incident57.com/codekit/) and give it a go. I think you’ll find it’s definitely worth paying for.

{{< figure >}}
  {{< link href="http://incident57.com/codekit/" >}}
  	{{< imgsrcset alt="screenshot of the Codekit website" original="codekit.png" >}}
  {{< /link >}}
{{< /figure >}}

In order to get started with Codekit and Sass, you’ll need a /sass folder in your project where you keep all your Sass files. Sass files can contain plain old CSS or Sass-style CSS but they must have the extension .scss.

{{< imgsrcset alt="screenshot showing .scss file in the /sass folder" original="sass-folder.png" >}}

Next you open Codekit and add your project folder in the Files section.

{{< imgsrcset alt="screenshot of adding a new project to the Files pane in Codekit" original="codekit-new1.png" >}}

After you’ve added your project folder, Codekit will automatically find the Sass file inside your project.

{{< imgsrcset alt="screenshot of a project in Codekit" original="project-in-codekit.png" >}}

If you then go into your .scss file and add some Sass, as soon as you save that file, Codekit will compile it into CSS for you.

{{< imgsrcset alt="screenshot of basic Sass being written into a .scss file" original="new-sass.png" >}}

If you go to the Log tab in Codekit, you can see that your Sass was successfully compiled into CSS.

{{< imgsrcset alt="screenshot of the Log in Codekit showing a file successfully compiled" original="codekit-log1.png" >}}

If you then go back to look in your project folder, you can see where Codekit has compiled your CSS into a /css folder containing a .css file. It’s this file that you will reference in your HTML, not the .scss file.

{{< imgsrcset alt="screenshot showing the /css folder created by Codekit" original="css-folder.png" >}}

Codekit is very smart. If you write invalid Sass, it will give you an error. This can be really helpful if you’re new to writing Sass. For example, here I’ve used a `#` hash symbol instead of a `$` dollar sign when creating a variable.

{{< imgsrcset alt="screenshot of invalid Sass using # instead of $" original="bad-sass.png" >}}

As with all validators, it’s not always easy to understand what the validation error message means (!) but it can be helpful to be pointed towards the line where the error occurs.

{{< imgsrcset alt="screenshot of Codekit showing an error in the Sass" original="codekit-error.png" >}}

## And you’re done

Those are the very basics you need when getting started with Sass. If anyone has any further suggestions for Sass tools, particularly on other OSes, please let me know!

## One comment

<ol class="commentlist">
	<li class="comment even thread-even depth-1" id="li-comment-426">
			<div class="comment-author vcard">
			<img alt='' src='https://secure.gravatar.com/avatar/30237178832faefa2a7e79998d46648d?s=72&amp;d=mm&amp;r=g' srcset='https://secure.gravatar.com/avatar/30237178832faefa2a7e79998d46648d?s=144&amp;d=mm&amp;r=g 2x' class='avatar avatar-72 photo' height='72' width='72' /><cite class="fn">Dave Rutter</cite>
				<aside class="comment-meta commentmetadata"><p><a href="#comment-426"><time datetime="2013-01-07T22:33:09+00:00" pubdate class="published">
		 at <span class="hours">22:33pm</span></time></a></p>
	</aside>
	</div>
	<div class="comment-entry">
		Hi Laura

You may have seen this already since writing this post but Hammer app looks very interesting ([http://hammerformac.com/](http://hammerformac.com/" rel="nofollow)). OSX only again I’m afraid. The in development mixture.io may also be of interest, especially for multi-device testing.

I’ve just come across your site and really enjoyed digging around. Keep up the good work.
	</div>
</li>
</ol>
