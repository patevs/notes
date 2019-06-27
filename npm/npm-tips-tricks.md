
# NPM Tips & Tricks

> Speed up your JavaScript development workflow with npm and package.json

---

## Links & Resources

- [NPM Tricks](https://medium.com/@bretcameron/13-npm-tricks-for-faster-javascript-development-4fe2a83f87a2)

---

### Setting Default `init` Configuration:

```bash
npm config set init.author.name  "Joe Bloggs"
npm config set init.author.email "joebloggs@gmail.com"
npm config set init.author.url   "joebloggs.com"
npm config set init.license      "MIT"
```

To check that these properties were added correctly, type `npm config edit` to bring up the configuration file. You can also edit details by typing values directly into this file. If you want to edit global npm setting, use `npm config edit -g`.

---

### List and Select Available Scripts

Listing the scripts available in a `package.json` file is easy: just go to the root directory of your project and type `npm run` in the terminal.

But there’s an even more convenient way to get a list of scripts, which you can run immediately: to do this, install the NTL (npm Task List) module globally:

```bash
npm install --global ntl
# OR: npm i -g ntl
```

Then run the ntl command in the project folder. You’ll get a list of available scripts, with the option of selecting one of them to run.

---
