# IPFS Design Style Guide

A shared style guide for UI design in the IPFS universe.

Reuse these [colors](#colors), [typography](#typography), and spacing values (TBD) to create a coherent feel across all ipfs applications.

## Colors

| teal       | turquoise | blue      | grey
|------------|-----------|-----------|---------------  
| `#3469ea2` | `#6acad1` | `#00b0e9` | `#666666`
| <img title='teal' src='http://swatches.now.sh/?color=%23469ea2'/> | <img title='turquoise' src='http://swatches.now.sh/?color=%236acad1'/> | <img title='blue' src='http://swatches.now.sh/?color=%2300b0e9'/> | <img title='blue' src='http://swatches.now.sh/?color=%23666666'/>

## Typography

### Font family

Use the system font for general instructional text.

```css
.system-ui-font {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
```
https://css-tricks.com/snippets/css/system-font-stack/

Provide the main content in a font that blends in with the users system, and is already installed.

### Font size

Use a type scale to pick a small set of font sizes that work together. The [tachyons type scale] is good.

| class name | px   | rem    | Example
| ----------:|:-----|:-------|----------
|      `.f1` | 48px | 3      | Main header `<h1 class="f1">`
|      `.f2` | 36px | 2.25   | Sub head `<h2 class="f2">`
|      `.f3` | 24px | 1.5    | `<h3 class="f3">`
|      `.f4` | 20px | 1.25   | `<h3 class="f4">`
|      `.f5` | 16px | 1      | General copy `<p class='f5'>`
|      `.f6` | 14px | 0.875  | Small header `<h4 class="f6 b uppercase">`
|      `.f7` | 12px | 0.75   | Small print `<small class='f7'>`

Capturing the font sizes for your app as isolated, single purpose css classes, adds flexibility by decoupling your design from your markup semantics. An `<h1>` doesn't have to be the largest text on the page.

Agreeing to a finite set of font sizes prevents the font-size sprawl that often occurs when trying to maintain a ui and associated css over time. (GitHub, at time of writing has **56 unique font sizes** defined: [github cssstats](http://cssstats.com/stats?url=http%3A%2F%2Fgithub.com&ua=Browser%20Default))

### Headers and Heros

Sometimes you need really big text, for fancy splash pages and hero sections.

| class name       | px   | rem  | Example
| ----------------:|:-----|:-----|----------
| `.f-headline`    | 48px | 6    | Hero headline `<h1 class="f-headline">`
| `.f-subheadline` | 36px | 5    | `<h2 class="f-subheadline">`

These are just there to help get things done quickly. Use whatever font-size the design calls for. If the it's a one time use for a big impact intro, then just use an inline style.

## Credits

This style guide uses ideas from http://tachyons.io/docs/ and http://basscss.com/ and was inspired by https://airbnb.design/building-a-visual-language/

## License

This repository is mainly for documents. All of these are licensed under the [CC-BY-SA 3.0](https://ipfs.io/ipfs/QmVreNvKsQmQZ83T86cWSjPu2vR3yZHGPm5jnxFuunEB9u) license © 2016 Protocol Labs Inc. Any code is under an [MIT license](LICENSE) © 2016 Protocol Labs Inc.

[tachyons]: http://tachyons.io
[tachyons type scale]: http://tachyons.io/docs/typography/scale/