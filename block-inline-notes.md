# Block vs Inline:
- most elements are default block elements, blocks appear stacked on each other, each new element is on a new line
- inline elements begin on the same line, <a> is an inline element
    - **you generally dont want to add padding and margin on inline elements**
- inline-block behave like inline elements but with block-style padding and margin, **You will probably use flexbox to line up a bunch of boxes**

## Divs and spans:
- these dont have meaning to their context, unlike paragraph elements
- div elements are block-level elements by default
- span elements are inline-level elements by default


## Normal layout flow:
- elements lay out in **normal flow** if theres no css applied. you can adjust positions by adjusting in normal flow or removing them from it alltogether
- ways to override normal flow:
1) display property (block, inline or inline-block): change how elements behave by making them act inline or block. 
    - e.g. display: inline
2) float: causes block-level ements to wrap along one side of an element
    - e.g. float:left
3) position: precisely control placement of boxes inside other boxes
    - e.g. position: fixed
4) grid: alter how child elements are laid out inside their parent
    - e.g. display: grid
5) flexbox: alter how child elements are laid out inside their parent
    - e.g. display: flexbox
6) responsive designs: adapts layout depending on what device web page is rendered on
