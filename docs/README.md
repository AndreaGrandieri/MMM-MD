# MMM-MD

Write MD. Render it on the MagicMirror!

This module enables you to write whatever you want directly rendering it on your MagicMirror screen! 

You just need:

- Basic knowledge of Markdown [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)
- Creativity

Any MD syntax is supported. Multimedia is supported too!
Autoscroll if content is too much.

Usage:

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
cd `~/MagicMirror/modules/MMM-MD`
npm install
```

or

```shell
cd `~/MagicMirror`

# "npm-recursive-install" needs to be installed separately 
npm-recursive-install 
```

---

## Properties (Config Section)

| Property   | Type      | Values                                                                                       | Default Value          | Mandatory  | Description                         |
| ---------- | --------- | -------------------------------------------------------------------------------------------- | ---------------------- | ---------- | ----------------------------------- |
| `interval` | `Integer` | Any value `>= 45` (ms)                                                                       | `50` (ms)              | `OPTIONAL` | Autoscroll velocity.                |
| `width`    | `String`  | Any CSS valid string value                                                                   | `"calc(100 % - 25 %)"` | `OPTIONAL` | Module width.                       |
| `height`   | `String`  | Any CSS valid string value                                                                   | `"500px"`              | `OPTIONAL` | Module height.                      |
| `docname`  | `String`  | Path to a valid document. __The document has to be placed into: `./modules/MMM-MD/public/`__ | `"content.md"`         | `OPTIONAL` | MD document to parse markdown from. |

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

![module_focus](assets/module_focus.PNG)

Module interface (2):

![module_overview](assets/module_overview.PNG)

---

## Documents path

All MD documents and assets (multimedia) has to be placed into __`./modules/MMM-MD/public/`__ to be used
by the module. Only one document at time can be active and rendered.

To point an asset from the MD document, you will need to follow this _path pattern_:

```md
![{assetName}](modules/MMM-MD/public/{assetName.extension})
```
