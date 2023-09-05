---
# Front matter of "classic" page

# Theme to use. Resides in the "_layouts" folder.
layout: default

# Page title. If omitted, the page will not be included in the navbar.
title: MMM-MD

#################################################################

# Specifies the order of the current page from the point of view of the navbar. Can have repetition in the numbers, for parent-child hierarchies.
nav_order: 1

# Let exclude the page from the navbar
nav_exclude: false

# Let exclude the page from the built-in search engine
search_exclude: false

#################################################################

# Set "true" if this page has childrens, "false" otherwise.
has_children: false

# If this page is some page's child, specify the parent's name, otherwise comment out the option. If this page is some page's grandchild, specify grandparent's name, otherwise comment out the option.
# # parent: NOME_PAGINA_GENITORE
# # grand_parent: NOME_PAGINA_NONNO__GENITORE_DEL_GENITORE

# If this page is a parent page, a Table Of Contents will be automatically generated containing all related child pages. Use the option below to disable this functionality. Should always be set to "false".
has_toc: false

#################################################################

# Specify the current language of this page
lang: en

# Specify all other available languages in which this page is available. If there's no other language in addition to "lang", comment out this option.
# # availableLanguages:
# #   - 

# Notice: codeblocks highlighting supported languages listed here: https://www.fabriziomusacchio.com/blog/2021-08-11-Syntax_Highlighting_in_Jekyll/
---

# MMM-MD
{: .no_toc }
{: .d-inline-block }

<div id="legenda-labels-label-3"></div>
{: .d-inline-block }

<script type="module">
  selfsustainable_fill_labels_state("legenda-labels-label-3");
</script>

<div id="projects-label-2"></div>

<script type="module">
  selfsustainable_fill_labels_state("projects-label-2");
</script>

---

<!-- Table of contents -->
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

{: .motto-title }
> <p class="blockquote-title-fixer-purple">tl;dr</p>
>
> Write MD. Render it on the MagicMirror!
> This module enables you to write whatever you want directly rendering it on your MagicMirror screen!

---

## What you need

You just need:

- Basic knowledge of Markdown: [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)
- Creativity

Any MD syntax is supported. Multimedia is supported too!
Autoscroll if content is too much.

---

## Usage

1. Locate: `~/MagicMirror/modules`
2. Clone:

    ```shell
    git clone https://www.github.com/AndreaGrandieri/MMM-MD
    ```

3. Add fragment to `~/MagicMirror/config/config.js`

    ```js
    {
        module: "MMM-MD",
        position: "center",
        config: {
            // Alternative configuration properties are optional
        }
    }
    ```

4. Build:

    ```shell
    cd ~/MagicMirror/modules/MMM-MD
    npm install
    ```

    or

    ```shell
    cd ~/MagicMirror

    # "npm-recursive-install" needs to be installed separately 
    npm-recursive-install 
    ```

---

## Properties (Config Section)

| Property   | Type      | Values                                                                                       | Default Value          | Mandatory  | Description                                                                     |
| ---------- | --------- | -------------------------------------------------------------------------------------------- | ---------------------- | ---------- | ------------------------------------------------------------------------------- |
| `interval` | `Integer` | Any value `>= 45` (ms)                                                                       | `50` (ms)              | `OPTIONAL` | Autoscroll velocity.                                                            |
| `staller`  | `Integer` | Any value `>= 0` (ms)                                                                        | `100` (ms)             | `OPTIONAL` | Time before restarting from __TOP__ after reaching autoscroll __BOTTOM__ limit. |
| `width`    | `String`  | Any CSS valid string value                                                                   | `"calc(100 % - 25 %)"` | `OPTIONAL` | Module width.                                                                   |
| `height`   | `String`  | Any CSS valid string value                                                                   | `"500px"`              | `OPTIONAL` | Module height.                                                                  |
| `docname`  | `String`  | Path to a valid document. __The document has to be placed into: `./modules/MMM-MD/public/`__ | `"content.md"`         | `OPTIONAL` | MD document to parse markdown from.                                             |

---

## Notifications

Notifications are a piece of software used by modules to communicate with:

- MagicMirror OS
- Other modules
- Human actors

_None._

---

## Screenshots

Module interface (1):

[![module_focus](/MMM-MD/assets/module_focus.PNG)](/MMM-MD/assets/module_focus.PNG)

Module interface (2):

[![module_overview](/MMM-MD/assets/module_overview.PNG)](/MMM-MD/assets/module_overview.PNG)

---

## Documents path

All MD documents and assets (multimedia) has to be placed into __`./modules/MMM-MD/public/`__ to be used
by the module. Only one document at time can be active and rendered.

To point an asset from the MD document, you will need to follow this _path pattern_:

```md
![{assetName}](modules/MMM-MD/public/{assetName.extension})
```
