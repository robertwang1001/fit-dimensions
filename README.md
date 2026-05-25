<h1 align="center">Welcome to fit-dimensions 👋</h1>

![GitHub License](https://img.shields.io/github/license/robertwang1001/fit-dimensions)
![GitHub commit activity](https://img.shields.io/github/commit-activity/w/robertwang1001/fit-dimensions)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/robertwang1001/fit-dimensions/release.yaml)
![GitHub Release](https://img.shields.io/github/v/release/robertwang1001/fit-dimensions)
![GitHub Release Date](https://img.shields.io/github/release-date/robertwang1001/fit-dimensions)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/robertwang1001/fit-dimensions)
![GitHub watchers](https://img.shields.io/github/watchers/robertwang1001/fit-dimensions)
![GitHub forks](https://img.shields.io/github/forks/robertwang1001/fit-dimensions)
![GitHub Repo stars](https://img.shields.io/github/stars/robertwang1001/fit-dimensions)
![NPM Version](https://img.shields.io/npm/v/fit-dimensions)
![NPM Type Definitions](https://img.shields.io/npm/types/fit-dimensions)
![NPM Downloads](https://img.shields.io/npm/dw/fit-dimensions)
![Node Current](https://img.shields.io/node/v/fit-dimensions)

A tiny utility function to fit a source rectangle within a target rectangle using popular object-fit modes (`contain`, `cover`, `fill`, `none`, `scale-down`). Maintains aspect ratio as needed. Useful for images, videos, UI elements, and more.

## Use Cases

* Fitting images, videos, or canvases into containers
* UI layout calculations
* Responsive design utilities
* Viewport-aware rendering in games or data viz

## Mode

| Mode | Description
| ---- | ----
| contain | Scale to fit inside target, maintain aspect ratio
| cover | Fill target, cropping as needed, maintain aspect ratio
| fill | Stretch to fill target, ignore aspect ratio
| none | No scaling, original size
| scale-down | Use smaller of none or contain

## Installation

Using pnpm:

```sh
pnpm add fit-dimensions
```

Using yarn:

```sh
yarn add fit-dimensions
```

Using npm:

```sh
npm install fit-dimensions
```

## Usage

### Parameters

* `srcWidth`: width of the source rectangle. (number)
* `srcHeight`: height of the source rectangle. (number)
* `maxWidth`: width of the target rectangle. (number)
* `maxHeight`: height of the target rectangle. (number)
* `mode`: one of *contain* | *cover* | *fill* | *none* | *scale-down*. (string) (optional) (default: *contain*)

### Return

An object:

* `width`: fitted width. (number)
* `height`: fitted height. (number)
* `x`: offset from the left. (number)
* `y`: offset from the top. (number)

> `x` and `y` are the position used to center the fitted rectangle

### Example

```javascript
import { fitDimensions } from 'fit-dimensions'
// or: const { fitDimensions } = require('fit-dimensions')

// Example:
const fit = fitDimensions(800, 600, 400, 400, 'contain')
// fit = { width: 400, height: 300, x: 0, y: 50 }
```

## Contributing

Contributions are welcome! If you have ideas, bug fixes, or improvements, please open an issue or submit a pull request on the
[GitHub repository](https://github.com/robertwang1001/fit-dimensions).

Give a ⭐️ if this project helped you!

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.
