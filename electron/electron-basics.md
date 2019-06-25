
# Electron Basics

> 14/06/2019

---

## Links & Resources

* [`Electron`](https://github.com/electron/electron)
  * [Documentation](https://electronjs.org/docs)
  * [Awesome List](https://github.com/sindresorhus/awesome-electron)
  * [`electron-forge`](https://www.electronforge.io/)
  * [`webpack-template`](https://www.electronforge.io/templates/webpack-template)
  * [`react-boilerplate`](https://github.com/electron-react-boilerplate/electron-react-boilerplate)

---

## Electron Development

```bash
# Electron global install
$ npm install --global electron
# Check electron installation:
$ electron --help
```

```bash
# Electron forge cli build tool
$ npm install --global @electron-forge/cli
# Generate basic project template:
$ npx create-electron-app <my-app>
# Generate webpack project template:
$ npx create-electron-app <my-app> --template=webpack
```

### Live Reloading

* [`electron-reloader`](https://github.com/sindresorhus/electron-reloader)

**Example:**

The following must be included in the app entry file, usually named `index.js`:

```javascript
  try {
    require('electron-reloader')(module);
  } catch (_) {}
```

You have to pass the `module` object so we can read the module graph and figure out which files belong to the main process.

The `try/catch` is needed so it doesn't throw `Cannot find module 'electron-reloader'` in production.

---
