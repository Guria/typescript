# Northbrook TypeScript Mocha

> Test your packages with mocha + ts-node

# Get it

```sh
npm install --save-dev @northbrook/ts-mocha
```

# Configure it

```js
// northbrook.json
{
  "plugins": [
    "ts-mocha" // add to registered plugins
  ],
  // optional configuration
  "ts-mocha": {
    // default : []
    exclude: ["somePackage"] // exclude a managed package from testing
    // default: 'test/'
    directory: "src/" a place to find your test,
    // default: ['.ts', '.tsx']
    extensions: ['.spec.ts'] // extensions to match
  }
}

// tsconfig.json - TypeScript 2.x
{
  "compilerOptions": {
    ...
    "types": [
      "node",
      "mocha"
    ]
  }
}
```

# Use it

```sh
northbrook ts-mocha
# only run for a specific package
northbrook ts-mocha --only somePackage
```
