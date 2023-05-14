# vite-vue3-chrome-extension-v3

[![build](https://github.com/mubaidr/vite-vue3-chrome-extension-v3/actions/workflows/build.yml/badge.svg)](https://github.com/mubaidr/vite-vue3-chrome-extension-v3/actions/workflows/build.yml)

A [Vite](https://vitejs.dev/) powered WebExtension ([Chrome](https://developer.chrome.com/docs/extensions/reference/), [FireFox](https://addons.mozilla.org/en-US/developers/), etc.) starter template.

## Features

- [CRXJS Vite Plugin](https://crxjs.dev/vite-plugin) Build a Chrome Extension with Vite
- HMR for extension pages and content scripts
- Vue 3 - Composition API, `Script setup` and more!
- Vue Router setup incuding `vite-plugin-pages` for automatic route registration
- Effortless communications - powered by [`webext-bridge`](https://github.com/zikaari/webext-bridge) and [VueUse](https://github.com/antfu/vueuse) storage
- [Components auto importing](./src/components)
- [Icons](./src/components) - Access to icons from any iconset directly
- [TypeScript](https://www.typescriptlang.org/) - type safe
- `Eslint` & `Prettier` configured for `vue`, `javascript`, `typescript`

## Pre-packed

### WebExtension Libraries

- [`webext-bridge`](https://github.com/zikaari/webext-bridge) - effortlessly communication between contexts
- [`webextension-polyfill`](https://github.com/mozilla/webextension-polyfill) - A lightweight polyfill library for Promise-based WebExtension APIs in Chrome

### Vite Plugins

- [`vite-plugin-pages`](https://github.com/hannoeru/vite-plugin-pages) - File system based route generator for Vite
- [`unplugin-auto-import`](https://github.com/antfu/unplugin-auto-import) - Directly use `browser` and Vue Composition API without importing
- [`unplugin-vue-components`](https://github.com/antfu/vite-plugin-components) - components auto import
- [`unplugin-icons`](https://github.com/antfu/unplugin-icons) - icons as components
  - [Material Design Icons](https://icon-sets.iconify.design/mdi/) - Material Design Icons

### Vue Plugins

- [VueUse](https://github.com/antfu/vueuse) - collection of useful composition APIs

### UI Frameworks

- [tailwindcss](https://tailwindcss.com) - A utility-first CSS framework

### Coding Style

- Use Composition API with [`<script setup>` SFC syntax](https://github.com/vuejs/rfcs/pull/227)

## Use the Template

### GitHub Template

[Create a repo from this template on GitHub](https://github.com/antfu/vitesse-webext/generate).

### Clone to local

If you prefer to do it manually with the cleaner git history

> If you don't have pnpm installed, run: npm install -g pnpm

```bash
npx degit antfu/vitesse-webext my-webext
cd my-webext
pnpm i
```

## Usage

### Folders

- `src` - main source.
  - `content-script` - scripts and components to be injected as `content_script`
  - `background` - scripts for background.
  - `popup` - popup pages
  - `options` - options pages
  - `components` - auto-imported Vue components that are shared in popup and options page.
  - `assets` - assets used in Vue components
- `dist` - built files, also serve stub entry for Vite on development.

### Development

```bash
pnpm dev
```

Then **load extension in browser with the `extension/` folder**.

### Build

To build the extension, run

```bash
pnpm build
```

And then pack files under `extension`, you can upload `extension.crx` or `extension.xpi` to appropriate extension store.

## Credits

This template is heavenly inspired by: https://github.com/antfu/vitesse-webext
