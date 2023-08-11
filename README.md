# Data Integrity Polyfill for React Native _(@digitalcredentials/data-integrity-rn)_

[![Build status](https://img.shields.io/github/actions/workflow/status/digitalcredentials/data-integrity-rn/main.yml?branch=main)](https://github.com/digitalcredentials/data-integrity-rn/actions?query=workflow%3A%22Node.js+CI%22)
[![NPM Version](https://img.shields.io/npm/v/@digitalcredentials/data-integrity-rn.svg)](https://npm.im/@digitalcredentials/data-integrity-rn)

> React Native polyfill for globals required for Data Integrity and VC apps (TextEncoder, crypto.subtle, etc).

## Table of Contents

- [Background](#background)
- [Security](#security)
- [Install](#install)
- [Usage](#usage)
- [Contribute](#contribute)
- [License](#license)

## Background

There are several global objects such as `TextEncoder` and `crypto` that are
present in Node.js and most browsers, but not in React Native.

This is a polyfill for these objects, which exports the following globals:

* `TextEncoder` and `TextDecoder`
* `crypto` and `crypto.subtle` (WebCryptography API)

## Install

- Node.js 20+ is recommended.

### NPM

To install via NPM:

```
npm install @digitalcredentials/data-integrity-rn
```

### Development

To install locally (for development):

```
git clone https://github.com/digitalcredentials/data-integrity-rn.git
cd data-integrity-rn
npm install
```

## Usage

When developing for React Native and using various DCC-provided libraries such
as [`@digitalcredentials/vc`](https://github.com/digitalcredentials/vc),
make sure to import this polyfill before importing the DCC libraries:

```js
import '@digitalcredentials/data-integrity-rn'
// Now you can import various libraries
import '@digitalcredentials/vc'
// ...
```

## Contribute

PRs accepted.

If editing the Readme, please conform to the
[standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

[MIT License](LICENSE.md) © 2023 Digital Credentials Consortium.
