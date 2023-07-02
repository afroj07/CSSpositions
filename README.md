# CSSpositions

The position CSS property sets how an element is positioned in a document. The top, right, bottom, and left properties determine the final location of positioned elements.
There are five different types of position property available in CSS:

Fixed position: Any HTML element with position: fixed property will be positioned relative to the viewport. An element with fixed positioning allows it to remain in the same position even we scroll the page. We can set the position of the element using the top, right, bottom, and left.
<!DOCTYPE html>
<html>
<head>
<style>
div.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 300px;
  border: 3px solid #73AD21;
}
</style>
</head>
<body>

<h2>position: fixed;</h2>

<p>An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled:</p>

<div class="fixed">
This div element has position: fixed;
</div>

</body>
</html>

Static: This method of positioning is set by default. If we don’t mention the method of positioning for any element, the element has the position: static method by default. By defining Static, the top, right, bottom, and left will not have any control over the element. The element will be positioned with the normal flow of the page.
position: static;

Relative: An element with position: relative is positioned relatively with the other elements which are sitting on top of it. If we set its top, right, bottom, or left, other elements will not fill up the gap left by this element. An element with its position set to relative and when adjusted using top, bottom, left, and right will be positioned relative to its original position.
position: relative;
top: 40px; left: 40px;
HTML
<div class="box" id="one">One</div>
<div class="box" id="two">Two</div>
<div class="box" id="three">Three</div>
<div class="box" id="four">Four</div>

CSS
* {
  box-sizing: border-box;
}

.box {
  display: inline-block;
  width: 100px;
  height: 100px;
  background: red;
  color: white;
}

#two {
  position: relative;
  top: 20px;
  left: 20px;
  background: blue;
}

Absolute: An element with position: absolute will be positioned with respect to its nearest Non-static ancestor. The positioning of this element does not depend upon its siblings or the elements which are at the same level.

position: absolute;
top: 30px; left: 50px;
HTML
<div class="box" id="one">One</div>
<div class="box" id="two">Two</div>
<div class="box" id="three">Three</div>
<div class="box" id="four">Four</div>
CSS
* {
  box-sizing: border-box;
}

.box {
  display: inline-block;
  width: 100px;
  height: 100px;
  background: red;
  color: white;
}

#two {
  position: absolute;
  top: 20px;
  left: 30px;
  background: blue;
}


Sticky: Element with position: sticky and top:0 played a role between fixed & relative based on the position where it is placed. If the element is placed in the middle of the document then when the user scrolls the document, the sticky element start scrolling until it touched the top. When it touches the top, it will be fixed at the top place in spite of further scrolling. we can stick the element at the bottom, with the bottom property.

#one {
  position: sticky;
  top: 10px;
}
