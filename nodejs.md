# NodeJS

### Debugging

`node --inspect build/src/index.js`

Example @TM:   
`npm run build &&  node --inspect build/src/index.js`

### Use Local Repository as Package

```text
$ cd my-package/
$ npm link
$ cd ../main-app
$ npm link "<name given above>"
```

