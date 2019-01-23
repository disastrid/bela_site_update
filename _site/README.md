# Bela site

- [Site structure](#site-structure)
- [Editing hero images at the top of pages](#editing-hero-images)
- About
- Products
- Education
- Resources

## Site structure
The site consists of a number of pages. These are:
- index.md(the home page)
- about.md
- education.md
- products.md
- resources.md

Each of these pages has content that is included from two places: The frontmatter, and data files. These are the only two things you need to edit.

## Editing page content

Each page's content (the `.md` files in the top level domain) can be written in markdown, like this:

```
# Section title

Section content goes here.
```

### Frontmatter

This is the stuff at the top of the file that specifies the page title and other basic data. It looks like this:

```
---
layout: default
title: Page Title
hero-image: image.png
---
```
If you want to change the *title* or *hero image* of a page, this is where you do it. For title, just change the text.

## Editing hero images

### About hero images
The big image at the top of each page is known as a hero image. These should be different for each page, to create visual interest.

Hero images *must* be:
- In focus (this is vitally important)
- Have good colour balance (not overly yellow for instance)
- At least 1200px in width

Store your hero images in `images/hero/yourImage.jpg`. This is the directory where Jekyll looks for and includes them.

### Including hero images
In your page's frontmatter, specify the file name of the image like this:

```
---
layout: default
title: Page Title
hero-image: yourImageName.jpg
---
```

You don't need the whole file path, just the file name - the file path is already set for you.

## Page layouts and updating content

### Why use layouts?
Each page on this site has slightly different needs - the About page, for instance, has lots of sections, and the Education page has lots of text. Usually a site will re-use layouts but each of these is pretty different, so they all have their own layouts.

The reason I have made layouts for each page instead of just putting a ton of HTML in the page files is because this approach makes it harder to break the site accidentally when updating it. When you need to edit the site, edit the [pageName].html in the **root of the site** which contains the frontmatter and room for a blurb. Don't change the files in `_layouts/` unless you really want to!

### Making new pages

If you need a single page (for example, for a product launch), you can use the `_layouts/default.html` page for a layout that will be plain but fit into this theme.

To initialise the page, do this:
1. Create a new text file and save it in the root of the site as [pageName].html (this will also create a link to `bela.io/pageName`)
2. In this file, add frontmatter like this:
```
---
layout: default
section_id: [usually the same name as your page]
title: Your Page Title
hero-image: nameOfFile.jpg (see the section above for more info about hero images!)
----
```
3. Save the file as an `.md` file, and add your content.

## Data files

The text content for repetative sections is typically brought in using data files. Find these in `_data/`. 

The reason for these files is that it all your text content is in one editable place, and you can mess with that without worrying that you'll accidentally break something. 

### Creating new data

If you want to create a new data file, create it in `_data/` with the file extension `.yml`. There's a few things to know, though:

1. `.yml` files can't use tabs, only spaces. If you create it and it doesn't compile, make sure that you don't have tabs.
2. You can make objects and sub objects and sub-sub objects, like this:
```
- thing: 
  - name: The Name
    description: Some text describing this.
    image: image.jpg
    specs:
      - spec: First
        spec: Second
        spec: Third
  - name: The other name
    description: Some text describing this.
    image: otherImage.jpg
```    

Much like JSON you can add and remove fields as you like, and you must have key/value pairs. If your objects don't all have the same key/value pairs, though, make sure you account for this in the file where you're bringing in this data. If Jekyll looks for a data field that doesn't exist, it won't compile.

## Includes

Includes are little snippets of content that you can include in your page, so you don't have to add a bunch of HTML and risk breaking something.

For example, on the home page the carousel of features is an include called `roundels.html`. This file takes in the data from the `_data/features.yml` file (data files are described in the previous section) and displays it in a nice-looking carousel. 

Instead of having to add in that knot of HTML, this include lets us use one line in the page: `{% include roundels.html %}` Again, this ensures that nothing breaks when updating. 
