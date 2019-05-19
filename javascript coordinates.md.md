# Coordinates in Javascript

Types of Coordinate Systems you may deal in js- 

 1. Relative to browser window (viewport) (clientX, clientY)
 2. Relative to document (pageX, pageY)

## Relative to Browser Window
Method `elem.getBoundingClientRect()` returns the position of element edges from the parent window/iframe. The position is calculated from upper left corner of window. So when not on screen/ scrolled out the values may be negative.

![http://javascript.info/article/coordinates/coords.png](http://javascript.info/article/coordinates/coords.png)
```javascript
const coords = field.getBoundingClientRect();
console.log(coords)
// coords out put
{
  "x": 28,
  "y": 100,
  "width": 220, // including border/offset. Same as field.offsetWidth
  "height": 170, // including offset/border. Same as field.offsetHeight
  "top": 100, // position from top without offset
  "right": 248,
  "bottom": 270,
  "left": 28
}
```
## Relative to document (pageX, pageY)

```javascript
const field = document.getElementById("field");
// element width with border etc
field.offsetWidth
// element height with border etc
field.offsetHeight
// left border/offset width
field.clientLeft
// top border/offset width
field.clientTop
// width without border/offset
field.clientWidth
// height without border
field.client

```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NzQ5MjcxMjcsLTQ3NDI5ODkwMywyMD
Y2ODMzNDcwXX0=
-->