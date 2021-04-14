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
        // Alternative configuration parameters are optional
    }
}
```

