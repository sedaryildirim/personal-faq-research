# Personal Frequently Asked Questions

- [How does position: Work? (css)](#how-does-position:-work?-(css))
- [How does :not work (css)](#how-does-:not-work-(css))
- [How does z-index: work? (css)](#How-does-z-index:-work?-(css))
- [How do ::before and ::after work? (css)](#How-do-::before-and-::after-work?-(css))
- [Difference between display: flex and display: inline-flex (css)](#Difference-between-display:-flex-and-display:-inline-flex-(css))
- [## Difference between display: block and display: inline-block (css)](#Difference-between-display:-block-and-display:-inline-block-(css))
- [## Difference between display: block and display: inline-block (css)](#Difference-between-display:-block-and-display:-inline-block-(css))

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

## How does :not work? (css)

## How does z-index: work? (css)

## How do ::before and ::after work? (css)

## Difference between display: flex and display: inline-flex (css)

## Difference between display: block and display: inline-block (css)