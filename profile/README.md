# substrate system

Building blocks for the frontend.

## Web components

__*featuring*__

* [no shadow DOM](https://gomakethings.com/the-shadow-dom-is-an-antipattern/)
* no external runtime dependencies

### see also

* [@substrate-system/tonic](https://github.com/substrate-system/tonic) &mdash;
A Low Profile Component Framework
* [@substrate-system/template-web-component](https://github.com/substrate-system/template-web-component)
&mdash;  A template for vanilla web componenets
* [@substrate-system/web-component](https://github.com/substrate-system/web-component)
&mdash; A minimal parent component to inherit from
* [Where web components shine](https://daverupert.com/2024/10/super-web-components-sunshine/)
* [HTML Web Components](https://gomakethings.com/html-web-components/)
* [Let's create a Web Component from scratch!](https://gomakethings.com/lets-create-a-web-component-from-scratch/)

## Conventions

There is a strict convention with how these components are factored. To keep
server-side rendering easy, an isomorphic file is exposed at `/ssr`. This file
exposes a single function , `html`, that takes attributes as an object and
returns a string of HTML.

The frontend component uses this to render itself in the [`connectedCallback`](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_custom_elements#custom_element_lifecycle_callbacks)
function.

This makes it easy to render a component serverside. Just import the
`/ssr` path:

```js
import { html } from '@substrate-system/example-component/ssr'

// return an HTML string
html({
    disabled: true,
    placeholder: 'hello'
})
```


## Misc

Some other frontend libraries:

* [@substrate-system/tapzero](https://github.com/substrate-system/tapzero) &mdash;
Zero dependency test framework
* [@substrate-system/dom](https://github.com/substrate-system/dom) &mdash; Helpers
for working with the DOM in tests
* [route-event](https://github.com/substrate-system/route-event) &mdash; Simple
client side route event
* [@substrate-system/routes](https://github.com/substrate-system/routes) &mdash;
Route matcher
* [@substrate-system/debug](https://github.com/substrate-system/debug) &mdash;
Debug utility
