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
{
  "x": 28,
  "y": 100,
  "width": 220,
  "height": 170,
  "top": 100,
  "right": 248,
  "bottom": 270,
  "left": 28
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMDEzMDIxODcsLTQ3NDI5ODkwMywyMD
Y2ODMzNDcwXX0=
-->