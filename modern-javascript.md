# Modern JavaScript

Modern JavaScript is often defined as ES6 (from 2015) or newer.

Legacy JavaScript is considered ES5 (from 2009).  Older versions are obsolete.

## Adoption
95% of browser traffic supports:
- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes): [`class`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/class)
- [Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions): `=>`
- [Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator): [`function*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*)/[`yield*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield*)
- [Block](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block) [scoping](https://developer.mozilla.org/en-US/docs/Glossary/Scope): [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)/[`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
- [object shorthand](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer): `{a, b, c}`
- [`async`/`await`](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)

94% of browser traffic supports:
- [destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
- [rest](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)/[spread](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

For the remaining 6% of traffic that doesn't support modern JS, we can
[transpile](https://en.wikipedia.org/wiki/Source-to-source_compiler) modern JS
into older JS, at a cost to both bandwidth and execution speed of 6x or more.

- 95% of web traffic comes from browsers that support ES2017.
- 70% of web traffic comes from browsers that support ES2021.

## Package Exports
The `exports` field in a `package.json` file was first supported in Node v12.8,
which support ES2019 syntax.

### Modern-only `package.json`
```js
{
  "name": "foo",
  "exports": "./foo.js",
}
```

### Modern with fallback `package.json`
```js
{
  "name": "foo",
  "exports": "./foo.js",
  "main": "./foo-es5.js",
}
```

## Client Fallback
For the 95% of browser traffic that supports ES8 from 2017, use:
```html
<script type="module" src="app.modern.js"></script>
```
For the 5% of browser traffic that supports ES5 from 2009, use:
```html
<script nomodule src="app.legacy.js"></script>
```

## ECMAScript Versions
- ES1: June 1997
- ES2: June 1998
- ES3: December 1999
- ES4: June 2003 (abandoned)
- ES5: December 2009
- ES5.1: June 2011
- ES6: June 2015
- ES7: June 2016
- ES8: June 2017
- ES9: June 2018
- ES10: June 2019

## Resources
- [Google Chrome Developers: Transitioning to modern JavaScript](https://youtu.be/cLxNdLK--yI)
- [Wikipedia: ECMAScript](https://en.wikipedia.org/wiki/ECMAScript)
- [EStimator](https://estimator.dev/) analyzes how modernizing a site's JS can save bandwidth

