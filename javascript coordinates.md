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

In this the position is relative to Page/Document do on scroll it remains same. We can use these to drawUnderElement etc.

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
field.clientHeight
```
![https://pbs.twimg.com/media/D67HxxkUYAARPNI.png](https://pbs.twimg.com/media/D67HxxkUYAARPNI.png)

### How to draw mouse under? 
To draw under mouse or any element we need to set a trigger when mouse is hovered on that element then we grab `{clientX, clientY}` from event and set draw under element position to `clientX, clientY`
```javascript
let div = document.createElement("div");
div.classList.add("draw-under", "gone"); // position: absolute etc
document.body.append(div)
document.addEventListener("mousemove", e=>{
  div.classList.remove("gone")
  const {clientX, clientY} = e;
  console.log(clientX, clientY)
  div.style.setProperty("top", `${clientY}px`);
  div.style.setProperty("left", `${clientX}px`)
});
document.addEventListener("mouseleave", e=>{
  div.classList.add("gone");
});
```


<!--stackedit_data:
eyJoaXN0b3J5IjpbNTQ0MDQ5ODI3LC0xNjI2NDM4Mzg3LDE0MD
MyNTgxOF19
-->