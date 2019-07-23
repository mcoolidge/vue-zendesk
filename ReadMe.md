# vue-zendesk

[![npm version][npm-version-src]][npm-version-href]
[![npm downloads][npm-downloads-src]][npm-downloads-href]
[![Dependencies][david-dm-src]][david-dm-href]
[![Standard JS][standard-js-src]][standard-js-href]

> Vue.js plugin for Zendesk Web Widget

This plugin allows you to configure and add Zendesk Web Widget

[Zendesk Web Widget Documentation](https://developer.zendesk.com/embeddables/docs/widget/introduction)

## Setup

1. Add the `@dansmaculotte/vue-zendesk` dependency with `yarn` or `npm` to your project
2. Configure it:

```js
import Vue from 'vue'
import Zendesk from '@dansmaculotte/vue-zendesk'

Vue.use(Zendesk, {
  key: 'YOUR_ZENDESK_KEY',
  disabled: true,
  settings: {
    webWidget: {
      color: {
        theme: '#78a300'
      }
    }
  }
})
```

`disabled` option allows you to prevent automatic script loading, to comply with GDPR.

You can manually load it by calling `this.$zendesk.load(YOUR_ZENDESK_KEY)`.

You can view available settings [here](https://developer.zendesk.com/embeddables/docs/widget/settings).

## Usage

You can use any method coming from the official documentation.

For example:
```js
Vue.$zendesk('webWidget', 'hide')
// In a vue component
this.$zendesk('webWidget', 'show')
```

## Development

1. Clone this repository
2. Install dependencies using `yarn install` or `npm install`
3. Start development server using `npm run dev`

## License

[MIT License](./LICENSE.md)

<!-- Badges -->
[npm-version-src]: https://img.shields.io/npm/dt/@dansmaculotte/vue-zendesk.svg?style=flat-square
[npm-version-href]: https://npmjs.com/package/@dansmaculotte/vue-zendesk

[npm-downloads-src]: https://img.shields.io/npm/v/@dansmaculotte/vue-zendesk/latest.svg?style=flat-square
[npm-downloads-href]: https://npmjs.com/package/@dansmaculotte/vue-zendesk

[david-dm-src]: https://david-dm.org/dansmaculotte/vue-zendesk/status.svg?style=flat-square
[david-dm-href]: https://david-dm.org/dansmaculotte/vue-zendesk

[standard-js-src]: https://img.shields.io/badge/code_style-standard-brightgreen.svg?style=flat-square
[standard-js-href]: https://standardjs.com
