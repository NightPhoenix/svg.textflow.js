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

## Dependencies
This plugin requires svg.js v0.11.