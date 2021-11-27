# Personal Frequently Asked Questions

- [How does position: Work? (css)](#how-does-position:-work?-(css))
- [How do ::before and ::after work? (css)](#how-do-::before-and-::after-work?-(css))
- [Difference between display: flex and display: inline-flex (css)](#difference-between-display:-flex-and-display:-inline-flex-(css))
- [Difference between display: block and display: inline-block (css)](#difference-between-display:-block-and-display:-inline-block-(css))

## How does position: work? (css)

*position:absolute works by positioning item relative to the last parent with a position: relative tag*

```html
<div class="parent">
  <div class="child">
    </div>
</div>
```

```css
.parent {
  position: relative;
}

.child {
  position: absolute;
  top: 0;
  left: 0;
}
```
*above would position the child in the parent, if parent had no position: relative, it would default to the next element with position:relative, and if no elements had position:relative, it would default to the body*

*it is removed from the document flow, where it will float above the current element/div, unless given a z-index:*

*z-index does not work unless item has a position: setting*

*relative position and static position are the same, but relative lets you use top: right: left: bottom*
- Source: https://www.youtube.com/watch?v=jx5jmI0UlXU
- Source: https://www.youtube.com/watch?v=P6UgYq3J3Qs

*position fixed ignores the parent elements even with position:relative, they always default to body flow and they also stay in same place when page is scrolled*

*sticky positioning works as position:relative and position:fixed together, eg if you give a element position: sticky, it defaults as relative, but once you start scrolling the page it becomes fixed:position*

## How do ::before and ::after work? (css)
*:: are pseudo-elements*
- Source: https://www.youtube.com/watch?v=zGiirUiWslI
- Source: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements
- Source: https://www.youtube.com/watch?v=e1KpKBHJOrA

*A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). For example, ::first-line can be used to change the font of the first line of a paragraph.*
```html
/* The first line of every <p> element. */
p::first-line {
  color: blue;
  text-transform: uppercase;
}
```

**content can be blank and does not work on images**
```html
content: '';
```

**adds hello before every p element**
```html
p::before {
    content: 'hello';
    background: red;
}
```

**adds goodbye after every p element**
```html
p::after { 
    content: 'goodbye';
    background: red;
}
```

*In CSS, ::after creates a pseudo-element that is the last child of the selected element. It is often used to add cosmetic content to an element with the content property. It is inline by default.*
```html
/* Add an arrow after all links */
a::after {
  content: "→";
}
```

*In CSS, ::before creates a pseudo-element that is the first child of the selected element. It is often used to add cosmetic content to an element with the content property. It is inline by default.*
```html
/* Add a heart before all links */
a::before {
  content: "♥";
}
```

## Difference between display: flex and display: inline-flex (css)

- Source: https://www.youtube.com/watch?v=9e-lWQdO-DA

*Flex: Flex displays an element as a flexible structure. To use flex display, a flex level container has to be created. Flex level container is nothing, but an element with the display property set to flex. The flex container itself is displayed in a new line, just like the block element. The flex container can contain other elements in it and thus, the flex container is the parent element and the elements that are part of it are the child elements. Display flex property helps us to align and distribute space among items in a container, even when their size is unknown and/or dynamic.*

*Inline: Just as the name suggests, inline displays an element in the same line as the rest. Specifying any height and width properties will be of no use, as it follows the height and width of the line, of which it is a part.*

## Difference between display: block and display: inline-block (css)

**display: block elements always stack on top of each other, on a new line and take up 100% of the space available from their parent**
**display: inline-block live in other elements and do not force new lines**

- Source: https://www.youtube.com/watch?v=x_i2gga-sYg&list=RDCMUCJZv4d5rbIKd4QHMPkcABCw&start_radio=1

*Block: Displays an element as a block element. It starts on a new line and takes up take up as much horizontal space as they can. Block-level elements do not appear in the same line, but breaks the existing line and appear in the next line.*

*Inline: Just as the name suggests, inline displays an element in the same line as the rest. Specifying any height and width properties will be of no use, as it follows the height and width of the line, of which it is a part.*