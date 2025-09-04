---
## sidebar_position: 9
---
# Get the code
There are several ways to get the Blockly code, and several ways to load it once you've gotten it.

## Create-package script
Blockly provides a script that bootstraps a starter application, which you can then modify. It uses common web development tools like [webpack](https://webpack.js.org/guides/) and [eslint](https://eslint.org/), but doesn't include a framework, like React or Angular.

This requires you to install [node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) before running the following commands.

To create an application written in JavaScript in a ```new hello-world``` directory:

```bash
npx @blockly/create-package app hello-world
```

To create an application written in TypeScript in a new `hello-world` directory:

```
npx @blockly/create-package app hello-world --typescript
```

These create a package that imports package targets. It also uses a package.json file to manage dependencies, which makes it easy to stay up-to-date with the latest version of Blockly.

It also comes with some handy starter scripts, such as one to test the project locally in a browser:

```bash
cd hello-world
npm run start
```

You can refer to the generated package.json file for other commands.

## Unpkg
If you are just playing around with ideas and don't want to bootstrap a full application, you can load Blockly from unpkg using script tags.

If you add the following to any HTML page, you can open the HTML directly in a browser to experiment with Blockly:

```bash
<!-- Load Blockly core -->
<script src="https://unpkg.com/blockly/blockly_compressed.js"></script>
<!-- Load the default blocks -->
<script src="https://unpkg.com/blockly/blocks_compressed.js"></script>
<!-- Load a generator -->
<script src="https://unpkg.com/blockly/javascript_compressed.js"></script>
<!-- Load a message file -->
<script src="https://unpkg.com/blockly/msg/en.js"></script>
```

This is not a good long-term solution for acquiring Blockly, because it doesn't work with bundlers like webpack, but it is good for prototyping and experimentation.

## Get the code
There are several ways which you can get the code to run Blockly.

The Blockly team recommends requiring Blockly through a package manager (like [NPM](https://www.npmjs.com/package/blockly) or [Yarn](https://yarnpkg.com/package/blockly)) because:
- It is easier to stay up to date with changes in Blockly
- It encourages [using plugins](https://developers.google.com/blockly/guides/programming/plugin_overview) instead of monkeypatching Blockly

### NPM

```bash
npm install blockly --save
```

### Yarn

```bash
yarn add blockly
```

### GitHub
You can also download the compressed code from our [GitHub releases](https://github.com/google/blockly/releases). However, this requires you to manually download the code at regular intervals in order to receive the latest updates and fixes to Blockly.

:::warning
Github downloads are only provided for convenience for developers who were previously forking Blockly. If you are a new developer, you should use a package manager.
:::

## Load the code
Once you've gotten the code, there are several ways you can access it from your code.

#### Script tags

```bash
<!-- Load Blockly core -->
<script src="./my-lib-directory/blockly/blockly_compressed.js"></script>
<!-- Load the default blocks -->
<script src="./my-lib-directory/blockly/blocks_compressed.js"></script>
<!-- Load a generator -->
<script src="./my-lib-directory/blockly/javascript_compressed.js"></script>
<!-- Load a message file -->
<script src="./my-lib-directory/blockly/msg/en.js"></script>
```

When using script tags, you can access imports from the global namespace:

```bash
// Access Blockly.
Blockly.thing;

// Access the default blocks.
Blockly.libraryBlocks['block_type'];

// Access the generator.
javascript.javascriptGenerator;
```

:::note
When using script tags you cannot have multiple message files because the messages get applied directly to the Blockly.Msg array.
:::

#### Imports
:::note
Using imports of our package targets requires you to be using a bundler (like webpack), since Blockly is packaged as a UMD, rather than an ESM.
:::

```bash
// Import Blockly core.
import * as Blockly from 'blockly/core';
// Import the default blocks.
import * as libraryBlocks from 'blockly/blocks';
// Import a generator.
import {javascriptGenerator} from 'blockly/javascript';
// Import a message file.
import * as En from 'blockly/msg/en';
```

When you import the message files, you also need to apply them.

```bash
Blockly.setLocale(En);
```

#### Requires

```bash
// Require Blockly core.
const Blockly = require('blockly/core');
// Require the default blocks.
const libraryBlocks = require('blockly/blocks');
// Require a generator.
const {javascriptGenerator} =  require('blockly/javascript');
// Require a message file.
const En = require('blockly/msg/en');
```
0
When you require the message files, you also need to apply them.

```
Blockly.setLocale(En);
```