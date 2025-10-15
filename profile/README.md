# substrate system

Building blocks for the frontend.

<details><summary><h2>Contents</h2></summary>

<!-- toc -->

- [Web components](#web-components)
  * [Conventions](#conventions)
    + [SSR](#ssr)
  * [Components](#components)
  * [See Also](#see-also)
- [Cryptography](#cryptography)
- [Misc](#misc)

<!-- tocstop -->

</details>

## Web components

__*featuring*__

* [no shadow DOM](https://gomakethings.com/the-shadow-dom-is-an-antipattern/)
* no external runtime dependencies

### Conventions

#### SSR

To keep server-side rendering easy, an isomorphic file is exposed at `/html`.
This file exposes a single function that takes attributes as an object
and returns a string of HTML.

The frontend component uses this to render itself in the
[`connectedCallback`](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_custom_elements#custom_element_lifecycle_callbacks)
function.

This makes it easy to render a component serverside. Just import the
`/html` path:

```js
import { render } from '@substrate-system/example-component/html'

// return an HTML string
html({
    disabled: true,
    placeholder: 'hello'
})
```

### Components

Web components and related libraries.

* [@substrate-system/tonic](https://github.com/substrate-system/tonic) &mdash;
  Low Profile Component Framework
* [@substrate-system/template-web-component](https://github.com/substrate-system/template-web-component)
  &mdash; A template for vanilla web componenets
* [@substrate-system/web-component](https://github.com/substrate-system/web-component)
  &mdash; A minimal parent component to inherit from
* [@substrate-system/wavy-hr](https://github.com/substrate-system/wavy-hr) &mdash;
  `hr`, but wavy.
* [@substrate-system/icons](https://github.com/substrate-system/icons) &mdash;
  convenient icons
* [@substrate-system/copy-button](https://github.com/substrate-system/copy-button)
  &mdash; icon/button to copy some text
* [@substrate-system/input](https://github.com/substrate-system/input) &mdash;
  a parent input element to inherit from
* [@substrate-system/blur-hash](https://github.com/substrate-system/blur-hash) &mdash;
  blurry placeholder images
* [@substrate-system/progress-indicator](https://github.com/substrate-system/progress-indicator)
  &mdash; progress indicator, for downloads and things
* [@substrate-system/button](https://github.com/substrate-system/button) &mdash;
  button element with a visual loading state
* [@substrate-system/radio-input](https://github.com/substrate-system/radio-input)
  &mdash; radio inputs with style
* [@substrate-system/password-field](https://github.com/substrate-system/password-field)
  &mdash; password input with a visible/hidden button
* [@substrate-system/text-input](https://github.com/substrate-system/text-input)
  &mdash; Text input with style
* [@substrate-system/hamburger-two](https://github.com/substrate-system/hamburger-two)
  &mdash; Hamburger menu as a web component


### See Also

* [Where web components shine](https://daverupert.com/2024/10/super-web-components-sunshine/)
* [HTML Web Components](https://gomakethings.com/html-web-components/)
* [Let's create a Web Component from scratch!](https://gomakethings.com/lets-create-a-web-component-from-scratch/)


-------


## Cryptography

Modules that use the [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API),
for cryptography in the browser.

* [@substrate-system/keys](https://github.com/substrate-system/keys) &mdash;
  Create and securely store asymmetric keys in the browser.
* [@substrate-system/simple-aes](https://github.com/substrate-system/simple-aes)
  &mdash; The simplest way to use AES keys in the browser.
* [@substrate-system/request](https://github.com/substrate-system/request)
  &mdash; Use Bearer tokens with web crypto to authenticate http requests.
* [@substrate-system/message](https://github.com/substrate-system/message) &mdash;
  Create and verify signed messages.
* [@substrate-system/webauthn-keys](https://github.com/substrate-system/webauthn-keys)
  &mdash; Use biometrics to secure keys.
* [@substrate-system/frost](https://github.com/substrate-system/frost) &mdash;
  [Flexible Round-Optimized Schnorr Threshold Protocol](https://www.rfc-editor.org/rfc/rfc9591.html)
  for the browser.
* [@substrate-system/frost-dkg](https://github.com/substrate-system/frost-dkg)
  &mdash; Distributed key generation + FROST signatures
* [@substrate-system/webcrypto-x3dh](https://github.com/substrate-system/webcrypto-x3dh)
  &mdash; X3DH for the browser
* [@substrate-system/shamirs-secret-sharing](https://github.com/substrate-system/shamirs-secret-sharing)
  &mdash; Shamir's Secret Sharing for the browser


-------


## Misc

Some other frontend libraries:

* [@substrate-system/signs](https://github.com/substrate-system/signs) &mdash;
  Smaller, simpler signals
* [@substrate-system/mergeparty](https://github.com/substrate-system/mergeparty) &mdash;
  [Automerge](https://automerge.org/) + [Partykit](https://www.partykit.io/)
* [@substrate-system/tapout](https://github.com/substrate-system/tapout) &mdash;
  The easiest way to run tests in a browser from the command line.
* [@substrate-system/tapzero](https://github.com/substrate-system/tapzero) &mdash;
  Zero dependency test framework
* [@substrate-system/dom](https://github.com/substrate-system/dom) &mdash; Helpers
  for working with the DOM in tests
* [route-event](https://github.com/substrate-system/route-event) &mdash; Simple
  client side route event
* [@substrate-system/routes](https://github.com/substrate-system/routes) &mdash;
  route matcher
* [@substrate-system/debug](https://github.com/substrate-system/debug) &mdash;
  Debug utility
* [@substrate-system/a11y](https://github.com/substrate-system/a11y) &mdash;
  helpers for accessibility
* [@substrate-system/webrtc](https://github.com/substrate-system/webrtc) &mdash;
  simpler webrtc
* [@substrate-system/report](https://github.com/substrate-system/report) &mdash;
  What browser and OS?
* [@substrate-system/drag-drop](https://github.com/substrate-system/drag-drop)
  &mdash; simpler HTML5 drag and drop
