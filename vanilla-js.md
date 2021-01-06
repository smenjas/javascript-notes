# Vanilla JavaScript

You can manipulate the DOM using vanilla JS.  You don't need jQuery or npm.

## Get & Set HTML
These methods work with a single element:
- `getElementById`: Accepts an `id`.
- `querySelector`: Accepts a CSS selector.
- The `style` property allows you to set CSS rules dynamically.

These methods work with multiple elements:
- `getElementsByClassName`: Accepts a `class`.
- `getElementsByTagName`: Accepts an HTML element's tag name.
- `querySelectorAll`: Accepts a CSS selector.

## Add & Remove HTML
- `appendChild`
- `removeChild`
- `innerHTML`

## Get & Set Text
- `nodeValue` sets or gets the text content of a *text node*.
- `textContent` sets or gets the text of the containing *element*.

## Traverse the DOM
- `firstChild`: Get the first child element of a node.
- `lastChild`: Get the last child element of a node.
- `parentNode`: Access a parent node of an element.
- `nextSibling`: Get the element after the selected element.
- `previousSibling`: Get the element before the selected element.

## Attributes
- `getAttribute`: Get an attribute, e.g. `class`, `id`, `href`, etc.
- `setAttribute`: Set a new attribute on an element, accepts the attribute and its name.
- `hasAttribute`: check if an attribute exists, accepts an attribute.
- `removeAttribute`: remove an attribute, accepts an attribute.
- `id`: Set or get the `id` of an element.
- `className`: Set or get the `class` of an element.

## Event Handling
```js
document.addEventListener('click', function (event) {
  if (event.target.id === 'clickity') {
    // Someone clicked something.
  }
}, false);
```

## When is the DOM ready?
```js
document.addEventListener('DOMContentLoaded', function(event) {
  // The DOM is ready!
})
```

## Resources
- [How to manipulate the DOM with Vanilla JavaScript](https://www.freecodecamp.org/news/dom-manipulation-in-vanilla-js-2036a568dcd9/)
- [Why event delegation is a better way to listen for events in vanilla JS](https://gomakethings.com/why-event-delegation-is-a-better-way-to-listen-for-events-in-vanilla-js/)
- [How to wait for the DOM ready event in plain JavaScript](https://flaviocopes.com/dom-ready/)
- [MDN: `DOMContentLoaded`](https://developer.mozilla.org/en-US/docs/Web/API/Window/DOMContentLoaded_event)

