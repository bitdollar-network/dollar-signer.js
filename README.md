[![Join the chat at https://gitter.im/bitdollar-network/dollar.js](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/bitdollar-network/dollar-signer.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![npm](https://img.shields.io/npm/dm/dollar-signer.svg)](https://www.npmjs.com/package/dollar-signer)

# INSTALL
`npm install dollar-signer`

# USAGE

  - [example](https://github.com/bitdollarjs/dollar-signer/blob/master/examples/transactions.js)

```javascript
// Currently only supporting use as vanilla JS
// Please move and use the dist/dollar-signer.min.js file.
// const dollarSigner = require('dollar-signer')
const privateKey = Buffer.from('your_private_key', 'hex')

const parameters = {
  nonce: '0x00',
  gasPrice: '0x09184e72a000', 
  gasLimit: '0x2710',
  to: '0x0000000000000000000000000000000000000000', 
  value: '0x00', 
  data: '0x7f7465737432000000000000000000000000000000000000000000000000000000600057',
  chainId: 8773873
}

const transaction = new dollarSigner(parameters)
transaction.sign(privateKey)
const serializedTransaction = transaction.serialize()
```

**Note:** this package expects ECMAScript 6 (ES6) as a minimum environment. From browsers lacking ES6 support, please use a shim (like [es6-shim](https://github.com/paulmillr/es6-shim)) before including any of the builds from this repo.


# API
[./docs/](./docs/index.md)
