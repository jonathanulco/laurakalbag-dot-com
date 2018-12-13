---
title: "Processing Responsive Images with Hugo"
date: 2018-12-13T11:42:31Z
draft: true
tags: ["responsive", "Image Processing", "Hugo"]
categories: ["Development"]
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
imagealt: ""
---

I’d got to the point where I was embarrassed to share my blog posts, particularly image-heavy posts, as I was handling responsive images so badly. The images were all huge and it was my only big barrier in web performance (no tracking here!). With an archive of blog posts going back nearly a decade, it was going to be a big job to get my whole site working consistently, but I had an inkling I might be able to do it with [Hugo’s Image Processing](https://gohugo.io/content-management/image-processing/).<!--more-->

Over the last few weeks, iteratively and clumsily, I’ve developed a system that works for me:

For writing content:
- My content is written in markdown, using shortcodes that mirror the HTML output as closely as possible.
- Images live in the same folder as their post (in [page bundles](https://gohugo.io/content-management/page-bundles/)).
- Every image can be used alone, wrapped in a `figure` with a `figcaption`, and/or wrapped in a link. Multiple images can be used inside one figure.
- Every image has `alt` text, even if it’s used outside of its post.

For responsiveness:
- Each image is resized into multiple sizes by Hugo, and included in the `srcset` list for the `img`.
- Images grouped in figures can be arranged in a responsive grid.

For maintainability:
- An example of the shortcode is included by default with every new post. Because I have a terrible memory, and I can only keep updating my blog if it’s *really* easy to do so.

## Hugo page bundles

[Hugo’s page bundles](https://gohugo.io/content-management/page-bundles/) are a way to structure your Hugo content hierarchy. Page bundles are useful as they enable you to group resources (such as images) with a post without having to include them in that post’s front matter. You could just include a shortcode in the post (or outside the post) that says “grab all the images that match these criteria.”

Resources with a type of `image` can also be processed by [Hugo’s Image Processing](https://gohugo.io/content-management/image-processing/). Processing is what enabled me to generate multiple image sizes from one original image. So I had to ensure all my posts used the page bundle content hierarchy.

It took a long time to get my head around page bundles. The Hugo documentation can be abstract as it tries to cover as many use cases as possible. (The brevity of the Hugo documentation can also be infuriating, and if one more person tells me that it’s “open to pull requests,” I will scream.) My understanding on page bundles boils down to this:

- if a file is called `_index.md`, it is considered the index of a section/kind, and so uses the list.html template.
- if a file is called `index.md`, it is considered the index of a page/post, and so uses the single.html template.

So, to put my blog posts in page bundle hierarchy, where its images could be used as resources, I had to restructure them to match the following pattern:

```
/processing-responsive-images-with-hugo
- index.md
- screenshot.jpg
- screenshot2.jpg
```

If you name your page `_index.md`, the images will not register as page resources, the image processing will not work. I lost an hour to that, I hope you don’t!

As my blog posts were all previously in a WordPress-style hierarchy that had been hurriedly refactored into Hugo, my blog posts were named `processing-responsive-images-with-hugo.md`, and all images were held in date-based folders inside the /static folder. Cue a lot of RegEx, a renaming script kindly written for me by [Aral](https://ar.al), and a lot of time manually moving images around until running `hugo server -D` no long spat out errors.

## Shortcodes

*Caveat*: I’m relatively new to Hugo, Go, and the templating language (I don’t know what it’s called). My code may not be pretty, but it works! If you have any suggestions for improvement, I’d appreciate them.

### Images

In a post, I can include an image in the markdown using the `img` shortcode:

{{< highlight markdown >}}
{{</* img src="theonion.jpg" alt="Screenshot of the Onion homepage" */>}}
{{< /highlight >}}

This will output the final HTML, resizing `theonion.jpg` into three sizes, 500px wide, 800px wide, and 1200px wide. For browsers that do not support the `srcset` attribute, the `src` is set to one of the middle-sized images (hopefully not too big too load or too small to look ok.) The `sizes` attribute has a sensible default for images that fill most of/the whole width of the viewport, but this can be overridden in the shortcode:

{{< highlight html >}}
<img sizes="(min-width: 35em) 1200px, 100vw" 
  srcset="/you-wont-believe-what-happens-next/006_…_472240_500x0_resize_q100_gaussian.jpg 500w, /you-wont-believe-what-happens-next/006_…_472240_800x0_resize_q100_gaussian.jpg 800w, /you-wont-believe-what-happens-next/006_…_472240_1200x0_resize_q100_gaussian.jpg 1200w" src="/you-wont-believe-what-happens-next/006_…_472240_1200x0_resize_q100_gaussian.jpg" 
  alt="Screenshot of the Onion homepage">
{{< /highlight >}}

[See this image example in action on my post ‘Digital Assistants, Facebook Quizzes, And Fake News! You Won’t Believe What Happens Next’](/you-wont-believe-what-happens-next/).

Using the shortcode code:

`layouts/shortcodes/img.html`:
{{< highlight go-html-template >}}
{{/* get file that matches the filename as specified as src="" in shortcode */}}
{{ $src := .Page.Resources.GetMatch (printf "*%s*" (.Get "src")) }}

{{/* set image sizes, these are hardcoded for now, x dictates that images are resized to this width */}}

{{ $tinyw := default "500x" }}
{{ $smallw := default "800x" }}
{{ $mediumw := default "1200x" }}
{{ $largew := default "1500x" }}

{{/* resize the src image to the given sizes */}}

{{ .Scratch.Set "tiny" ($src.Resize $tinyw) }}
{{ .Scratch.Set "small" ($src.Resize $smallw) }}
{{ .Scratch.Set "medium" ($src.Resize $mediumw) }}
{{ .Scratch.Set "large" ($src.Resize $largew) }}

{{/* add the processed images to the scratch */}}

{{ $tiny := .Scratch.Get "tiny" }}
{{ $small := .Scratch.Get "small" }}
{{ $medium := .Scratch.Get "medium" }}
{{ $large := .Scratch.Get "large" }}

{{/* only use images smaller than or equal to the src (original) image size, as Hugo will upscale small images */}}
{{/* set the sizes attribute to (min-width: 35em) 1200px, 100vw unless overridden in shortcode */}}

<img 
  {{ with .Get "sizes" }}sizes='{{.}}'{{ else }}sizes="(min-width: 35em) 1200px, 100vw"{{ end }}
  srcset='
  {{ if ge $src.Width "500" }}
    {{ with $tiny.RelPermalink }}{{.}} 500w{{ end }}
  {{ end }}
  {{ if ge $src.Width "800" }}
    {{ with $small.RelPermalink }}, {{.}} 800w{{ end }}
  {{ end }}
  {{ if ge $src.Width "1200" }}
    {{ with $medium.RelPermalink }}, {{.}} 1200w{{ end }}
  {{ end }}
  {{ if ge $src.Width "1500" }}
    {{ with $large.RelPermalink }}, {{.}} 1500w {{ end }}
  {{ end }}'
  {{ if .Get $medium }}
    src="{{ $medium.RelPermalink }}" 
  {{ else }}
    src="{{ $src.RelPermalink }}" 
  {{ end }}
  {{ with .Get "alt" }}alt='{{.}}'{{ end }}>
{{< /highlight >}}

Reading the comments above, you might notice that Hugo will upscale small images, so if your original image is only 1200px wide, it will still generate a blurry mess at 1500px wide. My solution was to include the images in the srcset list only if they were narrower than the original width.

### Figures

In a post, I can include one or more images wrapped in a figure using the `figure` shortcode:

{{< highlight markdown >}}
{{</* figure class="grid two" figcaption="Inevitable" */>}}
  {{</* img src="osky-1.jpg" alt="Selfie of me and Oskar the huskamute, he’s looking at me." */>}}
  {{</* img src="osky-2.jpg" alt="Selfie of me and Oskar the huskamute, he’s licking my face." */>}}
{{</* /figure */>}}
{{< /highlight >}}

This uses the `img` shortcode, and wraps it in the `figure` shortcode, just as you would with the `<img>` and `<figure>` elements in the HTML. The figcaption is included in the figure shortcode though (this wouldn’t work in HTML!) I may adjust that part of the shortcode to behave more like the `<figure>` HTML in the future.

I’ve also included CSS that uses the `grid` and `two` class names to lay out the images to make better use of the available space. This will output the following HTML, similar to the previous example, but with an extra `figure` around it:

{{< highlight html >}}
<figure class="grid two">
  <img sizes="(min-width: 35em) 1200px, 100vw" srcset="
  /photos/5/osky-1_…_500x0_resize_q100_gaussian.jpg 500w, /photos/5/osky-1_…_800x0_resize_q100_gaussian.jpg 800w" src="/photos/5/osky-1_…_1200x0_resize_q100_gaussian.jpg" 
  alt="Selfie of me and Oskar the huskamute, he’s looking at me.">
  <img sizes="(min-width: 35em) 1200px, 100vw" srcset="/photos/5/osky-2_…_500x0_resize_q100_gaussian.jpg 500w, /photos/5/osky-2_…_800x0_resize_q100_gaussian.jpg 800w"   
  src="/photos/5/osky-2_…_1200x0_resize_q100_gaussian.jpg" 
  alt="Selfie of me and Oskar the huskamute, he’s licking my face.">
  <figcaption>
    <p>Inevitable</p>
  </figcaption>
</figure>
{{< /highlight >}}

[See this image example in action on a photo post](/photos/5/).

Using the shortcode code:

`layouts/shortcodes/figure.html`:

{{< highlight go-html-template >}}
<figure {{ with .Get "class" }}class="{{.}}"{{ end }}>
  {{.Inner}}
    <figcaption>
      <p>{{ .Get "figcaption" }}</p>
  </figcaption>
</figure>
{{< /highlight >}}

This shortcode is much simpler than the default Hugo `figure.html` shortcode because I’m fairly sure I use figures consistently on my site.

### Linked images

Previously, I had a strange setup where, if I wanted an image to link to elsewhere, I would wrap the shortcode in a markdown link:

{{< highlight markdown >}}
[{{</* img etc */>}}](https://website.com)
{{< /highlight >}}

Nesting that many brackets makes it way too easy to make typos, so I just made a quick little shortcode for links. It will work with anything, not just images, but is ideal for wrapping around other shortcodes:

{{< highlight markdown >}}
{{</* link href="https://theonion.com" */>}}
  {{</* img src="theonion.jpg" alt="Screenshot of the Onion homepage" */>}}
{{</* /link */>}}
{{< /highlight >}}

Using this shortcode `layouts/shortcodes/link.html`:
{{< highlight go-html-template >}}
<a {{ with .Get "href" }}href="{{.}}"{{ end }}>
  {{.Inner}}
</a>
{{< /highlight >}}

I could’ve called the shortcode “`a`” to be more consistent with HTML, but with my forgetful future self in mind, I thought `link` to be more memorable.

### Archetypes

Even though these shortcodes are (mostly) consistent with their HTML output, I have a terrible memory for shortcodes, acronyms, and any type of code that doesn’t follow a memorable pattern. To save myself the time copy-pasting the shortcodes every time I write a new post, I added little placeholder shortcodes to the [archetypes](https://gohugo.io/content-management/archetypes) for each post type. So my `archetypes/post.md` file looks a little like this:

{{< highlight markdown >}}
---
title: "{{ replace .TranslationBaseName "-" " " | title }}"
date: {{ .Date }}
draft: true
tags: []
categories: []
type: "post"
body_classes: "blog"
---

Post text<!--more-->

{{</* figure figcaption="caption text" */>}}

  {{</* img src="filenameX" alt="alt text" */>}}

{{</* /figure */>}}
{{< /highlight >}}

### Handling galleries

One of the great features when using image processing in page bundles is that you can grab the images outside of the post for a gallery. It’s what I’m doing for my [Photos page](/photos/).

Each photo list page gets all the photo posts, and then uses my `summary-photo.html` partial to render each image. I needed the images in the photo gallery to display differently from a blog post. There’s no need to load massive images in for small thumbnails. I also wanted the photos arranged in a grid, so I used image processing to resize and crop the images the fill the desired space:

{{< highlight go-html-template >}}
<li class="post photo-post">
  <a href="{{.Permalink}}">
    <img
      {{ with .Resources }}
        {{ with .GetMatch "{*.*,*.jpg,*.png,*.jpeg}" }}
        {{ $photo := .Fill "600x600" }}
        {{ with $photo }}
          src='{{ .Permalink }}'  
        {{ end }}
      {{ end }}
    {{ end }}
    alt="{{ .Params.imagealt }}"/>
  </a>
</li>
{{< /highlight >}}

This code just grabs the first image associated with each photo post. But there’s a problem with only grabbing an image: there’s no alternative text (`alt` attribute) associated with that image file alone.

### Making the gallery more accessible

This is where the `alt="{{ .Params.imagealt }}"` comes in. For each photo post, it checks the post’s [front matter](https://gohugo.io/content-management/front-matter) for some alternative text. Going back to my earlier example, the first image in the figure looks like this:

{{< highlight markdown >}}
{{</* img src="osky-1.jpg" alt="Selfie of me and Oskar the huskamute, he’s looking at me." */>}}
{{< /highlight >}}

So all I need to do is duplicate that `alt` text in the front matter of that post. The whole post looks something like this:

{{< highlight markdown >}}
---
title: 20 July 2018 21:28 IST
date: 2018-07-20T21:28:23+01:00
tags: ["oskar"]
aliases:
  - /photos/2018/07/20/21/28/index.md
body_classes: "notes latest"
imagealt: "Selfie of me and Oskar the huskamute, he’s licking my face."
---

{{</* figure class="grid two" figcaption="Inevitable" */>}}
  {{</* img src="osky-1" alt="Selfie of me and Oskar the huskamute, he’s looking at me." */>}}
  {{</* img src="osky-2" alt="Selfie of me and Oskar the huskamute, he’s licking my face." */>}}
{{</* /figure */>}}

{{< /highlight >}}

In the future, I could probably find a way to automate this, rather than creating the repetition. But for now, my images are that bit more accessible, and that’s the important thing!

I hope documenting all of this will help someone else. I’m sorry my code examples aren’t very pretty, and I’ve not yet got all the dashes in to wrangle the [whitespace in Go](https://gohugo.io/templates/introduction/). Just before this post was published, I also got social media meta images in the `<head>` of my pages generating at the right sizes, so let me know if that might be a useful snippet to blog too!
