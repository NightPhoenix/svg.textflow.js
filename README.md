# svg.textflow.js

A plugin for the [svgjs.com](http://svgjs.com) library to create auto-wrapping text flow elements in svg.

Svg.textflow.js is licensed under the terms of the MIT License.

## Usage
Include this plugin after including the svg.js library in your html document.

To make an element draggable

```javascript
var draw = SVG('canvas').size(400, 400)
var flow = draw.textflow('Some long text, including \nline breaks. Although line breaks are not required unless absolutely necessary for the context.').size(300,200)

flow.font({ family: 'Georgia, serif', size: 36 })
```

Important note: if you are using custom web fonts, make sure they are fully loaded before using them.

## Overflow
By default the size of the textflow area is set to 100 px x 100 px. The text flow element will only show the text inside the box, nothing more. If the defined box is too small to show all text content, the overflowing text will be stored in a data attribute:

```javascript
var overflow = flow.data('overflow')
```

This makes it possible to create an new textflow element with the remaining content for example.

## Example
Test the [textflow plugin](http://svgjs.com/textflow/) on a resizable and framed flow area.


## Dependencies
This plugin requires svg.js v0.11.