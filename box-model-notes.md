- Everything on a webpage is a rectangular box
- can use "padding", "border", "margin" to manupulate size of these boxes, and space between them
    - padding increases space between border of a box and content of box
    - border adds space between margin and padding
    - margin increases space between borders of a box and borders of adjacent boxes

![img](./box%20model.png)

- You can add the following to change the element size to take into account the padding and border as well
```
box-sizing: border-box
```
- usually the box sizing is added to the head for easier use
- use chrome dev tools to inspect boxes and see what the dimensions are
- can also do stuff like:
```
box-sizing: content-box
```

- best practice for resetting box-sizing
- Old style:
```
*
    {
        box-sizing: border-box;
    }
```
- New style: (best practice!)
``` 
html {
    box-sizing: border-box;
}
*, *:before, *:after {
    box-sizing: inherit;
}
```

- You can use longhand properties to define exactly what side of the box (for margin, border, padding - this example uses margin):
```
margin-top:350px;
margin-bottom:100px;
margin-left:100px;
margin-right:100px;
```
- You can also specify properties of specific sides, e.g.:
```
border-top-color;
border-right-width;
border-bottom-style
```
- see online about margin collapsing - basically:
 1) if both margins are positive - the size will be the larget margin value
 2) two negative margins will collapse and smallest (furthest from zero) will be used
 3) if one margin is negative, the value will be subtracted from the positive margin

## Using Display:
- use "display: inline-block" to make item stay inline but respect width and height. Because with "display: inline", width and height are ignored

## Shorthand for margin:
```
margin: 0 3em 0 50px
```
- default values are margin top, margin right, bottom, then left
- if first 2 values are set, then following pair will be assumed:
```
margin: 0 1.5em;
margin: 0 1.5em 0 1.5em;
```

## Auto and centering:
- setting auto as the value will in most cases make it 0 or else whatever space is available on that side of the element, useful for horizontal centering, **not vertical**