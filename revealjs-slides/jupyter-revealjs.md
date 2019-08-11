
---
title: How to add interactivity to revealjs slides from jupyter notebooks
---

## Preparation
- First clone or wget the reveal.js-master in a folder
- Make sure that you have git and pandoc installed
- Create a github repository (let's say 'foo')
- Create a gh-pages branch where you will push the changes
- Your slide deck will be viewable at 
- `https://username.github.io/foo/slides.html`

## Create the slides in jupyter notebooks
- Write the content of the slide as a markdown block
- Use the conventions of images, tables, and lists to style your markdown block
- Your analyses will produce tables and images
- You can add those tables and images directly to the markdown block

## Using Pandoc to produce reveal.js slides
- This is most intuitive unless you want to directly add markdown blocks
- First convert the jupyter notebook to a markdown file using `jupyter nbconvert`
- Then use pandoc to convert the markdown file to html using reveal.js

## Code for jupyter nbconvert

```
jupyter nbconvert --to markdown foo.ipynb
```

## Code for converting markdown to html using pandoc
```
pandoc -t revealjs -s -o myslides.html myslides.md 
        -V revealjs-url="reveal.js-master"
        -V theme=$theme -V transition=cube
```

##  Link to learn more about this
[Pandoc link](https://github.com/jgm/pandoc/wiki/Using-pandoc-to-produce-reveal.js-slides)

## Let's add some interactivity to the slides
- How to step through the slides
- How to add an iframe 
- How to add a background image for a slide

# Pandoc slide deck creation rules

## Slide level
- Highest heading level followed by text
- At the slide level: new slide
- Below the slide level: headings within a slide
- Above the slide level: title slides
- Above the slide level: title slide for a section
- Do not produce more than two levels (1 and 2)

## Start a new slide
- Horizontal rule
- A heading at slide level

## How to produce incremental lists
- Use the i option
- Use the > sign
- Specify that it is incremental

## This is an incremental list
::: incremental

- This is the first element
- The second element will wait for a mouse click

::: 

## This is another incremental list
> - This is the first element
> - This is the second element that waited for mouse click

## Show two columns in a slide
:::::::::::: {.columns}

::: {.column width="50%"}
> Left column text
:::

::: {.column with="50%"}
> Right column text
:::

::::::::::::::::

## Background image {data-baclground-image="photo.jpg"}


## Page that contains rules for revealjs

[revealjs](https://github.com/hakimel/reveal.js#configuration)


