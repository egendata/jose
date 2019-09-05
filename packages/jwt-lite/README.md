# jwt-lite

## Install

`npm install @egendata/jwt-lite`

## Usage

```javascript
const jwt = require('@egendata/jwt-lite')

const decoded = jwt.decode('somejwt');
const {
  header,         // jose header
  claimsSet,      // claimsSet as a JSON object
  signedContent,  // UintArray of the signed content
  signature       // UintArray of the signature
} = decoded;

jwt.sign(payload, jwk)
.then(jwtToken => console.log(jwtToken))

jwt.verify(jwtToken, jwk)
.then(payload => console.log(payload))
```

## Can it be smaller?

If you use ES6 imports with a bundler that supports tree-shaking, yes!

```javascript
import { sign } from '@egendata/jwt-lite'
```

## License

MIT
