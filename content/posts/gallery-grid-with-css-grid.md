---
title: "Gallery Grid With CSS Grid"
date: 2018-07-02T19:25:46+01:00
tags: ["css", "CSS grid layout", "html"]
categories: ["development"]
body_classes: "blog colours-006"
---

[CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) is great. My site layout is fairly simple, so had no need for lots of grid—I only used it for lining up comments and avatars on old blog posts.<!--more-->

Working on my [Notes](/notes) section, I realised I’d sometimes be adding multiple images (dog photos) in one note. The default style for my images is big and full-width, but two or three full-width images in rows would likely be overwhelming. It’d be much tidier if all the images auto-filled across the row. Regardless of how many images there are in the notes.

My HTML for these notes looks something like this:

```
<figure class="note-image">
	<img src="2018/06/14/21/osky1.jpg" alt="Oskar with his head on a cushion and begging eyes."/>
	<img src="2018/06/14/21/osky2.jpg" alt="Oskar with his head on a cushion and closed eyes."/>
	<img src="2018/06/14/21/osky3.jpg" alt="Oskar with his head on a cushion and begging eyes open again."/>
    <figcaption><p>How could you say no to this face?</p></figcaption>
</figure>
```

Sometimes there is one image, sometimes two or three. I concluded there would rarely be more than three, though I’ll adjust the CSS accordingly if that is ever the case. Sometimes there is a caption, sometimes there isn’t.

The CSS is remarkably minimal:

```
figure {
    display: grid;
    grid-template-areas:
        "image1 image2 image3"
        "figcaption figcaption figcaption";
}

figcaption {
    grid-area: figcaption;
}
```

The images auto-fill across the first row, filling all available space. If there’s no image2 or image3, image1 fills 100% of the available width.

The figcaption always fills the whole width, regardless of whether there is one, two, or three images above it.

<figure class="note-image always-full-height">
    <a href="/images/2018/07/figures.jpg">
        <img src="/images/2018/07/figures.jpg" alt="Four sets of images showing single, double, and triple image layouts." width="500px">
    </a>
    <figcaption>
        <p>The results. Note the two side-by-side portrait images do not fill the width of the viewport as the <code>max-height</code> of the images is set to <code>100vh</code>.</p>
    </figcaption>
</figure>

Isn’t that fabulous?

As always, everything I’m learning about CSS Grid Layout is from work by Rachel Andrew and Jen Simmons. Resources I used to inform my decisions/cobble this together were from:

- [Auto-Sizing Columns in CSS Grid: `auto-fill` vs `auto-fit` by Sara Soueidan on CSS Tricks](https://css-tricks.com/auto-sizing-columns-css-grid-auto-fill-vs-auto-fit/)
- [Flexible Sized Grids with auto-fill and minmax by Rachel Andrew](https://www.rachelandrew.co.uk/archives/2016/04/12/flexible-sized-grids-with-auto-fill-and-minmax/)
- [No Clearing Required by Rachel Andrew on Grid By Example](https://gridbyexample.com/examples/example12/)