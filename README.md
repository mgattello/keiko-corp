## Improve Website Performance

First thing first, I opened PageSpeed and WebPage Test, and see the results:

### Mobile and Desktop:

![mobile](/img/a.png) ![desktop](/img/b.png)

Suggestion from PageSpeed:

![mobile_suggestion](/img/a1.png) ![desktop_suggestion](/img/b1.png)

### Plan

1. It's clear that the images are the main problem in this website. They are too heavy and not compressed. I'm going to delete the metadata and compress the images. 

2. The scripts will be placed before the `</body>`, preventing the DOM to be blocked.

3. I'll check all the CSS and JS files:

    - CSS: I'll delete the unecessary code and merge the files in 1 if possible
    - JS: I'll merge all the files if possible

    >   reset.css empty file not needed
    >   scrollTo.js not needed
    >   I used the Above the fold loading technique, for loading owl.carosuel, theme and transitions   used only at the end of the website

Doing so will help me to reduce the total requests and preventing interuption during the creation of the Render Tree.

4. Check if I could use `<script async>` or `<script defer>`

    >   jQuery must be loaded 

5. Check if I could use media query

6. Minify HMTL, CSS and JS files