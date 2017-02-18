

This site is published at
https://stitchfix.github.io/weave/

# Weave Style Guide and Documentation

## Instructions for Getting Your Local Set Up

1. Open terminal: `applications > terminal`
2. Make sure Jekyll is installed: `gem install jekyll`
  1. *Note*: You may have to run `sudo gem install jekyll`. Terminal will ask for your computer's user password. 
3. Clone the **weave** repository: `git clone git@github.com:stitchfix/weave.git`
  1. This will download a direct copy of the repository to a directory called `weave`.
  2. If you want to control where you download it, use the command `cd my/desired/directory` to change directory. The default is in the `home` directory.
4. Change directory to the newly downloaded one: `cd weave`
5. Change directory to the weave style guide directory: `cd docs`
6. Run the site locally if you want: `jekyll serve` (unsafe mode). You can also run in safe-mode (how gh-pages runs) this way `jekyll serve --safe`
7. Navigate your browser to: http://localhost:4000/weave/

## Creating a New Post

1. Easiest way is to copy an existing documentation file. Documentation files are in a format called *Markdown* and are located in the directory called `_posts`.
2. Find an existing markdown file in the appropriate subdirectory. E.g. `_posts/components/0000-01-01-buttons.md` and copy + paste it.
3. Name your file in the same format, but using the name of the component you're documenting. E.g. `0000-01-01-cards.md`
4. Pay attention to the formatting (referred to as *front matter*) at the beginning of the file:
```
---
layout: post
title: Buttons
permalink: /buttons/
categories: components
---
```
Modify yours to be in the same format:
```
---
layout: post
title: Cards
permalink: /cards/
categories: components
---
```
5. Use the editor of your choice (like Textedit) to write your new documentation. You can use an existing Markdown file as a template if it's helpful.
6. After you save your work, and if you have the site running locally, you can view it at http://localhost:4000/weave/ and see how it looks.

## Publishing a Post

1. After you've saved all of your work, go back to the terminal window (and navigate to the `weave` directory if you need to).
2. Make sure you pull the latest code, just in case: `git pull`
3. Stage your work: `git add .`
4. Commit your work with a message: `git commit -m "documentation for cards"`
5. Push your work: `git push origin master`
6. After about 15-30 seconds, the site will automatically generate the **live** site here: https://stitchfix.github.io/weave/
7. And that's all there is to it! Make sure it looks the way you want it to. Reach out to @yorthehunter (Brian) if you need any help.

## Adding Images to Your Documentation
In the future, we want to be able to automatically generate UI elements via the markup and CSS. In the meantime, we can use images as representations of our UI components.

1. Images can be added to the `assets/images` directory. Images can be any format, but SVG seems to be an appropriately scalable format.
2. After you've added your image, you can link to it using markdown: `![XL]({{ site.baseurl }}/assets/images/breakpoints--xl.svg)`
  1. The first part of that—`[XL]`—is the alt attribute of the image, which displays text if the image can't be shown for some reason.
  2. The next part looks confusing, but feel free to copy + paste this as an example, changing the part after `/images` to be the file name of your image.

### How I've Been Handling SVGs

1. Find a component in the sketch file that you want to reference.
2. Detach it from it's symbol: right-click and choose `detach from symbol`
3. Outline any text: select all text and `cmd-shift-O`
4. Select everything you want in the image and right click, then select `copy SVG code`
5. Copy an existing `.svg` or create a new blank file called `component-name--details.svg` <- whatever you need to call it
6. Paste your copied SVG code from Sketch into the file you just created
7. Save it and reference it like any other file. This will give you a completely accurate image from Sketch

## Documentation Checklist
##### High level docs
- [x] Principles
- [x] Overview (Why styleguide?)

##### Guidelines
- [x] Colors
- [x] Viewports
- [x] Grid
- [x] Typography
- [ ] Icons

##### Components
- [x] Z-Depth
- [ ] Forms
- [x] Buttons
- [ ] Page-level navigation (pagination, breadcrumb)
- [ ] Lists
- [ ] Tables
- [ ] Modal
- [ ] Calendar widget
- [ ] Tags
- [ ] Labels
- [ ] Tooltips
- [ ] Cards
- [x] Dialogs
- [ ] Filters
- [ ] Contextual Popover/Modal

##### Flows
- [ ] Sign In
- [ ] Data Visualizations
- [ ] Top Nav
