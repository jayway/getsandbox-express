# @jayway/getsandbox-express
A getsandbox.com to express adapter

## Usage

### as command-line tool, without installing

```bash
npx @jayway/getsandbox-express <main.js> [<port>]
```

Alternatively, if you want to install it globally:

```bash
npm install -g @jayway/getsandbox-express
sandbox <main.js> [<port>]
```

Default port is `8080`.

### as Node.js module

```js
const sandbox = require('@jayway/getsandbox-express')
const express = require('express')

const app = express()
sandbox.loadSandbox(app, __dirname + '/mysandbox/main.js')

const port = 8080
app.listen(port, () => {
  console.log(`Sandbox listening on port ${port}.`)
})
```
