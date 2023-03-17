
# To reproduce

```sh
cd main
yarn install
yarn link ../linkable
yarn install
node index.js
```

You should see this error:

```
❯ node index.js
18.2.0
node:internal/modules/cjs/loader:998
  throw err;
  ^

Error: Cannot find module 'linkable'
Require stack:
- /Users/v7rulnik/projects/aviasales/yarn-test/main/index.js
    at Module._resolveFilename (node:internal/modules/cjs/loader:995:15)
    at Module._load (node:internal/modules/cjs/loader:841:27)
    at Module.require (node:internal/modules/cjs/loader:1061:19)
    at require (node:internal/modules/cjs/helpers:103:18)
    at Object.<anonymous> (/Users/v7rulnik/projects/aviasales/yarn-test/main/index.js:2:1)
    at Module._compile (node:internal/modules/cjs/loader:1159:14)
    at Module._extensions..js (node:internal/modules/cjs/loader:1213:10)
    at Module.load (node:internal/modules/cjs/loader:1037:32)
    at Module._load (node:internal/modules/cjs/loader:878:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:81:12) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [ '/Users/v7rulnik/projects/aviasales/yarn-test/main/index.js' ]
}
```