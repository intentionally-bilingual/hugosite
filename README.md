# CytoData Society Website

Welcome to the code of our website.
In here is the instruction to update things on the website.

The website is made using [hugo](https://gohugo.io).
This is a static site generator that uses markdowns.
If you need to update text you only need to though the markdown.

## Local testing

If you want to test the site locally [install hugo](https://gohugo.io/getting-started/installing/), open your terminal (powershell, cmd, bash, ect.), go to the root of this folder, and run `hugo server -D`.
You now have the site running at [localhost:1313](http://localhost:1313/).

## Updating text

To update text go the `/content` and locate the text you want to alter.
Every page has it own folder.

`_index.md`: Main text of this page.
The one `/content/_index.md` is for the main page, `/content/society/_index.md` is for the society page ect.

```
---
title: "Title of the page"
---

Here the text of page goes.
# You can use markdown to style your text

An image can be added like this.
These image are in static/main_files/
![CytoData banner](/./main_files/cytodata-banner.png)
```

## Updating/adding list element

A folder can have more markdowns.
This means a list is created.
`/content/symposiums/_index.md` will have the top text of the page.
Under need an element will be created for every other markdown file (`2016.md`, `2017.md`, `2018.md` ect.).
These are the list elements.

If you want a new element in the list just add a new markdown file.

The main page will have the text of `index.md` and underneath a list with every other markdown file.
Of these files the title and avatar is used.
If you click it you will be brought to a page with the full text.

- **Title** Name in the list and of the page
- **data** will be used in the list
- **publishdate** from what point it will be visable on the site (if in the future it will NOT be shown)
- **weight** where in the list it will be placed (lowest number first)
- **Image** needs to be name of an image in the folder `static/main_files`.

example:
```
---
title: "CytoData 2017 - by Institute of Cancer Research"
date: 2017-06-28
publishdate: 1970-01-01
weight: -2017
image: ICRAvatar.jpg
---

Here the text of page goes.
# You can use markdown to style your text

An image can be added like this.
These image are in static/main_files/
![CytoData banner](/./main_files/cytodata-banner.png)
```

## Create new page

To make new page you need to make the folder and markdown, but also need to add it to `config.toml`.
In there you find the menu.
Add you new page to here, use the weight to set its position and you are done.

```
# Menu
[menu]
  [[menu.main]]
    identifier = "symposiums"
    name = "Symposiums"
    url = "/symposiums"
    weight = 10

  [[menu.main]]
    identifier = "resources"
    name = "Resources"
    url = "/resources"
    weight = 20
```

## Change styling

We now go out of the pure markdown and into html.
In `\layouts` you can find the HTML used to make the page.

The styling is done with `/partials/style.html` and [bootstrap 5](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
A page will be rendered by the following logic:

- The folder ONLY has a `_index.md` we use `_default/single.html`
- The folder has an other markdown than `_index.md` we use `_default/list.html`. Even if `_index.md` is missing

The page has multiple hugo elements `{{ . }}`.
The `partial` are part of html in the folder `\partials` that are repeated.
`.Title` means it takes the title from the markdown and uses it here.
`.Content` is the content of the markdown.

``` html
{{ partial "header.html" . }}

<div class="container-fluid">
<h1>{{ .Title }}</h1>

{{ .Content }}
</div>

{{ partial "footer.html" . }}
```
