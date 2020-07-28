# Vue Product Carousel
[![Build Status](https://badgen.net/circleci/github/probil/vue-product-carousel/master)](https://circleci.com/gh/probil/vue-product-carousel/tree/master)
[![npm](https://img.shields.io/npm/v/vue-product-carousel.svg)](https://www.npmjs.com/package/vue-product-carousel)
[![Github file size](https://img.shields.io/github/size/probil/vue-product-carousel/dist/lib/VueProductCarousel.umd.min.js.svg)](https://raw.githubusercontent.com/probil/vue-product-carousel/master/dist/lib/VueProductCarousel.umd.min.js)
[![npm](https://img.shields.io/npm/dm/vue-product-carousel.svg)](https://www.npmjs.com/package/vue-product-carousel)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/probil/vue-product-carousel/master/LICENSE)
[![Vue2](https://img.shields.io/badge/Vue-2.x-brightgreen.svg)](https://vuejs.org/)

> Simple product carousel with hot image replacement, Zoom and Swipe mode

## Usage

To be able to use this component you should install it first
```bash
npm i --save vue-product-carousel
```
Then import it:
```js
import ProductCarousel from 'vue-product-carousel'
```

Use `ProductCarousel` component and pass your images as `images` prop:

```vue
<template>
  <ProductCarousel :images="images">
    Sidebar content here
  </ProductCarousel>
</template>
<script>
export default {
  components: {
    ProductCarousel,
  },
  data() {
    return {
      images: [
        'http://lorempixel.com/1000/1000/business/1/',
        'http://lorempixel.com/1000/1000/business/2/',
        'http://lorempixel.com/1000/1000/business/3/',
      ]
    }
  },
}
</script>
```

## Polyfills

Library use few browser built-ins and *doesn't* include polyfills for them. This ensures you don't include unnecessary polyfills in your code, as it should be the responsibility of the consuming app to include them.

[Vue CLI includes them in babel config by default](https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/babel-preset-app#polyfills) but here is a list (in case you what to add them manually):
```
# for core-js@2
es6.object.assign
es6.symbol # optional

# for core-js@3
es.object.assign
es.symbol  # optional
```

For direct usage in browser consider using https://polyfill.io/v3/


## Scripts

``` bash
# installs dependencies
npm install

# serves demo with hot reloading
npm run serve

# builds demo
npm run build:demo

# builds lib
npm run build:lib

# lints and fixes files
npm run lint
```

## Params

|  Name                | Type   | Default  | Required | Description  |
|  ---               | ---   | ---     | ---      | ---         |
|  `images`            | Array  | []       | `true`    | Array of image urls that will be used in slider |
| `body-class-on-zoom` | String | `zoom`   | `false`   | Class that will be added to the `body` while Zoom mode is active. Very useful to hide header/footer in Zoom mode. |

## Credits

- [kalicki](https://github.com/kalicki) for idea.
- [thebird](https://github.com/thebird/Swipe) for [Swipe](https://github.com/thebird/Swipe) lib
