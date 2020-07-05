# dollar-signer.js

[![Join the chat at https://gitter.im/bitdollar-network/dollar.js](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/bitdollar-network/dollar-signer.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![npm](https://img.shields.io/npm/dm/dollar-signer.svg)](https://www.npmjs.com/package/dollar-signer)

# INSTALL
`npm install dollar-signer`

# USAGE

  - [example](https://github.com/bitdollar-network/dollar-signer.js/)

```javascript
const BitdollarSigner = require('dollar-signer')
const privateKey = Buffer.from('your_private_key', 'hex')

const parameters = {
  nonce: '0x00',
  gasPrice: '0x09184e72a000', 
  gasLimit: '0x2710',
  to: '0x0000000000000000000000000000000000000000', 
  value: '0x00',
  chainId: 8773873
}

const transaction = new BitdollarSigner(parameters)
transaction.sign(privateKey)
const serializedTransaction = transaction.serialize()
```

- **Note:** ECMAScript 6 (ES6) is the a minimum requirement.
- **Note:** Please use a shim (such as [es6-shim](https://github.com/paulmillr/es6-shim)) before including anything from this repo if you need compatibility for browsers without ES6 support.


# API
[./docs/](./docs/index.md)
