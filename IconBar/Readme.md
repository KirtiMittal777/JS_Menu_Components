1. The append() method does not accept a string of HTML directly—it requires a DOM node (like an element or text node).

2. To fix this, you need to either use innerHTML to directly set the HTML inside the list item or create an actual i element programmatically.

3. The classList.add() method in JavaScript is used to add one or more classes to an HTML element's class list. 
   Syntax - element.classList.add(class1, class2);

4. Use :first-child when you want to target the very first element in its parent, regardless of its type.
Use :first-of-type when you want to target the first occurrence of a specific element type within a parent, regardless of other types of elements present.

p:first-child {
    color: red;
}

p:first-of-type {
    color: blue;
}

:first	- Does not exist in CSS.

<div>
    <span>Span 1</span>
    <p>Paragraph 1</p>
    <span>Span 2</span>
    <p>Paragraph 2</p>
</div>

The key differences between inline-flex and inline-block in CSS are related to how they handle layout and the types of items they contain:

1. Display Behavior:
inline-flex: This value makes the element behave like an inline element (i.e., it stays in line with surrounding text or other inline elements) but allows it to have the layout properties of a flex container. Inside the container, child elements are aligned and laid out according to flexbox rules.
inline-block: This value makes the element behave like an inline element in terms of its position, but allows the element itself to have block-level layout characteristics, like setting width, height, padding, etc. The children are not automatically flex items, so they behave as they would in a normal block context (e.g., flow one below the other by default).
2. Child Layout:
inline-flex: All child elements of the container are treated as flex items, meaning they are laid out in a row (or column, if configured), and flex properties like justify-content, align-items, and flex-grow can be used to control their alignment and distribution.
inline-block: Child elements do not have any special layout applied. They are laid out like in a typical block-level container, stacking vertically unless other styles like float or display are applied to the children.
3. Use Cases:
inline-flex: Use when you need the element to be inline but also need flexbox features to align or distribute its child elements.
inline-block: Use when you want the element to behave as an inline element but still be able to define its own dimensions and spacing like a block element.
Example:
inline-flex:
css
Copy code
.container {
  display: inline-flex;
  justify-content: center;
  align-items: center;
}
inline-block:
css
Copy code
.container {
  display: inline-block;
  width: 200px;
  height: 100px;
}
In summary:

inline-flex allows the element to act as a flex container while still staying inline.
inline-block lets the element behave like a block element but remain inline with text or other inline elements.

The vertical-align CSS property works only for inline or inline-block elements,