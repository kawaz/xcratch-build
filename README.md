# Xcratch Command to Build Extension Module
This command supports to build a module file of an extension for [Xcratch: Extendable Scratch3 Programming Environment](https://xcratch.github.io/).

## How to Build a Module

`xcratch-build` is a Node executable script to build a module of an extension for Xcratch.

This command adds a extension in a local Scratch server. It makes links of source path on local scratch-vm/scratch-gui, and modifies code of the Scratch to appear the extension in its extension selector. 

### Module Building

`xcratch-build` bundles entry/block code and resources into one module file. It copy files to temporal directories in scratch-gui/scratch-vm and bundles them using [rollup.js](https://rollupjs.org/guide/en/).

```sh
cd xcx-my-extension
npx xcratch-build --module=extensionID
```

This command accepts these command-line arguments.

- --module: name of the module file (without '.mjs')
- --block : location of block files from current dir (optional, default: "./src/block")
- --entry : location of entry files from current dir (optional, default: "./src/entry")
- --gui : location of scratch-gui from current dir (optional, default: "../scratch-gui")
- --vm : location of scratch-vm form current dir (optional, default: "gui/node_modules/scratch-vm")
- --url : URL to get its module as a loadable extension for Xcratch (optional)
- --output : location to save module form current dir (optional, default: "./dist")


## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/xcratch/xcratch-build/issues). 
## Show your support

Give a ⭐️ if this project helped you!


## 📝 License

Copyright © 2021 [Koji Yokokawa](https://github.com/yokobond).<br />
This project is [MIT](https://github.com/xcratch/xcratch-build/blob/master/LICENSE) licensed.
