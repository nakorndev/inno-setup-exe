# Inno Setup Exe

> Repository for bundle [Inno Setup](https://jrsoftware.org/isdl.php) to npm package.

## Usage

1. Install with `npm install inno-setup-exe`.
2. Use `const iscc = require('inno-setup-exe')` on node to get the path of main Inno Setup compiler.

## Example to run iscc command on node

```js
const { spawnSync } = require('child_process')
const iscc = require('inno-setup-exe')

const outputPath = './output' // should not empty folder
const outputFilename = 'setup' // output as "setup.exe"
const issFile = './main.iss' // the .iss file

spawnSync(iscc, [
  `/O${outputPath}`,
  `/F${outputFilename}`,
  issFile
])
```
