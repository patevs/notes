# TypeScript NodeJS Setup

> TypeScript has had first class support for Node.js since inception. Here's how to setup a quick Node.js project:

---

## Links & Resources

- [`typescript-book`](https://github.com/basarat/typescript-book)
- [TypeScript Deep Dive](https://basarat.gitbooks.io/typescript/)
  - [TypeScript with NodeJS](https://basarat.gitbooks.io/typescript/content/docs/quick/nodejs.html)

---

## Basic Setup

1. Setup a Node.js project `package.json`. Quick one : `npm init -y`
2. Add TypeScript (`npm install typescript --save-dev`)
3. Add node.d.ts (`npm install @types/node --save-dev`)
4. Init a `tsconfig.json` for TypeScript options with a few key options in your tsconfig.json (`npx tsc --init --rootDir src --outDir lib --esModuleInterop --resolveJsonModule --lib es6,dom --module commonjs`)

### Live Compile & Run

1. Add `ts-node` which we will use for live compile + run in node (`npm install ts-node --save-dev`)
2. Add `nodemon` which will invoke ts-node whenever a file is changed (`npm install nodemon --save-dev`)

Now just add a `script` target to your `package.json` based on your application entry e.g. assuming its `index.ts`:

```json
"scripts": {
  "start": "npm run build:live",
  "build": "tsc -p .",
  "build:live": "nodemon --watch 'src/**/*.ts' --exec 'ts-node' src/index.ts"
},
```

So you can now run `npm start` and as you edit `index.ts`:

- `nodemon` reruns its command (ts-node)
- `ts-node` transpiles automatically picking up `tsconfig.json` and the installed TypeScript version,
- `ts-node` runs the output JavaScript through Node.js.

And when you are ready to deploy your JavaScript application run `npm run build`.

---
