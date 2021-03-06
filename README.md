# rollup-plugin-manifest-json

[![Build Status](https://travis-ci.org/adamzerella/rollup-plugin-manifest-json.svg?branch=master)](https://travis-ci.org/adamzerella/rollup-plugin-manifest-json)
[![Coverage Status](https://coveralls.io/repos/github/adamzerella/rollup-plugin-manifest-json/badge.svg?branch=master)](https://coveralls.io/github/adamzerella/rollup-plugin-manifest-json?branch=master)
![NPM Version][npm-version-badge]

> Rollup plugin to generate a manifest.json file used to tell the browser about your web app.

## Install

```
npm i --save-dev rollup-plugin-manifest-json
```

## Usage

```js
import manifestJson from "rollup-plugin-manifest-json";

export default {
    input: "main.js",
    plugins: [
        manifestJson({
            input: "public/manifest.json", // Required
            minify: true,
            manifest: {
                short_name: "custom-short-name"
            }
        })
    ]
}
```

## Options

### input

**Required**

Type: `string`

Default: `""`

The `manifest.json` file location  that will be modified and copied into the Rollup build directory.

### minify

_Optional_

Type: `boolean`

Default: `false`

Whether or not to mangle the output file, it's recommended to minify the file as it will reduce the file size.

### manifest

Type: `object`

Default: `{}`

The key values you wish to add or modify to the existing `manifest.json` file. For a full list of key values to use [see here.](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json)

### output

_Optional_

Type: `string`

Default: `manifest.json`

Unique output directory to write the manifest file to, useful for building your app outside of the root rollup folder.

## Contributors

Don't be scared to raise an issue or a pull request! Any contributions, no matter how big or small will land your picture here and be greatly appreciated ❤️

<div style="display:inline;">
  <a href="https://github.com/adamzerella"><img width="48" height="48" src="https://avatars0.githubusercontent.com/u/1501560?s=460&v=4" alt="Adam Zerella"/></a>
  <a href="https://github.com/benmccann"><img width="48" height="48" src="https://avatars1.githubusercontent.com/u/322311?s=460&u=4303e3b2c87b6eab07d258faf5090deedef4550b&v=4" alt="Ben McCann"/></a>
</div>

[npm-version-badge]:https://img.shields.io/npm/v/rollup-plugin-manifest-json