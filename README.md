## Improve Website Performance

First thing first, I opened PageSpeed and WebPage Test, and see the results:

### Mobile and Desktop:

![mobile](/img/a.png) ![desktop](/img/b.png)

Suggestion from PageSpeed:

![mobile_suggestion](/img/a1.png) ![desktop_suggestion](/img/b1.png)

## Plan

1. It's clear that the images are the main problem in this website. They are too heavy and not compressed. I'm going to delete the metadata and compress the images.

#### Action

>   All images are now compressed but they still to many

2. The scripts will be placed before the `</body>`, preventing the DOM to be blocked.

#### Action

>   All script are before the `</body>`

3. I'll check all the CSS and JS files:

    - CSS: I'll delete the unecessary code and merge the files in 1 if possible
    - JS: I'll merge all the files if possible

Doing so will help me to reduce the total requests and preventing interuptions during the creation of the Render Tree.

#### Action

>   Bin: reset.css, scrollTo.js, jquery (CDN used), ajaxchimp.js (CDN used), nicescroll.js (CDN used), wow.js (CDN used), bootstrap.css (CDN used), animate.css (CDN used), parallex.js *

* parallelx.js: (although is used in the intro for creating an animation, I think removing it will be more beneficial for the overall performance, considering that is used only for a small animation and creating a weird effect when you open the page. )


4. Check if I could use `<script async>` or `<script defer>`

#### Action

>   `<script defer>` for ajaxchimp.js 
>   `<script async>` for carousel and nicescroll


6. Minify HMTL, CSS and JS files

#### Action

> All files minified




