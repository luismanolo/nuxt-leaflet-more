# Nuxt Leaflet

[![npm version][npm-version-src]][npm-version-href]
[![npm downloads][npm-downloads-src]][npm-downloads-href]
[![License][license-src]][license-href]
[![Nuxt][nuxt-src]][nuxt-href]

A Nuxt 3 module to use Leaflet of https://www.npmjs.com/package/vue-leaflet-more.
It was made using [Vue Leaflet](https://github.com/vue-leaflet/vue-leaflet) which is a Vue 3 wrapper for Leaflet, that exposes the original Leaflet API as Vue components.

This module is really just about making it work with Nuxt 3 without the need to configure anything.

## Features

- ⚡ &nbsp;No configuration needed
- 🦺 &nbsp;Typescript support
- 🚠 &nbsp;Auto import

## Quick Setup

1. Add `nuxt3-leaflet` dependency to your project

```bash
# Using pnpm
pnpm add -D nuxt3-leaflet

# Using yarn
yarn add --dev nuxt3-leaflet

# Using npm
npm install --save-dev nuxt3-leaflet
```

2. Add `nuxt3-leaflet` to the `modules` section of `nuxt.config.ts`

```js
export default defineNuxtConfig({
  modules: ["nuxt3-leaflet"],
});
```

That's it! You can now use Leaflet in your Nuxt app ✨

## Usage

For a complete list of the components available, check out the original [Vue Leaflet](https://github.com/vue-leaflet/vue-leaflet) library.

Please note that components are exported in PascalCase, so for example, write `<LMap>` instead of `<l-map>`.

### Basic

```vue
<template>
  <div style="height:100vh; width:100vw">
    <LMap ref="map" :zoom="zoom" :center="[47.21322, -1.559482]">
      <LTileLayer
        url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
        attribution='&amp;copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors'
        layer-type="base"
        name="OpenStreetMap"
      />
    </LMap>
  </div>
</template>

<script setup>
import { ref } from "vue";
const zoom = ref(6);
</script>

<style>
body {
  margin: 0;
}
</style>
```

## Development

```bash
# Install dependencies
npm install

# Generate type stubs
npm run dev:prepare

# Develop with the playground
npm run dev

# Build the playground
npm run dev:build

# Run ESLint
npm run lint

# Run Vitest
npm run test
npm run test:watch

# Release new version
npm run release
```

<!-- Badges -->

[npm-version-src]: https://img.shields.io/npm/v/nuxt3-leaflet/latest.svg?style=flat&colorA=18181B&colorB=28CF8D
[npm-version-href]: https://npmjs.com/package/nuxt3-leaflet
[npm-downloads-src]: https://img.shields.io/npm/dm/nuxt3-leaflet.svg?style=flat&colorA=18181B&colorB=28CF8D
[npm-downloads-href]: https://npmjs.com/package/nuxt3-leaflet
[license-src]: https://img.shields.io/npm/l/nuxt3-leaflet.svg?style=flat&colorA=18181B&colorB=28CF8D
[license-href]: https://npmjs.com/package/nuxt3-leaflet
[nuxt-src]: https://img.shields.io/badge/Nuxt-18181B?logo=nuxt.js
[nuxt-href]: https://nuxt.com
