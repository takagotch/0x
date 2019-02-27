### 0x
---
https://github.com/davidmarkclements/0x

```
npm install -g 0x
0x my-app.js
0x -o my-app.js
0x -P 'autocannon localhost:$PORT' my-app.js
0x -- /path/to/node my-app.js
0x -- node --zero-fill-buffers my-app.js
0x examples/rest-api
npm run stress-rest-example
0x -P 'autocannon localhost:$PORT' app.js

node --stack-size=8024 $(which 0x) my-app.js
```

```js
const zeroEks = require('0x');
const path = require('path')

async function capture () {
  const opts = {
    argv: [path.join(__dirname, 'my-app.js'), '--my-flag', '"value for my flag"'],
    workingDir: __dirname
  }
  try {
    const file = await zeroEks(opts)
    console.log(`flamegraph in ${file}`)
  } catch (e) {
    console.error(e)
  }
}

capture()
```

```
```


